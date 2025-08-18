# Security Information and Event Management (SIEM) Policy (Kanske via Sentinel one istället...)

**Document Version:** 2.0  
**Effective Date:** [Date]  
**Last Reviewed:** 2025-01-09  
**Policy Owner:** Security Manager  
**Document Type:** Information Security Policy

## 1. Purpose

This policy establishes requirements for centralized security logging from all endpoints and infrastructure at Fröjd Interactive AB to ensure comprehensive security monitoring and threat detection using Datadog Cloud SIEM as the SIEM platform.

## 2. Scope

This policy applies to:
- All endpoints (workstations, laptops) monitored by SentinelOne EDR
- All servers and cloud infrastructure monitored by Datadog
- SentinelOne EDR integration with Datadog Cloud SIEM
- Security event collection, analysis, and retention

## 3. Architecture Overview

### 3.1 Log Flow
1. **Workstations:** SentinelOne agents collect security events → API → Datadog Cloud SIEM
2. **Servers/Cloud:** Datadog agents collect logs → Direct to Datadog platform
3. **Datadog Cloud SIEM** receives, analyzes, and correlates all security data
4. **Security team** monitors unified dashboards and responds to incidents

### 3.2 Integration Architecture
- **Workstations:** SentinelOne Management API → Datadog (no Datadog agents required)
- **Servers:** Datadog Infrastructure agents with log collection
- **Authentication:** API key-based integration with SentinelOne
- **Data transfer:** HTTPS encrypted connections

## 4. Endpoint Logging Requirements

### 4.1 Mandatory Log Collection
**Workstations (via SentinelOne API):**
- Security threats and alerts
- EDR behavioral detections
- Management activity logs
- Compliance violations

**Servers/Cloud (via Datadog agents):**
- Security events (OS-level)
- Authentication logs
- Application logs
- System events
- Network security logs

### 4.2 Log Sources Configuration
- **SentinelOne EDR:** API integration for endpoint security events
- **Datadog Agents:** Direct collection from servers and cloud resources
- **Cloud Providers:** AWS CloudTrail, Azure Activity Logs
- **Applications:** Business-critical application logs via Datadog

## 5. Datadog Cloud SIEM Configuration

### 5.1 Core Components
- **Datadog Cloud SIEM:** Threat detection and investigation platform
- **Log Management:** Ingestion, indexing, and retention service
- **Security Monitoring:** Real-time threat detection engine
- **Dashboards:** Unified security visualization

### 5.2 Detection Rules
- Deploy Datadog's 350+ out-of-the-box detection rules
- SentinelOne-specific detection rules (pre-built integration)
- Custom rules for Fröjd-specific threats

### 5.3 Log Retention
- Datadog SIEM signals: 15 months
- Detections and notifications: Open-ended retention

## 6. Monitoring Requirements

### 6.1 Real-time Monitoring
- 24/7 automated monitoring via Datadog Cloud SIEM
- Real-time threat detection (within seconds)
- Integration with Slack
### 6.3 Alert Thresholds
- Failed logins: 5 attempts in 5 minutes
- Malware detection: Immediate alert
- Compliance violations: Daily summary
- System anomalies: Hourly review

## 7. Compliance

### 7.1 Coverage Requirements
- 100% endpoint coverage required
- Quarterly audit of agent status and log collection validation
- Annual security assessment

## 8. Enforcement
- Workstations without SentinelOne agents are blocked from network
- API integration health monitored continuously
- Monthly review of detection coverage

## 9. References

- ISO 27001:2022 - Information Security Management
- NIST SP 800-92 - Guide to Computer Security Log Management
- Datadog Cloud SIEM Documentation
- SentinelOne API Documentation