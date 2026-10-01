# 🏭 TryHackMe Writeup: OT/ICS Security

## 📝 Room Overview
* **Room Name:** OT/ICS Security
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Operational Technology

## 🎯 Objective
Understand the fundamentals of Operational Technology (OT) and Industrial Control Systems (ICS), focusing on PLCs, HMIs, and why physical safety is prioritized over traditional IT security concepts like encryption.

---

## 💡 Tasks & Answers

### Task: How Does OT/ICS Work?
* **Question:** What does the 'O' in OT stand for?
* **Answer:** `Operational`
* **Question:** What does the 'C' in ICS stand for?
* **Answer:** `Control`
* **Question:** When a PLC needs to send a signal to turn off a motor in the real world, it sends a signal through what type of connection?
* **Answer:** `Output`
* **Question:** What source provides the environmental data that inputs feed into a PLC?
* **Answer:** `Sensor`

### Task: Differences Between OT & IT Cyber Security
* **Question:** What type of system is used by a human operator to interact with a PLC and control a physical process in the real world?
* **Answer:** `Human Machine Interface`
* **Question:** Which 2021 incident marked a turning point for OT/ICS security, after which annual cyberattacks against these networks doubled?
* **Answer:** `Colonial Pipeline`
* **Question:** What is the most important requirement for OT/ICS cyber security?
* **Answer:** `Safety`
* **Question:** What do many OT environments not leverage?
* **Answer:** `Encryption`

### Task: What a Human Operator Sees in OT Environments
* **Question:** Based on a review of the HMI, what type of environment is this?
* **Answer:** `ICS`
* **Question:** When you first look at the HMI, what is the current percentage level indicated by the tank level sensor?
* **Answer:** `65`
* **Question:** Click on the START button to turn on the pump... At what percentage level do you first receive an alert in a yellow warning banner?
* **Answer:** `85`
* **Question:** Continue to allow water to flow into the tank. At what percentage level does the control system realize there is danger and shuts off the pump?
* **Answer:** `95`
* **Question:** With the pump stopped, click OPEN on the valve on the outtake pipe. What happens to the water level in the tank? The water level <fill in the blank>.
* **Answer:** `Lowers`
*
