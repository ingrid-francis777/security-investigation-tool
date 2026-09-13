# security-investigation-tool
Automated log analysis and threat detection tool developed in PowerShell for the Advanced Scripting module at TU Dublin. Parses auth.log, powershell_log, and access.log to identify SSH brute-force attacks, malicious script execution patterns, and cross-correlate indicators of compromise (IoCs).


# Security Investigation Tool: Log Analysis & Threat Detection

An automated security utility written in PowerShell designed to parse system logs, analyze operational data, and surface actionable security threats. Developed as part of the BSc (Hons) Computing in Digital Forensics & Cyber Security curriculum at TU Dublin Blanchardstown.

## Project Overview
This tool automates the ingestion and analysis of multiple log sources within a simulated SOC (Security Operations Centre) environment to accelerate threat hunting and incident response workflows.

### Key Features
* **SSH Authentication Analysis (`auth.log`):** Identifies brute-force behavior, invalid user enumeration, and unauthorized root access patterns.
* **PowerShell Activity Auditing (`powershell_log.txt`):** Scans for obfuscated Base64 payloads, execution policy bypasses, malicious downloads, and indicators mapped to the MITRE ATT&CK® framework.
* **Web Access Correlation (`access.log`):** Cross-checks server logs against known malicious indicators in `ioc.txt` to identify active compromises.

## Tech Stack & Automation
* **Language:** PowerShell
* **Framework Alignment:** MITRE ATT&CK™ Matrix (Techniques T1027, T1087, T1560, T1059)
* **Validation:** Findings corroborated using VirusTotal and CrowdStrike Falcon Sandbox report data.

## Getting Started

### Installation & Setup
1. Clone the repository to your local analysis environment:
   ```bash
   https://github.com/ingrid-francis777/security-investigation-tool
   ```
2. Ensure the log files (`auth.log`, `powershell_log.txt`, `access.log`, and `ioc.txt`) are placed in the script directory.

### Execution
Run the automated master utility script from a PowerShell terminal:
```powershell
./Master-Log-Scanner.ps1
```

## Academic Attribution
* **Course:** BSc (Hons) Computing in Digital Forensics & Cyber Security (2nd Year)
* **Module:** Advanced Scripting (COMP H2705) - CA2 Project
* **Institution:** Technological University Dublin (TU Dublin) - Blanchardstown Campus
* **Author:** Ingrid Francis
* **Lecturer:** Dr. Jin Xu
* **Submission Date:** 24 April 2026

## License
This project is intended exclusively for educational and academic evaluation purposes.
