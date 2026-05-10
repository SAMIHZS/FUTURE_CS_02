# Email Sample 03 Analysis — Suspicious Contextual Mismatch Email

## Case Information

**Sample ID:** Email Sample 03  
**Email Type:** Suspicious Promotional Email  
**Analysis Environment:** Kali Linux on Oracle VirtualBox  
**Analysis Type:** Header Analysis, Authentication Validation, Domain Verification, DNS Validation, Behavioral Analysis  

---

## Email Overview

The analyzed email promoted future-oriented energy content using persuasive marketing language.

### Subject

> "Stay Ahead: The Future of Energy is Here"

The content referenced Elon Musk and energy-related messaging.

Initial review did not immediately confirm phishing activity, but multiple trust inconsistencies required deeper investigation.

---

## Header Analysis (Kali Linux)

Raw `.eml` header analysis identified:

### Return Path

deaglefilomena@richmondanglicanchurch.com

### Sender Domain

richmondanglicanchurch.com

### Analyst Observation

The sender domain appeared related to a church organization.

However, the email content promoted:

- Elon Musk
- Future energy
- Marketing-oriented persuasion

This created a major contextual mismatch.

This was identified as the strongest suspicious indicator.

---

## Authentication Analysis

Authentication validation was performed using Kali Linux and Google Admin Toolbox:

[Google Admin Toolbox Message Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/?utm_source=chatgpt.com)

### Results

**SPF:** NONE  
**DKIM:** PASS (Unknown Signing Domain)  
**DMARC:** NONE  

### Analyst Observation

The email showed partial technical legitimacy.

However:

- No visible SPF enforcement
- No DMARC protection
- DKIM alone did not establish strong sender trust

These findings created uncertainty rather than confidence.

---

## Domain Validation

WHOIS analysis was performed on the sender domain.

### Findings

**Domain:** richmondanglicanchurch.com  
**Creation Date:** 2025  
**Registrar:** Gname

### Analyst Observation

The domain was legitimate and registered.

However:

- The domain was relatively new
- The content theme did not align with the organization identity

This increased suspicion.

---

## DNS Validation

DNS analysis was performed using `dig`.

### Result

NOERROR

### Additional Findings

The domain existed in DNS but did not return strong active infrastructure evidence.

### Analyst Observation

DNS confirmed technical existence only.

It did not establish business legitimacy.

---

## Behavioral Analysis

The email used the following psychological techniques:

### FOMO (Fear of Missing Out)

Examples:

- "Stay Ahead"
- Future-oriented messaging
- Innovation positioning

### Contextual Mismatch

A church-related domain promoting Elon Musk / energy content significantly reduced trust.

---

## Final Classification

# SUSPICIOUS

---

## Confidence Level

4/5

---

## Final Verdict

This email was classified as **SUSPICIOUS**.

Although the infrastructure showed partial technical legitimacy, multiple contextual inconsistencies, weak authentication confidence, and behavioral manipulation indicators prevented classification as safe.
