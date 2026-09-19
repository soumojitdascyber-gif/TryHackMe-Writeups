# 🐉 TryHackMe Writeup: Hydra

## 📝 Room Overview
* **Room Name:** Hydra
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Offensive Security Tooling / Brute Forcing

## 🎯 Objective
Learn about and use Hydra, a fast network logon cracker, to brute-force authentication portals and obtain valid credentials for web applications and SSH services[span_20](start_span)[span_20](end_span).

---

## 💡 Tasks & Answers

### Task: Practical Application
* **Question:** Use Hydra to brute-force molly's web password. What is the value of flag 1?
* **Answer:** `THM{2673a7dd116de68e85c48ec0b1f2612e}`[span_21](start_span)[span_21](end_span)
* **Question:** Use Hydra to brute-force molly's SSH password. What is the value of flag 2?
* **Answer:** `THM{c8eeb0468febbadea859baeb33b2541b}`[span_22](start_span)[span_22](end_span)

---

## 🧠 Key Learnings
* **What is Hydra?** Unlike vulnerability scanners that look for broken code, Hydra specifically targets login pages and remote access services (like SSH, FTP, or HTTP-POST forms)[span_23](start_span)[span_23](end_span). 
* **The Brute-Force Methodology:** Hydra works by taking a target (IP or URL), a known username (like 'molly[span_24](start_span)'[span_24](end_span)), and a massive dictionary list of common passwords. It rapidly fires every password in the list at the login portal until the server accepts one.
* **Service Versatility:** The power of Hydra is its modularity. You use the exact same command structure whether you are cracking a website's login form or attempting to crack a Linux server's SSH remote login[span_25](start_span)[span_25](end_span).
*
