# 🔍 TryHackMe Writeup: Intro to Digital Forensics

## 📝 Room Overview
* **Room Name:** Intro to Digital Forensics
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Defensive Security / Digital Forensics

## 🎯 Objective
Learn the foundational processes of digital forensics, the legal importance of evidence handling, and practically extract hidden metadata from files (PDFs and Images) to track down adversaries.

---

## 💡 Tasks & Answers

### Task: Digital Forensics Process
* **Question:** Consider the desk in the photo above. In addition to the smartphone, camera, and SD cards, what would be interesting for digital forensics?
* **Answer:** `laptop`

### Task: Practical Example of Digital Forensics (Evidence Handling)
* **Question:** It is essential to keep track of who is handling it at any point in time to ensure that evidence is admissible in the court of law. What is the name of the documentation that would help establish that?
* **Answer:** `Chain of Custody`

### Task: Practical Example of Digital Forensics (Metadata Extraction)
* **Question:** Using `pdfinfo`, find out the author of the attached PDF file, `ransom-letter.pdf`.
* **Answer:** `Ann Gree Shepherd`
* **Question:** Using `exiftool` or any similar tool, try to find where the kidnappers took the image they attached to their document. What is the name of the street?
* **Answer:** `Milk Street`
* **Question:** What is the model name of the camera used to take this photo?
* **Answer:** `Canon EOS R6`

---

## 🧠 Key Learnings
* **The Crime Scene:** In digital forensics, the crime scene isn't just a network. Any physical device that can hold data—a laptop, a smartphone, or even a tiny SD card—is a potential goldmine of evidence.
* **Chain of Custody:** Imagine this as a highly strict "sign-out sheet" for evidence. If the police seize a hacker's laptop, they must document exactly who touched it, when, and why. If there is a gap in this documentation, a lawyer in court can argue that the evidence was tampered with, making it completely useless.
* **Metadata ("Data about Data"):** When you take a photo with your phone or create a document, the device secretly embeds hidden information inside the file. 
  * `pdfinfo` revealed the author's computer username just from a ransom letter.
  * `exiftool` acts like a digital magnifying glass for photos (EXIF data). It revealed the exact camera model used and the precise GPS coordinates of where the kidnappers stood to take the picture!
