# 🖥️ Windows PowerShell Learning Guide (Beginner to Advanced)

This repository contains a **structured, hands-on learning path** for mastering **Windows PowerShell**, starting from basics to advanced automation and cybersecurity usage.

PowerShell is a powerful scripting and automation tool built on the .NET framework that uses **object-oriented pipelines** instead of plain text.

---

# ⚡ Phase 1: Beginner (Fundamentals)

---

## 🧪 Task 1: Introduction to PowerShell

### 🔑 Keywords
- Cmdlets, Verb-Noun, Object-based pipeline

### 🧠 Explanation
PowerShell uses **cmdlets (command-lets)** in a structured format:

Verb-Noun

Examples:
- Get-Process  
- Set-Content  

Unlike traditional CMD, PowerShell works with **objects instead of plain text**, allowing more powerful data handling and automation.

---

## 🧪 Task 2: Basic Commands

### 🔑 Keywords
- Get-Command, Get-Help, Get-Process

### 🧠 Explanation
These commands help discover and understand available functionality in PowerShell.

Commands:
    Get-Command
    Get-Help Get-Process
    Get-Process

- Get-Command → Lists all available cmdlets  
- Get-Help → Provides documentation for commands  
- Get-Process → Lists running processes  

---

## 🧪 Task 3: File System Navigation

### 🔑 Keywords
- Get-Location, Get-ChildItem, ls, pwd

### 🧠 Explanation
Used to navigate and view the file system.

Commands:
    Get-Location
    Get-ChildItem
    ls
    pwd

- Get-Location → Shows current directory  
- Get-ChildItem → Lists files and folders  
- ls, pwd → Shortcuts  

---

## 🧪 Task 4: Directory Navigation

### 🔑 Keywords
- cd

### 🧠 Explanation
Used to move between directories.

Commands:
    cd Desktop
    cd ..

- cd Desktop → Move into folder  
- cd .. → Move back  

---

## 🧪 Task 5: Create Files and Folders

### 🔑 Keywords
- New-Item

### 🧠 Explanation
Used to create files and directories.

Commands:
    New-Item -ItemType Directory test-folder
    New-Item file.txt

---

## 🧪 Task 6: Read and Write Files

### 🔑 Keywords
- Set-Content, Get-Content

### 🧠 Explanation
Used to write and read file contents.

Commands:
    Set-Content file.txt "Hello PowerShell"
    Get-Content file.txt

---

# ⚡ Phase 2: Intermediate (Core Power)

---

## 🧪 Task 7: Filtering Data

### 🔑 Keywords
- Where-Object, pipeline

### 🧠 Explanation
Filters data using conditions.

Command:
    Get-Process | Where-Object {$_.CPU -gt 100}

---

## 🧪 Task 8: Selecting Specific Data

### 🔑 Keywords
- Select-Object

### 🧠 Explanation
Selects specific properties from objects.

Command:
    Get-Process | Select-Object Name, CPU

---

## 🧪 Task 9: Sorting Data

### 🔑 Keywords
- Sort-Object

### 🧠 Explanation
Sorts output based on a property.

Command:
    Get-Process | Sort-Object CPU -Descending

---

## 🧪 Task 10: Searching Files

### 🔑 Keywords
- Get-ChildItem, recursion

### 🧠 Explanation
Searches files recursively.

Command:
    Get-ChildItem -Recurse | Where-Object {$_.Name -like "*test*"}

---

## 🧪 Task 11: Managing Services

### 🔑 Keywords
- Get-Service

### 🧠 Explanation
Used to manage system services.

Commands:
    Get-Service
    Get-Service | Where-Object {$_.Status -eq "Running"}

---

## 🧪 Task 12: Stop a Process

### 🔑 Keywords
- Stop-Process

### 🧠 Explanation
Stops running processes.

Command:
    Stop-Process -Name notepad

⚠️ Use carefully.

---

# ⚡ Phase 3: Advanced (Scripting & Automation)

---

## 🧪 Task 13: Variables

### 🔑 Keywords
- Variables

### 🧠 Explanation
Stores data for reuse.

Command:
    $name = "Kush"
    Write-Output $name

---

## 🧪 Task 14: Loops

### 🔑 Keywords
- for loop

### 🧠 Explanation
Repeats execution of code.

Command:
    for ($i=1; $i -le 5; $i++) {
        Write-Output "Number $i"
    }

---

## 🧪 Task 15: Conditional Statements

### 🔑 Keywords
- if statement

### 🧠 Explanation
Executes code based on conditions.

Command:
    $cpu = 120

    if ($cpu -gt 100) {
        Write-Output "High CPU Usage"
    }

---

## 🧪 Task 16: Creating and Running Scripts

### 🔑 Keywords
- script.ps1

### 🧠 Explanation
PowerShell scripts automate tasks.

Commands:
    notepad script.ps1
    .\script.ps1

Example:
    Get-Process | Sort-Object CPU -Descending | Select-Object -First 5

---

## 🧪 Task 17: Execution Policy

### 🔑 Keywords
- ExecutionPolicy

### 🧠 Explanation
Controls script execution permissions.

Commands:
    Get-ExecutionPolicy
    Set-ExecutionPolicy RemoteSigned

---

# ⚡ Phase 4: Cybersecurity Use Cases

---

## 🧪 Task 18: System Information

### 🔑 Keywords
- Get-ComputerInfo

### 🧠 Explanation
Retrieves detailed system information.

Command:
    Get-ComputerInfo

---

## 🧪 Task 19: Network Information

### 🔑 Keywords
- Get-NetIPAddress, Get-NetTCPConnection

### 🧠 Explanation
Displays network configuration and connections.

Commands:
    Get-NetIPAddress
    Get-NetTCPConnection

---

## 🧪 Task 20: Logged-in Users

### 🔑 Keywords
- query user

### 🧠 Explanation
Shows currently logged-in users.

Command:
    query user

---

## 🧪 Task 21: Event Logs

### 🔑 Keywords
- Get-EventLog

### 🧠 Explanation
Accesses system event logs.

Command:
    Get-EventLog -LogName Security

---

## 🧪 Task 22: Detect Suspicious Processes

### 🔑 Keywords
- process monitoring

### 🧠 Explanation
Identifies high resource usage processes.

Command:
    Get-Process | Sort-Object CPU -Descending

---

# 🧠 Key Takeaways

- PowerShell works with **objects, not text**  
- Pipeline (`|`) is the most powerful feature  
- Automation is the main goal of PowerShell  
- Essential for **system administration + cybersecurity**  

---

# 🚀 Future Improvements

- Add automation scripts  
- Build security monitoring tools  
- Integrate PowerShell with Python  
- Create real-world cybersecurity projects  

---

# ⭐ Conclusion

This guide provides a **complete roadmap** to mastering PowerShell from beginner to advanced level with hands-on practice.
Practice consistently and apply these commands in real-world scenarios to become proficient.
