# 📱 TryHackMe Writeup: Mobile Acquisition

## 📝 Room Overview
* **Room Name:** Mobile Acquisition
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Digital Forensics / DFIR

## 🎯 Objective
Prepare for mobile acquisition by understanding the security challenges, hardware protections, and extraction methodologies used during digital forensic investigations.

---

## 💡 Tasks & Answers

### Task: Mobile Device Forensics & Security
* **Question:** In what country was it where there is a famous example of mobile devices being used within investigations?
* **Answer:** `South Africa`
* **Question:** What is the technical term for a device that has become the initial access method of an attacker?
* **Answer:** `Entrypoint`
* **Question:** Which manufacturer protection prevents untrusted code from loading during boot?
* **Answer:** `Secure boot process`
* **Question:** Are encryption keys stored in software or hardware?
* **Answer:** `hardware`

### Task: Acquisition Techniques & Malware
* **Question:** What app store was found to have malicious applications available to users?
* **Answer:** `Google Play`
* **Question:** What is the name of the sophisticated malware that used a combination of "one click" and "zero click" attacks?
* **Answer:** `Pegasus`

### Task: Acquisition Methods
* **Question:** If I wanted to recover deleted data, what acquisition method would I try?
* **Answer:** `Physical`
* **Question:** Which acquisition method involves using features of the Operating System to extract data?
* **Answer:** `Logical Acquisition`
* **Question:** What is the name of the utility used to perform a full backup of an iPhone via the CLI?
* **Answer:** `idevicebackup2`
* **Question:** What is the name of the tool that can be used to perform a backup of an Android, via the CLI? Please note that we are looking for the acronym.
* **Answer:** `ADB`

### Task: Practical Extraction
* **Question:** What is the name of the technique that boots the device into a temporary Operating System, often bypassing security mechanisms?
* **Answer:** `Custom Boot Loading`
* **Question:** What is the name of the technique that exploits a known vulnerability within the device? Granting it full or "root" access?
* **Answer:** `Jailbreaking`
* **Question:** What is the flag displayed once the capture is complete?
* **Answer:** `THM{MOBILE_ACQUISITION}`

---

## 🧠 Key Learnings
* **Logical vs. Physical Backup:** A "Logical" backup is like asking the phone politely to hand over its normal files. A "Physical" backup ignores the phone's rules and copies the raw memory chip directly, which is the only way to recover files that have been deleted.
* **Hardware Security:** Phones are extremely secure now. They have a "Secure boot process" to ensure no tampered or hacked code runs when you turn them on. Also, their master passwords (encryption keys) are locked inside actual physical hardware chips, not just floating around in the software.
* **Bypassing Locks for Evidence:** Sometimes, police or forensic investigators have to use hacker tricks. They might use "Jailbreaking" to get super-user access, or "Custom Boot Loading" to start the phone with a temporary system just to bypass the lock screen and grab the evidence.
* **Zero-Click Malware:** Extremely advanced malware like 'Pegasus' is terrifying because it can infect a phone without the user ever clicking a link or making a mistake ("zero click"). 
*
