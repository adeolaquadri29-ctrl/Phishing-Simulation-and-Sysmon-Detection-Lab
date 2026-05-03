6"}
# 🛡️ Phishing Attack Investigation Report

## 📌 Executive Summary
A phishing attack simulation was conducted in a controlled lab environment to evaluate detection capabilities and analyze user interaction with malicious email content.

The attack successfully resulted in credential submission, which was detected using endpoint monitoring tools.

---

## 🎯 Objectives
- Simulate phishing attack using Gophish
- Capture user credentials
- Detect attack using Sysmon logs
- Analyze indicators of compromise

---

## 🧠 Attack Scenario

1. A phishing email was sent to the victim
2. The victim opened the email
3. The victim clicked the embedded link
4. A fake login page was displayed
5. Credentials were entered and submitted

---

## 📩 Phishing Email Analysis

- Subject: Security Alert / Account Verification  
- Technique: Social Engineering  
- Link: Dynamically generated tracking URL  

---

## 🌐 Landing Page Analysis

- Fake login interface
- Designed to capture credentials
- No real authentication performed

---

## 🔐 Credential Harvesting

- Username and password successfully captured
- Data recorded in Gophish dashboard

---

## 🔍 Detection Analysis (Sysmon)

### Evidence:

- Browser execution observed (Event ID 1)
- Network connection to attacker IP (Event ID 3)
- DNS query activity (Event ID 22)

---

## 🧬 Indicators of Compromise (IOCs)

| Type | Value |
|------|------|
| IP Address | 192.168.0.117 |
| URL | http://192.168.0.117 |
| Process | edge.exe |
| Event ID | 3 |

---

## 🧠 MITRE ATT&CK Mapping

- T1566 → Phishing  
- T1204 → User Execution  
- T1056 → Credential Harvesting  

---

## ⚠️ Impact Assessment

- User credentials exposed (simulated)
- Demonstrates risk of phishing attacks
- Highlights importance of user awareness

---

## 🛡️ Recommendations

- Do not click suspicious links  
- Verify sender identity  
- Implement endpoint monitoring (Sysmon)  
- Conduct phishing awareness training  

---

## 📈 Conclusion

The simulation demonstrates how phishing attacks can successfully deceive users and how endpoint logging tools like Sysmon can be used to detect and investigate such incidents.

---

## ⚠️ Disclaimer

This project was conducted in a controlled lab environment using simulated data for educational purpose
