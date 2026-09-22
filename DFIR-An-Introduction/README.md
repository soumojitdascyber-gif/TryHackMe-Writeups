# 🔍 TryHackMe Writeup: DFIR: An Introduction

## 📝 Room Overview
* **Room Name:** DFIR: An Introduction.
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Incident Response

## 🎯 Objective
Introductory room for the DFIR module. Learn the basic concepts of combining digital forensics with incident response, understand data volatility, and navigate the core phases of the IR lifecycle.

---

## 💡 Tasks & Answers

### Task: Basic Concepts & Tools
* **Question:** What does DFIR stand for?
* **Answer:** `Digital Forensics and Incident Response`
* **Question:** DFIR requires expertise in two fields. One of the fields is Digital Forensics. What is the other field?
* **Answer:** `Incident Response`
* **Question:** From amongst the RAM and the hard disk, which storage is more volatile?
* **Answer:** `RAM`
* **Question:** Complete the timeline creation exercise in the attached static site. What is the flag that you get after completion?
* **Answer:** `THM{DFIR_REPORT_DONE}`

### Task: Incident Response Process
* **Question:** At what stage of the IR process is the threat evicted from the network after performing the forensic analysis?
* **Answer:** `Eradication`
* **Question:** At what stage of the IR process are disrupted services brought back online as they were before the incident?
* **Answer:** `Recovery`
* **Question:** What is the NIST-equivalent of the step called "Lessons learned" in the SANS process?
* **Answer:** `Post-incident Activity`
---

## 🧠 Key Learnings
* **The Synergy of DFIR:** **D**igital **F**orensics and **I**ncident **R**esponse are two halves of the same coin. While IR focuses on stopping the bleeding and kicking the attacker out, Digital Forensics investigates *how* they got in by analyzing digital evidence.
* **Order of Volatility (RAM vs. Disk):** When collecting evidence, responders must grab the most volatile data first. **RAM** is highly volatile (data disappears if the computer loses power), whereas a hard disk holds data permanently.
* **The IR Lifecycle in Action:**
  * **Eradication:** This is where you actively evict the threat from the network based on forensic analysis.
  * **Recovery:** Carefully bringing disrupted systems back online to normal operation.
  * **Post-incident Activity:** Often called "Lessons Learned" in SANS, this is where the team figuress[ out how to prevent the attack from ever happening again.
