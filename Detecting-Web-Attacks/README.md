# 🚨 TryHackMe Writeup: Detecting Web Attacks

## 📝 Room Overview
* **Room Name:** Detecting Web Attacks
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Web Security

## 🎯 Objective
Explore the mechanisms of common web attacks (Client-Side vs. Server-Side) and learn how to detect them through network traffic analysis, log review, and configuring Web Application Firewalls (WAF).

---

## 💡 Tasks & Answers

### Task: Client-Side Attacks
* **Question:** What class of attacks relies on exploiting the user's behavior or device?
* **Answer:** `Client-Side`
* **Question:** What is the most common client-side attack?
* **Answer:** `XSS`

### Task: Server-Side Attacks
* **Question:** What class of attacks relies on exploiting vulnerabilities within web servers?
* **Answer:** `Server-Side`
* **Question:** Which server-side attack lets attackers abuse forms to dump database contents?
* **Answer:** `SQLi`

### Task: Network-Based Detection (Log Analysis)
* **Question:** What is the attacker's User-Agent while performing the directory fuzz?
* **Answer:** `FFUF v2.1.0`
* **Question:** What is the name of the page on which the attacker performs a brute-force attack?
* **Answer:** `/login.php`
* **Question:** What is the complete, decoded (opens in new tab) SQLi payload the attacker uses on the `/changeusername.php` form?
* **Answer:** `%' OR '1'='1`
* **Question:** What password does the attacker successfully identify in the brute-force attack?
* **Answer:** `astrongpassword123`
* **Question:** What is the flag the attacker found in the database using SQLi?
* **Answer:** `THM{dumped_the_db}`

### Task: Web Application Firewall (WAF)
* **Question:** What do WAFs inspect and filter?
* **Answer:** `Web Requests`
* **Question:** Create a custom firewall rule to block any User-Agent that matches "BotTHM".
* **Answer:** `IF User-Agent CONTAINS "BotTHM" THEN block`

---

## 🧠 Key Learnings
* **Client-Side vs. Server-Side:** 
  * *Client-Side (e.g., XSS):* The attacker hacks the *user* visiting the website. The malicious script runs in the victim's browser.
  * *Server-Side (e.g., SQLi):* The attacker hacks the company's actual *database or server*, potentially stealing thousands of records at once.
* **Log Analysis (Tracing Footprints):** Every time someone visits a website, the server writes it down in a log. By analyzing these logs, defenders can spot attackers. If you see thousands of rapid requests hitting `/login.php`, or a tool declaring its User-Agent as `FFUF` (a popular hacking tool), you immediately know an attack is happening.
* **The Classic SQLi Payload (`%' OR '1'='1`):** This is a logic trick used against databases. It's like telling a security guard: "Give me the secret files if my username is Admin, OR if 1 equals 1." Because 1 always equals 1, the condition is always true, and the database blindly hands over the data.
* **WAF (Web Application Firewall):** A WAF is like a highly intelligent bouncer at the front door of your web server. It reads the contents of every HTTP request. If it spots a hacker's tool (`User-Agent: BotTHM`) or a malicious SQL injection string, it blocks the request before it even reaches the vulnerable application.
*
