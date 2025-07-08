# Endpoint Security Policy

**Document Version:** 1.0  
**Effective Date:** [Date]  
**Policy Owner:** Security Manager  
**Document Type:** Information Security Policy

## 1. Purpose

This policy establishes USB port controls and endpoint security requirements for Fröjd Interactive AB to protect against unauthorized data transfers.

## 2. Scope

This policy applies to all company-owned endpoints and removable storage devices.

## 3. USB Port Management Requirements

### 3.1 Default Configuration
- **All USB ports for removable storage:** Disabled
- **Exception:** Access with documented approval
- **Implementation:** SentinelOne Device Control

### 3.2 Blocked Devices
All removable storage media, such as USB drives, smartphones in mass storage mode, unknown/unclassified storage devices.

### 3.3 Allowed Devices (Whitelist)
Non-storage peripherals, such as keyboards, mice and monitors.

### 3.4 Exception Process
1. Business justification required
2. Leadership approval required
3. USB must be scanned for malware

## 4. Technical Implementation

### 4.1 SentinelOne Device Control Configuration
- USB storage devices: Block by default
- Exceptions: Configurable per exception
- Real-time policy enforcement

## 5. Compliance and Enforcement
- USB port blocking must be active on all endpoints
- Annual review of exceptions
- Policy violations investigated within 72 hours
- Repeated violations escalated to management
- Unauthorized USB use may result in disciplinary action

## 6. References

- ISO 27001:2022 - Information Security Management
- CIS Controls - Endpoint Security