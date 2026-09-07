# 🎯 TryHackMe Writeup: Threat Hunting: Introduction

## 📝 Room Overview
* **Room Name:** Threat Hunting: Introduction
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Threat Hunting

## 🎯 Objective
Learn the foundational concepts, approaches, and techniques of threat hunting. Understand how to proactively search for undetected adversaries in a network using indicators, intelligence, and behavioral patterns.

---

## 💡 Tasks & Answers

### Task: Hunting Approaches
* **Question:** What is the average number of days an attacker remains undetected in a network called?
* **Answer:** `dwell time`
* **Question:** Is threat hunting reactive or proactive?
* **Answer:** `proactive`

### Task: Hunting Targets
* **Question:** Which threat hunting approach would you use if you have received threat intelligence about an APT group targeting your industry?
* **Answer:** `intelligence-driven hunting`
* **Question:** Which threat hunting approach is most efficient when you have a list of file hashes and IOCs from a threat feed?
* **Answer:** `indicator-driven hunting`

### Task: Hunting Techniques
* **Question:** What category of hunting target represents artifacts left behind by attackers during their attack?
* **Answer:** `attack residues`
* **Question:** Which hunting technique uses file hashes, IP addresses, and domain names to search for specific artifacts?
* **Answer:** `Indicators of compromise`
* **Question:** What hunting technique is represented by searching for: "Word.exe spawns cmd.exe spawns powershell.exe that connects to external IP"?
* **Answer:** `behavioral pattern analysis`

### Task: Practical (APT-Serpent Simulation)
* **Question:** How many known campaigns has APT-Serpent conducted since 2021?
* **Answer:** `4`
* **Question:** In which phase of the attack does CustomBackdoor get dropped?
* **Answer:** `Execution & Persistence`
* **Question:** What is the primary initial access vector used by APT-Serpent?
* **Answer:** `Spear-phishing`
* **Question:** What is the time interval between CustomBackdoor's HTTPS C2 beacons? (Answer the number of seconds)
* **Answer:** `300`
* **Question:** What is the flag received after choosing the correct threat hunting approach and target?
* **Answer:** `THM-APT-SERPENT-INTEL`

---

## 🧠 Key Learnings
* **Dwell Time & Proactive Defense:** Dwell time is the amount of time a hacker hides inside your network before getting caught. Threat Hunting is "proactive" because you don't wait for an antivirus alert; you assume the hacker is already inside and actively go looking for them to reduce this dwell time.
* **Indicator vs. Intelligence Driven:** 
  * *Indicator-driven* is like looking for a specific fingerprint (e.g., searching the network for a known malicious IP address).
  * *Intelligence-driven* is like knowing a specific gang targets banks using phishing emails, so you specifically hunt for weird email attachments, even if you don't know the exact file name.
* **Behavioral Pattern Analysis:** Instead of looking for a bad file, you look for a bad *action*. A user opening Microsoft Word is normal. But if Microsoft Word suddenly opens a Command Prompt to download a file from the internet, that is highly suspicious behavior, regardless of what the files are called.
*
