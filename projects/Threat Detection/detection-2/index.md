# Threat Detection — [Sigma Rule Name]

## 📝 Overview
Explain the malicious behavior this Sigma rule detects.

## 🎯 Objectives
- Detect suspicious process execution  
- Identify encoded or obfuscated commands  
- Map to MITRE ATT&CK  

## 🔧 Tools Used
- Sigma  
- Sysmon  
- Windows Event Logs  

## 🛡️ Sigma Rule

```yaml
title: [Add Title]
id: [unique-id]
status: experimental
logsource:
  product: windows
  service: sysmon
detection:
  selection:
    CommandLine|contains: "[keyword]"
  condition: selection
level: high
tags:
  - attack.execution
  - attack.t1059

🧪 Testing the Rule
Describe how you validated it.

📊 Screenshots


🧠 What I Learned
Key takeaway 1

Key takeaway 2

Key takeaway 3


---

# 🔭 **KQL Detection Template (Azure Sentinel)**  
**Location:**  
