# 🚨 TryHackMe Writeup: SOC L1 Alert Triage

## 📝 Room Overview
* **Room Name:** SOC L1 Alert Triage
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Blue Team / SIEM

## 🎯 Objective
The objective of this room is to simulate a Tier 1 SOC Analyst's daily workflow. It involves navigating a SIEM dashboard, analyzing security alerts, investigating logs, and determining whether the alerts are True Positives or False Positives.

---

## 💡 Tasks & Investigation Steps

### Alert 1: First-Priority Alert
* **Investigation:** Analyzed the SIEM logs to identify unusual activities and verified the context of the alert.
* **Flag Received:** `THM{looks_like_lots_of_zoom_meetings}`

### Alert 2: Second-Priority Alert
* **Investigation:** Investigated the suspected phishing/malicious activity and traced the source within the provided dashboard.
* **Flag Received:** `THM{how_could_this_user_fall_for_it?}`

### Alert 3: Third-Priority Alert
* **Investigation:** Correlated the events related to unauthorized or suspicious application usage by analyzing the source and destination logs.
* **Flag Received:** `THM{should_we_allow_github_for_devs?}`

---

## 🧠 Key Learnings
* Gained hands-on experience in triaging alerts using a simulated SIEM environment.
* Learned how to effectively distinguish between False Positives and True Positives.
* Improved log analysis and critical thinking skills for Incident Response.
*
