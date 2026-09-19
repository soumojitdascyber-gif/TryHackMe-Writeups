# 👁️ TryHackMe Writeup: Nmap Basic Port Scans

## 📝 Room Overview
* **Room Name:** Nmap Basic Port Scans
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Offensive Security Tooling / Reconnaissance

## 🎯 Objective
Learn in-depth how Nmap TCP connect scans, TCP SYN port scans, and UDP port scans work under the hood[span_0](start_span)[span_0](end_span). Understand port states, TCP flags (SYN, RST), and how to fine-tune Nmap's performance using parallelism and timing templates.

---

## 💡 Tasks & Answers

### Task: Basic Services and Port States
* **Question:** Which service uses UDP port 53 by default?
* **Answer:** `DNS`[span_1](start_span)[span_1](end_span)
* **Question:** Which service uses TCP port 22 by default?
* **Answer:** `SSH`[span_2](start_span)[span_2](end_span)
* **Question:** How many port states does Nmap consider?
* **Answer:** `6`[span_3](start_span)[span_3](end_span)
* **Question:** Which port state is the most interesting to discover as a pentester?
* **Answer:** `Open`[span_4](start_span)[span_4](end_span)

### Task: TCP Connect Scan
* **Question:** What 3 letters represent the Reset flag?
* **Answer:** `RST`[span_5](start_span)[span_5](end_span)
* **Question:** Which flag needs to be set when you initiate a TCP connection (first packet of TCP 3-way handshake)?
* **Answer:** `SYN`[span_6](start_span)[span_6](end_span)

### Task: Interpreting Scan Results
* **Question:** What is the state of the FTP service running on port 21?
* **Answer:** `open`[span_7](start_span)[span_7](end_span)
* **Question:** What is Nmap's guess about the service running on port 53?
* **Answer:** `domain`[span_8](start_span)[span_8](end_span)
* **Question:** After launching a TCP SYN scan, how many SYN-ACK packets are successfully received in AttackBox?
* **Answer:** `4`[span_9](start_span)[span_9](end_span)
* **Question:** How many ports are open on the target machine?
* **Answer:** `4`[span_10](start_span)[span_10](end_span)
* **Question:** What is the state of port number 161 over UDP in the target machine?
* **Answer:** `closed`[span_11](start_span)[span_11](end_span)
* **Question:** What is the service name according to Nmap on port 161?
* **Answer:** `snmp`[span_12](start_span)[span_12](end_span)

### Task: Fine-Tuning Scope and Performance
* **Question:** What is the option to scan all the TCP ports between 5000 and 5500?
* **Answer:** `-p5000-5500`[span_13](start_span)[span_13](end_span)
* **Question:** How can you ensure that Nmap will run at least 64 probes in parallel?
* **Answer:** `--min-parallelism=64`[span_14](start_span)[span_14](end_span)
* **Question:** What option would you add to make Nmap very slow and paranoid?
* **Answer:** `-T0`[span_15](start_span)[span_15](end_span)

---

## 🧠 Key Learnings
* **The 6 Port States:** Nmap doesn't just see "open" or "closed." It has 6 states (Open, Closed, Filtered, Unfiltered, Open|Filtered, Closed|Filtered). As a pentester, an `Open` port is your front door, but a `Filtered` port tells you a firewall is actively watching your traffic[span_16](start_span)[span_16](end_span).
* **Controlling Speed vs. Stealth:** 
  * If you want to blast through a network quickly, you increase parallel probes (`--min-parallelism=64`)[span_17](start_span)[span_17](end_span).
  * If you are trying to sneak past an Intrusion Detection System (IDS) that blocks rapid scanning, you use the "Paranoid" timing template (`-T0`), which sends packets painfully slow to avoid triggering alarms[span_18](start_span)[span_18](end_span).
* **UDP vs TCP Service Defaults:** By default, connection-heavy protocols like SSH rely on TCP (Port 22), while fast, query-based protocols like DNS rely on UDP (Port 53)[span_19](start_span)[span_19](end_span). Knowing these defaults helps you quickly identify what a server is primarily used for.
*
