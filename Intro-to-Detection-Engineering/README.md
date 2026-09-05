# 🧠 TryHackMe Writeup: Intro to Detection Engineering

## 📝 Room Overview
* **Room Name:** Intro to Detection Engineering
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Detection Engineering

## 🎯 Objective
Understand the core principles of Detection Engineering, how detection teams operate inside a SOC, and how to build, test, and maintain robust alert logic using the Detection Engineering Life Cycle.

---

## 💡 Tasks & Answers

### Task: Detection Engineering Life Cycle & Simulation
* **Question:** What is the first flag?
* **Answer:** `THM{PR0ACT1V3_D3T3CT10N_3NG1N33R}`
* **Question:** What is the second flag?
* **Answer:** `THM{V3RS10N_C0NTR0L_1S_K3Y}`
* **Question:** What is the third flag?
* **Answer:** `THM{D4T4_R3V13W_B3F0R3_D3S1GN}`
* **Question:** What is the fourth flag?
* **Answer:** `THM{P33R_R3V13W_B3F0R3_D3PL0Y}`
* **Question:** What is the fifth flag?
* **Answer:** `THM{PR3C1S10N_PR0BL3M_D3T3CT3D}`
* **Question:** What is the sixth flag?
* **Answer:** `THM{B3HAV10UR_0V3R_10CS}`
* **Question:** What is the seventh flag?
* **Answer:** `THM{D3_G03S_B3Y0ND_RUL3S}`
* **Question:** What is the eighth flag?
* **Answer:** `THM{D3T3CT10N_L1BR4RY_D3GR4D3S}`

---

## 🧠 Key Learnings
* **What is Detection Engineering?:** Instead of waiting for an alarm to go off, a Detection Engineer builds the actual alarm system. You study how attackers break in and write precise rules so the SOC gets notified immediately when suspicious activity happens.
* **Behaviour Over IOCs:** Just like we learned in the Pyramid of Pain, writing rules for specific IP addresses or hashes is useless because attackers change them instantly. Great detection engineers write rules that catch attacker *behaviour* (e.g., "Alert me whenever a word document launches PowerShell").
* **Data Review Before Design:** You cannot detect what you do not log. Before writing a rule, you must verify that your servers are actually recording the right events (telemetry) needed to catch the threat.
* **Detection as Code (Git & Peer Review):** Detection rules should be treated like software. You keep them in version control (like GitHub) and have teammates review them (`Peer Review`) before turning them on in production to avoid flooding the SOC with false alarms.
* **Detection Decay:** Old detection rules go stale. As systems update and company tools change, existing rules will either stop working or start firing false alerts. A detection library must be constantly tested and tuned.
*
