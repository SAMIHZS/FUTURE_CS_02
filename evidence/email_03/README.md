# Email Sample 03 — Suspicious Email Evidence

## Case Overview

This folder contains forensic evidence collected during the investigation of Email Sample 03.

The analyzed email promoted energy-related content using Elon Musk branding and persuasive marketing language.

Initial investigation did not immediately confirm phishing activity, but multiple trust inconsistencies required deeper validation.

---

## Evidence Included

### 1. Kali Header Extraction

Contains:

- From address
- Return-Path
- Message-ID
- Received headers

Purpose:

To identify sender identity and infrastructure.

### Key Observation

The sender domain was:

richmondanglicanchurch.com

This created a contextual mismatch with the email content.

---

### 2. Authentication Analysis

Contains:

- SPF results
- DKIM results
- DMARC results

Purpose:

To verify email authentication and trust signals.

### Results

- SPF: NONE
- DKIM: PASS
- DMARC: NONE

### Key Observation

The email showed partial technical legitimacy, but authentication results did not establish strong trust.

---

### 3. WHOIS Domain Validation

Contains:

- Domain creation date
- Registrar information
- Registration details

Purpose:

To validate sender domain legitimacy.

### Key Observation

The domain was recently created in 2025, increasing analyst scrutiny.

---

### 4. DNS Validation

Contains:

- DIG results

Purpose:

To verify active DNS infrastructure.

### Key Observation

The domain existed in DNS but only confirmed technical existence, not business legitimacy.

---

### 5. Google Header Analysis

Contains:

- External authentication validation
- Mail routing information
- Delivery chain analysis

### Key Observation

Google Header Analyzer confirmed:

- SPF: NONE
- DKIM: PASS
- DMARC: NONE

---

## Final Classification

# SUSPICIOUS

---

## Analyst Conclusion

This email was classified as **SUSPICIOUS** due to:

- Church domain + Elon/Energy content mismatch
- FOMO-based marketing language
- Missing SPF
- Missing DMARC
- Partial authentication trust

Although the infrastructure appeared partially legitimate, multiple trust inconsistencies prevented classification as safe.
