# WEEK3-PROJECT--PASSWORD-CRACKING-LABS
# Week 3 Project — Password Cracking Labs

Cybersecurity & Ethical Hacking coursework (Networkwalks Academy). This repo documents two lab exercises focused on recovering a password from a protected PDF file, using two different toolchains.

## 🎯 Objective

Given a password-protected PDF (`My Locked PDF1.pdf`), extract its password hash and crack it using dictionary-based attacks — demonstrating how weak passwords can be recovered and why strong passwords matter.

## 🧪 Lab 1: Password Cracking with John the Ripper (JTR) + Johnny GUI

**Tools:** John the Ripper (jumbo build), Johnny GUI, onlinehashcrack.com's PDF hash extractor

**Steps:**
1. Extracted the PDF's crackable hash (`$pdf$...` format) using an online PDF-to-hash tool
2. Saved the hash to a text file (`hash1.txt`)
3. Loaded the hash into Johnny (GUI front-end for John the Ripper)
4. Ran a dictionary attack via **Start new attack**
5. Password recovered: `good-luck`

**Also tested on Kali Linux**, where JTR ships pre-installed, using the built-in `pdf2john.pl` script to extract the hash directly from the terminal instead of an online tool.

## 🧪 Lab 2: Password Cracking with Networkwalks Tools

**Tools:** Networkwalks Hash Calculator, Networkwalks Password Cracker (browser-based, no install)

**Steps:**
1. Uploaded the PDF to the [Hash Calculator](https://networkwalks.com/hash-calculator/) to extract the `$pdf$...` hash
2. Pasted the hash into the [Password Cracker](https://networkwalks.com/password-cracker/)
3. Ran the built-in dictionary attack — not found in the default 100-word list
4. Uploaded a custom single-entry wordlist containing `good-luck`
5. Password matched instantly: `good-luck`

## 🔑 Key Takeaways

- **Encryption vs. Hashing:** Encryption is reversible with the right key; hashing is one-way and used to verify rather than store passwords in plain text.
- **Dictionary attacks** succeed quickly against common/short passwords, but fail against passwords outside the wordlist — reinforcing the value of long, unique passwords.
- The same cracking logic (hash extraction → dictionary matching) underlies both GUI tools (Johnny) and browser-based tools, whether run on Windows or Kali Linux.

## ⚠️ Disclaimer

This project was completed in a controlled training environment using a sample file provided by the course. Password cracking techniques shown here are for educational purposes only and should only be used on systems/files you own or have explicit authorization to test.

---
*Part of Networkwalks Academy — Cybersecurity & Ethical Hacking Training*
