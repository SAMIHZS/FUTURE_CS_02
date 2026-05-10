# Email Sample 01 Analysis — X Security Alert

## Case Information

**Sample ID:** Email Sample 01  
**Email Type:** Security Notification  
**Platform:** X (formerly Twitter)  
**Analysis Environment:** Kali Linux on Oracle VirtualBox  
**Analysis Type:** Header Analysis, Authentication Validation, DNS Validation, Behavioral Verification  

---

## Email Overview

The analyzed email claimed to be a security alert from X regarding a new or unusual login attempt detected on the user's account.

---

## Header Analysis (Kali Linux)

The raw `.eml` file was extracted and analyzed in Kali Linux.

### Key Findings:

**From Address:**
X <verify@x.com>

**Return Path:**
bounce.x.com

**Message-ID Domain:**
x.com

**Mail Routing Server:**
spruce-goose-ce.x.com

### Analyst Observation:

The sender domain, return-path, message-id, and routing infrastructure were all aligned with X infrastructure. No spoofing indicators were observed.

---

## Authentication Analysis

Authentication checks were verified using Gmail Original Message and Google Admin Toolbox.

### Results:

**SPF:** PASS  
**DKIM:** PASS  
**DMARC:** PASS  

### Analyst Observation:

The email successfully passed all three major email authentication mechanisms, strongly supporting sender legitimacy.

---

## Domain and Infrastructure Validation

Domain validation was performed in Kali Linux.

### Tools Used:

- whois
- dig

### Findings:

**WHOIS Validation:**  
Confirmed that x.com is a legitimate registered domain.

**DNS Validation:**  
The domain resolved successfully and returned valid production infrastructure records.

### Analyst Observation:

Domain ownership and DNS behavior supported the legitimacy of the sender infrastructure.

---

## Behavioral Analysis

### Content Review:

- The email created urgency regarding account security.
- No password, OTP, or credential harvesting behavior was observed.
- The login location matched the user's legitimate activity.

### Analyst Observation:

The urgency present in the email was consistent with legitimate security alert behavior rather than phishing tactics.

---

## Final Classification

# SAFE

---

## Final Verdict

Based on header analysis, authentication validation, infrastructure verification, and behavioral context, this email was classified as a legitimate security notification from X.
