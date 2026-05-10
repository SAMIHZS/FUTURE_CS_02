# Email Sample 02 — Phishing Evidence

## Case Overview

This folder contains forensic evidence collected during the investigation of Email Sample 02.

The analyzed email claimed to represent **UPS Partner**, offering an exclusive earning opportunity.

Initial analysis identified multiple phishing indicators including brand impersonation, social engineering techniques, domain inconsistencies, and infrastructure anomalies.

---

## Evidence Included

### 1. Kali Header Extraction
Contains:
- From address
- Return-Path
- Message-ID
- Received headers

Purpose:
To identify sender infrastructure and header inconsistencies.

---

### 2. Authentication Analysis
Contains:
- SPF results
- DKIM results
- DMARC results

Purpose:
To validate whether the email was technically authenticated.

Key Observation:
Although SPF and DKIM passed, the sender domain did not align with the claimed UPS brand identity.

---

### 3. WHOIS Domain Validation
Contains:
- Domain registration details
- Registrar information
- Domain creation date

Purpose:
To verify sender domain legitimacy and ownership.

Key Observation:
The domain showed no business relationship with UPS.

---

### 4. DNS Validation
Contains:
- DIG results

Purpose:
To verify active sender infrastructure.

Key Observation:
The sender subdomain returned **NXDOMAIN**, indicating that the subdomain did not currently resolve.

---

### 5. Google Header Analysis
Contains:
- External header validation
- Mail routing
- Authentication verification

Key Observation:
SPF and DKIM passed, but DMARC was not configured.

---

## Final Classification

# PHISHING

---

## Analyst Conclusion

This email was classified as **phishing** due to:

- Brand impersonation (UPS)
- Financial incentive lure
- Unknown sender infrastructure
- DNS inconsistencies
- Lack of trusted business alignment
