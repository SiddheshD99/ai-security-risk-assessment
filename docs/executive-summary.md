# Executive Summary — ChatGPT Enterprise Security Risk Assessment

## Assessment Overview
This document presents the findings of a structured security risk assessment 
conducted on ChatGPT (OpenAI GPT-4) deployed as an enterprise productivity 
tool. The assessment evaluates the platform against the OWASP Top 10 for 
Large Language Model Applications and maps findings to the NIST Cybersecurity 
Framework 2.0 and EU AI Act (2024).

This assessment was conducted to help organisations operating in Ireland and 
Europe understand the security risks associated with enterprise ChatGPT 
deployment and implement appropriate controls to protect business data, 
maintain regulatory compliance, and manage AI-related risk exposure.

---

## Scope
- **Target System:** ChatGPT (OpenAI GPT-4)
- **Deployment Context:** Enterprise SaaS — employee-facing productivity tool
- **Assessment Framework:** OWASP Top 10 for LLM Applications (2025)
- **Compliance Frameworks:** NIST CSF 2.0, EU AI Act (2024), ISO/IEC 42001
- **Assessment Date:** June 2026

---

## Key Findings

### Critical Risks Identified — Immediate Action Required

**LLM01 — Prompt Injection**
The most critical risk identified. Attackers can manipulate ChatGPT inputs 
to override system instructions, bypass safety controls, and exfiltrate 
sensitive business data. In an enterprise environment with multiple 
integrations this risk has the potential for significant business impact.
Immediate implementation of input validation and prompt hardening is required.

**LLM06 — Sensitive Information Disclosure**
Employees routinely paste sensitive business data into ChatGPT for analysis 
creating significant data exposure risk. Without session isolation and DLP 
controls confidential business data and PII can be exposed to unauthorised 
users, creating GDPR breach notification obligations.
Immediate implementation of session isolation and DLP controls is required.

---

### High Risks Identified — Action Required Within 90 Days

| Risk | Finding | Priority |
|---|---|---|
| LLM02 Insecure Output Handling | Raw LLM output rendered in applications creates XSS and injection risks | High |
| LLM03 Training Data Poisoning | Fine-tuned models vulnerable to insider threat data manipulation | High |
| LLM04 Model Denial of Service | No rate limiting exposes enterprise API to availability attacks | High |
| LLM05 Supply Chain Vulnerabilities | Third party plugins lack security vetting and monitoring | High |
| LLM07 Insecure Plugin Design | Plugins operate with excessive permissions and no approval workflows | High |
| LLM08 Excessive Agency | Autonomous AI agents can execute destructive actions without oversight | High |
| LLM09 Overreliance | Employees treat AI output as authoritative without verification | High |
| LLM10 Model Theft | Fine-tuned models vulnerable to systematic extraction attacks | High |

---

## Risk Summary

| Risk Rating | Count | % of Total |
|---|---|---|
| Critical | 2 | 20% |
| High | 8 | 80% |
| Medium | 0 | 0% |
| Low | 0 | 0% |

**Overall Risk Posture: HIGH**
No risks assessed as low or medium. Immediate action required across all 
identified risk categories before enterprise deployment can be considered secure.

---

## Recommendations Summary

### Immediate Actions (0-30 days)
- Deploy input validation and prompt hardening for LLM01
- Implement session isolation and DLP controls for LLM06
- Enforce API rate limiting across all ChatGPT integrations
- Publish AI acceptable use policy to all employees

### Short Term Actions (30-90 days)
- Conduct security reviews of all third party plugins
- Implement human-in-the-loop approval for autonomous AI actions
- Deploy output sanitisation across all LLM integration points
- Deliver employee awareness training on AI risks and hallucination

### Medium Term Actions (90-180 days)
- Establish formal AI governance committee
- Conduct full red team exercise targeting LLM attack vectors
- Implement third party risk management programme for AI vendors
- Complete EU AI Act compliance gap remediation

---

## EU AI Act Compliance Summary
Several ChatGPT use cases in enterprise environments qualify as high-risk 
under the EU AI Act including HR decision support, legal drafting, and 
financial analysis. Organisations must establish risk management systems, 
implement human oversight mechanisms, and develop AI governance policies 
to meet their compliance obligations before enforcement begins.

---

## Conclusion
Enterprise deployment of ChatGPT introduces significant security risks that 
require immediate attention. All 10 OWASP LLM risks are present in a typical 
enterprise deployment with 2 rated Critical and 8 rated High. Organisations 
that implement the controls recommended in this assessment will significantly 
reduce their AI-related risk exposure and position themselves for EU AI Act 
compliance.

The security of AI deployments is a shared responsibility between the AI 
provider and the deploying organisation. This assessment provides the 
foundation for a structured AI security programme that grows with the 
organisation's AI adoption maturity.

---

*Last Updated: June 2026*