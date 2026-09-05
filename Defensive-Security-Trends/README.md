# 📈 TryHackMe Writeup: Defensive Security Trends

## 📝 Room Overview
* **Room Name:** Defensive Security Trends
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Threat Intelligence

## 🎯 Objective
Analyze modern cyber threats by exploring real-world supply chain attacks, the rise of infostealers, and how threat actors abuse legitimate administrative tools to bypass security detection.

---

## 💡 Tasks & Answers

### Task: Supply Chain & Infostealers
* **Question:** The GitHub breach started from an infection of an employee's device. Which VS Code extension was backdoored with an infostealer?
* **Answer:** `Nx Console`
* **Question:** The extension was compromised through another supply chain attack. Which open-source package ecosystem was the root cause?
* **Answer:** `npm`

### Task: Threat Actor Tactics & IABs
* **Question:** Open the Verizon report to page 40 (System Intrusion section). How much has threat actor RMM usage grown year-over-year?
* **Answer:** `240%`
* **Question:** Continue to the Infostealer to ransomware pipeline section a few pages later. Which access type do Initial Access Brokers most commonly sell?
* **Answer:** `VPN`

---

## 🧠 Key Learnings
* **Supply Chain Attacks:** Instead of hacking a highly secure company directly, hackers attack the weaker tools the developers use (like a VS Code extension or an open-source `npm` package). It is like poisoning a city's water supply at the source instead of breaking into every individual house.
* **Infostealers:** These are sneaky viruses designed purely to steal saved passwords, browser cookies, and session tokens. If an employee's laptop gets infected, hackers can bypass MFA (Multi-Factor Authentication) and simply "log in" to the company network as that employee.
* **RMM Abuse (Remote Monitoring and Management):** Hackers are increasingly using legitimate IT support tools (like AnyDesk or TeamViewer) to control infected computers. This trend has grown by 240% because it helps them blend in—antivirus systems see a normal IT tool and often ignore it!
* **Initial Access Brokers (IABs):** These are the "middlemen" of the dark web. They infect computers, steal remote access credentials (specifically VPNs) using infostealers, and then sell that direct network access to big Ransomware gangs for a profit.
*
