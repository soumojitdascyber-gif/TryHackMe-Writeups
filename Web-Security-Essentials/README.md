# 🌐 TryHackMe Writeup: Web Security Essentials

## 📝 Room Overview
* **Room Name:** Web Security Essentials
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Web Security

## 🎯 Objective
Learn the foundational concepts of how the web works, common security risks, and the multi-layered protections (Defense-in-Depth) required to secure a web application, its server, and the underlying host machine.

---

## 💡 Tasks & Answers

### Task: Web Infrastructure Basics
* **Question:** What does your web browser send to a server to receive a web page?
* **Answer:** `Request`
* **Question:** What web server is most commonly used to host WordPress websites?
* **Answer:** `Apache`
* **Question:** What do we call the OS and environment that runs the web server and application?
* **Answer:** `Host Machine`
* **Question:** Have applications shifted from desktop to web over the past couple of decades (Yea/Nay)?
* **Answer:** `Yea`
* **Question:** Who is ultimately responsible for ensuring the security of users' data within a web application?
* **Answer:** `Web App Owner`

### Task: Defense Systems & Controls
* **Question:** What cyber security concept involves stopping or limiting damage from threats?
* **Answer:** `Mitigation`
* **Question:** What security control involves ensuring all software and components are up to date?
* **Answer:** `Patch Management`

### Task: WAFs & Practice Scenario
* **Question:** Which type of Web Application Firewall operates by running on the same system as the application itself?
* **Answer:** `Host-Based`
* **Question:** Which common WAF detection technique works by matching incoming requests against known malicious patterns?
* **Answer:** `Signature-Based`
* **Question:** What flag did you receive for securing the Web Application?
* **Answer:** `THM{web_app_secured!}`
* **Question:** What flag did you receive for securing the Web Server?
* **Answer:** `THM{server_security_expert!}`
* **Question:** What flag did you receive for securing the Host Machine?
* **Answer:** `THM{the_final_security_layer!}`

---

## 🧠 Key Learnings
* **Defense-in-Depth (The Security Layer Cake):** Securing a website isn't just about writing safe code. An attacker can bypass the application completely if the underlying systems are weak. You must secure all three layers: 
  1. The **Application** (e.g., WordPress, fixing SQLi bugs).
  2. The **Web Server** (e.g., Apache, hiding version headers).
  3. The **Host Machine** (e.g., Linux OS, updating passwords and applying OS patches).
* **Mitigation vs. Patching:** 
  * *Mitigation* is like putting a bucket under a leaking roof—it stops the immediate damage from spreading (e.g., turning off a vulnerable feature temporarily). 
  * *Patch Management* is actually fixing the roof permanently by installing the latest software updates.
* **Signature-Based WAFs:** A Web Application Firewall (WAF) acts as a security guard for your app. "Signature-Based" detection means the WAF has a "Wanted Poster" of known hacker attacks (like specific SQL injection strings). If an incoming HTTP request matches the signature on the poster, the WAF blocks it instantly.
*
