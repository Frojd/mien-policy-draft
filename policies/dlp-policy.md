# Data Loss Prevention (DLP) Policy

**Document Version:** 1.0  
**Effective Date:** [Date]  
**Policy Owner:** Security Manager  
**Document Type:** Information Security Policy

## 1. Purpose

This policy establishes the DLP program for Fröjd Interactive AB to protect sensitive information from unauthorized disclosure across all data transmission channels.

## 2. Scope

This policy applies to:
- All systems and devices that process, store, or transmit sensitive data
- All data transmission channels: email, web, removable media, instant messaging, and social media
- All employees and contractors

## 3. DLP Implementation Requirements

### 3.1 Technical Controls

**SentinelOne Device Control (USB/Removable Media Only):**
- USB and removable media controls must be enabled
- Block all unauthorized data transfers to external storage devices

**Cloudflare Gateway DLP (Web Traffic):**
- Scan and prevent data loss across:
  - Web uploads
  - Cloud storage services (Google Drive, Dropbox, etc.)
  - Email
  - Outgoing traffic http/https traffic
- Implement SSL inspection for encrypted traffic

### 3.2 Mandatory DLP Rules

**Blocking Rules:**
- Block upload of files containing credit card numbers
- Block external sharing of files marked "Confidential" or "Restricted"
- Block unencrypted transmission of PII

## 4. Data Classification

- **Restricted:** PII, PCI data, financial records, client confidential information
- **Confidential:** Sensitive business information, intellectual property
- **Internal:** Information for internal use only
- **Public:** Information intended for public disclosure

## 5. Incident Response

- DLP violations must be investigated in a timely manner
- Security team reviews all DLP alerts
- Repeated violations escalated to management

## 6. References

- ISO 27001:2022 - Information Security Management
- GDPR - Data Protection Requirements