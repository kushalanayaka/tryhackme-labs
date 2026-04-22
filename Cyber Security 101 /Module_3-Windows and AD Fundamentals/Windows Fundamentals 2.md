# 🪟 Windows Fundamentals 2 (Cybersecurity-Focused Notes)

This document covers Windows system tools and configurations with a focus on:
- System enumeration
- Misconfiguration analysis
- Monitoring & troubleshooting
- Attack surface identification

---

## 🧪 Task 1: Introduction



### 🧠 Explanation
This module focuses on built-in Windows utilities that provide visibility into system configuration, performance, and internal operations.

### 🔐 Cybersecurity 
- These tools are used heavily in:
  - Enumeration (offensive)
  - Monitoring (defensive)
- Attackers and defenders use the **same tools**, but with different intent

---

## 🧪 Task 2: System Configuration & Advanced System Settings



### 🧠 Explanation
`msconfig` (System Configuration) is used to control how Windows starts.

Key tabs:
- **General** → Normal / Diagnostic / Selective startup
- **Boot** → OS boot options (safe mode, timeout)
- **Services** → Background services (can enable/disable)
- **Startup** → Redirects to Task Manager (modern systems)

This tool is used to troubleshoot boot issues and manage startup behavior.

### 🔐 Cybersecurity 
- Misconfigurations can:
  - Disable security services
  - Allow malicious services to persist
- Attackers may:
  - Add malicious startup entries
  - Hide services among legitimate ones
- Analysts use this to:
  - Identify abnormal startup behavior

---

## 🧪 Task 3: Change UAC Settings



### 🧠 Explanation
User Account Control (UAC) controls when administrative privileges are required. It enforces a separation between standard user actions and elevated operations.

### 🔐 Cybersecurity 
- Lower UAC settings = easier privilege escalation
- Attackers attempt:
  - UAC bypass techniques
- Strong UAC settings:
  - Prevent silent execution of malicious code
- Important for:
  - Privilege boundary enforcement

---

## 🧪 Task 4: Computer Management



### 🧠 Explanation
`compmgmt.msc` is a centralized management console combining multiple administrative tools:

### 🔹 System Tools
- Task Scheduler → automate tasks
- Event Viewer → logs
- Local Users and Groups (`lusrmgr.msc`) → user management

### 🔹 Storage
- Disk Management → partitions, volumes

### 🔹 Services and Applications
- Manage system services

### 🔐 Cybersecurity 
- Task Scheduler:
  - Used for **persistence (malicious scheduled tasks)**
- Services:
  - Attackers create or modify services to maintain access
- Users & Groups:
  - Adding users to Admin group = privilege escalation
- Disk Management:
  - Can expose hidden partitions or data

---

## 🧪 Task 5: System Information


### 🧠 Explanation
`msinfo32` provides detailed system information categorized into:

- System Summary → OS, BIOS, RAM
- Hardware Resources → IRQs, memory
- Components → drivers, devices
- Software Environment → running tasks, environment variables

### 🔐 Cybersecurity 
- Key enumeration tool:
  - OS version → exploit targeting
  - Installed drivers → potential vulnerabilities
- Environment variables:
  - PATH hijacking opportunities
- Network info:
  - Internal IP → lateral movement planning

---

## 🧪 Task 6: Resource Monitor



### 🧠 Explanation
`resmon` provides real-time visibility into system resource usage:

- CPU → running processes
- Disk → file access
- Network → active connections
- Memory → usage patterns

### 🔐 Cybersecurity 
- Detect:
  - Suspicious processes
  - Unusual network activity
- Identify:
  - Malware using system resources
- Useful for:
  - Behavioral analysis

---

## 🧪 Task 7: Command Prompt


### 🧠 Explanation
Command Prompt (`cmd`) provides CLI access to system operations.

Key commands:
- `hostname` → system name
- `whoami` → current user
- `ipconfig` → network configuration
- `netstat` → active connections and ports

### 🔐 Cybersecurity 
- Core enumeration commands:
  - Identify user privilege
  - Discover network interfaces
  - Detect open ports
- `netstat`:
  - Shows active connections (potential C2 communication)

---

## 🧪 Task 8: Registry Editor


### 🧠 Explanation
The Windows Registry is a hierarchical database storing system and application configuration.

It contains:
- System settings
- User configurations
- Startup entries

### 🔐 Cybersecurity 
- High-value target for attackers:
  - Persistence via registry keys
- Common abuse:
  - Run / RunOnce keys (auto-start programs)
- Misconfigurations can:
  - Expose sensitive data
  - Allow unauthorized execution

---

## 🧪 Task 9: Conclusion



### 🧠 Explanation
This module provides deeper visibility into Windows internal tools and configurations.

### 🔐 Cybersecurity 
- These tools enable:
  - System enumeration
  - Misconfiguration detection
  - Performance monitoring
- Foundation for:
  - Privilege escalation
  - Incident response
  - Threat hunting

---

## 🔥 Final Understanding

Windows Fundamentals 2 is about **visibility and control**.

If you master:
- System tools (msconfig, compmgmt, msinfo32)
- Monitoring tools (resmon, task manager)
- CLI commands (cmd)

You can:
- Analyze a system
- Identify weaknesses
- Detect suspicious behavior

This is the bridge between:
➡️ Basic knowledge  
➡️ Real-world cybersecurity operations
