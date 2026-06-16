# SOC Lab 1 — NMAP Packet Investigation Project

🔍 Overview:
This project demonstrates how to perform a full SOC packet investigation workflow using only Nmap, designed for environments where GUI tools like Wireshark are unavailable or unstable.

Using a Chromebook Linux container and Nmap, this project replicates real Tier 1/Tier 2 SOC analyst techniques:

  Host discovery

  Service enumeration

  OS fingerprinting

  Full port sweeps

  Vulnerability scanning

  Targeted NSE script analysis

  Threat intelligence correlation

  SOC‑style reporting

🧠 Why This Project Matters:
Most SOC analysts don’t get full packet captures.
They rely on:

  Nmap

  Logs

  Threat intel

  Behavioral patterns

🚦 Environment Setup
Device: Chromebook
Linux container: Debian-based
Primary interface: eth0  
Tools used:

  nmap

  bash

  whois

  curl

  dig

1️⃣ Trigger Identification:
A packet investigation begins when something looks suspicious:

  Unknown outbound IP

  Repeated connection attempts

  High‑volume DNS

  Unusual ports

  Beaconing behavior

This project simulates that workflow using safe targets.

2️⃣ Host Discovery
Code: nmap -sn <IP>
Purpose: 
  Determine if the host is alive

  Identify ICMP filtering

  Detect hardened hosts

Output stored in: projects/soc-labs/lab-1/images

3️⃣ Service & Version Enumeration
Code: nmap -sV <IP>
Purpose:

Identify open ports

Detect running services

Extract version info

Spot misconfigurations

Output stored in: projects/soc-labs/lab-1/images

4️⃣ Aggressive Fingerprinting
Code: nmap -A <IP>
Provides:

OS fingerprint

Traceroute

Script results

Service banners

SSL/TLS info

Output stored in: projects/soc-labs/lab-1/images

5️⃣ Vulnerability Scanning
Code: nmap --script vuln <IP>
Checks for:

SMB vulnerabilities

SSL weaknesses

HTTP misconfigurations

Known CVEs

Output stored in: projects/soc-labs/lab-1/images
