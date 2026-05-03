# 🎣 Gophish Setup and Phishing Simulation

## 📌 Overview
This section documents the setup and configuration of Gophish for simulating a phishing attack in a controlled lab environment.

---

## 🖥️ Environment Setup

- Attacker Machine: Kali Linux  
- Tool Used: Gophish  
- Victim Machine: Windows 10 Virtual Machine  

---

## ⚙️ Gophish Installation

1. Download Gophish and extract files:
      unzip gophish-v*.zip    cd gophish   

2. Make executable:
      chmod +x gophish   

3. Start Gophish:
      sudo ./gophish   

4. Access Admin Panel:
      https://127.0.0.1:3333   

---

## 🌐 Configuration

- Phish Server configured to listen on all interfaces:
    "listen_url": "0.0.0.0:80"  

- Campaign URL:
    http://192.168.0.117

---

## 📩 Email Template

A phishing email was created with a dynamic tracking link:

html <a href="{{.URL}}">Verify Account</a> 

This ensures each email contains a unique tracking identifier.

---

## 🌐 Landing Page

A fake login page was created to simulate credential harvesting.

Key features:
- Username and password fields
- POST method for submission
- Data capture enabled in Gophish

---

## 🚀 Campaign Execution

Steps:
1. Created user group (victim email)
2. Selected email template
3. Selected landing page
4. Configured sending profile
5. Launched campaign

---

## 📊 Results

- Email successfully delivered
- Link clicked by victim
- Credentials submitted and captured

---

## ⚠️ Note

This simulation was conducted in an isolated lab environment using fake credentials for educational purposes only
