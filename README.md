# AI Security Risk Assessment — OWASP LLM Top 10
### Applied to ChatGPT (OpenAI GPT-4) in Enterprise Environments

## Overview
This project presents a structured security risk assessment of ChatGPT (OpenAI GPT-4) deployed in an enterprise environment, evaluated against the OWASP Top 10 for Large Language Model Applications. As organisations across Ireland and Europe increasingly adopt AI tools like ChatGPT for business operations, understanding and managing the associated security risks becomes critical.

This assessment identifies real-world threat scenarios, evaluates risk exposure, documents findings in a formal risk register, and recommends security controls aligned to the EU AI Act and NIST Cybersecurity Framework.

## Objectives
- Identify and analyse the top 10 security risks in LLM applications as defined by OWASP
- Evaluate realistic enterprise attack scenarios for each risk category
- Build a structured risk register with likelihood and impact scoring
- Map recommended controls to NIST CSF 2.0 and EU AI Act requirements
- Provide actionable remediation recommendations for enterprise security teams

## Frameworks & Standards Used
- OWASP Top 10 for LLM Applications (2025)
- NIST Cybersecurity Framework (CSF) 2.0
- EU AI Act (2024)
- ISO/IEC 42001 — AI Management System

## Target System
- **Platform:** ChatGPT (OpenAI GPT-4)
- **Deployment Context:** Enterprise SaaS — employee-facing productivity tool
- **Users:** Internal employees across business units
- **Data Sensitivity:** Potentially high — business data, customer data, internal documents
- **Integration Points:** Microsoft 365, internal APIs, third party plugins

## Project Structure
- /docs — threat scenarios, risk register, control recommendations, EU AI Act mapping, executive summary
- /diagrams — threat model diagram
- /references — frameworks and sources

## Risk Assessment Summary

| Risk ID | Risk Name | Likelihood | Impact | Risk Rating |
|---|---|---|---|---|
| LLM01 | Prompt Injection | High | Critical | Critical |
| LLM02 | Insecure Output Handling | High | High | High |
| LLM03 | Training Data Poisoning | Medium | Critical | High |
| LLM04 | Model Denial of Service | Medium | High | High |
| LLM05 | Supply Chain Vulnerabilities | Medium | High | High |
| LLM06 | Sensitive Information Disclosure | High | Critical | Critical |
| LLM07 | Insecure Plugin Design | Medium | High | High |
| LLM08 | Excessive Agency | Medium | High | High |
| LLM09 | Overreliance | High | High | High |
| LLM10 | Model Theft | Low | Critical | High |

## Key Findings
Two critical risks identified — Prompt Injection (LLM01) and Sensitive Information 
Disclosure (LLM06) require immediate remediation. All 10 OWASP LLM risks present 
in a typical enterprise ChatGPT deployment. Full findings in /docs/executive-summary.md

## Recommendations
Immediate action required on input validation, session isolation, and DLP controls. 
Full recommendations with 90-day roadmap in /docs/control-recommendations.md

## EU AI Act Alignment
ChatGPT deployed in enterprise contexts may qualify as a high-risk AI system under the EU AI Act depending on use case. This assessment considers transparency requirements, risk management systems, human oversight mechanisms, and data governance obligations applicable to organisations operating within the EU.

## Author
**Siddhesh Dahiphale**  
MSc Cybersecurity — National College of Ireland, Dublin  
[LinkedIn](https://www.linkedin.com/in/siddhesh-dahiphale) | [GitHub](https://github.com/SiddheshD99)