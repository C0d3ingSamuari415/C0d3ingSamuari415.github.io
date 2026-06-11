# Packet Analysis Lab — Malware Beaconing Detection

## 📝 Overview
This lab focuses on identifying beaconing behavior in network traffic, often associated with malware communicating with a command-and-control (C2) server.

## 🎯 Objectives
- Detect periodic outbound connections  
- Identify suspicious IPs/domains  
- Validate with OSINT  
- Document findings  

## 🔧 Tools Used
- Wireshark  
- Zeek  
- OSINT platforms  

## 🧪 Investigation Steps
1. Load PCAP into Wireshark  
2. Apply filters (ip.addr, tcp.stream, dns)  
3. Identify repeating intervals  
4. Validate destination IP/domain  
5. Document findings  

## 📊 Screenshots



## 🛡️ MITRE ATT&CK Mapping
- T1071 — Application Layer Protocol  
- T1041 — Exfiltration Over C2 Channel  

## 🧠 What I Learned
- How to identify beaconing patterns  
- How to validate IOCs  
- How to document network-based threats  
