# 🛡️ TryHackMe Writeup: Introduction to EDR

## 📝 Room Overview
* **Room Name:** Introduction to EDR
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Blue Team / Endpoint Security

## 🎯 Objective
Learn the fundamentals of Endpoint Detection and Response (EDR), explore its features, understand how it works beyond traditional Antivirus, and investigate alerts using EDR telemetry.

---

## 💡 Tasks & Investigation Answers

### Investigating Alerts on EDR (Task 7)
* **Question 1:** Which tool was launched by CMD.exe to download the payload on DESKTOP-HR01?
* **Answer:** `CURL.exe`

* **Question 2:** What is the absolute path to the downloaded malware on the DESKTOP-HR01 machine?
* **Answer:** `C:\Users\Public\install.exe`

* **Question 3:** What is the absolute path to the suspicious syncsvc.exe on the WIN-ENG-LAPTOP03 machine?
* **Answer:** `C:\Users\haris.khan\AppData\Local\Temp\syncsvc.exe`

* **Question 4:** On which URL was the exfiltration attempt being made on WIN-ENG-LAPTOP03?
* **Answer:** `https://files-wetransfer.com/upload/session/ab12cd34ef56/dump_2025.dmp`

* **Question 5:** What was UpdateAgent.exe labelled by Threat Intel on DESKTOP-DEV01?
* **Answer:** `Known internal IT utility tool`

---

## 🧠 Key Learnings
* Understood the limitations of traditional Antivirus and the necessity of EDR solutions.
* Learned how EDR telemetry collects and analyzes endpoint data for threat hunting.
* Practically investigated a simulated EDR alert by tracing malicious processes, payload paths, and exfiltration attempts.
*
