# 🔄 TryHackMe Writeup: The Hacker Methodology

## 📝 Room Overview
* **Room Name:** The Hacker Methodology
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Offensive Security

## 🎯 Objective
Learn the standard step-by-step process that penetration testers and ethical hackers follow to compromise a target and report their findings.

---

## 💡 Tasks & Answers

### Task: Reconnaissance & Enumeration
* **Question:** What is the first phase of the Hacker Methodology?
* **Answer:** `Reconnaissance`
* **Question:** Who is the CEO of SpaceX?
* **Answer:** `Elon Musk`
* **Question:** Do some research into the tool: sublist3r, what does it list?
* **Answer:** `subdomains`
* **Question:** What is it called when you use Google to look for specific vulnerabilities or to research a specific topic of interest?
* **Answer:** `Google Dorking`
* **Question:** What does enumeration help to determine about the target?
* **Answer:** `Attack Surface`
* **Question:** Do some reconnaissance about the tool: Metasploit, what company developed it?
* **Answer:** `Rapid7`
* **Question:** What company developed the technology behind the tool Burp Suite?
* **Answer:** `portswigger`

### Task: Exploitation & Privilege Escalation
* **Question:** What is one of the primary exploitation tools that pentester(s) use?
* **Answer:** `Metasploit`
* **Question:** In Windows what is usually the other target account besides Administrator?
* **Answer:** `System`
* **Question:** What thing related to SSH could allow you to login to another machine (even without knowing the username or password)?
* **Answer:** `Keys`

### Task: Reporting
* **Question:** What would be the type of reporting that involves a full documentation of all findings within a formal document?
* **Answer:** `full formal report`
* **Question:** What is the other thing that a pentester should provide in a report beyond: the finding name, the finding description, the finding criticality
* **Answer:** `remediation recommendation`

---

## 🧠 Key Learnings
* **The 5 Phases of Hacking:** 
  1. **Reconnaissance:** Gathering open-source intelligence (OSINT) about the target without actively touching their systems (e.g., Google Dorking).
  2. **Enumeration & Scanning:** Actively scanning the target to map out the Attack Surface (finding open ports, services, and hidden directories).
  3. **Exploitation:** Using tools like Metasploit to break into the system using the vulnerabilities found in the previous step.
  4. **Privilege Escalation & Covering Tracks:** Moving from a low-level user to a superadmin (like System in Windows) and stealing SSH Keys to maintain access.
  5. **Reporting:** The most important phase for a professional. Writing a full formal report that not only lists the critical findings but also provides a remediation recommendation so the client can fix the holes.
