# 🤖 TryHackMe Writeup: BankGPT

## 📝 Room Overview
* **Room Name:** BankGPT
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** AI Security / Prompt Injection

## 🎯 Objective
Interact with a live LLM customer service assistant used by a banking system to find vulnerabilities and extract hidden information.

---

## 💡 Tasks & Answers

### Task: LLM Interaction
* **Question:** What is the secret key?
* **Answer:** `THM{support_api_key_123}`

---

## 🧠 Key Learnings
* **LLM Prompt Injection:** AI models used in customer service can often be manipulated by carefully crafted prompts. Attackers can trick the AI into ignoring its initial instructions and revealing sensitive backend data, such as API keys or secret flags.
*
