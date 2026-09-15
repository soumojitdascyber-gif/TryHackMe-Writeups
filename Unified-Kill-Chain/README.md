# 🔗 TryHackMe Writeup: Unified Kill Chain

## 📝 Room Overview
* **Room Name:** Unified Kill Chain
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Threat Intelligence

## 🎯 Objective
Understand the Unified Kill Chain (UKC) framework, which establishes the 18 phases of a cyber attack. Learn how attackers plan and execute breaches, and how defenders can use this framework to identify, mitigate, and break the attack chain at various stages.

---

## 💡 Tasks & Answers

### Task: Introduction & Framework Basics
* **Question:** Where does the term "Kill Chain" originate from?
* **Answer:** `Military`
* **Question:** What is the technical term for a piece of software or hardware in IT (Information Technology?)
* **Answer:** `Asset`
* **Question:** In what year was the Unified Kill Chain framework released?
* **Answer:** `2017`
* **Question:** According to the Unified Kill Chain, how many phases are there to an attack?
* **Answer:** `18`

### Task: Kill Chain Phases
* **Question:** What is the name of the attack phase where an attacker employs techniques to evade detection?
* **Answer:** `Defense Evasion`
* **Question:** What is the name of the attack phase where an attacker employs techniques to remove data from a network?
* **Answer:** `Exfiltration`
* **Question:** What is the name of the attack phase where an attacker achieves their objectives?
* **Answer:** `Objectives`

### Task: Tactics and Techniques
* **Question:** What is an example of a tactic to gain a foothold using emails?
* **Answer:** `Phishing`
* **Question:** Impersonating an employee to request a password reset is a form of what?
* **Answer:** `Social Engineering`
* **Question:** An adversary setting up the Command & Control server is what phase of the Unified Kill Chain?
* **Answer:** `Weaponization`
* **Question:** Exploiting a vulnerability present on a system is what phase of the Unified Kill Chain?
* **Answer:** `Exploitation`
* **Question:** Moving from one system to another is an example of?
* **Answer:** `Pivoting`
* **Question:** Leaving behind a malicious service that allows the adversary to log back into the target is what?
* **Answer:** `Persistence`

### Task: SOC Analysis & Scenario Mapping
* **Question:** As a SOC analyst, you pick up an alert pointing to failed logins from an administrator account. What phase of the Unified Kill Chain would an attacker be seeking to achieve?
* **Answer:** `Privilege Escalation`
* **Question:** Mimikatz, a known post-exploitation tool, was detected on the IT Manager's workstation. The Security logs show that the tool was attempting to dump OS and user secrets. Which Unified Kill Chain phase does this activity correspond to?
* **Answer:** `Credential Access`
* **Question:** While monitoring the network as a SOC analyst, you observe a big traffic spike. Most of the network traffic is sent to an unknown, suspicious IP address. What Unified Kill Chain phase could describe this activity?
* **Answer:** `Exfiltration`
* **Question:** Personally identifiable information (PII) has been released to the public by an adversary. Your organisation is facing reputational losses and scrutiny for the breach. What part of the CIA triad would be affected by this action?
* **Answer:** `Confidentiality`

### Task: Practical
* **Question:** Match the scenario prompt to the correct phase of the Unified Kill Chain to reveal the flag at the end. What is the flag?
* **Answer:** `THM{UKC_SCENARIO}`

---

## 🧠 Key Learnings
* **The "Kill Chain" Concept:** Originally a military term, a kill chain is the sequence of events needed to attack a target (e.g., locate target -> aim -> fire). In cybersecurity, if a defender can "break" *any single link* in this chain (e.g., block the phishing email, or stop the malware from calling home), the entire attack fails.
* **Unified Kill Chain (2017):** It merges the older Lockheed Martin Kill Chain with the detailed tactics of the MITRE ATT&CK framework, resulting in 18 distinct phases that better represent modern, complex cyber attacks.
* **Key Phases Explained:**
  * **Weaponization:** Preparing the weapon. (e.g., The attacker sets up a hidden Command & Control server).
  * **Persistence:** Making sure they don't get kicked out if the victim restarts their computer. (e.g., Creating a hidden user account or a malicious startup service).
  * **Privilege Escalation & Credential Access:** Starting as a standard user and stealing the "Master Key" (Administrator passwords/hashes using tools like Mimikatz).
  * **Pivoting / Lateral Movement:** Hacking the receptionist's computer is just the start. "Pivoting" is using that compromised computer as a launchpad to hack deeper into the company's internal servers.
  * **Exfiltration:** Smuggling the stolen data out of the network, which causes a huge traffic spike and breaches the "Confidentiality" of the CIA Triad.
