# ⚔️ Offensive Security Intro (TryHackMe)

## 🎯 Objective
Experience a basic offensive security (Red Team) workflow by exploiting logical flaws in a web application.

## 🧠 Core Concepts & Execution
* **Execution Environment:** Simulated browser desktop on TryHackMe.
* **Tasks Performed:**
  * Discovered a hidden admin panel on the target web application.
  * Manipulated the application by directly accessing the `/bank-transfer` directory via the URL.
  * Exploited the logic flaw by using account number `8881` to deposit `$2000` (or more).
  * Successfully manipulated the account balance to turn it positive, triggering the final success state.

## 🚩 Proof of Compromise
* **Flag Found:** `BANK-HACKED`
*
