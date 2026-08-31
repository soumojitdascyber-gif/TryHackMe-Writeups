# ⚔️ TryHackMe Writeup: Common Attacks

## 📝 Room Overview
* **Room Name:** Common Attacks
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Threat Intelligence / Defensive Security

## 🎯 Objective
Analyze standard attack vectors, profile threat actor methodologies, and establish core cyber hygiene practices including MFA implementation and disaster recovery.

---

## 💡 Tasks & Answers

### Task: Malware & Historical Threats
* **Question:** What was the original target of Stuxnet?
* **Answer:** `The Iran Nuclear Programme`
* **Question:** What currency did the Wannacry attackers request payment in?
* **Answer:** `Bitcoin`

### Task: Social Engineering & Phishing
* **Question:** Identify the phishing messages in the static site simulation to retrieve the flag.
* **Answer:** `THM{I_CAUGHT_ALL_THE_PHISH}`

### Task: Passwords and Authentication
* **Question:** Crack the provided MD5 hash using the browser-based hash cracker. What is the password?
* **Answer:** `TryHackMe123!`
* **Question:** Where you have the option, which should you use as a second authentication factor between SMS-based TOTPs or Authenticator App-based TOTPs?
* **Answer:** `App`

### Task: Backups & Disaster Recovery (3-2-1 Rule)
* **Question:** What is the minimum number of up-to-date backups you should make?
* **Answer:** `3`
* **Question:** Of these, how many (at minimum) should be stored in another location?
* **Answer:** `1`

---

## 🧠 Key Learnings
* **Threat History:** Analyzed high-profile historical attacks (Stuxnet, WannaCry) to understand state-sponsored targeting and ransomware monetization mechanics.
* **Authentication Hardening:** Validated the security superiority of Authenticator App-based TOTP over SMS-based TOTP due to the risks of SIM swapping and SS7 vulnerabilities.
* **Disaster Recovery:** Implemented the industry-standard 3-2-1 backup strategy (3 copies of data, 2 different media, 1 offsite) to ensure resilience against localized hardware failures and ransomware encryption.
* **Cryptographic Weaknesses:** Demonstrated the vulnerability of simple passwords hashed with fast algorithms (MD5) against basic dictionary attacks.
*
