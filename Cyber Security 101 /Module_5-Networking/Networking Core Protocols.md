# 🌐 Networking Core Protocols (Cybersecurity-Focused Notes)

This module focuses on core network protocols that enable communication between systems.
Understanding these protocols is essential for:
- Network analysis
- Traffic inspection
- Exploitation and defense

These protocols are widely used in **penetration testing and cybersecurity operations**.

---

## 🧪 Task 1: Introduction

### 🔑 Keywords
- Protocols, communication rules, data exchange

### 🧠 Explanation
Network protocols define the rules for communication between devices. They determine how data is formatted, transmitted, and received across a network.

Each protocol serves a specific purpose, such as:
- Web communication
- File transfer
- Email transmission

### 🔐 Cybersecurity Relevance
- Every network attack targets a protocol
- Understanding protocols helps:
  - Identify vulnerabilities  
  - Analyze malicious traffic  
- Protocol knowledge is essential for:
  - Packet analysis  
  - Exploitation  

---

## 🧪 Task 2: ARP (Address Resolution Protocol)

### 🔑 Keywords
- ARP, MAC address, IP mapping

### 🧠 Explanation
ARP is used to map an IP address to a MAC (hardware) address within a local network.

Process:
- System sends ARP request → "Who has this IP?"
- Target responds with MAC address

### 🔐 Cybersecurity Relevance
- Vulnerable to:
  - ARP Spoofing (Man-in-the-Middle attack)
- Attackers can:
  - Intercept traffic  
  - Redirect communication  
- Used in:
  - Network sniffing attacks  

---

## 🧪 Task 3: DHCP (Dynamic Host Configuration Protocol)

### 🔑 Keywords
- DHCP, IP assignment, automatic configuration

### 🧠 Explanation
DHCP automatically assigns IP addresses to devices in a network.

Process:
- Discover → Offer → Request → Acknowledge (DORA)

### 🔐 Cybersecurity Relevance
- Attackers can:
  - Perform DHCP spoofing  
  - Assign malicious gateway  
- Leads to:
  - Traffic interception  
- Important for:
  - Network configuration security  

---

## 🧪 Task 4: DNS (Domain Name System)

### 🔑 Keywords
- DNS, domain resolution

### 🧠 Explanation
DNS converts human-readable domain names into IP addresses.

Example:
    example.com → 93.x.x.x

### 🔐 Cybersecurity Relevance
- Target for:
  - DNS spoofing  
  - DNS poisoning  
- Attackers can:
  - Redirect users to malicious sites  
- Used in:
  - Phishing attacks  

---

## 🧪 Task 5: HTTP & HTTPS

### 🔑 Keywords
- HTTP, HTTPS, web communication

### 🧠 Explanation

### 🔹 HTTP
- Transfers web data in plain text  
- Default port: 80  

### 🔹 HTTPS
- Secure version of HTTP  
- Uses encryption (TLS)  
- Default port: 443  

### 🔐 Cybersecurity Relevance
- HTTP:
  - Vulnerable to sniffing  
- HTTPS:
  - Protects data using encryption  
- Attackers target:
  - Weak SSL/TLS configurations  
  - Web vulnerabilities  

---

## 🧪 Task 6: FTP (File Transfer Protocol)

### 🔑 Keywords
- FTP, file transfer

### 🧠 Explanation
FTP is used to transfer files between systems over a network.

Default port:
- 21  

### 🔐 Cybersecurity Relevance
- Sends data in plain text  
- Vulnerable to:
  - Credential theft  
- Attackers use:
  - Anonymous login  
- Secure alternative:
  - SFTP  

---

## 🧪 Task 7: SMTP, POP3, IMAP (Email Protocols)

### 🔑 Keywords
- SMTP, POP3, IMAP, email communication

### 🧠 Explanation

### 🔹 SMTP
- Sends emails  
- Port: 25  

### 🔹 POP3
- Retrieves emails (downloads)  
- Port: 110  

### 🔹 IMAP
- Retrieves emails (syncs)  
- Port: 143  

### 🔐 Cybersecurity Relevance
- Email is a major attack vector:
  - Phishing  
  - Malware delivery  
- Weak configurations can expose:
  - Credentials  
- Attackers exploit:
  - Open mail relays  

---

## 🧪 Task 8: Conclusion

### 🔑 Keywords
- core protocols

### 🧠 Explanation
This module introduces essential network protocols used in communication across systems and services.

### 🔐 Cybersecurity Relevance
- Each protocol represents:
  - A potential attack vector  
- Understanding them helps in:
  - Detection  
  - Prevention  
  - Exploitation  

---

## 🔥 Final Understanding

Core protocols are the backbone of networking.

By understanding:
- ARP → local network mapping  
- DHCP → IP assignment  
- DNS → domain resolution  
- HTTP/HTTPS → web communication  
- FTP & Email protocols → data exchange  

You can:
- Analyze network traffic  
- Identify vulnerabilities  
- Perform attacks and defenses  

These are essential for:
- Penetration Testing  
- Network Security  
- Traffic Analysis (Wireshark)
