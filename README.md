# TryHackMe-Writeups
My practical lab write-ups and CTF solutions from TryHackMe.
# 🛡️ Cybersecurity Operations & Pentesting Vault
Welcome to my personal cybersecurity knowledge base! This repository serves as a documented journey of my hands-on experience in **Network Security, SOC (Blue Teaming), and Offensive Security**. 
My focus is on practical skill-building, analyzing network artifacts, and understanding attacker TTPs (Tactics, Techniques, and Procedures).
---
## 📂 Repository Structure
Each folder in this repository represents a dedicated lab or project. Inside each folder, you will find a `README.md` containing my detailed write-up, including:
* 🎯 **Objective**
* 🛠️ **Tools Used**
* 💻 **Execution Steps (Commands & Logic)**
* 🧠 **Key Takeaways (What I Learned)**
---
## 📜 Lab & Project Index
### 🌐 Networking Core &  ⚙️ Fundamentals

| Status | Lab / Room Name | Category | Description |
| :--- | :--- | :--- | :--- |
| ✅ | [DNS in Detail](./DNS-in-Detail) | Networking | Understanding DNS records and resolution. |
| ✅ | [HTTP in Detail](./HTTP-in-Detail) | Networking | Web server requests and HTTP protocol. |
| ✅ | [What is Networking?](./What-is-Networking) | Networking | OSI Model and basic network architecture. |
| ✅ | [Networking Concepts](./Networking-Concepts) | Networking | TCP/IP protocol suite deep dive. |
| ✅ | [Linux Fundamentals (Pt1)](Linux-Fundamentals-Pt1/README.md) | Networking | Understanding basic Linux commands and interactive terminal usage. |
| ✅ | [Intro to LAN](./Intro-to-LAN/README.md) | Networking | Learn LAN topologies (Bus, Star) and private networks. |
| ✅ | [Cold Boot](./Cold-Boot/README.md) | Fundamentals | Basic physical components of a computer system. |
| ✅ | [Operating Systems: Introduction](./Operating-Systems-Introduction/README.md) | Fundamentals | Basic OS features and file system navigation. |
| ✅ | [Windows Basics](./Windows-Basics/README.md) | Fundamentals | Navigate Windows OS, manage files, and use Windows Defender. |
| ✅ | [History of Malware](./History-of-Malware/README.md) | Threat Intel | Learn the evolution of early malware into modern threats. |
| ✅ | [Security Awareness](Security-Awareness/README.md) | Fundamentals | Introduction to threat actors, breach impacts, and basic account security. |
| ✅ | [Windows Fundamentals 1](Windows-Fundamentals-1/README.md) | Fundamentals | Basic Windows OS navigation, NTFS, UAC, and User Management. |

### 🛡️ Defensive Security (SOC / Blue Team)

