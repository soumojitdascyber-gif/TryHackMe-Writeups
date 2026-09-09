# 👨‍🍳 TryHackMe Writeup: CyberChef: The Basics

## 📝 Room Overview
* **Room Name:** CyberChef: The Basics
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security Tooling

## 🎯 Objective
Learn how to use CyberChef, the "Swiss Army Knife" of cybersecurity, to decode, encode, parse, and analyze various types of data formats including Base64, URL encoding, Hex, and Unix Timestamps.

---

## 💡 Tasks & Answers

### Task: Before Anything Else
* **Question:** In which area can you find "From Base64"?
* **Answer:** `operations`
* **Question:** Which area is considered the heart of the tool?
* **Answer:** `Recipe`

### Task: Practice, Practice, Practice
* **Question:** At which step would you determine, "What do I want to accomplish?"
* **Answer:** `1`
* **Question:** What is the hidden email address?
* **Answer:** `hidden@hotmail.com`
* **Question:** What is the hidden IP address that ends in .232?
* **Answer:** `102.20.11.232`
* **Question:** Which domain address starts with the letter "T"?
* **Answer:** `TryHackMe.com`
* **Question:** What is the binary value of the decimal number 78?
* **Answer:** `01001110`
* **Question:** What is the URL encoded value of `https://tryhackme.com/r/careers` ?
* **Answer:** `https%3A%2F%2Ftryhackme.com%2Fr%2Fcareers`
* **Question:** Using the file you downloaded in Task 5, which IP starts and ends with "10"?
* **Answer:** `10.10.2.10`
* **Question:** What is the base64 encoded value of the string "Nice Room!"?
* **Answer:** `TmljZSBSb29tIQ==`
* **Question:** What is the URL decoded value for `https%3A%2F%2Ftryhackme%2Ecom%2Fr%2Froom%2Fcyberchefbasics` ?
* **Answer:** `https://tryhackme.com/r/room/cyberchefbasics`
* **Question:** What is the datetime string for the Unix timestamp `1725151258` ?
* **Answer:** `Sun 1 September 2024 00:40:58 UTC`
* **Question:** What is the Base85 decoded string of the value `<+oue+DGm>ApXu7` ?
* **Answer:** `This is fun!`

---

## 🧠 Key Learnings
* **How CyberChef Works:** It is a web-based tool structured like a kitchen. You throw your raw data into the **Input** box, pick tools from the **Operations** menu (like "From Base64" or "Extract IP"), stack them together to build a **Recipe** (the heart of the tool), and the final result automatically pops out in the **Output** box.
* **Base64 Encoding:** Computers often need to send complex binary files (like images or encrypted keys) over text-based protocols like email. Base64 translates that messy binary into safe, normal text characters. You can often spot Base64 because it frequently ends with one or two equals signs (`=`).
* **URL Encoding:** Web browsers get confused by special characters like spaces, slashes (`/`), or colons (`:`) in a web address. URL encoding translates these into safe codes. For example, a `/` becomes `%2F` and a `:` becomes `%3A`.
* **Unix Timestamp:** Computers don't natively understand "September 1, 2024". Instead, they track time by counting the exact number of seconds that have passed since January 1, 1970. CyberChef easily converts these giant numbers back into human-readable dates.
*
