# 🛰️ TryHackMe Writeup: Nmap Live Host Discovery

## 📝 Room Overview
* **Room Name:** Nmap Live Host Discovery
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Network Security / Reconnaissance

## 🎯 Objective
Master host discovery techniques using Nmap to actively map out live devices across local and remote subnets via ARP, ICMP, TCP, and UDP scanning methods.

---

## 💡 Tasks & Answers

### Task: Network Subnets & Target Specification
* **Question:** What is the first IP address Nmap would scan if you provided 10.10.12.13/29 as your target?
* **Answer:** `10.10.12.8`
* **Question:** How many IP addresses will Nmap scan if you provide the following range: 10.10.0-255.101-125?
* **Answer:** `6400`

### Task: Host Discovery Across the TCP/IP Layers (ARP & ICMP)
* **Question:** How many devices can see the ARP Request? (First Scenario)
* **Answer:** `4`
* **Question:** Did computer6 receive the ARP Request? (yea/nay)
* **Answer:** `nay`
* **Question:** How many devices can see the ARP Request? (Second Scenario)
* **Answer:** `4`
* **Question:** Did computer6 reply to the ARP Request? (yea/nay)
* **Answer:** `yea`
* **Question:** What type of packet did computer1 send before the ping?
* **Answer:** `ARP Request`
* **Question:** What type of packet did computer1 receive before it was able to send the ping?
* **Answer:** `ARP Response`
* **Question:** How many computers responded to the ping request?
* **Answer:** `1`
* **Question:** What is the name of the first device that responded to the first ARP Request?
* **Answer:** `router`
* **Question:** What is the name of the first device that responded to the second ARP Request?
* **Answer:** `computer5`
* **Question:** Send another Ping Request. Did it require new ARP Requests? (yea/nay)
* **Answer:** `nay`

### Task: Nmap Discovery via ARP & ICMP Options
* **Question:** How many hosts are found alive after scanning the CONNECTION_IP/24?
* **Answer:** `3`
* **Question:** What is the option required to tell Nmap to use ICMP Timestamp to discover live hosts?
* **Answer:** `-PP`
* **Question:** What is the option required to tell Nmap to use ICMP Address Mask to discover live hosts?
* **Answer:** `-PM`
* **Question:** What is the option required to tell Nmap to use ICMP Echo to discover live hosts?
* **Answer:** `-PE`

### Task: Nmap Discovery via TCP, UDP & DNS
* **Question:** Which TCP ping scan does not require a privileged account?
* **Answer:** `TCP SYN Ping`
* **Question:** Which TCP ping scan requires a privileged account?
* **Answer:** `TCP ACK Ping`
* **Question:** What option do you need to add to Nmap to run a TCP SYN ping scan on the telnet port?
* **Answer:** `-PS23`
* **Question:** We want Nmap to issue a reverse DNS lookup for all the possible hosts on a subnet, hoping to get some insights from the names. What option should we add?
* **Answer:** `-R`

---

## 🧠 Key Learnings
* **ARP within Local Networks (LAN):** Inside your home or office Wi-Fi, computers don't just speak IP; they need physical MAC addresses. If computer A wants to ping computer B, it first yells out to everyone: "Who has this IP? Tell me your MAC address!" (ARP Request). This request never leaves the local room/router.
* **Bypassing Firewalls with ICMP (-PP, -PM):** Everyone knows standard ping (`-PE`). Most modern firewalls instantly drop it to stay hidden. But Nmap can sneak past by asking strange questions like "What time is it on your clock?" (`-PP` Timestamp) or "What is your subnet mask?" (`-PM`). Lazy firewalls often forget to block these and accidentally reveal that the computer is alive.
* **Privileged vs. Unprivileged Scans:** 
  * Running a **TCP SYN Ping (`-PS`)** can be done by any regular user because the operating system simply opens a normal network connection.
  * Running a **TCP ACK Ping (`-PA`)** requires administrator (root) rights because you have to handcraft a custom "raw" packet pretending you are in the middle of an already open conversation.
* **Reverse DNS (`-R`):** Computers often have names like `mail-server-01.company.local` or `finance-database.local`. By forcing Nmap to ask DNS servers for names (`-R`), you can find the most valuable machines on a network before you even touch them.
*
