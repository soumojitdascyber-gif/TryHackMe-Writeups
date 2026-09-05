# 📈 TryHackMe Writeup: Defensive Security Trends

## 📝 Room Overview
* **Room Name:** Defensive Security Trends
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Threat Intelligence

## 🎯 Objective
Explore the modern security landscape to understand emerging trends, including supply chain vulnerabilities, the Infostealer-to-Ransomware pipeline, RMM abuse, and the realistic role of AI in SOC operations.

---

## 💡 Tasks & Answers

### Task: Supply Chain Attacks
* **Question:** The GitHub breach started from an infection of an employee's device. Which VS Code extension was backdoored with an infostealer?
* **Answer:** `Nx Console`
* **Question:** The extension was compromised through another supply chain attack. Which open-source package ecosystem was the root cause?
* **Answer:** `TanStack`
* **Question:** Refer to the explained Vercel supply chain incident. What malware was the first link in the attack chain?
* **Answer:** `Lumma Stealer`
* **Question:** Imagine a supply chain attack hits your organization. Would attack TTPs fundamentally differ from other intrusions? (Yea/Nay)
* **Answer:** `Nay`

### Task: Valid Accounts & Initial Access Brokers
* **Question:** Refer to the screenshot of the Verizon 2024 report. What percentage of incidents contained Valid accounts?
* **Answer:** `39%`
* **Question:** How do you call cyber criminals who sell access to organizations' networks?
* **Answer:** `Initial Access Brokers`
* **Question:** Continue to the Infostealer to ransomware pipeline section a few pages later. Which access type do Initial Access Brokers most commonly sell?
* **Answer:** `VPN`

### Task: RMM Abuse & Perimeter Defense
* **Question:** Open the Verizon report to page 40 (System Intrusion section). How much has threat actor RMM usage grown year-over-year?
* **Answer:** `240%`
* **Question:** Which of the mentioned remote access tools was used by DarkGate malware?
* **Answer:** `AnyDesk`
* **Question:** Is the network perimeter becoming more predictable in modern environments? (Yea/Nay)
* **Answer:** `Nay`

### Task: SOC Response & AI Integration
* **Question:** Refer to the mentioned Huntress report. What is the reported average time-to-ransomware?
* **Answer:** `17 hours`
* **Question:** What should SOCs do with triage routine to speed up response?
* **Answer:** `Automate it`
* **Question:** Should AI become a final decision maker in a SOC? (Yea/Nay)
* **Answer:** `Nay`
* **Question:** Which MITRE technique became obsolete due to AI?
* **Answer:** `None`

---

## 🧠 Key Learnings
* **The Modern Attack Pipeline:** Hackers no longer need to "break down the door." They use an infostealer (like *Lumma Stealer*) to quietly steal a legitimate employee's VPN credentials. *Initial Access Brokers* sell this login data to ransomware gangs. Because they log in using "Valid Accounts" (seen in 39% of attacks), it bypasses normal security alerts.
* **Speed of Attack (Time-to-Ransomware):** Once a hacker logs in, they are incredibly fast. The average time before they encrypt the network with ransomware is just 17 hours. SOCs must *automate* their triage process to catch them in this short window.
* **RMM Abuse (Blending In):** Instead of using suspicious custom hacking tools, attackers now use normal IT support software like *AnyDesk* (used by DarkGate malware). This tactic grew by 240% because antivirus programs assume it's just the IT department fixing a computer.
* **AI's True Role in Security:** AI is a powerful assistant to automate boring tasks and process logs faster, but a human must always be the final decision maker (No to auto-blocking critical infrastructure). AI doesn't make old hacking techniques obsolete; it just executes them faster.
*
