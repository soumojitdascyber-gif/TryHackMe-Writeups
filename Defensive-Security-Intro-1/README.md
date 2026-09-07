# 🛡️ TryHackMe Writeup: Defensive Security Intro

## 📝 Room Overview
* **Room Name:** Defensive Security Intro
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / SOC

## 🎯 Objective
Experience a simulated cyber attack on FakeBank to understand the primary responsibilities of a defensive security team, including alert triaging, containment, intelligence gathering, and incident reporting.

---

## 💡 Tasks & Answers

### Task: Introduction
* **Question:** What does the acronym "SOC" stand for?
* **Answer:** `Security Operations Centre`

### Task: Phase 2: Stopping the Attack
* **Question:** Review the "Suspicious Login" alert. What username is being used?
* **Answer:** `dave.saunders`

### Task: Phase 3: Investigating the Attacker
* **Question:** Lock the dave.saunders account by clicking the padlock icon next to the name. What value (flag) has appeared once this was done?
* **Answer:** `THM{ACCOUNT-LOCKED}`

### Task: Phase 4: Submitting Your Report
* **Question:** Update FakeBank's systems to include what page - and username - ShadowFigures tried to hack. A green success message will appear. What is the value (flag) of that?
* **Answer:** `THM{INTEL-UPDATED}`
* **Question:** What is the Identifier of the incident report that you submit?
* **Answer:** `SEC-2026-341`

---

## 🧠 Key Learnings
* **The SOC (Security Operations Centre):** The central hub of defensive security. It's like the digital CCTV control room of a company, monitoring for any suspicious activity.
* **Triage & Investigation (Finding the leak):** When an alert fires (e.g., a "Suspicious Login"), the first step is figuring out *who* or *what* is compromised. In this scenario, Dave Saunders' account was breached.
* **Containment (Stopping the bleeding):** You cannot investigate properly while the attacker is still actively destroying things. The immediate action is to block the attacker's access—such as locking Dave's compromised account.
* **Threat Intelligence & Remediation:** Once the attack is stopped, you analyze the attacker's tools and methods (e.g., the ShadowFigures group). You use this intel to update the company's defense systems so this specific attack never works again.
* **Incident Reporting:** Every action taken during an attack must be officially documented with a unique tracking ID (like `SEC-2026-341`). This is crucial for legal reasons, post-incident reviews, and training.
*
