# 🪟 Windows Fundamentals 1


---

## 🧪 Task 1: Windows Editions

### 🧠 Explanation
Windows Editions (Home, Pro, Enterprise) define the system’s capabilities and available security features. Using tools like `systeminfo`, we can gather detailed information about the operating system, including version, architecture, installed updates, and domain membership.

### 🔐 Cybersecurity 
- `systeminfo` is used in **enumeration phase**
- Helps identify:
  - Missing patches (potential vulnerabilities)
  - OS version (exploit targeting)
  - Domain-joined systems (Active Directory attack surface)
- Enterprise editions introduce security controls like BitLocker and Group Policy

---

## 🧪 Task 2: The Desktop (GUI)


### 🧠 Explanation
The Graphical User Interface (GUI) is the primary way users interact with Windows. Components such as the Start Menu and Search Box provide access to applications and system utilities. The Taskbar and Notification Area display active processes and background services, while Display Settings and Personalization control the user environment.

### 🔐 Cybersecurity
- Taskbar and Startup programs may reveal **persistence mechanisms**
- Search functionality can expose:
  - Sensitive files
  - Installed tools
- Notification area may indicate:
  - Disabled antivirus
  - Suspicious background services
- GUI elements often expose **attack surface for social engineering**

---

## 🧪 Task 3: Introduction to Windows



### 🧠 Explanation
Windows is a multi-user operating system with a layered architecture, including kernel mode and user mode. It manages processes, memory, and system resources while providing both GUI and command-line interfaces.

### 🔐 Cybersecurity 
- Separation of user mode and kernel mode is critical:
  - User → limited privileges
  - Kernel → full system control
- Many attacks aim to escalate privileges from user to kernel
- Understanding OS structure helps in:
  - Process injection
  - Exploit development

---

## 🧪 Task 4: The File System


### 🧠 Explanation
Windows supports multiple file systems, but NTFS is the standard. NTFS provides advanced features such as Access Control Lists (ACLs) and Encrypting File System (EFS). Permissions define what actions users can perform on files and folders.

Permission Levels:
- Full Control → complete access
- Modify → read, write, delete
- Read & Execute → view and run files
- List Folder → view directory contents

### 🔐 Cybersecurity 
- NTFS permissions are a **primary access control mechanism**
- Misconfigured permissions can lead to:
  - Unauthorized access
  - Privilege escalation
- Writable system files can be replaced by attackers
- EFS protects data but is ineffective if encryption keys are compromised

---

## 🧪 Task 5: The Windows\System32 Folder



### 🧠 Explanation
`%windir%` refers to the Windows installation directory (usually `C:\Windows`). The System32 folder contains critical system files, including executables, DLLs, and core OS components required for system operation.

### 🔐 Cybersecurity 
- High-value target for attackers:
  - DLL hijacking
  - Binary replacement
- If System32 files are writable:
  - Full system compromise is possible
- PATH misconfigurations can allow execution of malicious binaries instead of legitimate ones

---

## 🧪 Task 6: User Accounts, Profiles, and Permissions



### 🧠 Explanation
Windows manages access using user accounts and groups. Local users can be created and managed through tools like `lusrmgr.msc`, which allows administrators to assign users to groups and define access privileges.

### 🔐 Cybersecurity 
- Attackers often:
  - Create hidden users
  - Add accounts to the Administrators group
- Group membership defines privilege level
- Misconfigured accounts can lead to:
  - Unauthorized access
  - Privilege escalation
- Monitoring user creation is critical in incident response

---

## 🧪 Task 7: User Account Control (UAC)



### 🧠 Explanation
User Account Control (UAC) is a security feature that prompts users for permission before executing actions that require elevated privileges.

### 🔐 Cybersecurity 
- Prevents silent execution of privileged operations
- Acts as a barrier between user and administrator privileges
- Many malware techniques attempt to bypass UAC
- Misconfigured UAC settings reduce system security

---

## 🧪 Task 8: Settings and the Control Panel



### 🧠 Explanation
Settings and Control Panel provide interfaces to configure system behavior and manage installed applications. Programs and Features lists all installed software on the system.

### 🔐 Cybersecurity 
- Used for **software enumeration**
- Helps identify:
  - Outdated applications
  - Vulnerable software
- Attackers target known vulnerable versions of software
- Uninstall logs can reveal system usage patterns

---

## 🧪 Task 9: Task Manager



### 🧠 Explanation
Task Manager provides real-time information about running processes, system performance, and startup applications. It allows users to monitor and control system activity.

### 🔐 Cybersecurity 
- Detect suspicious or unknown processes
- Identify malware through:
  - High CPU usage
  - Unusual behavior
- Used to terminate malicious processes
- Startup tab reveals persistence mechanisms

---

## 🧪 Task 10: Conclusion

### 🧠 Explanation
This module provides a structured understanding of Windows components, including system architecture, file systems, user management, and system tools.

### 🔐 Cybersecurity 
- Forms the foundation for:
  - Windows enumeration
  - Privilege escalation
  - Malware analysis
  - Incident response
- Understanding these concepts enables both offensive and defensive security operations

---

## 🔥 Final Understanding

Windows is a primary target in real-world environments.  
Understanding its internal structure, permissions, and processes is essential for:

- Penetration Testing (Offensive Security)
- Threat Detection (Defensive Security)

Mastery of these fundamentals enables deeper exploration into:
- Active Directory
- Privilege Escalation
- Windows Exploitation
