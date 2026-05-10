# Email Investigation Evidence

## Overview

This directory contains forensic evidence collected during the investigation of multiple email samples.

Evidence was collected using:

- Kali Linux (Oracle VirtualBox)
- Terminal-based forensic commands
- Raw `.eml` header extraction
- Domain intelligence tools
- External authentication validation

Additional validation performed using:

[Google Admin Toolbox Message Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/?utm_source=chatgpt.com)

---

## Evidence Categories

### Email Sample 01 — SAFE

Evidence includes:

- Raw header extraction
- Authentication validation
- Domain verification
- DNS verification
- External header analysis

### Key Findings

- SPF PASS
- DKIM PASS
- DMARC PASS
- Trusted sender infrastructure

---

### Email Sample 02 — PHISHING

Evidence includes:

- Header analysis
- Authentication review
- WHOIS domain validation
- DNS infrastructure validation
- External header verification

### Key Findings

- UPS brand impersonation
- Financial lure
- NXDOMAIN sender infrastructure
- Domain mismatch

---

### Email Sample 03 — SUSPICIOUS

Evidence includes:

- Header extraction
- Authentication analysis
- WHOIS domain investigation
- DNS verification
- External header analysis

### Key Findings

- Contextual mismatch
- Partial authentication trust
- Missing SPF
- Missing DMARC

---

## Analyst Summary

This evidence demonstrates that email investigations require:

- Technical verification
- Infrastructure analysis
- Domain intelligence
- Behavioral analysis

Technical authentication alone does not guarantee trust.
