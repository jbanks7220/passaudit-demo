# PassAudit Demo 🔐

**Educational password audit tool** that evaluates password strength, simulates hash-based attacks, and generates reports in **JSON**, **HTML**, and **Markdown** formats.  
Created to demonstrate ethical password auditing and Python scripting skills.

[![Python](https://img.shields.io/badge/python-3.x-blue.svg)](#)

---

## 🔍 Overview

`passaudit-demo` is a hands-on educational project that shows how password audits and hash comparisons work.  
It’s built entirely in Python and emphasizes transparency, ethics, and professional report generation.

Use this tool to:

- **Analyze plaintext passwords** for strength and entropy  
- **Simulate dictionary attacks** on SHA-1 or SHA-256 hashes  
- **Generate easy-to-read reports** in `.json`, `.html`, and `.md` formats

All output files are created in the current working directory (where you run the script).

---

## 📂 Project Contents (actual layout)

passaudit-demo/  
├── docs/  
│ ├── demo_hashes_sha1.txt # SHA-1 hashes for demo use  
│ ├── demo_hashes_sha256.txt # SHA-256 hashes for demo use  
│ ├── passwords_mixed.txt # Example weak passwords  
│ └── passwords_weak.txt # Mixed password samples
├── README.md  
├── passaudit.py  
├── requirements.txt  
└── audit_report.* # Generated reports (after running)


---

## ⚙️ Setup & Usage

### 1. Clone the repository
```bash
git clone https://github.com/jbanks7220/passaudit-demo.git
cd passaudit-demo
```
## 2. (Optional) Install dependencies
```
pip install -r requirements.txt
```

## 3. Run a plaintext password strength audit
```
python3 passaudit.py --input docs/passwords_mixed.txt --report audit_report 
```

Output files created in the repo root: audit_report.json, audit_report.html, audit_report.md

## 4. Run a hash-based audit (dictionary matching)

For SHA-1:
```
python3 passaudit.py --hashes docs/demo_hashes_sha1.txt --wordlist docs/passwords_weak.txt --algo sha1 --report audit_report 
```

## Demo — Quick Walkthrough 🎥

Watch the short demo to see `passaudit.py` in action: I run a plaintext audit, perform a hash-based dictionary check, and open the generated HTML report to review results.

https://github.com/user-attachments/assets/5b3ef056-038b-4c14-ab3f-8ba1eafe705f

**What’s shown**
1. Running a plaintext password audit: analyzes each password and produces JSON / HTML / MD reports.  
2. Running a hash audit: compares SHA-1 / SHA-256 hashes against a wordlist and surfaces matched (weak) passwords.  
3. Opening the generated `audit_report.html` in a browser to review the human-friendly report.

**Commands used in the demo**
```bash
# Plaintext audit (creates audit_report.json / .html / .md)
python3 passaudit.py --input docs/passwords_mixed.txt --report audit_report --verbose

# Hash audit (SHA-256 example)
python3 passaudit.py --hashes docs/demo_hashes_sha256.txt --wordlist docs/passwords_mixed.txt --algo sha256 --report audit_report --verbose

```
## 📊 Report Breakdown

Each generated report includes:

Timestamp of the audit

Plaintext password strength results (when --input is used)

Cracked hash results (when --hashes + --wordlist are used)

Readable HTML for demos and Markdown for quick GitHub viewing

Structured JSON for programmatic use

## 🧠 Skills Demonstrated

Python CLI tool development

Password strength & entropy analysis

Hashing & dictionary comparison (SHA-1, SHA-256)

File parsing and validation

Report generation (JSON, HTML, Markdown)

Security-minded, ethical tooling practices

## 👨‍💻 Author

Built by Jamir Banks

Navy veteran & former CTR | Cybersecurity hobbyist | Signals intelligence & secure comms background | Focused on defense, recon & red team skills







