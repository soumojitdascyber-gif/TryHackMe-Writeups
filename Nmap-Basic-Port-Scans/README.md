# 👁️ TryHackMe Writeup: Nmap Basic Port Scans

## 📝 Room Overview
* **Room Name:** Nmap Basic Port Scans
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Offensive Security Tooling / Reconnaissance

## 🎯 Objective
Learn in-depth how Nmap TCP connect scans, TCP SYN port scans, and UDP port scans work under the hood. Understand port states, TCP flags (SYN, RST), and how to fine-tune Nmap's performance using parallelism and timing templates.

---

## 💡 Tasks & Answers

### Task: Basic Services and Port States
* **Question:** Which service uses UDP port 53 by default?
* **Answer:** `DNS`
* **Question:** Which service uses TCP port 22 by default?
* **Answer:** `SSH`
* **Question:** How many port states does Nmap consider?
* **Answer:** `6`
* **Question:** Which port state is the most interesting to discover as a pentester?
* **Answer:** `Open`

### Task: TCP Connect Scan
* **Question:** What 3 letters represent the Reset flag?
* **Answer:** `RST`
* **Question:** Which flag needs to be set when you initiate a TCP connection (first packet of TCP 3-way handshake)?
* **Answer:** `SYN`

### Task: Interpreting Scan Results
* **Question:** What is the state of the FTP service running on port 21?
* **Answer:** `open`
* **Question:** What is Nmap's guess about the service running on port 53?
* **Answer:** `domain`
* **Question:** After launching a TCP SYN scan, how many SYN-ACK packets are successfully received in AttackBox?
* **Answer:** `4`
* **Question:** How many ports are open on the target machine?
* **Answer:** `4`
* **Question:** What is the state of port number 161 over UDP in the target machine?
* **Answer:** `closed`
* **Question:** What is the service name according to Nmap on port 161?
* **Answer:** `snmp`

### Task: Fine-Tuning Scope and Performance
* **Question:** What is the option to scan all the TCP ports between 5000 and 5500?
* **Answer:** `-p5000-5500`
* **Question:** How can you ensure that Nmap will run at least 64 probes in parallel?
* **Answer:** `--min-parallelism=64`
* **Question:** What option would you add to make Nmap very slow and paranoid?
* **Answer:** `-T0`
---

## 🧠 Key Learnings
* **The 6 Port States:** Nmap doesn't just see "open" or "closed." It has 6 states (Open, Closed, Filtered, Unfiltered, Open|Filtered, Closed|Filtered). As a pentester, an `Open` port is your front door, but a `Filtered` port tells you a firewall is actively watching your traffic.
* **Controlling Speed vs. Stealth:** 
  * If you want to blast through a network quickly, you increase parallel probes (`--min-parallelism=64`).
  * If you are trying to sneak past an Intrusion Detection System (IDS) that blocks rapid scanning, you use the "Paranoid" timing template (`-T0`), which sends packets painfully slow to avoid triggering alarms.
* **UDP vs TCP Service Defaults:** By default, connection-heavy protocols like SSH rely on TCP (Port 22), while fast, query-based protocols like DNS rely on UDP (Port 53). Knowing these defaults helps you quickly identify what a server is primarily used for.
*
