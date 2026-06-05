# Control Recommendations — ChatGPT Enterprise Deployment

## Overview
The following security controls are recommended to mitigate risks identified 
in the OWASP LLM Top 10 assessment of ChatGPT deployed in an enterprise 
environment. Controls are prioritised by risk rating and mapped to NIST CSF 2.0.

---

## Priority 1 — Critical Risk Controls

### Prompt Injection (LLM01)
- Implement strict input validation and sanitisation at all entry points
- Architect a clear separation between user input and system instructions
- Apply least privilege — restrict what data and systems the model can access
- Deploy a Web Application Firewall (WAF) with LLM-specific ruleset
- Conduct regular red team testing focused on prompt injection techniques

### Sensitive Information Disclosure (LLM06)
- Enforce strict session isolation — no shared context between users
- Implement Data Loss Prevention (DLP) at the API layer
- Define and enforce data classification policies for AI tool usage
- Prohibit pasting of PII, credentials, or confidential data into ChatGPT
- Conduct regular audits of data being passed to the model

---

## Priority 2 — High Risk Controls

### Insecure Output Handling (LLM02)
- Treat all LLM output as untrusted — never render raw HTML responses
- Implement output encoding before passing to downstream systems
- Deploy Content Security Policy (CSP) headers on all web interfaces
- Conduct security code reviews of all LLM integration points
- Sanitise model output before database insertion or API forwarding

### Training Data Poisoning (LLM03)
- Enforce strict access controls on training data pipelines
- Implement data provenance tracking and integrity verification
- Apply separation of duties in AI development and fine-tuning workflows
- Conduct regular audits of fine-tuning datasets for anomalies
- Monitor model behaviour post-deployment for unexpected outputs

### Model Denial of Service (LLM04)
- Implement API rate limiting and throttling per user and session
- Set maximum token limits on all inputs and outputs
- Monitor API usage patterns and alert on anomalies
- Implement circuit breakers to prevent cascade failures
- Define resource quotas per business unit and enforce them

### Supply Chain Vulnerabilities (LLM05)
- Maintain a complete inventory of all third party plugins and integrations
- Conduct third party risk assessments before approving any integration
- Monitor plugin behaviour and API calls continuously
- Establish a Software Bill of Materials (SBOM) for all AI deployments
- Apply automatic security scanning to plugin updates before deployment

### Insecure Plugin Design (LLM07)
- Apply least privilege to all plugin permissions — no admin level access
- Require explicit user confirmation before destructive or sensitive actions
- Implement strong authentication between plugins and backend systems
- Conduct security reviews of all plugins before production deployment
- Monitor and log all plugin API calls for anomalies

### Excessive Agency (LLM08)
- Implement human-in-the-loop approval for all high risk autonomous actions
- Define strict action boundaries for all AI agents
- Require explicit confirmation before any irreversible system action
- Log and audit all autonomous actions taken by AI systems
- Apply least privilege to all agent system permissions

### Overreliance (LLM09)
- Establish mandatory human review for AI outputs used in business decisions
- Develop and enforce an AI acceptable use policy across the organisation
- Deliver regular employee awareness training on AI hallucination risks
- Document AI usage in decision making processes for audit and compliance
- Define categories of decisions where AI output cannot be used without verification

### Model Theft (LLM10)
- Implement strict API rate limiting to prevent systematic model extraction
- Monitor query patterns continuously for signs of extraction attempts
- Watermark model outputs to detect unauthorised reproduction
- Restrict access to fine-tuned models to authenticated users only
- Conduct regular threat modelling of all AI asset attack surfaces

---

## Control Implementation Roadmap

| Timeframe | Actions |
|---|---|
| Immediate (0-30 days) | Input validation, session isolation, DLP, rate limiting |
| Short Term (30-90 days) | Plugin security reviews, SBOM, employee training, output sanitisation |
| Medium Term (90-180 days) | Full red team exercise, supply chain assessments, TPRM programme |
| Ongoing | Continuous monitoring, quarterly risk register review, annual assessment |

---

## NIST CSF 2.0 Control Mapping Summary

| NIST Function | Controls Addressed |
|---|---|
| Identify | Asset inventory, supply chain risk, AI governance |
| Protect | Access control, data security, awareness training, secure configuration |
| Detect | Continuous monitoring, anomaly detection, audit logging |
| Respond | Incident response, mitigation procedures |
| Recover | Recovery planning, lessons learned |

*Last Updated: June 2026*