| Status | Lab / Room Name | Category | Description |
| :--- | :--- | :--- | :--- |
| ✅ | [SOC Fundamentals](./SOC-Fundamentals) | Blue Team | Core SOC processes and analyst workflows. |
| ✅ | [SOC Role in Blue Team](./SOC-Role-in-Blue-Team) | Blue Team | Escalation, incident response, and SOC levels. |
| ✅ | [The Phishing Pond](./The-Phishing-Pond) | Blue Team | Email header analysis and phishing detection. |
| ✅ | [SOC L1 Alert Reporting](SOC-L1-Alert-Reporting/README.md) | Blue Team | Learn how to properly report, escalate, and communicate about high-risk SOC alerts. |
| ✅ | [SOC L1 Alert Triage](./SOC-L1-Alert-Triage/README.md) | Blue Team | Triage and investigate security alerts using a SIEM dashboard. |
| ✅ | [The CIA Triad](./The-CIA-Triad/README.md) | Blue Team | Understand the CIA Triad and how it shapes cyber security mindset. |
| ✅ | [Cryptography Intro](./Cryptography-Intro/README.md) | Blue Team | Basics of encryption, decryption, and Caesar Cipher. |
| ✅ | [Introduction to EDR](./Intro-to-EDR/README.md) | Blue Team | Learn EDR fundamentals, telemetry, and alert investigation. |
| ✅ | [Traffic Analysis Essentials](./Traffic-Analysis-Essentials/README.md) | Blue Team | Network Security basics and identifying network anomalies. |
| ✅ | [Defensive Security Intro](Defensive-Security-Intro/README.md) | Blue Team | Investigating an ongoing attack at FakeBank and handling incident response. |
| ✅ | [Search Skills](Search-Skills/README.md) | Blue Team | Efficient internet search, OSINT, and domain-to-IP analysis. |
| ✅ | [Malware Classification](./Malware-Classification/README.md) | Blue Team | Identify and classify common types of malware. |
| ✅ | [Junior Security Analyst Intro](./Junior-Security-Analyst-Intro/README.md) | Blue Team | A day in the life of a SOC analyst, escalations, and firewalls. |
| ✅ | [Introduction to SIEM](Introduction-to-SIEM/README.md) | Blue Team | Learning SIEM fundamentals, features, and event analysis. |
| ✅ | [Phishing Basics](Phishing-Basics/README.md) | Red Team | Exploring phishing techniques and social engineering concepts. |
| ✅ | [Cyber Kill Chain](Cyber-Kill-Chain/README.md) | Blue Team | Understanding adversary methodologies and network intrusion prevention via the Cyber Kill Chain. |
| ✅ | [SOC L2 Alert Triage](./SOC-L2-Alert-Triage/README.md) | Blue Team | Triage escalated alerts and respond to cyber threats. |
| ✅ | [Network Traffic Basics](./Network-Traffic-Basics/README.md) | Blue Team | Analyze HTTP/DNS traffic to find malware and C2 servers. |
| ✅ | [Phishing Analysis Fundamentals](./Phishing-Analysis-Fundamentals/README.md) | Blue Team | Analyze email headers, attachments, and decode Base64 payloads. |
| ✅ | [Phishing Emails in Action](./Phishing-Emails-in-Action/README.md) | Blue Team | Examine real phishing emails and practice defanging malicious URLs. |
| ✅ | [Network Security Essentials](./Network-Security-Essentials/README.md) | Blue Team | Investigate Firewall, VPN, and IDS logs to track C2 beaconing and exfiltration. |
| ✅ | [Senior Security Analyst Intro](./Senior-Security-Analyst-Intro/README.md) | Blue Team | Explore duties beyond triage: Threat Hunting & Incident Response. |
| ✅ | [Intro to Endpoint Security](./Intro-to-Endpoint-Security/README.md) | Blue Team | Learn methodologies and tooling for endpoint monitoring. |
| ✅ | [Common Attacks](Common-Attacks/README.md) | Blue Team | Threat actor profiling, phishing detection, and hash cracking. |
| ✅ | [Security Principles](Security-Principles/README.md) | Blue Team | Core security concepts (CIA/DAD), security models, and ISO/IEC 19249 design principles. |
| ✅ | [Mobile Acquisition](Mobile-Acquisition/README.md) | Blue Team | Digital forensics methodologies, physical vs logical acquisition, and bypassing mobile hardware security. |
| ✅ | [Pyramid Of Pain](Pyramid-Of-Pain/README.md) | Blue Team | Understanding indicators of compromise (IOCs) and how to effectively disrupt adversary TTPs. |
| ✅ | [Junior Security Analyst](Junior-Security-Analyst/README.md) | Blue Team | A day in the life of a SOC analyst: triaging alerts, escalation, and firewall blocks. |


### ⚔️ Offensive Security (Red Team)

| Status | Lab / Room Name | Category | Description |
| :--- | :--- | :--- | :--- |
| ✅ | [Offensive Security Intro](./Offensive-Security-Intro) | Red Team | Basic web exploitation and ethical hacking intro. |
| ✅ | [Careers in Cyber](Careers-in-Cyber/README.md) | General | Exploring cybersecurity career paths and industry roles. |
| ✅ | [Training Impact on Teams](Training-Impact-on-Teams/README.md) | General | Calculating security ROI, vendor selection, and team upskilling metrics. |
| ✅ | [Passive Reconnaissance](Passive-Reconnaissance/README.md) | Red Team | Gather target intelligence stealthily using Whois, DNS, Shodan, and DNSDumpster. |
| ✅ | [Active Reconnaissance](Active-Reconnaissance/README.md) | Red Team | Active footprinting and banner grabbing using Ping, Traceroute, Telnet, and Netcat. |
| ✅ | [Pentesting Fundamentals](Pentesting-Fundamentals/README.md) | Red Team | Introduction to ethical hacking, RoE, and White/Black Box methodologies. |

### 🌐 Web Security & AppSec

| Status | Lab / Room Name | Category | Description |
| :--- | :--- | :--- | :--- |
| ✅ | [OWASP Top 10 2025: IAAA Failures](./OWASP-Top-10-2025-IAAA-Failures/README.md) | Web Security | Understand Authentication failures, Horizontal Escalation, and IDOR. |
| ✅ | [OWASP Top 10 2025: Insecure Data Handling](./OWASP-Top-10-2025-Insecure-Data-Handling/README.md) | Web Security | Explore SSTI, Insecure Deserialization, and Crypto failures. |
| ✅ | [Web Application Security](Web-Application-Security/README.md) | Web Security | Introduction to web app vulnerabilities, Cryptographic Failures, and IDOR. |

### 🧠 Emerging Threats (AI)

| Status | Lab / Room Name | Category | Description |
| :--- | :--- | :--- | :--- |
| ✅ | [AI Threat Modelling Assessment](./AI-Threat-Modelling-Assessment/README.md) | AI Security | Apply threat modelling frameworks to secure AI systems. |

---
## 🛠️ Tools & Technologies I Use
* **OS/Environments:** Kali Linux, Windows 
* **Networking & Discovery:** Nmap, Telnet
* **Documentation & Version Control:** Markdown, Git/GitHub
---
> *"In cybersecurity, hands-on experience and practical logic speak louder than words."*
