# SOC-Analyst-Projects
Phishing Email Analysis and Defense Documentation as Part of my #100DaysOfCybersecurityChallenge and SOC Analyst Portfolio

# 📧 Phishing Email Analysis Report

## Headers
- **Date:** Sun, 23 Jul 2023 07:04:11 +0300  
- **Subject:** #CRYPTO#  
- **From:** "Mary" <noreply@att.net>  
- **To:** ruben@ruben.org  
- **Reply-To:** noreply@att.net  
- **Return-Path:** noreply@att.net  
- **CC:** phishing@pot, collin@colony.io, chris.pierce360@gmail.com, raminhenke@gmail.com  
- **Authentication Results:**  
  - SPF: None  
  - DKIM: Ignored  
  - DMARC: none  
- **Sender IP:** 192.232.233.127  
- **Resolved Host:** unifiedlayer.com  
- **Message-ID:** <BCAAD0A3.7732363@att.net>  

---

## Malicious URLs
hxxps://dsgo[.]to/CQECQECnpqY3NDSGtODt9ft2...

---

##  Description
- The email impersonates Chase Bank, claims account suspension due to unusual activity, and urges the user to click a **"Reactivate Your Account"** link.
- The sender domain and return-path are mismatched.
- The message uses **urgency**, **fear**, and **authority** to manipulate the recipient.

---

##  Artifact Analysis

### **Sender Analysis**
- Display Name: **Chase**
- Header From: `no.reply.alerts@chase.com`
- Actual Sender: `info-yagcfgyuze@boonsupply.com`
- Return Path: `att.net`
- IP Address: `192.232.233.127` (linked to `heritagejewelryandloan.com`)
- Authentication: SPF/DKIM/DMARC failed

---

##  URL Analysis
- **Reputation Check Tools Used**: URLScan, URLVoid, VirusTotal, URL2PNG
- The URL redirects to a **phishing site** aimed at stealing credentials.

---

##  Verdict
This is a **phishing attempt** leveraging impersonation, urgency, and a malicious link. The sender and URL are suspicious and have been verified as malicious through threat intelligence tools.

---

## Defense Actions 
In the real-world scenario, I will take the following Defense Actions:
a. Report the phishing email to the internal security team and log the incident for tracking and awareness.

b. Document the key indicators of compromise (IOCs), including:
i). Spoofed sender domain: boonsupply.com
ii). Return-path: att.net
iii). Suspicious IP address: 192.232.233.127
iv). Impersonated display name: “Chase”

c. Recommend that the sender domain boonsupply.com should be blocked or I will personally block it at the email gateway to prevent similar phishing emails from reaching users. 

d. Add the phishing URL (from the “Reactivate Your Account” link) to the organization's denylist on secure web gateways and firewalls.

e. Create an email filtering rule to block incoming emails that contain boonsupply.com or any related malicious URLs.

f. Block access to the phishing website on endpoint detection and response (EDR) tools and web proxy solutions to stop users from connecting to the malicious domain. Tools like Microsoft 365 Defender would be used if the organization have it.

g. Use the phishing email as part of future phishing awareness training to educate employees on recognizing urgent, bank-themed scams.

---

**1. Phishing Email Body**
![Phishing Email Body](https://github.com/user-attachments/assets/57766542-94a9-48bb-9731-e989c72c9d0a)

**2. Email Header Details**
![Ubuntu Linux Terminal View](https://github.com/user-attachments/assets/9dcd749e-4112-45b1-9a7f-e32d4bb41308)
![Sublime Text View](https://github.com/user-attachments/assets/4a9ac1e8-d2f9-4979-812d-c6e4b3476e1b)

**3. VirusTotal Scan Result**
![VirusTotal Scan Result](https://github.com/user-attachments/assets/8d012c55-948a-42a3-9616-9d6f49bb2d35)

**4. URLScan.oi Scan Result**
![URLScan io Result](https://github.com/user-attachments/assets/fc6df4a4-cf86-4120-9ab4-bd5220a9e117)
![Landing Page of Email URL scanned from URLScan io](https://github.com/user-attachments/assets/67d1b843-ed37-4b69-a277-38f96be2e2a1)

**5. URLVoid Scan Result**
![URLVoid Scan Result](https://github.com/user-attachments/assets/8308fe4d-0f97-4f17-bcc2-781212dea4e7)

**6. URL2PNG Scan Result**
![URL2PNG - Scan Result](https://github.com/user-attachments/assets/d6200ed6-1907-4238-b505-2ca51d0f0f38)



---

##  Analyst Notes
- This report is part of a SOC Analyst training and documentation project.
- Simulated response actions reflect real-world enterprise security procedures.
- **Source of Phishing Emails:** ![Phishing Pot](https://github.com/rf-peixoto/phishing_pot/tree/main/email)
  
  
--- 
**Project By:**  ![Martin Bassey](linkedin.com/in/martin-bassey)
