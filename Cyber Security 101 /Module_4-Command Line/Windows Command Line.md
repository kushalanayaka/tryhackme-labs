# 🪟 Windows Command Line 

This module focuses on using the Windows Command Line (CMD) for:
- System enumeration
- Network troubleshooting
- File and disk management
- Process monitoring

These commands are widely used in both **penetration testing** and **incident response**.

---

## 🧪 Task 1: Introduction

### 🔑 Keywords
- Command Prompt (cmd), CLI

### 🧠 Explanation
The Command Prompt (cmd) is a command-line interface that allows users to interact with the Windows operating system using text-based commands instead of a graphical interface.

It provides direct access to system functions, making it faster and more efficient for administrative, troubleshooting, and automation tasks.

### 🔐 Cybersecurity Relevance
- Used in:
  - Enumeration
  - Post-exploitation
  - Privilege escalation
- Attackers prefer CLI for:
  - Speed
  - Automation
- Defenders use it for:
  - Investigation
  - System diagnostics

---

## 🧪 Task 2: Basic System Information

### 🔑 Keywords
- systeminfo, hostname, whoami

### 🧠 Explanation
These commands are used to gather important system-level information.

Commands:
    systeminfo
    hostname
    whoami

- systeminfo → Displays OS version, installed patches, system architecture  
- hostname → Shows the computer name  
- whoami → Displays the currently logged-in user  

### 🔐 Cybersecurity Relevance
- First step in system enumeration  
- Helps identify:
  - OS version → used for exploit selection  
  - Installed patches → vulnerability assessment  
  - Current user privileges  
- whoami helps determine privilege level  

---

## 🧪 Task 3: Network Troubleshooting

### 🔑 Keywords
- ipconfig, ping, tracert, netstat

### 🧠 Explanation
These commands help analyze network configuration and connectivity.

Commands:
    ipconfig
    ping <target>
    tracert <target>
    netstat -ano

- ipconfig → Displays IP address, subnet, gateway  
- ping → Checks connectivity to another host  
- tracert → Shows route packets take to destination  
- netstat -ano → Lists active connections, ports, and associated processes  

### 🔐 Cybersecurity Relevance
- Used for:
  - Network enumeration  
  - Identifying reachable systems  
- netstat helps detect:
  - Suspicious connections  
  - Malware communication  
- Attackers use these to:
  - Map network structure  
  - Identify open services  

---

## 🧪 Task 4: File and Disk Management

### 🔑 Keywords
- dir, cd, copy, move, del

### 🧠 Explanation
These commands are used to navigate and manage files within the system.

Commands:
    dir
    cd <directory>
    copy <source> <destination>
    move <source> <destination>
    del <file>

- dir → Lists files and directories  
- cd → Changes current directory  
- copy → Copies files  
- move → Moves or renames files  
- del → Deletes files  

### 🔐 Cybersecurity Relevance
- Used to:
  - Locate sensitive files  
  - Navigate system directories  
- Attackers:
  - Search for credentials, configs, logs  
- Defenders:
  - Verify file integrity  
  - Investigate suspicious files  

---

## 🧪 Task 5: Task and Process Management

### 🔑 Keywords
- tasklist, taskkill

### 🧠 Explanation
These commands allow users to monitor and control running processes.

Commands:
    tasklist
    taskkill /PID <pid> /F

- tasklist → Displays all running processes  
- taskkill → Terminates a process by PID  

### 🔐 Cybersecurity Relevance
- Used to:
  - Identify suspicious or malicious processes  
- Attackers:
  - Kill antivirus or monitoring tools  
- Defenders:
  - Detect abnormal behavior  
  - Stop malicious programs  

---

## 🧪 Task 6: Conclusion

### 🔑 Keywords
- Command-line usage

### 🧠 Explanation
This module introduces essential command-line tools for interacting with Windows systems and performing system-level operations.

### 🔐 Cybersecurity Relevance
- Command-line skills are critical for:
  - System enumeration  
  - Network analysis  
  - Process monitoring  
- Used in:
  - Offensive security  
  - Defensive security  

---

## 🔥 Final Understanding

The Windows Command Line is a core tool in cybersecurity operations.

By mastering:
- System commands → understand the environment  
- Network commands → analyze connectivity  
- Process commands → detect threats  

These skills are essential for:
- Penetration Testing  
- Digital Forensics  
- Incident Response  
