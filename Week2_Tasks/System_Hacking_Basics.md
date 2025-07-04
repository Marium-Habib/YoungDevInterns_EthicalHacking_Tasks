# 🔐 System Hacking Basics – Week 2

This section focuses on understanding how passwords are stored, cracked, and exploited using real-world tools. The goal was to learn different password cracking methods, hash formats, and perform practical exploitation on vulnerable systems.

---

## 🔑 Password Cracking Tools

### 1. **John the Ripper**
- A fast password cracker used to perform dictionary and brute-force attacks.
- Supports many hash types including MD5, SHA1, etc.


### 2. **Hydra**

* A powerful tool for brute-force login credentials on various protocols (SSH, FTP, HTTP, etc.).
* Supports multi-threaded attacks for faster cracking.


---

## 🧾 Understanding Password Hashes

* **Hashes** are encrypted representations of plain-text passwords.
* Common hash formats: MD5, SHA1, bcrypt
* Linux password hashes are usually stored in `/etc/shadow`
* Tools like `unshadow` are used to prepare these hashes for cracking:


---

## 🎯 Practical Exploitation using Metasploitable2

* Used Metasploitable2 as the target machine for practice.
* Launched `msfconsole` to search and run common exploits.
* Cracked weak service credentials and gained shell access.


---

## 🧠 Learnings

* Understood how password hashes are stored and secured in Linux systems.
* Learned to use `John the Ripper` and `Hydra` for cracking weak passwords.
* Explored the impact of weak credentials through hands-on practice on Metasploitable2.
* Experienced using Metasploit Framework (`msfconsole`) for real-world exploitation.

---
