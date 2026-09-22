# 🕵️ TryHackMe Writeup: Network Discovery Detection

## 📝 Room Overview
* **Room Name:** Network Discovery Detection[span_1](start_span)[span_1](end_span)
* **Platform:** TryHackMe[span_2](start_span)[span_2](end_span)
* **Difficulty:** Easy
* **Category:** Defensive Security / SOC Analysis

## 🎯 Objective
Understand how attackers discover assets in a network, and how to detect that activity[span_3](start_span)[span_3](end_span). Learn to differentiate between internal vs. external scanning, horizontal vs. vertical scanning, and how to analyze log files (using tools like Kibana and Zeek) to spot reconnaissance patterns.

---

## 💡 Tasks & Answers

### Task: Discovery Concepts & Log Analysis
* **Question:** What do attackers scan, other than, IP addresses, ports, and OS version, in order to identify vulnerabilities in a network?
* **Answer:** `Services`[span_4](start_span)[span_4](end_span)
* **Question:** Which file contains logs that showcase internal scanning activity?
* **Answer:** `log-session-2.csv`[span_5](start_span)[span_5](end_span)
* **Question:** How many log entries are present for the internal IP performing internal scanning activity?
* **Answer:** `2276`[span_6](start_span)[span_6](end_span)
* **Question:** What is the external IP address that is performing external scanning activity?
* **Answer:** `203.0.113.25`[span_7](start_span)[span_7](end_span)

### Task: The Mechanics of Scanning (Horizontal vs Vertical)
* **Question:** One of the log files contains evidence of a horizontal scan. Which IP range was scanned? Format X.X.X.X/X
* **Answer:** `203.0.113.0/24`[span_8](start_span)[span_8](end_span)
* **Question:** In the same log file, there is one IP address on which a vertical scan is performed. Which IP address is this?
* **Answer:** `192.168.230.145`[span_9](start_span)[span_9](end_span)
* **Question:** On one of the IP addresses, only a few ports are scanned which host common services. Which are the ports that are scanned on this IP address? Format: port1, port2, port3 in ascending order.
* **Answer:** `80, 445, 3389`[span_10](start_span)[span_10](end_span)

### Task: Conclusion / Kibana Dashboard Analysis
* **Question:** Which source IP performs a ping sweep attack across a whole subnet?
* **Answer:** `192.168.230.127`[span_11](start_span)[span_11](end_span)
* **Question:** The zeek.conn.conn_state value shows the connection state. Using the information provided by this value, identify the type of scan being performed by 203.0.113.25 against 192.168.230.145
* **Answer:** `TCP SYN Scan`[span_12](start_span)[span_12](end_span)
* **Question:** Is there any UDP scanning attempt in the logs? Y/N
* **Answer:** `N`[span_13](start_span)[span_13](end_span)

---

## 🧠 Key Learnings
* **Horizontal vs. Vertical Scanning:** 
  * **Horizontal Scan:** Imagine a thief walking down a street checking the *front door* of every single house to see which one is unlocked[span_14](start_span)[span_14](end_span). In networking, this is scanning a single port (like Port 80 for HTTP) across an entire range of IP addresses (like a /24 subnet)[span_15](start_span)[span_15](end_span).
  * **Vertical Scan:** Imagine a thief focusing on *one specific house* and trying to open every single door and window[span_16](start_span)[span_16](end_span). In networking, this is scanning hundreds of different ports on one single target IP address (e.g., `192.168.230.145`)[span_17](start_span)[span_17](end_span).
* **Spotting Scans in Logs:** Attackers use tools like Nmap to perform TCP SYN Scans (half-open scans)[span_18](start_span)[span_18](end_span). As a defender, you can spot these in network logs (like Zeek logs) by looking for thousands of connection attempts originating from a single IP within a very short timeframe, often with a connection state indicating incomplete handshakes[span_19](start_span)[span_19](end_span).
* **Internal vs External Scanners:** An external IP (`203.0.113.25`)[span_20](start_span)[span_20](end_span) scanning your network is likely an attacker doing reconnaissance. However, if an internal IP is doing thousands of scans (`2276` entries)[span_21](start_span)[span_21](end_span), it means an attacker has probably already compromised a machine inside your network and is trying to move laterally.
*
