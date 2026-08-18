# 🌐 DNS in Detail (TryHackMe)

## 🎯 Objective
The goal of this room was to understand how the Domain Name System (DNS) translates human-readable domain names into IP addresses, and to learn about the DNS hierarchy and various DNS record types.

## 🧠 Core Concepts Learned
* **DNS Hierarchy:** Understood the complete resolution flow: Root Servers ➔ TLD (Top-Level Domain) Servers ➔ Authoritative Name Servers.
* **DNS Records:** 
  * `A Record`: Maps a domain to an IPv4 address.
  * `AAAA Record`: Maps a domain to an IPv6 address.
  * `CNAME`: Maps a domain to another domain (alias).
  * `MX Record`: Directs email to a mail server.
  * `TXT Record`: Holds text information (often used for domain verification and security policies like SPF/DKIM).

## 🛠️ Tools & Commands Used
* **Tool:** Terminal / Command Line
* **Command:** `nslookup` (or `dig`)
  * *Usage:* Used to query DNS servers manually to retrieve IP addresses or specific DNS records for a target domain.

## 💡 Key Takeaways (Security Perspective)
DNS acts as the "phonebook of the internet." Understanding DNS is critical for a SOC Analyst or Pentester because attackers frequently abuse DNS for data exfiltration, Command and Control (C2) communication, or phishing via domain spoofing.
