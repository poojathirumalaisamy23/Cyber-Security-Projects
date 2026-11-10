# Cyber-Security-Projects
# Cyber Security Projects: Intrusion Detection & Secure File Storage

This repository contains two Python-based cybersecurity projects developed to demonstrate practical skills in defensive security (Blue Team) and cryptography. Both tools are built with a focus on automation, data integrity, and threat detection.

## Table of Contents
1. [Project 1: Log File Analyzer for Intrusion Detection](#project-1-log-file-analyzer-for-intrusion-detection)
2. [Project 2: Secure File Storage System with AES](#project-2-secure-file-storage-system-with-aes)
3. [Installation & Requirements](#installation--requirements)

---

## Project 1: Log File Analyzer for Intrusion Detection

**Objective:** 
To build a lightweight Security Information and Event Management (SIEM) tool that parses web and system logs to detect common attack patterns such as SSH brute-forcing, web scanning, and malicious user-agent activity.

**Tools Used:** Python, Pandas, Matplotlib, Regex (`re`).

### Key Features
- **Log Parsing:** Uses advanced Regular Expressions to extract fields (IP, timestamp, method, status code, user-agent) from Apache access logs and SSH authentication logs.
- **Threat Detection Engine:** 
  - *SSH Brute Force:* Detects IPs generating an abnormal volume of "Failed password" attempts within a 5-minute sliding window.
  - *Web Scanning:* Flags IPs generating excessive 404 errors (Directory Fuzzing) and accessing sensitive paths (e.g., `/admin`, `/.env`, `/wp-login.php`).
  - *Malicious User-Agents:* Identifies automated scanning tools (e.g., `sqlmap`, `nikto`, `nmap`) based on the HTTP User-Agent header.
- **Visualization & Reporting:** Generates visual charts (Top offending IPs, Request spikes over time) and exports a structured Markdown `incident_report.md` containing evidence and timestamps.

---

## Project 2: Secure File Storage System with AES

**Objective:** 
To develop a local file encryption/decryption vault that ensures the Confidentiality and Integrity of data at rest using AES-256 encryption.

**Tools Used:** Python, `cryptography` (Fernet), `hashlib` (SHA-256).

### Key Features
- **AES-256 Encryption:** Utilizes symmetric encryption (Fernet) to securely encrypt files, protecting them from unauthorized access.
- **Integrity Verification (Anti-Tampering):** 
  - Calculates and stores the SHA-256 hash of the original plaintext.
  - Calculates and stores the SHA-256 hash of the encrypted ciphertext.
- **Tamper Detection:** During the decryption process, the system verifies the hash of the encrypted file. If a single byte has been modified by an attacker, the system detects the hash mismatch and aborts the decryption process (`[!] TAMPER DETECTED`).
- **Metadata Management:** Automatically logs file size, timestamps, and hashes into a local JSON metadata database.
- **CLI Interface:** Supports intuitive commands: `encrypt`, `decrypt`, `verify`, and `list`.

---

## Installation & Requirements

To run these scripts locally, ensure you have Python 3 installed.

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/Cyber-Security-Projects.git
   cd Cyber-Security-Projects
   Install the required dependencies:

bash
pip install pandas matplotlib cryptography
Navigate to the respective project folders to view the source code, screenshots of the working tools, and usage instructions.

Developed as part of a Cybersecurity Internship Program.

text

### Final Step:
Click **Commit changes** after pasting it. Then copy the URL of your GitHub page and submit it on your Google Form! You are officially done. 🚀
