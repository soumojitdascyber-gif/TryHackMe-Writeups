# 🥷 TryHackMe Writeup: Red Team Fundamentals

## 📝 Room Overview
* **Room Name:** Red Team Fundamentals
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Offensive Security / Red Team

## 🎯 Objective
Learn the basics of a Red Team engagement, its core components, the stakeholders involved (Red, Blue, and White cells), and how stealthy red teaming significantly differs from standard vulnerability assessments and penetration testing.

---

## 💡 Tasks & Answers

### Task: Vulnerability Assessment and Penetration Testing
* **Question:** Would vulnerability assessments prepare us to detect a real attacker on our networks? (Yay/Nay)
* **Answer:** `Nay`
* **Question:** During a penetration test, are you concerned about being detected by the client? (Yay/Nay)
* **Answer:** `Nay`
* **Question:** Highly organised groups of skilled attackers are nowadays referred to as ...
* **Answer:** `Advanced Persistent Threats`

### Task: Red Team Engagements
* **Question:** The goals of a red team engagement will often be referred to as flags or...
* **Answer:** `crown jewels`
* **Question:** During a red team engagement, common methods used by attackers are emulated against the target. Such methods are usually called TTPs. What does TTP stand for?
* **Answer:** `Tactics, techniques and procedures`
* **Question:** The main objective of a red team engagement is to detect as many vulnerabilities in as many hosts as possible (Yay/Nay)
* **Answer:** `Nay`

### Task: Teams and Functions of an Engagement
* **Question:** What cell is responsible for the offensive operations of an engagement?
* **Answer:** `Red Cell`
* **Question:** What cell is the trusted agent considered part of?
* **Answer:** `White Cell`

### Task: Overview of a Red Team Engagement
* **Question:** If an adversary deployed Mimikatz on a lab machine, where would they be placed in the Lockheed Martin cyber kill chain?
* **Answer:** `Installation`
* **Question:** What technique's purpose is to exploit the target's system to execute code?
* **Answer:** `Exploitation`

### Task: Practical
* **Question:** Click the "View Site" button and follow the example engagement to get the flag
* **Answer:** `THM{RED_TEAM_ROCKS}`

---

## 🧠 Key Learnings
* **Penetration Testing vs. Red Teaming:** 
  * A *Penetration Test* is loud. You try to find as many vulnerabilities as possible in a short time. You don't care if the security team sees you.
  * A *Red Team Engagement* is stealthy. You don't care about finding *all* bugs; your only goal is to sneak in, steal the ultimate prize (the "Crown Jewels"), and test if the Blue Team (defenders) can catch a real, sophisticated hacker (APT).
* **The "Cells" (Team Structure):** 
  * **Red Cell:** The offensive hackers running the attack.
  * **Blue Cell:** The defenders (SOC) trying to stop the attack.
  * **White Cell:** The referees or managers. They know the attack is happening, set the rules, and make sure the Red Team doesn't accidentally break actual company servers.
* **The Cyber Kill Chain:** A step-by-step military model used to describe the phases of a cyber attack. For example, exploiting a vulnerability is the "Exploitation" phase, while dropping a hacking tool (like Mimikatz) onto the server so you can use it later is called the "Installation" phase.
*
