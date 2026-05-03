
# 🔍SSysmon Detection and Analysis

## 📌 Overview
This section analyzes endpoint activity generated during the phishing attack using Sysmon logs.

---

## 🛠️ Tool Used
- Sysmon (System Monitor)
- Windows Event Viewer / PowerShell

---

## 🎯 Detection Objective
To identify evidence of phishing interaction on the victim machine.

---

## 📊 Key Sysmon Event IDs

### 🟢 Event ID 1 — Process Creation
Indicates execution of browser processes such as:

- msedge.exe

---

### 🔴 Event ID 3 — Network Connection (CRITICAL)

This event confirms communication with the phishing server.

This indicates the victim accessed the phishing link.

---

### 🟡 Event ID 22 — DNS Query

Shows domain resolution activity triggered when accessing the phishing link.

---

## 🔎 Analysis Steps

1. Open PowerShell as Administrator

2. Filter network connections:
      Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" | Where-Object {$_.Id -eq 3}   

---

## 📌 Key Findings

- Browser process initiated outbound connection to phishing server
- Network activity confirms user interaction with malicious link
- DNS queries observed prior to connection

---

## 🧬 Indicators of Compromise (IOCs)

- Protocol: HTTP  
- Process: msedge.exe  

---

## 🎯 Conclusion

Sysmon logs successfully captured endpoint activity related to the phishing attack, providing clear evidence of user interaction and network communication with the attacker-controlled serv
