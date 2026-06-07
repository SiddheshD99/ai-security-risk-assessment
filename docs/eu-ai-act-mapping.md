# EU AI Act Mapping — ChatGPT Enterprise Deployment

## Overview
The EU AI Act (2024) introduces a risk-based regulatory framework for AI systems 
operating within the European Union. This document maps the security risks identified 
in the OWASP LLM Top 10 assessment to relevant EU AI Act obligations, helping 
organisations understand their compliance responsibilities when deploying ChatGPT 
in an enterprise environment.

---

## EU AI Act Risk Classification

### ChatGPT in Enterprise — Risk Category Assessment

| Use Case | EU AI Act Risk Category | Rationale |
|---|---|---|
| General productivity assistant | Limited Risk | Requires transparency obligations only |
| HR decision support | High Risk | Influences employment decisions |
| Legal and compliance drafting | High Risk | Influences legal interpretation |
| Customer service automation | Limited Risk | Requires transparency obligations |
| Financial analysis and reporting | High Risk | Influences financial decisions |
| Security operations support | High Risk | Influences critical infrastructure decisions |

---

## Key EU AI Act Obligations

### Article 9 — Risk Management System
Organisations deploying high-risk AI systems must establish a risk management 
system covering the entire lifecycle of the AI system.

**Mapping to Assessment:**
- Risk register maintained and reviewed regularly
- Threat scenarios documented for all identified risks
- Control recommendations defined and assigned to owners
- Implementation roadmap established with clear timeframes

**Compliance Status:** Partially addressed — full compliance requires ongoing 
risk management programme beyond initial assessment

---

### Article 10 — Data and Data Governance
Training, validation, and testing datasets must meet quality criteria and be 
free from errors and biases that could lead to discriminatory outcomes.

**Mapping to Assessment:**
- LLM03 (Training Data Poisoning) directly addresses data integrity risks
- Controls include data provenance tracking and integrity verification
- Separation of duties in fine-tuning workflows reduces insider threat risk

**Compliance Status:** Controls recommended — implementation required

---

### Article 13 — Transparency and Provision of Information
High-risk AI systems must be transparent — users must be informed they are 
interacting with an AI system and understand its capabilities and limitations.

**Mapping to Assessment:**
- LLM09 (Overreliance) addresses transparency and human oversight gaps
- Acceptable use policy and employee training controls address this obligation
- Documentation of AI usage in decision making processes required

**Compliance Status:** Controls recommended — policy development required

---

### Article 14 — Human Oversight
High-risk AI systems must be designed to allow effective human oversight, 
enabling humans to intervene, override, or shut down the system.

**Mapping to Assessment:**
- LLM08 (Excessive Agency) directly addresses human oversight failures
- Human-in-the-loop controls recommended for all high risk autonomous actions
- Explicit confirmation requirements before irreversible actions

**Compliance Status:** Controls recommended — implementation required

---

### Article 15 — Accuracy, Robustness and Cybersecurity
High-risk AI systems must achieve appropriate levels of accuracy and be 
resilient against attempts by unauthorised third parties to alter outputs.

**Mapping to Assessment:**
- LLM01 (Prompt Injection) — input validation and prompt hardening controls
- LLM04 (Model DoS) — rate limiting and availability controls
- LLM07 (Insecure Plugin Design) — plugin security and least privilege controls
- LLM10 (Model Theft) — extraction monitoring and watermarking controls

**Compliance Status:** Controls recommended — technical implementation required

---

### Article 28 — General Purpose AI Model Obligations
Providers of general purpose AI models like GPT-4 must maintain technical 
documentation, comply with copyright law, and publish summaries of training data.

**Mapping to Assessment:**
- Organisations using ChatGPT inherit obligations from OpenAI as the provider
- Enterprise deployments must ensure OpenAI's compliance documentation is reviewed
- Supply chain risk assessment (LLM05) addresses third party provider obligations

**Compliance Status:** Dependent on OpenAI compliance — vendor assessment recommended

---

## Compliance Gap Analysis

| EU AI Act Obligation | Current Status | Gap | Recommended Action |
|---|---|---|---|
| Risk Management System | Partial | No ongoing programme | Establish quarterly review cycle |
| Data Governance | Not implemented | No data classification policy | Develop and enforce AI data policy |
| Transparency | Not implemented | No user disclosure mechanism | Implement AI usage disclosure |
| Human Oversight | Not implemented | No approval workflows | Implement human-in-the-loop controls |
| Cybersecurity Controls | Partial | Technical controls not deployed | Implement priority 1 controls immediately |
| Provider Obligations | Partial | OpenAI compliance not reviewed | Conduct vendor security assessment |

---

## Recommended Next Steps

1. Classify all ChatGPT use cases by EU AI Act risk category
2. Establish a formal AI governance committee
3. Develop an AI acceptable use policy aligned to EU AI Act obligations
4. Implement technical controls identified in control-recommendations.md
5. Conduct annual EU AI Act compliance review
6. Monitor EU AI Act enforcement guidance as it develops

---

*Last Updated: June 2026*