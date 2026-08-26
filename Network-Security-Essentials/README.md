# 🛡️ TryHackMe Writeup: Network Security Essentials

## 📝 Room Overview
* **Room Name:** Network Security Essentials
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Blue Team / Network Security

## 🎯 Objective
Learn about key aspects of network security essentials and how to monitor and protect against adversaries using Firewall, VPN, and IDS logs.

---

## 💡 Tasks & Investigation Answers

### Task: Analyzing Firewall & VPN Logs
* **Question 1:** What external IP performed the most reconnaissance?
* **Answer:** `203.0.113.45`
* **Question 2:** Which internal host was targeted by scans?
* **Answer:** `10.0.0.20`
* **Question 3:** Which username was targeted in VPN logs?
* **Answer:** `svc_backup`
* **Question 4:** What internal IP was assigned after successful VPN login?
* **Answer:** `10.8.0.23`
* **Question 5:** Which port was used for lateral SMB attempts?
* **Answer:** `445`

### Task: Analyzing IDS & C2 Logs
* **Question 6:** In the IDS logs, which host beaconed to the C2?
* **Answer:** `10.0.0.60`
* **Question 7:** During the investigation, which IP was associated with C2?
* **Answer:** `198.51.100.77`
* **Question 8:** Which host showed the exfiltration attempts?
* **Answer:** `10.0.0.51`

---

## 🧠 Key Learnings
* Gained hands-on experience tracking adversary movements through network logs.
* Correlated logs from Firewalls, VPNs, and Intrusion Detection Systems (IDS).
* Successfully traced an attack lifecycle: Reconnaissance -> Initial Access (VPN) -> Lateral Movement (SMB/445) -> C2 Beaconing -> Data Exfiltration.
*
