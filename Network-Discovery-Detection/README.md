# 🕵️ TryHackMe Writeup: Network Discovery Detection

## 📝 Room Overview
* **Room Name:** Network Discovery Detection
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / SOC Analysis

## 🎯 Objective
Understand how attackers discover assets in a network, and how to detect that activity. Learn to differentiate between internal vs. external scanning, horizontal vs. vertical scanning, and how to analyze log files (using tools like Kibana and Zeek) to spot reconnaissance patterns.

---

## 💡 Tasks & Answers

### Task: Discovery Concepts & Log Analysis
* **Question:** What do attackers scan, other than, IP addresses, ports, and OS version, in order to identify vulnerabilities in a network?
* **Answer:** `Services`
* **Question:** Which file contains logs that showcase internal scanning activity?
* **Answer:** `log-session-2.csv`
* **Question:** How many log entries are present for the internal IP performing internal scanning activity?
* **Answer:** `2276`
* **Question:** What is the external IP address that is performing external scanning activity?
* **Answer:** `203.0.113.25`

### Task: The Mechanics of Scanning (Horizontal vs Vertical)
* **Question:** One of the log files contains evidence of a horizontal scan. Which IP range was scanned? Format X.X.X.X/X
* **Answer:** `203.0.113.0/24`
* **Question:** In the same log file, there is one IP address on which a vertical scan is performed. Which IP address is this?
* **Answer:** `192.168.230.145`
* **Question:** On one of the IP addresses, only a few ports are scanned which host common services. Which are the ports that are scanned on this IP address? Format: port1, port2, port3 in ascending order.
* **Answer:** `80, 445, 3389`
### Task: Conclusion / Kibana Dashboard Analysis
* **Question:** Which source IP performs a ping sweep attack across a whole subnet?
* **Answer:** `192.168.230.127`
* **Question:** The zeek.conn.conn_state value shows the connection state. Using the information provided by this value, identify the type of scan being performed by 203.0.113.25 against 192.168.230.145
* **Answer:** `TCP SYN Scan`
* **Question:** Is there any UDP scanning attempt in the logs? Y/N
* **Answer:** `N`
---

## 🧠 Key Learnings
* **Horizontal vs. Vertical Scanning:** 
  * **Horizontal Scan:** Imagine a thief walking down a street checking the *front door* of every single house to see which one is unlocked. In networking, this is scanning a single port (like Port 80 for HTTP) across an entire range of IP addresses (like a /24 subnet).
  * **Vertical Scan:** Imagine a thief focusing on *one specific house* and trying to open every single door and window. In networking, this is scanning hundreds of different ports on one single target IP address (e.g., `192.168.230.145`).
* **Spotting Scans in Logs:** Attackers use tools like Nmap to perform TCP SYN Scans (half-open scans). As a defender, you can spot these in network logs (like Zeek logs) by looking for thousands of connection attempts originating from a single IP within a very short timeframe, often with a connection state indicating incomplete handshakes.
* **Internal vs External Scanners:** An external IP (`203.0.113.25`) scanning your network is likely an attacker doing reconnaissance. However, if an internal IP is doing thousands of scans (`2276` entries), it means an attacker has probably already compromised a machine inside your network and is trying to move laterally.
*
