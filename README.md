# Email Security Analysis & Phishing Investigation

## Internship

Future Interns – Cyber Security Internship

Prepared by:

**Shaik Sami Hassan**

Portfolio: [samihzs.in](https://samihzs.in)

---

## Project Overview

This project documents a practical email security investigation conducted in Kali Linux.

The objective was to analyze real-world and simulated emails using forensic techniques to identify:

- Legitimate emails
- Phishing emails
- Suspicious emails requiring deeper validation

---

## Analysis Environment

- Kali Linux (Oracle VirtualBox)
- Terminal-based forensic analysis

---

## Tools Used

- grep
- dig
- whois
- Google Admin Toolbox
- Raw `.eml` header analysis

Useful tools:

[Google Admin Toolbox Message Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/?utm_source=chatgpt.com)

---

## Case Summary

| Sample | Category | Final Verdict |
|--------|----------|---------------|
| Email Sample 01 | X Security Alert | SAFE |
| Email Sample 02 | UPS Brand Impersonation | PHISHING |
| Email Sample 03 | Contextual Mismatch Marketing Email | SUSPICIOUS |

---

## Key Analyst Findings

### Sample 01 — SAFE

Validated through:

- SPF PASS
- DKIM PASS
- DMARC PASS
- DNS validation
- Behavioral verification

---

### Sample 02 — PHISHING

Indicators identified:

- UPS brand impersonation
- Financial incentive lure
- Sender domain mismatch
- NXDOMAIN sender infrastructure

---

### Sample 03 — SUSPICIOUS

Indicators identified:

- Church domain + Elon/energy content mismatch
- SPF missing
- DMARC missing
- FOMO marketing language

---

## Skills Demonstrated

- Email Header Analysis
- Domain Intelligence
- DNS Validation
- Authentication Analysis
- Social Engineering Detection
- Threat Classification

---

## Final Analyst Conclusion

This project demonstrates that email authentication alone does not guarantee trust.

A complete email investigation requires:

- Technical validation
- Domain reputation analysis
- Infrastructure consistency checks
- Human behavioral analysis
