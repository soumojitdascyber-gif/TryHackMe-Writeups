# 🔺 TryHackMe Writeup: Pyramid Of Pain

## 📝 Room Overview
* **Room Name:** Pyramid Of Pain
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Threat Intelligence / Defensive Security

## 🎯 Objective
Learn what the Pyramid of Pain is and how it ranks indicators by how painful they are for an adversary to change.

---

## 💡 Tasks & Answers

### Task: Hash Values
* **Question:** Analyse the report associated with the hash... What is the filename of the sample?
* **Answer:** `Sales_Receipt 5606.xls`

### Task: IP Addresses & Domain Names
* **Question:** What is the first IP address the malicious process (PID 1632) attempts to communicate with?
* **Answer:** `50.87.136.52`
* **Question:** What is the first domain name the malicious process ((PID 1632) attempts to communicate with?
* **Answer:** `craftingalegacy.com`
* **Question:** What type of attack uses Unicode characters in the domain name to imitate the a known domain?
* **Answer:** `Punycode attack`
* **Question:** Provide the redirected website for the shortened URL using a preview...
* **Answer:** `https://tryhackme.com/`

### Task: Host & Network Artifacts
* **Question:** A process named regidle.exe makes a POST request to an IP address based in the United States (US) on port 8080. What is the IP address?
* **Answer:** `96.126.101.6`
* **Question:** The actor drops a malicious executable (EXE). What is the name of this executable?
* **Answer:** `G_jugk.exe`
* **Question:** Look at this report by VirusTotal. How many vendors determine this host to be malicious?
* **Answer:** `9`

### Task: Tools
* **Question:** Which network indicator helped us identify the malware type (Emotet)?
* **Answer:** `User-Agent`
* **Question:** How many POST requests are in the screenshot from the PCAP file?
* **Answer:** `6`

### Task: TTPs (Tactics, Techniques & Procedures)
* **Question:** Provide the method used to determine similarity between the files.
* **Answer:** `Fuzzy Hashing` (also known as `context triggered piecewise hashes`)
* **Question:** Navigate to ATT&CK Matrix webpage. How many techniques fall under the Exfiltration category?
* **Answer:** `9`
* **Question:** Chimera is a China-based hacking group... What is the name of the commercial, remote access tool they use for C2 beacons and data exfiltration?
* **Answer:** `Cobalt Strike`

### Task: Practical
* **Question:** Complete the static site. What is the flag?
* **Answer:** `THM{PYRAMIDS_COMPLETE}`

---

## 🧠 Key Learnings
* **The Concept:** The Pyramid of Pain is simply a chart that shows how much headache you can cause a hacker when you block their attack methods. 
* **The Bottom (Trivial):** Blocking things like Hash Values or IP Addresses is easy for defenders, but it doesn't bother the hacker. They can just change one line of code to get a new hash, or switch to a new IP in seconds.
* **The Middle (Annoying):** Blocking Domain Names or specific Tools (like a custom `User-Agent` string) starts to annoy the hacker because they have to spend time buying new websites or rewriting their software.
* **The Top (Tough):** TTPs stand for Tactics, Techniques, and Procedures. This is the hacker's *behavior*. If you can detect and block *how* they act (for example, how they exfiltrate data), they have to learn completely new hacking skills to bypass you. This is the ultimate goal of a Blue Team analyst.
*
