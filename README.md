# Phishing-Simulation-and-Sysmon-Detection-Lab
A hands-on phishing attack simulation lab using Gophish, with detection and investigation performed using Sysmon logs to demonstrate real-world SOC analysis of credential harvesting attacks.


🛡️ Phishing Simulation and Sysmon Detection Lab

📌 Overview

This project demonstrates a phishing attack simulation using Gophish and detection using Sysmon logs on a Windows virtual machine.

The lab was conducted in an isolated environment for cybersecurity training and analysis.

🎯 Objectives

Simulate a phishing attack using Gophish

Create a realistic phishing email and landing page

Capture submitted credentials in a controlled lab

Detect and analyze attack activity using Sysmon logs

🧠 Lab Architecture

Kali Linux (Attacker)│├── Gophish (Phishing Server)│▼Windows VM (Victim)│├── Browser (User Interaction)├── Sysmon (Event Logging)

🚀 Phishing Simulation

📩 Email Delivery

A phishing email was created using Gophish with a malicious link generated using dynamic tracking.

🌐 Landing Page

A fake login page was designed to simulate credential harvesting.

🔐 Credential Capture

User-submitted credentials were successfully captured within the Gophish dashboard.

🔍 Detection with Sysmon

Key Events Observed:

Event ID 1 → Browser process execution

Event ID 3 → Network connection to phishing server

Event ID 22 → DNS query activity

Example Finding:

The browser process initiated an outbound connection to the attacker-controlled server, confirming successful interaction with the phishing infrastructure.

🧬 Indicators of Compromise (IOCs)

Type

Value

Phishing URL

http://192.168.0.1

Attacker IP

192.168.0.117

Process

 msedge.exe

Event ID

3 (Network Connection)

🛠️ Tools Used

Gophish

Sysmon

Kali Linux

Windows VM

⚠️ Disclaimer

This project was conducted in a controlled lab environment for educational purposes only. No real users or systems were targeted.

📈 Outcome

This project demonstrates practical SOC skills including phishing simulation, credential harvesting analysis, and endpoint log investigation using Sysmon.
