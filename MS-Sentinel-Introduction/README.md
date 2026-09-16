# 🛡️ TryHackMe Writeup: MS Sentinel: Introduction

## 📝 Room Overview
* **Room Name:** MS Sentinel: Introduction
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / SOC Tooling

## 🎯 Objective
Understand the fundamentals of Microsoft Sentinel, a cloud-native SIEM and SOAR solution. Learn how it fits into a Security Operations Center (SOC), the difference between Level 1 and Level 2 analysts, and how automation helps prevent alert fatigue.

---

## 💡 Tasks & Answers

### Task: Microsoft Security Operations Analyst
* **Question:** What security unit is responsible for protecting the organization against security threats?
* **Answer:** `Security Operations Center`
* **Question:** Generally, which level of SOC Analyst is responsible for responding to incidents?
* **Answer:** `SOC Level 2 Analyst`
* **Question:** Besides monitoring, what else do SOC Level 1 Analysts spend the majority of their time with?
* **Answer:** `triage`

### Task: Microsoft Sentinel Core Concepts
* **Question:** Microsoft Sentinel is a combination of two security concepts, namely SIEM and which other one?
* **Answer:** `SOAR`
* **Question:** Creating security alerts and incidents is part of which security concept?
* **Answer:** `SIEM`
* **Question:** By means of how many pillars does Microsoft Sentinel help us to perform security operations?
* **Answer:** `4`

### Task: Sentinel Architecture & Automation
* **Question:** What is used to ingest data into Sentinel?
* **Answer:** `data connectors`
* **Question:** Where are the ingested logs stored for further correlation and analysis?
* **Answer:** `log analytics workspaces`
* **Question:** Workbooks are essentially _____ used for visualization.
* **Answer:** `dashboards`
* **Question:** When SOC teams are flooded with security alerts and incidents, this is called?
* **Answer:** `alert fatigue`
* **Question:** In Microsoft Sentinel, automation is done via automated workflows, known as?
* **Answer:** `playbooks`
* **Question:** The output of running Analytics rules includes security alerts and?
* **Answer:** `Incidents`

### Task: Conclusion
* **Question:** Organizations use Microsoft Sentinel mainly because they need to _____ their cloud infrastructure.
* **Answer:** `monitor`
* **Question:** With Microsoft Sentinel, there is no need for server provisioning. This means it is?
* **Answer:** `cloud-native`

---

## 🧠 Key Learnings
* **SIEM vs. SOAR:** 
  * **SIEM (Security Information and Event Management):** The "Brain". It collects logs from everywhere and analyzes them to detect an attack (e.g., "Someone is trying to brute-force a login").
  * **SOAR (Security Orchestration, Automation, and Response):** The "Hands". Instead of waiting for a human, it automatically responds to the SIEM's alert (e.g., automatically blocking the attacker's IP using a "Playbook"). Sentinel does both.
* **Cloud-Native Advantage:** Unlike traditional SIEMs where you have to buy, install, and maintain expensive physical servers, Sentinel is "cloud-native." It lives entirely in Microsoft Azure, meaning it can scale up instantly without you needing to manage any hardware.
* **Alert Fatigue:** Imagine a car alarm that goes off every 5 minutes because of the wind. Eventually, people stop checking on it. In a SOC, if analysts get 10,000 low-priority alerts a day, they get "Alert Fatigue" and might miss a real attack. Sentinel uses SOAR (automated playbooks) to filter the noise so analysts only see what matters.
* **SOC Tiers:** 
  * *Level 1 Analysts* mostly do "Triage" (filtering out the False Positives from the True Positives).
  * *Level 2 Analysts* take the True Positives and actively respond/investigate the incident deeper.
