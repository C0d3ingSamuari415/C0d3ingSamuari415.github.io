
```markdown
# Threat Detection — [KQL Detection Name]

## 📝 Overview
Explain the Azure Sentinel detection and the behavior it identifies.

## 🎯 Objectives
- Query Azure logs  
- Identify suspicious activity  
- Build KQL detection logic  
- Validate detection  

## 🔧 Tools Used
- Azure Sentinel  
- Log Analytics Workspace  
- KQL  

## 🛡️ KQL Query

```kql
SecurityEvent
| where EventID == 4688
| where CommandLine contains "[keyword]"
| project TimeGenerated, Account, CommandLine, ParentProcessName

🧪 Testing the Detection
Describe how you tested the query.

📊 Screenshots

🧠 What I Learned
- Key takeaway 1  
- Key takeaway 2  
- Key takeaway 3  


---

# 🧠 **Behavior‑Based Detection Template**  
For detections that aren’t tied to a specific tool.

```markdown
# Threat Detection — [Behavior Name]

## 📝 Overview
Describe the attacker behavior and why it needs detection.

## 🎯 Objectives
- Identify suspicious behavior  
- Build logic based on patterns  
- Validate detection  

## 🔧 Tools Used
- Any SIEM  
- Sysmon  
- OSINT  

## 🛡️ Detection Logic
Describe the logic in plain language or pseudocode.

## 🧪 Testing the Detection
Explain how you validated it.

## 📊 Screenshots


## 🧠 What I Learned
- Key takeaway 1  
- Key takeaway 2  
- Key takeaway 3  

