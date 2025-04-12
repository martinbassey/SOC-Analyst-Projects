# SOC-Analyst-Projects
Phishing Email Analysis and Defense Documentation as part of my SOC Analyst Portfolio
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

## 📝 Description
- The email impersonates Chase Bank, claims account suspension due to unusual activity, and urges the user to click a **"Reactivate Your Account"** link.
- The sender domain and return-path are mismatched.
- The message uses **urgency**, **fear**, and **authority** to manipulate the recipient.

---

## 🔬 Artifact Analysis

### **Sender Analysis**
- Display Name: **Chase**
- Header From: `no.reply.alerts@chase.com`
- Actual Sender: `info-yagcfgyuze@boonsupply.com`
- Return Path: `att.net`
- IP Address: `192.232.233.127` (linked to `heritagejewelryandloan.com`)
- Authentication: SPF/DKIM/DMARC failed

---

## 🌐 URL Analysis
- **Reputation Check Tools Used**: URLScan, URLVoid, VirusTotal, URL2PNG
- The URL redirects to a **phishing site** aimed at stealing credentials.

---

## 🧠 Verdict
This is a **phishing attempt** leveraging impersonation, urgency, and a malicious link. The sender and URL are suspicious and have been verified as malicious through threat intelligence tools.

---

## 🛡️ Defense Actions Taken
1. **Report** phishing email and log the incident.
2. **Document IOCs**: spoofed domain, IP, return-path, fake display name.
3. **Recommend blocking** `boonsupply.com` at the email gateway.
4. **Add phishing URL** to the organization's URL denylist.
5. **Create filtering rules** to block emails containing the phishing domain.
6. **Block domain access** via EDR/web proxy.
7. **Use sample in phishing awareness training.**

---

## 🖼️ Screenshot Evidence
**1. Phishing Email Body**
![Phishing Email Body](images/phishing_email_body.png)

**2. Email Header Details**
![Email Headers](images/email_headers.png)

**3. VirusTotal Scan Result**
![VirusTotal Scan](images/virustotal_url_scan.png)


*Add screenshots of the email body, headers, URL scanner results, etc.*

---

## 👨🏽‍💻 Analyst Notes
- This report is part of a SOC Analyst training and documentation project.
- Simulated response actions reflect real-world enterprise security procedures.
