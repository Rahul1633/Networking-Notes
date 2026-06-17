# Common Ports — CompTIA A+ 220-1201 (2.1)
> 📺 Source: [Professor Messer - Common Ports](https://www.youtube.com/watch?v=_qGlbfZ44hg)

---

## Why Port Numbers Matter

- Port numbers identify which **application/service** network traffic belongs to
- Critical for **troubleshooting** communication issues
- Used by **firewalls** to allow or block traffic based on TCP/UDP port numbers
- For the A+ exam: know each port's **number**, **protocol (TCP/UDP)**, and **use case**

---

## Protocols & Ports

### 📁 FTP — File Transfer Protocol
- **Ports:** TCP/20 (data transfer), TCP/21 (control/admin)
- Transfers files between systems
- Requires username/password OR allows **anonymous login**
- Full-featured: list, add, delete, rename files

---

### 🔒 SSH — Secure Shell
- **Port:** TCP/22
- a cryptographic network protocol that allows you to safely connect to and manage a remote computer or server over an unsecured network like the internet
- **Preferred over Telnet** for all remote admin tasks

---

### ⚠️ Telnet — Telecommunications Network
- **Port:** TCP/23
- Same function as SSH but **no encryption** — all data sent in clear text (including usernames & passwords)
- Avoid on production networks; use SSH instead

---

### 📧 SMTP — Simple Mail Transfer Protocol
- **Port:** TCP/25
- Sends email **server-to-server**, or from a device to a mail server
- Used for **outgoing** mail only

---

### 🌐 DNS — Domain Name System
- **Port:** UDP/53
- Translates domain names (e.g. `professormesser.com`) into IP addresses
- Multiple DNS servers used for **redundancy**

---

### 🖥️ DHCP — Dynamic Host Configuration Protocol
- **Ports:** UDP/67 (server), UDP/68 (client)
- Automatically assigns IP address, subnet mask, default gateway, and DNS to devices
- IP addresses are **leased** for a period of time
- Can **reserve static IPs** for specific devices (e.g. printers, servers)

---

### 🌍 HTTP — Hypertext Transfer Protocol
- **Port:** TCP/80
- Unencrypted web traffic (sent in clear text)

---

### 🔐 HTTPS — Hypertext Transfer Protocol Secure
- **Port:** TCP/443
- Encrypted web traffic
- Most modern websites use HTTPS

---

### 📬 POP3 — Post Office Protocol v3
- **Port:** TCP/110
- POP works by contacting your email service and downloading all of your new messages from it. Once they are downloaded onto your PC or Mac, they are deleted from the email service. This means that after the email is downloaded, it can only be accessed using the same computer. If you try to access your email from a different device, the messages that have been previously downloaded won't be available to you.

---

### 📨 IMAP — Internet Message Access Protocol v4
- **Port:** TCP/143
- IMAP allows you to access your email wherever you are, from any device. When you read an email message using IMAP, you aren't actually downloading or storing it on your computer; instead, you're reading it from the email service. As a result, you can check your email from different devices, anywhere in the world: your phone, a computer, a friend's computer**

---

### 🪟 SMB — Server Message Block (also called CIFS)
- **Port:** TCP/445 (modern, direct)
- **Legacy ports:** TCP/139 + UDP/137 (older NetBIOS)
- Used by Windows for file sharing, printer queues, and device-to-device communication

---

### 📒 LDAP — Lightweight Directory Access Protocol
- **Port:** TCP/389
- Access to directory databases (users, devices, resources)
- Commonly used with **Microsoft Active Directory**

---

### 🔏 LDAPS — Lightweight Directory Access Protocol Secure
- **Port:** TCP/636
- Encrypted/secure version of LDAP

---

### 🖱️ RDP — Remote Desktop Protocol
- **Port:** TCP/3389
- View and control a **remote Windows desktop** over the network
- Clients available on Windows, Mac, Linux, iOS, and more
- Can control a full desktop or run a single remote application

---

## 🧠 Quick Reference Cheat Sheet

| Protocol | Full Name                          | Port(s)            | Transport |
|----------|------------------------------------|--------------------|-----------|
| FTP      | File Transfer Protocol             | 20 (data), 21 (ctrl) | TCP     |
| SSH      | Secure Shell                       | 22                 | TCP       |
| Telnet   | Telecommunications Network         | 23                 | TCP       |
| SMTP     | Simple Mail Transfer Protocol      | 25                 | TCP       |
| DNS      | Domain Name System                 | 53                 | UDP       |
| DHCP     | Dynamic Host Configuration Protocol| 67, 68             | UDP       |
| HTTP     | Hypertext Transfer Protocol        | 80                 | TCP       |
| HTTPS    | HTTP Secure                        | 443                | TCP       |
| POP3     | Post Office Protocol v3            | 110                | TCP       |
| IMAP     | Internet Message Access Protocol   | 143                | TCP       |
| SMB      | Server Message Block               | 445 (139/137 legacy)| TCP/UDP  |
| LDAP     | Lightweight Directory Access Protocol | 389             | TCP       |
| LDAPS    | LDAP Secure                        | 636                | TCP       |
| RDP      | Remote Desktop Protocol            | 3389               | TCP       |

---

## 💡 Key Exam Tips

- **SSH vs Telnet** — Both do remote command-line access, but only SSH encrypts traffic. Always prefer SSH.
- **HTTP vs HTTPS** — Port 80 = unencrypted, Port 443 = encrypted.
- **SMTP** = sending email. **POP3/IMAP** = receiving email.
- **DNS uses UDP**, not TCP (common trick question).
- **DHCP uses two ports** — 67 for the server, 68 for the client.
- **SMB port 445** is the modern one; 139/137 are legacy NetBIOS ports.
- **RDP port 3389** — if you see this in a firewall log or alert, someone is trying to remotely access a Windows machine.

---

> 🔗 These port numbers are essential not just for the A+ exam, but for real-world SOC work — you'll see them constantly in firewall rules, network logs, and security alerts.
