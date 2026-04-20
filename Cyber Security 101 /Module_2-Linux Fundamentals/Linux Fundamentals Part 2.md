# 🐧 Linux Fundamentals Part 2 

## Task 1: File Permissions Basics

This task focused on understanding file permissions in Linux.

Commands Used:
- `touch test.txt`
- `ls -l`
- `chmod 777 test.txt`

Key Takeaways:
- Linux uses read (r), write (w), and execute (x) permissions
- Permissions can be modified using chmod
- Numeric values like 777 represent full access


## Task 2: Changing File Ownership

This task introduced file ownership in Linux.

Commands Used:
- `ls -l`
- `sudo chown root:root test.txt`

Key Takeaways:
- Files have an owner and a group
- Ownership can be changed using chown
- Proper ownership is important for security

## Task 3: Creating Users

This task focused on user management in Linux.

Commands Used:
- `sudo adduser hacker`
- `su hacker`
- `whoami`

Key Takeaways:
- Linux supports multiple users
- Users can be created and switched easily
- User isolation improves security

## Task 4: Groups Management

This task introduced group management in Linux.

Commands Used:
- `groups`
- `sudo addgroup cyber`
- `sudo usermod -aG cyber hacker`

Key Takeaways:
- Groups help manage permissions efficiently
- Users can belong to multiple groups
- Group-based access control is widely used


## Task 5: Process Management

This task focused on managing running processes.

Commands Used:
- `ps`
- `top`
- `kill <PID>`

Key Takeaways:
- Processes represent running programs
- Each process has a unique PID
- Processes can be monitored and terminated

## Task 6: Package Management

This task introduced package management in Linux.

Commands Used:
- `sudo apt update`
- `sudo apt install tree`

Key Takeaways:
- Package managers are used to install software
- apt is commonly used in Debian-based systems
- Keeping packages updated is important for security

## Task 7: Viewing System Logs

This task focused on analyzing system logs.

Commands Used:
- `cat /var/log/syslog`

Key Takeaways:
- Logs contain important system and security information
- Useful for detecting suspicious activity
- Essential for defensive security

## Task 8: Networking Basics

This task introduced basic networking commands.

Commands Used:
- `ifconfig`
- `ip a`
- `ping google.com`

Key Takeaways:
- Helps identify IP addresses and network interfaces
- Ping is used to test connectivity
- Networking knowledge is essential in cybersecurity

## Task 9: File Permissions Challenge

This task focused on securing files using permissions.

Commands Used:
- `touch secret.txt`
- `chmod 600 secret.txt`

Key Takeaways:
- Restricting access improves security
- 600 allows only the owner to read and write
- Sensitive files should have limited permissions

## 🔥 My Understanding

Since the TryHackMe module required premium access, I recreated 
Linux Fundamentals Part 2 tasks locally using WSL.

This helped me gain practical experience in:
- File permissions and ownership
- User and group management
- Process handling
- Package installation
- Networking basics

This hands-on approach strengthened my Linux fundamentals 
for cybersecurity applications.
