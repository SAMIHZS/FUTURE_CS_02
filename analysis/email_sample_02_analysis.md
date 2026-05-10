# Email Sample 02 Analysis — UPS Brand Impersonation Phishing

## Case Information

**Sample ID:** Email Sample 02  
**Email Type:** Business Opportunity / Brand Impersonation Phishing  
**Claimed Brand:** UPS  
**Analysis Environment:** Kali Linux on Oracle VirtualBox  
**Analysis Type:** Header Analysis, Authentication Validation, Domain Verification, DNS Validation, Social Engineering Analysis  

---

## Email Overview

The analyzed email claimed to represent **UPS Partner** and presented a business opportunity promising financial rewards through an "exclusive partnership."

The subject line used persuasive language designed to attract user interest:

> "Exclusive UPS Partnership Opportunity - Unlock Your Earnings!"

Initial observations suggested possible phishing activity due to brand impersonation and financial incentive tactics.

---

## Header Analysis (Kali Linux)

Raw `.eml` header analysis revealed the following:

### From Address

UPS Partner <Hoffman_John_49321@ali001.sarakzit.za.com>

### Return Path

Hoffman_John_49321@ali001.sarakzit.za.com

### Message-ID Domain

dcccd.edu

### Analyst Observation

Multiple infrastructure inconsistencies were identified:

- The sender claimed to represent **UPS**, but the sender domain did not belong to UPS infrastructure.
- The message-id domain differed from the sender domain.
- The email showed signs of possible infrastructure relay abuse or deceptive sender identity.

These findings significantly reduced sender trust.

---

## Authentication Analysis

Authentication analysis was performed using Kali Linux and Google Admin Toolbox.

### Results

**SPF:** PASS  
**DKIM:** PASS  
**DMARC:** NONE  

### Analyst Observation

The sender domain successfully passed SPF and DKIM authentication for its own infrastructure.

However:

This authentication only validated the sender’s own domain—not the claimed UPS brand identity.

The absence of DMARC enforcement further reduced trust.

---

## Domain Validation

WHOIS analysis was performed on the registered root domain.

### Domain Investigated

za.com

### Findings

- Domain creation date: 1998
- Registered using a legitimate registrar
- No ownership or infrastructure relationship with UPS

### Analyst Observation

Although the domain itself was legitimately registered, there was no evidence connecting it to UPS business infrastructure.

This supported the brand impersonation hypothesis.

---

## DNS Validation

DNS validation was performed using `dig`.

### Sender Subdomain

ali001.sarakzit.za.com

### Result

NXDOMAIN

### Analyst Observation

The sender subdomain did not currently resolve in DNS.

This suggested:

- Disposable infrastructure
- Expired or temporary phishing infrastructure
- Suspicious sender inconsistency

This significantly increased phishing confidence.

---

## Social Engineering Analysis

The email used the following psychological tactics:

### Financial Incentive

"Unlock Your Earnings"

### Brand Authority

Use of UPS branding to create trust.

### Analyst Observation

The email attempted to lower user skepticism by combining:

- Trusted business branding
- Financial opportunity language
- Curiosity and greed-based persuasion

These are common phishing characteristics.

---

## Final Classification

# PHISHING

---

## Final Verdict

Although the email passed SPF and DKIM authentication for its own domain, multiple indicators confirmed phishing behavior:

- UPS brand impersonation
- Domain mismatch
- Message-ID inconsistency
- NXDOMAIN sender infrastructure
- Social engineering through financial incentives

Based on technical and behavioral analysis, this email was classified as **PHISHING**.
