# 🌐 DNS in Detail (TryHackMe)

## 🎯 Objective
Understand how the Domain Name System (DNS) works and manually extract various DNS records to understand domain configurations.

## 🧠 Core Concepts & Execution
* **Execution Environment:** Used the TryHackMe in-browser DNS emulator to build queries and view results.
* **Tasks Performed:**
  * Queried the `CNAME` record for `shop.website.thm` and found it points to `shops.myshopify.com`.
  * Extracted the `TXT` record for `website.thm` to uncover the hidden flag.
  * Checked the `MX` record to find the numerical priority value (which was 30).
  * Queried the `A` record of `www.website.thm` to resolve its IP address (`10.10.10.10`).

## 🚩 Proof of Compromise
* **Flag Found:** `THM{7012BBA60997F35A9516C2E16D2944FF}`

## 💡 Key Takeaway
Learned how to manually query specific DNS record types (A, CNAME, TXT, MX) and understand the distinct purpose of each record in routing internet traffic.
