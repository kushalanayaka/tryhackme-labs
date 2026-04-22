# 🪟 Windows Fundamentals 3 
This module focuses on built-in Windows security mechanisms and how they:
- Protect the system
- Get misconfigured
- Are abused by attackers

---

## 🧪 Task 1: Introduction

### 🧠 Explanation
Windows integrates multiple security layers including updates, antivirus, firewall, and encryption. These components work together to reduce attack surface and protect data.

### 🔐 Cybersecurity 
- Security is layered → breaking one control is not enough
- Attackers look for weakest control (misconfiguration)

---

## 🧪 Task 2: Windows Updates


### 🧠 Explanation
Windows Updates deliver security patches, bug fixes, and feature updates to keep the system secure and stable.

### 🔐 Cybersecurity 
- Unpatched systems = **easy targets**
- Many exploits depend on:
  - Outdated OS versions
- Attackers first check:
  - “Is this system patched?”

👉 Example:
- EternalBlue exploit worked because systems weren’t updated

---

## 🧪 Task 3: Windows Security



### 🧠 Explanation
Windows Security provides a centralized interface to manage:
- Antivirus
- Firewall
- Device protection
- App control

### 🔐 Cybersecurity 
- Gives overview of system security posture
- If disabled → system is exposed
- Attackers may try to:
  - Disable protections silently

---

## 🧪 Task 4: Virus & Threat Protection



### 🧠 Explanation
This feature scans and detects:
- Malware
- Viruses
- Suspicious behavior

It provides:
- Real-time protection
- Manual scanning
- Threat history

### 🔐 Cybersecurity 
- First line of defense against malware
- Attackers use:
  - Obfuscation to bypass detection
- Defender disabled = high risk

👉 Example:
- Malicious script blocked before execution

---

## 🧪 Task 5: Firewall & Network Protection


### 🧠 Explanation
Windows Firewall controls incoming and outgoing traffic based on network profile and defined rules.

### 🔐 Cybersecurity 
- Prevents unauthorized access
- Blocks:
  - Port scanning
  - Remote attacks
- Misconfigured firewall = exposed system

👉 Example:
- Open port → attacker gains entry point

---

## 🧪 Task 6: App & Browser Control



### 🧠 Explanation
This feature protects against:
- Malicious applications
- Unsafe downloads
- Browser-based threats

SmartScreen checks reputation of files and websites.

### 🔐 Cybersecurity 
- Blocks phishing and malicious downloads
- Attackers try to:
  - Trick users into bypassing warnings
- Helps prevent:
  - Social engineering attacks

👉 Example:
- Warning shown before opening unknown file

---

## 🧪 Task 7: Device Security


### 🧠 Explanation
Device Security ensures system integrity using hardware-based protections such as:
- Secure Boot
- TPM (Trusted Platform Module)

### 🔐 Cybersecurity 
- Prevents:
  - Boot-level malware
  - Rootkits
- Ensures OS is not tampered during startup

👉 Example:
- System blocks unsigned bootloader

---

## 🧪 Task 8: BitLocker



### 🧠 Explanation
BitLocker encrypts entire disk to protect data from unauthorized access.

### 🔐 Cybersecurity 
- Protects data if device is:
  - Stolen
  - Lost
- Without BitLocker:
  - Attacker can read disk offline

👉 Example:
- Remove hard drive → still unreadable without key

---

## 🧪 Task 9: Volume Shadow Copy Service (VSS)



### 🧠 Explanation
VSS creates snapshots (copies) of files for backup and recovery.

### 🔐 Cybersecurity 
- Useful for:
  - Data recovery
- BUT also abused by attackers:
  - Extract previous versions of sensitive files
  - Dump credentials

👉 Example:
- Attacker retrieves old password file from shadow copy

---

## 🧪 Task 10: Conclusion



### 🧠 Explanation
This module combines multiple Windows security features into a layered defense model.

### 🔐 Cybersecurity 
- Security depends on:
  - Proper configuration
  - Regular updates
- Attackers target:
  - Weakest link in system

---

## 🔥 Final Understanding

Windows security is not one tool — it is a **combination of controls**:

- Updates → fix vulnerabilities  
- Defender → detect malware  
- Firewall → block access  
- BitLocker → protect data  
- Device security → protect boot process  

👉 Real-world security = correct configuration of all these layers
