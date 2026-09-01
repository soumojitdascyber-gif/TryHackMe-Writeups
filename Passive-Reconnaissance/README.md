# 🔍 TryHackMe Writeup: Passive Reconnaissance

## 📝 Room Overview
* **Room Name:** Passive Reconnaissance
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Threat Intelligence / Reconnaissance

## 🎯 Objective
Learn the essential tools for passive reconnaissance (like whois, nslookup, and dig) to gather information about a target without directly interacting with their infrastructure.

---

## 💡 Tasks & Answers

### Task: Active vs. Passive Reconnaissance
* **Question:** You visit the Facebook page of the target company, hoping to get some of their employee names. What kind of reconnaissance activity is this? (A for active, P for passive)
* **Answer:** `P`
* **Question:** You ping the IP address of the company webserver to check if ICMP traffic is blocked. What kind of reconnaissance activity is this?
* **Answer:** `A`
* **Question:** You happen to meet the IT administrator of the target company at a party. You try to use social engineering to get more information about their systems. What kind of reconnaissance activity is this?
* **Answer:** `A`

### Task: Whois
* **Question:** When was TryHackMe.com registered?
* **Answer:** `20180705`
* **Question:** What is the registrar of TryHackMe.com?
* **Answer:** `namecheap.com`
* **Question:** Which company is TryHackMe.com using for name servers?
* **Answer:** `cloudflare.com`

### Task: nslookup and dig
* **Question:** Check the TXT records of thmlabs.com. What is the flag there?
* **Answer:** `THM{a5b83929888ed36acb0272971e438d78}`

### Task: DNSDumpster
* **Question:** Lookup tryhackme.com on DNSDumpster. Under Services / Banners, which one has the highest count?
* **Answer:** `cloudflare`

### Task: Shodan.io
* **Question:** According to Shodan.io, what is the first country in the world in terms of the number of publicly accessible Apache servers?
* **Answer:** `United States`
* **Question:** Based on Shodan.io, what is the 3rd most common port used for Apache?
* **Answer:** `8080`
* **Question:** Based on Shodan.io, what is the most common port used for nginx?
* **Answer:** `80`

---

## 🧠 Key Learnings
* **Passive vs. Active Recon:** Passive is like looking at a target's house from the public street—they don't know you are watching. Active is like knocking on their door or checking if the window is locked—they will see you on their security cameras (server logs).
* **Whois:** This is like a public phone book for websites. It tells you exactly who bought a website name, when they bought it, and where it is hosted.
* **DNS & TXT Records:** DNS is the internet's GPS system. Sometimes, IT administrators hide secret notes, verification codes, or flags in special records called "TXT records". We can use tools like `nslookup` or `dig` to read these hidden notes.
* **Shodan & DNSDumpster:** Shodan is a search engine for connected devices (like servers, cameras, and routers), not websites. DNSDumpster helps map out all the different sub-websites a company owns. Both tools let us gather a massive amount of intelligence without ever touching the target's actual network.
*
