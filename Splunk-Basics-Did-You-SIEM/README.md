# 📊 TryHackMe Writeup: Splunk Basics - Did you SIEM?

## 📝 Room Overview
* **Room Name:** Splunk Basics - Did you SIEM?
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / SIEM / Log Analysis

## 🎯 Objective
Learn how to ingest, parse, and analyze custom log data using Splunk. Utilize search queries to track a real-world attack scenario, identifying the attacker's IP, tools, attack vectors (Path Traversal), and data exfiltration metrics.

---

## 💡 Tasks & Answers

### Task: Log Analysis & Attacker Tracking
* **Question:** What is the attacker IP found attacking and compromising the web server?
* **Answer:** `198.51.100.55`
* **Question:** Which day was the peak traffic in the logs? (Format: YYYY-MM-DD)
* **Answer:** `2025-10-12`
* **Question:** What is the count of Havij user_agent events found in the logs?
* **Answer:** `993`
* **Question:** How many path traversal attempts to access sensitive files on the server were observed?
* **Answer:** `658`
* **Question:** Examine the firewall logs. How many bytes were transferred to the C2 server IP from the compromised web server?
* **Answer:** `126167`

---

## 🧠 Key Learnings
* **What is a SIEM (Splunk)?** Imagine your company has 1,000 computers, and each generates thousands of log entries every minute. You cannot read them manually. Splunk (a SIEM) acts like "Google for Logs." It sucks up all that data and lets you search, filter, and create graphs to instantly spot security threats.
* **Tracing the Attack Narrative:** By searching through the logs, we didn't just find isolated alerts; we built a story. We identified:
  * **The Source:** The attacker's IP (`198.51.100.55`).
  * **The Weapon:** The `Havij` User-Agent (a well-known automated SQL Injection tool).
  * **The Tactic:** Over 600 `Path Traversal` attempts (trying to break out of the web directory to read sensitive OS files like `/etc/passwd`).
* **Command & Control (C2) Exfiltration:** After a server is hacked, it usually "calls home" to receive instructions or send stolen data. By pivoting our search from web logs to *firewall logs*, we could see exactly how much data (`126167 bytes`) the compromised server secretly transferred out to the attacker's C2 server.
*
