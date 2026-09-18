# SOAR-Based-EDR-Endpoint-Response-Playbook
# SOAR-Based EDR Endpoint Response Playbook

> **Automated Endpoint Detection & Response Workflow for Controlled Security Operations**

## Overview

A security automation project that demonstrates how an EDR alert can be processed through an automated response workflow, with analyst approval before endpoint isolation.

The playbook integrates **LimaCharlie, Tines, Webhook, Slack, and HTTP-based response actions** to create a structured endpoint response process.

## Purpose

The purpose of this project is to demonstrate a practical and controlled approach to endpoint incident response by automating repetitive response steps while keeping the final isolation decision under analyst control.

It focuses on improving response consistency, reducing manual intervention, and providing a clear workflow for handling endpoint security alerts.

## Response Workflow

```text
EDR Alert
    ↓
Webhook
    ↓
Rules
    ↓
LimaCharlie
    ↓
Slack
    ↓
Analyst Decision
   ↙       ↘
 YES       NO
  ↓         ↓
HTTP      Skip
Request   Isolation
  ↓         ↓
Endpoint ──→ Slack
Isolation
```

## Key Capabilities

* EDR alert ingestion and processing
* Rule-based security workflow
* Analyst-controlled response decision
* Automated endpoint isolation
* HTTP-based response execution
* Slack-based alert and response communication
* Controlled Windows VM testing environment

## Technology Stack

**EDR:** LimaCharlie
**Orchestration:** Tines
**Integration:** Webhook, HTTP
**Communication:** Slack
**Testing:** Windows 10 VM, VMware

## Repository Structure

```text
├── workflow/          # Playbook JSON
├── documentation/     # Project documentation
├── research-paper/    # Research paper
├── figures/           # Workflow figures
└── README.md
```

## Security Focus

The project demonstrates a controlled approach to endpoint incident response by separating:

**Detection → Processing → Decision → Response → Notification**

This structure makes the workflow easier to test, maintain, and extend for additional security-response scenarios.

## Project Documentation

Detailed implementation documentation and the associated research paper are available in the repository.

## Conclusion

This project demonstrates how EDR detection and security automation can be combined into a structured endpoint response workflow. By integrating alert processing, analyst decision-making, automated isolation, and response notification, the playbook provides a practical foundation for controlled security operations and can be extended to support additional incident-response actions.

---

**Author:** Afnan Qureshi
**Domain:** Cybersecurity | EDR | Security Automation | Incident Response
