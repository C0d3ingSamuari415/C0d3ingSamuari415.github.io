# SOC Lab 2 — Threat Hunting: Suspicious PowerShell Activity

## 📝 Overview
This lab focuses on detecting and investigating suspicious PowerShell execution using Sysmon logs.  
The goal is to identify potential malicious activity such as encoded commands, remote downloads, or credential theft attempts.

---

## 🔧 Tools & Technologies
- Sysmon (Event ID 4104, 4688)
- Splunk / Elastic SIEM
- MITRE ATT&CK (T1059.001)
- PowerShell logging
- Sigma rules

---

## 📂 Lab Scenario
A workstation triggered multiple PowerShell Script Block Logging events.  
The SOC team suspects possible malicious execution.

Objectives:

1. Identify suspicious PowerShell commands  
2. Detect encoded or obfuscated activity  
3. Correlate parent/child processes  
4. Map activity to MITRE ATT&CK  
5. Build a detection rule  

---

## 🧪 Investigation Steps

### **1. Collected PowerShell Logs**
Queried Sysmon Event ID **4104** and **4688**.

### **2. Identified Suspicious Indicators**
- Encoded commands (`-enc`)  
- Base64 strings  
- Web requests (`Invoke-WebRequest`)  
- Download cradle patterns  
- Credential dumping attempts  

### **3. Correlated Processes**
Linked PowerShell to parent processes:

- `winword.exe`  
- `outlook.exe`  
- `explorer.exe`  

### **4. MITRE ATT&CK Mapping**
- **T1059.001 — PowerShell**  
- **T1105 — Ingress Tool Transfer**  
- **T1003 — Credential Dumping**  

---

title: Suspicious PowerShell Encoded Command
id: powershell-encoded-command
status: experimental
logsource:
  product: windows
  service: powershell
detection:
  selection:
    ScriptBlockText|contains: "-enc"
  condition: selection
level: high
tags:
  - attack.execution
  - attack.t1059.001

🧠 What I Learned...
-How to analyze PowerShell Script Block logs
-How to detect encoded/obfuscated commands
-How to correlate parent/child processes
-How to build Sigma detection rules
-How to document threat hunting investigations
