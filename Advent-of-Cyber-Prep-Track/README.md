# 🎄 TryHackMe Writeup: Advent of Cyber Prep Track

## 📝 Room Overview
* **Room Name:** Advent of Cyber Prep Track
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / General

## 🎯 Objective
Complete a series of 10 short, interactive missions designed to build essential cyber security skills. Topics include password security, malware scanning, command-line interface (CLI) navigation, OSINT, and log analysis.

---

## 💡 Tasks & Answers

### Task 5: Challenge 1 - Password Pandemonium
* **Question:** What's the flag?
* **Answer:** `THM{StrongStart}`

### Task 6: Challenge 2 - The Suspicious Chocolate.exe
* **Question:** What's the flag?
* **Answer:** `THM{NotSoSweet}`

### Task 7: Challenge 3 - Welcome to the AttackBox!
* **Question:** What's the flag?
* **Answer:** `THM{Ready2Hack}`

### Task 8: Challenge 4 - The CMD Conundrum
* **Question:** What's the flag?
* **Answer:** `THM{WhereIsMcSkidy}`

### Task 9: Challenge 5 - Linux Lore
* **Question:** What's the flag?
* **Answer:** `THM{TrustNoBunny}`

### Task 10: Challenge 6 - The Leak in the List
* **Question:** What's the flag?
* **Answer:** `THM{LeakedAndFound}`

### Task 11: Challenge 7 - WiFi Woes in Wareville
* **Question:** What's the flag?
* **Answer:** `THM{NoMoreDefault}`

### Task 12: Challenge 8 - The App Trap
* **Question:** What's the flag?
* **Answer:** `THM{AppTrapped}`

### Task 13: Challenge 9 - The Chatbot Confession
* **Question:** What's the flag?
* **Answer:** `THM{DontFeedTheBot}`

### Task 14: Challenge 10 - The Bunny's Browser Trail
* **Question:** What's the flag?
* **Answer:** `THM{EastmasIsComing}`

---

## 🧠 Key Learnings
* **Command-Line Investigations (Windows & Linux):** Graphical interfaces (GUIs) often hide things. By using CLI commands like `dir /a` (Windows) or `ls -la` (Linux), defenders can uncover hidden folders and secret files that attackers try to conceal on compromised workstations.
* **Malware Analysis Basics:** You shouldn't blindly run unknown files (like `chocolate.exe`). Using simulated tools or platforms like VirusTotal helps defenders check the file's hash against known malware databases to determine if it is safe or malicious.
* **OSINT & Credential Leaks:** Reusing passwords is a massive risk. Using Breach Checkers allows defenders to verify if an employee's email (e.g., `mcskidy@tbfc.com`) was involved in a public data breach, which could lead to credential stuffing attacks.
* **Securing Configurations (WiFi & OAuth Apps):** 
  * Leaving a router with default credentials (`admin:admin`) is like leaving the front door wide open.
  * Third-party apps connected to your accounts can go rogue. Regularly reviewing and revoking access to apps with unusual permissions (like "Password Vault" access) stops data leaks before they start.
* **Log Analysis & Privacy:** Automated bots leave footprints. By analyzing HTTP logs for unusual `User-Agent` strings (like `BunnyOS/1.0`), defenders can identify automated attacks. Similarly, reviewing chatbot inputs prevents users from accidentally oversharing sensitive internal URLs or passwords with AI tools.
*
