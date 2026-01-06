# Project 1: Telnet vs SSH Security Analysis using Wireshark

## 📌 Project Overview
This project demonstrates the security differences between Telnet and SSH by capturing and analyzing network traffic using Wireshark. The objective is to show how Telnet transmits credentials in plaintext, making it insecure, while SSH encrypts all communication, protecting against packet sniffing attacks.

---

## 🎯 Objective
- To analyze Telnet and SSH network traffic
- To demonstrate plaintext credential exposure in Telnet
- To verify encrypted communication in SSH
- To understand why SSH is preferred over Telnet in modern systems

---

## 🛠️ Tools Used
- Kali Linux
- Windows (Client System)
- Telnet
- SSH
- Wireshark

---

## 🚀 Steps Performed

### 1. User Configuration on Kali Linux
- A new non-root user (`shivam`) was created.
- User switching was tested to simulate real-world user access scenarios.

### 2. Telnet Service Configuration
- Telnet service was enabled using `openbsd-inetd`.
- Telnet login was tested locally and from a Windows machine.

### 3. Capturing Telnet Traffic
- Wireshark was used to capture Telnet packets on TCP port 23.
- Network traffic was filtered to analyze Telnet communication.

### 4. Telnet Login and Command Execution
- Login credentials were entered via Telnet.
- Commands were executed after successful authentication.

### 5. Plaintext Credentials Observation
- Wireshark TCP stream revealed usernames and passwords in plaintext.
- This confirmed Telnet’s vulnerability to packet sniffing attacks.

---

### 6. SSH Service Configuration
- SSH service was verified and started on Kali Linux.
- Secure connection was established from a Windows system.

### 7. Capturing SSH Traffic
- Wireshark captured SSH packets on TCP port 22.
- TCP stream analysis showed encrypted payloads.

### 8. SSH Login and Command Execution
- SSH login was performed successfully.
- Commands were executed securely without exposing credentials.

### 9. Encrypted Payload Verification
- SSH packets contained unreadable encrypted data.
- Even login credentials and commands were protected.

---

## 📊 Final Comparison Summary

| Feature | Telnet | SSH |
|------|-------|-----|
| Port | TCP 23 | TCP 22 |
| Encryption | ❌ No | ✅ Yes |
| Credential Security | Plaintext | Encrypted |
| Vulnerability | High | Low |
| Recommended Use | ❌ Never | ✅ Always |

---

## ✅ Key Learning Outcomes
- Telnet transmits credentials in plaintext and is highly insecure.
- SSH encrypts all communication, preventing packet sniffing.
- Wireshark effectively demonstrates real-world network security risks.
- Telnet should never be used in modern or production networks.
- SSH is the industry standard for secure remote access.

---

## 📸 Screenshots
All supporting screenshots (Wireshark captures, Telnet/SSH login, and packet analysis) are available in the `Screenshots/` folder.

---

## 🏁 Conclusion
This project clearly proves why Telnet is insecure and unsuitable for modern networks. SSH provides strong encryption and protects sensitive data even if network traffic is intercepted. The experiment reinforces the importance of encrypted communication in cybersecurity.

---

## 👤 Author
**Shivam Sahu**  
B.Tech | Cybersecurity
