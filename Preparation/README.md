# 🛡️ TryHackMe Writeup: Preparation (Incident Response)

## 📝 Room Overview
* **Room Name:** Preparation
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Incident Response

## 🎯 Objective
Understand the Preparation phase of the Incident Response (IR) lifecycle. Learn the NIST SP 800-61 framework, the difference between an alert and an incident, and how to identify detection gaps through asset inventory and security policy reviews.

---

## 💡 Tasks & Answers

### Task: IR Lifecycle & Triage
* **Question:** What is declared after a threat is confirmed?
* **Answer:** `Incident`
* **Question:** What must be completed on an alert before the IR process can formally begin?
* **Answer:** `Alert Triage`
* **Question:** How many phases does the NIST SP 800-61 IR lifecycle have?
* **Answer:** `4`
* **Question:** According to NIST SP 800-61, what phase follows Containment, Eradication, and Recovery?
* **Answer:** `Post-Incident Activity`

### Task: Visibility, Logging, and Detection
* **Question:** What document tracks the handling of evidence from collection through to storage?
* **Answer:** `Chain of Custody`
* **Question:** What type of log records who performed an action, what the action was, and how the system responded?
* **Answer:** `Audit Log`
* **Question:** What technology provides a centralized platform for collecting and analyzing logs across an organization's infrastructure?
* **Answer:** `SIEM`
* **Question:** What term describes the situation where logs are collected but no alerting rules exist to flag suspicious activity?
* **Answer:** `Detection Gap`

### Task: Policy Review & Asset Inventory (Practical)
* **Question:** According to the asset inventory, what is the IP address of the mail server?
* **Answer:** `10.10.10.2`
* **Question:** According to the pentest report, what authentication control is flagged as missing on standard user accounts?
* **Answer:** `Multi-Factor Authentication`
* **Question:** According to the pentest report, how many high-severity findings were identified?
* **Answer:** `2`
* **Question:** According to the historic incidents log, what type of attack was recorded in NXF-INC-001?
* **Answer:** `Phishing Campaign`
* **Question:** What is the minimum password length configured on this workstation?
* **Answer:** `6`
* **Question:** What is the audit setting configured for Audit account logon events?
* **Answer:** `No auditing`

---

## 🧠 Key Learnings
* **NIST SP 800-61 Framework:** This is the gold standard rulebook for handling cyber attacks. It consists of 4 phases: 1) Preparation, 2) Detection & Analysis, 3) Containment, Eradication & Recovery, 4) Post-Incident Activity.
* **Alert vs. Incident:** An *Alert* is just a warning (e.g., "5 failed logins"). You must investigate (*Triage*) it first. Only when you confirm it's actually an attacker, it officially becomes an *Incident* and the IR team is deployed.
* **Detection Gap:** Imagine having CCTV cameras recording everywhere, but no security guard watching the screens. If a hacker breaks in, the logs are saved, but no alarm rings because no one configured a rule to trigger it. This blind spot is called a Detection Gap.
* **The Importance of Preparation:** If your workstation isn't logging logon events ("No auditing") or users have weak 6-character passwords with no MFA, your IR team will have zero evidence to track down an attacker. Preparation means fixing these policies *before* the attack happens.
*
