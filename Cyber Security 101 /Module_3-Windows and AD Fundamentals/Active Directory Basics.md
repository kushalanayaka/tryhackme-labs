# 🛡️ Active Directory & Windows Domain – 
---

## 📌 Task 1: Introduction

- Small networks can be managed manually.
- Large organizations require **centralized management**.
- Solution → **Windows Domain**

### 🔑 Key Concepts:
- Domain = group of users & computers
- Central management system
- Scalable infrastructure

---

## 📌 Task 2: Windows Domains Overview

### 🧠 Active Directory (AD)
- Central database storing:
  - Users
  - Computers
  - Groups
  - Policies

### 🖥️ Domain Controller (DC)
- Server that runs AD services
- Handles authentication & authorization

### ✅ Advantages:
- Centralized identity management
- Policy enforcement across network

---

## 📌 Task 3: Active Directory Objects

### 👤 Users
- Security principals (can authenticate)
- Types:
  - Human users
  - Service accounts

### 💻 Machines
- Each domain computer has an account
- Format: `COMPUTERNAME$`

### 👥 Security Groups
- Used for permission management
- Example:
  - Domain Admins
  - Domain Users

### 📁 Organizational Units (OUs)
- Used for:
  - Organizing users/computers
  - Applying policies

### ⚖️ OU vs Group
| OU | Group |
|----|------|
| Apply policies | Assign permissions |
| One per user | Multiple allowed |

---

## 📌 Task 4: Managing Users in AD

### 🗑️ Delete OU
- Enable **Advanced Features**
- Disable:
  - "Protect object from accidental deletion"

### 👤 User Management
- Create / Delete users to match organization

### 🔐 Delegation
- Assign limited admin rights

Example:
- IT user (Phillip) → reset passwords

### ⚡ PowerShell Commands:

- `Set-ADAccountPassword sophie -Reset -NewPassword (Read-Host -AsSecureString)`
- `Set-ADUser -ChangePasswordAtLogon $true -Identity sophie powershell`

## 📌 Task 5: Managing Computers in AD

### 🚨 Problem
- All machines are stored in the default **Computers container**
- Difficult to manage and apply different policies

### ✅ Solution
Organize computers into separate OUs:

- Workstations
- Servers
- Domain Controllers (already exists)

### 📂 Organization Strategy:
- **Workstations** → User laptops and desktops
- **Servers** → Machines providing services
- **Domain Controllers** → Critical infrastructure

### 🛠️ Steps:
1. Open Active Directory Users and Computers
2. Create new OUs under domain:
   - Workstations
   - Servers
3. Move machines from "Computers" container:
   - PCs → Workstations
   - Servers → Servers

### 🎯 Benefit:
- Apply different Group Policies for each category
- Improve security and management

---

## 📌 Task 6: Group Policy Objects (GPOs)

### ⚙️ What is a GPO?
- A collection of configuration settings applied to:
  - Users
  - Computers

### 🛠️ Tool:
- Group Policy Management

### 🔗 How GPO Works:
1. Create a GPO
2. Configure settings
3. Link it to an OU

### 🔐 Default Policies:
- Default Domain Policy
- Default Domain Controllers Policy

### 🔧 Example Configuration:
- Minimum password length = 10 characters

## 📌 Task 7: Practical GPO Implementation

### 🔒 Restrict Control Panel Access

#### 🎯 Goal:
- Only IT department users can access the Control Panel
- Other departments are restricted

#### 🛠️ Steps:
1. Create a new GPO:
   - Name: `Restrict Control Panel Access`

2. Edit the GPO:
   - User Configuration → Administrative Templates → Control Panel

3. Enable:
- **Prohibit access to Control Panel and PC settings**

4. Link GPO to:
- Sales OU
- Marketing OU
- Management OU

#### 🧠 Note:
- This is a **User Configuration policy**, so it applies based on user accounts

---

### ⏱️ Auto Lock Screen Policy

#### 🎯 Goal:
- Automatically lock systems after 5 minutes of inactivity

#### 🛠️ Steps:
1. Create a new GPO:
- Name: `Auto Lock Screen`

2. Edit the GPO:
   - Computer Configuration → Windows Settings → Security Settings → Local Policies → Security Options

3. Configure:
- **Interactive logon: Machine inactivity limit = 300 seconds**

4. Link GPO to:
- Root domain (`thm.local`)

#### 🧠 Note:
- This is a **Computer Configuration policy**
- Applies to all domain-joined machines

## 📌 Task 8: Authentication Protocols

### 🟢 Kerberos (Default)

- Modern authentication protocol used in Windows domains
- Uses a **ticket-based system**

#### 🔄 Flow:
1. User logs in → receives **TGT (Ticket Granting Ticket)**
2. Uses TGT to request **TGS (Service Ticket)**
3. Uses TGS to access services

#### 🔑 Advantages:
- More secure than NTLM
- Password is not repeatedly sent over the network
- Efficient and faster authentication

---

### 🟡 NTLM (Legacy)

- Older authentication protocol
- Uses **challenge-response mechanism**

#### 🔄 Flow:
1. Server sends a random challenge
2. Client generates response using password hash
3. Domain Controller verifies response

#### ⚠️ Risks:
- Vulnerable to:
  - Pass-the-Hash attacks
  - NTLM Relay attacks

#### 🧠 Note:
- Still used for backward compatibility in many systems

## 📌 Task 9: Trees, Forests & Trusts

### 🌳 Tree
- Collection of domains with the **same namespace**

#### Example:
- uk.thm.local
- us.thm.local

---

### 🌲 Forest
- Collection of multiple domain trees with **different namespaces**

#### Example:
- thm.local
- mht.local

---

### 🤝 Trust Relationships

#### 🔹 One-Way Trust:
- Domain A trusts Domain B
- Users from B can access resources in A

#### 🔹 Two-Way Trust:
- Both domains trust each other
- Default in trees and forests

---

### ⚠️ Important:
- Trust allows **authentication between domains**
- Does **NOT automatically grant access**
- Access permissions must be explicitly assigned

---

## 🧠 Key Takeaways

- Trees organize domains with same namespace
- Forests combine multiple domain structures
- Trust relationships enable cross-domain communication
- Proper configuration is required for secure access
