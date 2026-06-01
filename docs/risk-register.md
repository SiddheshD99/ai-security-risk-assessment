# Risk Register — ChatGPT Enterprise Deployment
## OWASP LLM Top 10 Risk Assessment

| Risk ID | Risk Name | Likelihood | Impact | Risk Rating | Priority | Owner |
|---|---|---|---|---|---|---|
| LLM01 | Prompt Injection | High | Critical | Critical | 1 | Security Team |
| LLM06 | Sensitive Information Disclosure | High | Critical | Critical | 2 | Security Team |
| LLM02 | Insecure Output Handling | High | High | High | 3 | Development Team |
| LLM03 | Training Data Poisoning | Medium | Critical | High | 4 | AI/ML Team |
| LLM04 | Model Denial of Service | Medium | High | High | 5 | Infrastructure Team |
| LLM05 | Supply Chain Vulnerabilities | Medium | High | High | 6 | Security Team |
| LLM07 | Insecure Plugin Design | Medium | High | High | 7 | Development Team |
| LLM08 | Excessive Agency | Medium | High | High | 8 | Security Team |
| LLM09 | Overreliance | High | High | High | 9 | Business Owners |
| LLM10 | Model Theft | Low | Critical | High | 10 | Security Team |

---

## Risk Scoring Methodology

### Likelihood
| Rating | Description |
|---|---|
| High | Likely to occur — known attack vector, low barrier to execute |
| Medium | Possible — requires some skill or specific conditions |
| Low | Unlikely — requires significant resources or insider access |

### Impact
| Rating | Description |
|---|---|
| Critical | Severe business impact — data breach, regulatory action, major financial loss |
| High | Significant impact — service disruption, data exposure, reputational damage |
| Medium | Moderate impact — limited data exposure, recoverable disruption |
| Low | Minimal impact — negligible business consequence |

### Risk Rating Matrix
| | Critical Impact | High Impact | Medium Impact |
|---|---|---|---|
| High Likelihood | Critical | High | Medium |
| Medium Likelihood | High | High | Medium |
| Low Likelihood | High | Medium | Low |

---

## Critical Risks — Immediate Action Required

### LLM01 — Prompt Injection (Critical)
- **Current Status:** Unmitigated
- **Recommended Action:** Implement input validation and prompt hardening immediately
- **Target Completion:** 30 days
- **Residual Risk After Controls:** Medium

### LLM06 — Sensitive Information Disclosure (Critical)
- **Current Status:** Unmitigated
- **Recommended Action:** Implement session isolation and DLP controls
- **Target Completion:** 30 days
- **Residual Risk After Controls:** Low

---

## Risk Treatment Options

| Option | Description |
|---|---|
| Mitigate | Implement controls to reduce likelihood or impact |
| Accept | Acknowledge risk and monitor — acceptable residual risk |
| Transfer | Transfer risk via cyber insurance or third party agreement |
| Avoid | Discontinue the activity that introduces the risk |

---

## Review Schedule
- Critical risks — reviewed monthly
- High risks — reviewed quarterly
- Full register review — annually or after significant incidents

*Last Updated: June 2026*
