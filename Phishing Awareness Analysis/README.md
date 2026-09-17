# Phishing Awareness Analysis

## 1. Executive Summary
* **Objective:** Analyze simulated and real-world phishing methodologies to identify social engineering vectors, indicators of compromise (IoCs), and technical red flags.
* **Scope:** Covers threat taxonomies, attack vectors, behavioral indicators, and mitigation strategies.

---

## 2. What is Phishing?
Phishing is a prevalent cyber attack vector that relies heavily on social engineering rather than purely technical software exploitation. Attackers manipulate human psychology—such as fear, urgency, curiosity, or greed—to trick victims into:
* Disclosing sensitive credentials (passwords, MFA tokens, API keys).
* Exfiltrating confidential corporate or personal data.
* Downloading and executing malicious payloads (ransomware, infostealers, Remote Access Trojans).

---

## 3. Taxonomy: Major Types of Phishing Attacks

* **Email Phishing (Mass Phishing):** 
  * *Description:* Broad, untargeted campaigns broadcasted to millions of users simultaneously.
  * *Characteristics:* Usually impersonates popular consumer services, streaming platforms, or banks with generic greetings.
* **Spear Phishing:** 
  * *Description:* Highly customized, targeted attacks directed at specific individuals or small departments within an organization.
  * *Characteristics:* Attackers perform open-source intelligence (OSINT) gathering via LinkedIn or corporate sites to craft contextually accurate and convincing messages.
* **Whaling:** 
  * *Description:* A specialized form of spear phishing aimed explicitly at high-profile organizational targets, such as C-level executives (CEOs, CFOs), board members, or high-net-worth individuals.
  * *Characteristics:* Frequently attempts to compel fraudulent financial wire transfers or request sensitive legal/tax data (often referred to as Business Email Compromise or BEC).
* **Vishing (Voice Phishing):** 
  * *Description:* Phishing conducted over phone calls or Voice over IP (VoIP) channels.
  * *Characteristics:* Attackers often use caller ID spoofing to masquerade as internal IT desks, government tax authorities, or bank fraud departments, coercing victims into reading out One-Time Passwords (OTPs).
* **Smishing (SMS Phishing):** 
  * *Description:* Phishing carried out via text messages or mobile messaging applications (WhatsApp, Telegram).
  * *Characteristics:* Typically features urgent alerts regarding unpaid delivery customs, bank account freezes, or toll charges, complete with a shortened malicious URL.
* **Clone Phishing:** 
  * *Description:* Attackers intercept a legitimate, previously delivered email containing an attachment or link, replicate it precisely, and swap out the benign link or payload for a malicious one.
* **Watering Hole Attacks:** 
  * *Description:* A strategic attack vector where websites frequently visited by a specific target group (e.g., industry-specific news portals or vendor sites) are compromised to silently drop malicious payloads onto visitors' systems.

---

## 4. Key Indicators of Compromise (IoCs) & Red Flags

When evaluating an incoming message or email headers, analysts look for the following red flags:
* **Mismatched Sender Information:** Display names that claim to represent a trusted entity (e.g., "Microsoft Security"), while the underlying email header or domain uses a free or suspicious external domain.
* **Typosquatting & Lookalike Domains:** Domain names intentionally misspelled to fool the eye (e.g., `amaz0n.com` or `paypa1-support.com`).
* **Artificial Urgency & Coercion:** Language designed to induce panic or rush decision-making (e.g., "Your account will be deleted in 2 hours if you don't log in now").
* **Generic Salutations:** Mass phishing emails frequently default to generic openers like "Dear User" or "Dear Customer" instead of proper name addressing.
* **Suspicious Link Destinations:** Hyperlinks whose visible text points to a legitimate site, but whose actual underlying URL directs to an attacker-controlled infrastructure.
* **Unsolicited Attachments:** Unexpected document files (macros-enabled Word files, compressed archives, or ISO files) purporting to be invoices or resumes.
