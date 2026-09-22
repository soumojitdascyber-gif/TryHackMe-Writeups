# 🔍 TryHackMe Writeup: DFIR: An Introduction

## 📝 Room Overview
* **Room Name:** DFIR: An Introduction[span_16](start_span)[span_16](end_span)
* **Platform:** TryHackMe[span_17](start_span)[span_17](end_span)
* **Difficulty:** Easy
* **Category:** Defensive Security / Incident Response

## 🎯 Objective
Introductory room for the DFIR module[span_18](start_span)[span_18](end_span). Learn the basic concepts of combining digital forensics with incident response, understand data volatility, and navigate the core phases of the IR lifecycle.

---

## 💡 Tasks & Answers

### Task: Basic Concepts & Tools
* **Question:** What does DFIR stand for?
* **Answer:** `Digital Forensics and Incident Response`[span_19](start_span)[span_19](end_span)[span_20](start_span)[span_20](end_span)
* **Question:** DFIR requires expertise in two fields. One of the fields is Digital Forensics. What is the other field?
* **Answer:** `Incident Response`[span_21](start_span)[span_21](end_span)[span_22](start_span)[span_22](end_span)
* **Question:** From amongst the RAM and the hard disk, which storage is more volatile?
* **Answer:** `RAM`[span_23](start_span)[span_23](end_span)
* **Question:** Complete the timeline creation exercise in the attached static site. What is the flag that you get after completion?
* **Answer:** `THM{DFIR_REPORT_DONE}`[span_24](start_span)[span_24](end_span)

### Task: Incident Response Process
* **Question:** At what stage of the IR process is the threat evicted from the network after performing the forensic analysis?
* **Answer:** `Eradication`[span_25](start_span)[span_25](end_span)
* **Question:** At what stage of the IR process are disrupted services brought back online as they were before the incident?
* **Answer:** `Recovery`[span_26](start_span)[span_26](end_span)
* **Question:** What is the NIST-equivalent of the step called "Lessons learned" in the SANS process?
* **Answer:** `Post-incident Activity`[span_27](start_span)[span_27](end_span)

---

## 🧠 Key Learnings
* **The Synergy of DFIR:** **D**igital **F**orensics and **I**ncident **R**esponse are two halves of the same coin[span_28](start_span)[span_28](end_span). While IR focuses on stopping the bleeding and kicking the attacker out, Digital Forensics investigates *how* they got in by analyzing digital evidence[span_29](start_span)[span_29](end_span)[span_30](start_span)[span_30](end_span).
* **Order of Volatility (RAM vs. Disk):** When collecting evidence, responders must grab the most volatile data first. **RAM** is highly volatile (data disappears if the computer loses power), whereas a hard disk holds data permanently[span_31](start_span)[span_31](end_span).
* **The IR Lifecycle in Action:**
  * **Eradication:** This is where you actively evict the threat from the network based on forensic analysis[span_32](start_span)[span_32](end_span).
  * **Recovery:** Carefully bringing disrupted systems back online to normal operations[span_33](start_span)[span_33](end_span).
  * **Post-incident Activity:** Often called "Lessons Learned" in SANS, this is where the team figures out how to prevent the attack from ever happening again[span_34](start_span)[span_34](end_span).
