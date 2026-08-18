# 🚨 SOC L1 Alert Reporting (TryHackMe)

## 🎯 Objective
Learn the standardized process for reporting, escalating, and communicating high-risk security alerts within a Security Operations Center (SOC) environment.

## 🧠 Core Concepts & Execution
* **Execution Environment:** Web-based SOC Dashboard Emulator
* **Tasks Performed:**
  * Analyzed incoming phishing alerts, including sender verification (`support@microsoft.com`) and target identification (`m.boslan@tryhackme.thm`).
  * Utilized the "Five Ws" (Who, What, When, Where, Why) template to document incident details clearly and precisely.
  * Managed alert lifecycles by updating statuses to "In Progress" and documenting investigation findings.
  * Performed alert escalation to L2 analysts (E. Fleming) upon verification of malicious activity.
  * Assigned proper verdicts (True Positive/False Positive) based on investigation outcomes.

## 🚩 Proof of Compromise
* **Flag(s) Found:** 
  * `THM{nice_attempt_faking_microsoft_support}`
  * `THM{good_job_escalating_your_first_alert}`
  * `THM{looks_like_webshell_via_old_exchange}`

## 💡 Security Takeaway
Accurate reporting and structured escalation are the cornerstones of effective incident response. Mastering the "Five Ws" ensures that L2/L3 analysts receive high-quality data, which significantly reduces Mean Time to Respond (MTTR) and prevents critical details from being lost during handovers.
