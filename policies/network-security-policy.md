# Network Security Policy

**Document Version:** 1.0  
**Effective Date:** [Date]  
**Policy Owner:** Security Manager  
**Document Type:** Information Security Policy

## 1. Purpose

This policy establishes mandatory user proxy requirements for all internet access at Fröjd Interactive AB to ensure secure and monitored internet usage.

## 2. Scope

This policy applies to all end users accessing the internet from corporate devices or networks.

## 3. Mandatory Proxy Requirements

### 3.1 Internet Access Control
- **All internet traffic MUST go through Cloudflare Access Gateway**
- **Direct internet access is PROHIBITED** from all workstations
- SSL/TLS inspection enabled for all traffic
- No bypass mechanisms allowed

### 3.2 Technical Implementation

**Cloudflare Access Configuration:**
- Proxy authentication: Required
- Certificate validation: Enabled
- Content filtering: Active
- Malware scanning: Enabled
- Data loss prevention: Integrated

## 4. User Responsibilities

- Use only the configured proxy for internet access
- Do not attempt to bypass proxy controls
- Report any proxy access issues to IT

## 5. Monitoring and Logging

### 5.1 Required Logging
- All internet access attempts
- User authentication events
- Blocked/allowed sites
- Policy violations
- Suspicious traffic patterns

## 6. Exceptions
1. Business justification required
2. Leadership approval required

## 7. Enforcement

- Bypass attempts investigated in a timely manner
- Repeated violations: Disciplinary action

## 8. References

- ISO 27001:2022 - Information Security Management
- NIST Cybersecurity Framework - Network Security