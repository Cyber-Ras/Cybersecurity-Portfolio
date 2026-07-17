# Wazuh SIEM Homelab – Vulnerability Detection and Remediation

## Overview

This project demonstrates the deployment and operation of a two-node Wazuh SIEM homelab used to identify, investigate, remediate, and validate a high-severity vulnerability on a monitored Linux endpoint.

The lab simulates a real-world Security Operations Center (SOC) workflow by combining endpoint monitoring, vulnerability management, risk assessment, remediation, validation, and security hardening activities.

---

## Objectives

- Deploy a functional SIEM environment
- Monitor Linux endpoints with Wazuh
- Investigate high-severity vulnerabilities
- Apply risk-based remediation decisions
- Validate remediation effectiveness
- Improve overall security posture

---

## Lab Environment

### SIEM Platform

- Wazuh SIEM

### Infrastructure

| Component | Description |
|------------|-------------|
| Wazuh Manager | Dedicated Linux VM |
| Endpoint | Kali Linux VM |
| Monitoring | Wazuh Agent |
| Networking | VirtualBox NAT Network |

---

## Architecture

```text
Kali Linux Endpoint
        │
        │ Wazuh Agent
        ▼
Wazuh Manager SIEM
        │
        ▼
Dashboard Monitoring
```

---

## Detection Phase

The Wazuh dashboard identified a high-severity vulnerability on the monitored endpoint.

### Alert Details

| Item | Value |
|------|--------|
| Agent | kali |
| Package | weasyprint |
| Installed Version | 67.0 |
| Severity | High |
| CVE | CVE-2025-68616 |

---

## Investigation

The vulnerability was investigated to determine:

- Whether the software was intentionally installed
- Availability of patched versions
- Potential business impact
- Appropriate remediation strategy

Findings:

- Package was not required for current learning objectives
- Software likely existed as a dependency
- No patched version was available at time of review
- Retaining unnecessary vulnerable software increased attack surface

---

## Risk Assessment

Applied the security principle of:

### Attack Surface Reduction

Rather than retain vulnerable and unnecessary software, the decision was made to remove the package entirely.

This mirrors real-world security decision making where removal can be safer than accepting unnecessary risk.

---

## Remediation Actions

Executed the following commands:

```bash
sudo apt remove weasyprint -y
sudo apt autoremove -y
sudo systemctl restart wazuh-agent
```

---

## Validation Phase

Following remediation:

- Endpoint agent was refreshed
- Vulnerability data was rescanned
- Dashboard findings were reviewed

### Result

```text
High Severity Findings: 0
```

This confirmed successful remediation and reduction of endpoint risk.

---

## Post-Remediation Hardening

Additional hardening activities were performed.

### Administrative Security Improvements

- Accessed Wazuh server via SSH
- Rotated default administrator credentials
- Configured a strong replacement password
- Validated secure administrative access

---

## Security Concepts Demonstrated

- SIEM Operations
- Vulnerability Management
- Endpoint Security Monitoring
- Security Hardening
- Identity and Access Management
- Risk Assessment
- Attack Surface Reduction
- Security Validation

---

## Skills Demonstrated

- Wazuh Administration
- SIEM Monitoring
- Linux Administration
- Vulnerability Detection
- Security Investigation
- Threat Triage
- Remediation Planning
- Documentation
- Analytical Thinking

---

## SOC Workflow Demonstrated

1. Detect
2. Investigate
3. Assess Risk
4. Remediate
5. Validate
6. Harden
7. Document Findings

---

## Key Lessons Learned

- Not all vulnerabilities require patching.
- Removing unnecessary software can reduce attack surface.
- Validation is a critical part of remediation.
- Secure configuration practices extend beyond vulnerability management.
- Documentation transforms labs into demonstrable experience.

---

## Professional Relevance

This project demonstrates practical experience with tasks commonly performed by:

- SOC Analysts
- Security Operations Analysts
- Vulnerability Management Analysts
- Blue Team Analysts
- Incident Response Teams

The lab provides hands-on experience with SIEM operations, endpoint monitoring, risk reduction, and remediation workflows frequently encountered in enterprise environments.
