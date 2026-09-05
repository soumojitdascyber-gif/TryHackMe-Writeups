# 🔢 TryHackMe Writeup: Data Representation

## 📝 Room Overview
* **Room Name:** Data Representation
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / General

## 🎯 Objective
Learn the core concepts of how computers process and represent data using Base-2 (Binary), Base-10 (Decimal), and Base-16 (Hexadecimal) numbering systems, and how these systems apply to digital color representation (RGB).

---

## 💡 Tasks & Answers

### Task: Binary, Decimal, and Hexadecimal Conversions
* **Question:** What is the hexadecimal FF in binary?
* **Answer:** `1111 1111`
* **Question:** What is the hexadecimal AB in decimal?
* **Answer:** `171`
* **Question:** Convert the hexadecimal FF FF FF to decimal. After you round up the decimal value to the nearest million, how many millions is that?
* **Answer:** `17`

### Task: Colors (RGB and Hex)
* **Question:** Preview the color #3BC81E. In one word, what does this color appear to be?
* **Answer:** `green`
* **Question:** What is the binary representation of the color #EB0037?
* **Answer:** `11101011 00000000 00110111`
* **Question:** What is the decimal representation of the color #D4D8DF?
* **Answer:** `212 216 223`

---

## 🧠 Key Learnings
* **Binary (Base-2):** Computers only understand switches: "On" (1) and "Off" (0). This is binary. It is the lowest level of communication, but very hard for humans to read.
* **Hexadecimal (Base-16):** Because binary strings get extremely long and confusing (like `11111111`), we use Hexadecimal as a "shortcut." It uses numbers 0-9 and letters A-F. For example, the binary `1111 1111` simply becomes `FF` in Hex. It is much easier for analysts to read and write.
* **How Computers See Color (RGB):** Every color on your screen is just a mix of Red, Green, and Blue light. Each light can be turned up from a level of 0 (off) to 255 (max brightness). 
    * In Hexadecimal, 0 is `00` and 255 is `FF`. 
    * So, a color code like `#FF0000` tells the computer: Turn Red to max (`FF`), Green to zero (`00`), and Blue to zero (`00`). The result is pure red!
