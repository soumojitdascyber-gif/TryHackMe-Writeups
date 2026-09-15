# 📖 TryHackMe Writeup: IR Playbooks

## 📝 Room Overview
* **Room Name:** IR Playbooks
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Incident Response

## 🎯 Objective
Learn the basics of creating and using Incident Response (IR) playbooks. Understand how playbooks map to the IR lifecycle phases, how to triage alerts (False Positive vs. True Positive), and practically investigate a WannaCry ransomware infection.

---

## 💡 Tasks & Answers

### Task: IR Process and Playbooks (Preparation to Analysis)
* **Question:** Can multiple use cases trigger a single playbook? y/n
* **Answer:** `y`
* **Question:** What stage of the IR process can be translated into prerequisites for the playbooks?
* **Answer:** `Preparation`

### Task: Containment, Eradication, and Recovery
* **Question:** What steps should we follow if the incident is a False Positive?
* **Answer:** `Close incident`
* **Question:** To recover systems affected by an incident, which configuration should we bring them back to?
* **Answer:** `last known good configuration`

### Task: Post-Incident Activity
* **Question:** What is the last stage of the IR process?
* **Answer:** `Post-incident activity`

### Task: Practical (Malware Investigation)
* **Question:** What is the name of the process that initiated this communication?
* **Answer:** `taskhsvc.exe`
* **Question:** Is this process malicious, as per VirusTotal? y/n
* **Answer:** `y`
* **Question:** What is the name of the parent process of this process?
* **Answer:** `@WanaDecryptor@.exe`
* **Question:** This process's parent was launched by another process, which is a notorious ransomware. Which ransomware is that?
* **Answer:** `Wannacry`
* **Question:** Which playbook should be followed to respond to this incident?
* **Answer:** `malware playbook`
* **Question:** Is this incident an FP (False Positive) or a TP (True Positive)?
* **Answer:** `TP`
* **Question:** In case the incident is a TP, what will be the next step in the IR process?
* **Answer:** `Containment`

---

## 🧠 Key Learnings
* **What is an IR Playbook?** Think of it like a "fire drill manual" for a cyber attack. When an alert fires, an analyst shouldn't have to guess what to do. A playbook gives them a strict, step-by-step checklist to investigate, contain, and eradicate the threat efficiently.
* **FP vs. TP (Triage):** The first active step of a playbook is deciding if the alert is real. 
  * If it's a **False Positive (FP)** (e.g., an IT admin running a legitimate scan), you simply close the incident. 
  * If it's a **True Positive (TP)** (e.g., a real ransomware infection), you immediately move to the **Containment** phase to stop it from spreading.
* **Malware Behavior (Parent-Child Processes):** During the practical, we saw how malware operates. The notorious *WannaCry* ransomware didn't just encrypt files; it launched a parent process (`@WanaDecryptor@.exe`), which then spawned a child process (`taskhsvc.exe`) to execute its malicious tasks. Spotting these relationships in logs is key to confirming a True Positive.
* **Recovery:** After kicking the hacker out (Eradication), you don't just turn the machine back on. You restore the system from a clean backup, returning it to its "last known good configuration" to ensure no hidden backdoors remain.
*
