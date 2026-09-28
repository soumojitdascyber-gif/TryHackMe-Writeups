# 📝 TryHackMe Writeup: Report Writing for SOC L2

## 📝 Room Overview
* **Room Name:** Report Writing for SOC L2
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / SOC

## 🎯 Objective
Explore a vital skill for any senior role in a SOC: report writing. Learn how to draft executive summaries, create attack timelines, communicate with non-technical stakeholders, and utilize GenAI securely for context building.

---

## 💡 Tasks & Answers

### Task: Leadership Communication
* **Question:** Which SOC tier, L1 or L2, bridges the SOC and the outside world?
* **Answer:** `L2`
* **Question:** What do L2 analysts write to summarize SOC findings (one word)?
* **Answer:** `Reports`

### Task: The Executive Summary
* **Question:** Should you complete the analysis after sharing the initial SOC report? (Yea/Nay)
* **Answer:** `Yea`
* **Question:** Should you keep your team informed about the ongoing communication? (Yea/Nay)
* **Answer:** `Yea`
* **Question:** What flag did you receive after completing the task's challenge?
* **Answer:** `THM{executive_summary_approved}`

### Task: Handover Notes
* **Question:** Are L2 handover notes meant for a non-technical audience? (Yea/Nay)
* **Answer:** `Nay`
* **Question:** What part of the handover notes lists your findings chronologically?
* **Answer:** `Attack Timeline`
* **Question:** What flag did you receive after completing the task's challenge?
* **Answer:** `THM{trysaveme_would_be_proud}`

### Task: GenAI for Reports
* **Question:** What should you provide in the AI prompt to get the best reports?
* **Answer:** `Context`
* **Question:** Should you fully rely on GenAI for critical decision making? (Yea/Nay)
* **Answer:** `Nay`

---

## 🧠 Key Learnings
* **L2 Analyst Role:** While L1 analysts triage alerts, L2 analysts dive deeper into the investigation and bridge the gap between the technical SOC team and the outside business world by writing detailed Reports.
* **Executive Summaries vs Handover Notes:** 
  * *Executive Summaries* are for management and non-technical stakeholders. They focus on business impact and high-level findings.
  * *Handover Notes* are highly technical, containing chronologically ordered Attack Timelines, and are meant for other security professionals.
* **Using AI in SOC:** Generative AI is a great assistant for drafting reports, provided you give it proper Context. However, you should never blindly rely on AI for critical security decisions because it can hallucinate or misinterpret technical logs.
*
