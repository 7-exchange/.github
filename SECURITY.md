# Security Policy

7.Exchange is a non-custodial, cross-chain execution layer that moves real value across multiple networks. We take security extremely seriously and deeply appreciate the work of security researchers who help keep users safe.

This policy explains **how to report a vulnerability**, **what is in scope**, and **the rules for good-faith research**.

This policy follows the published [Bug Bounty Program](https://docs.7.exchange/security/bug-bounty-program).

---

## Reporting a vulnerability

**Do not open a public GitHub issue, pull request, or Discord/Telegram message for security vulnerabilities.** Public disclosure before a fix is deployed puts user funds at risk.

File a private ticket with your findings through our [bug report panel](https://discord.gg/DArANebGFm) on Discord.

Please include, where possible:

- A clear description of the issue and its security impact
- The affected component (contract address, repo, endpoint, or URL) and chain
- Step-by-step reproduction, proof-of-concept, or transaction hashes (testnet preferred)
- The commit hash / contract version and the environment you tested against
- Any suggested remediation

We will acknowledge your report, work with you on validation, and keep you updated through resolution.

### Our response targets

| Stage | Target |
|---|---|
| Acknowledge receipt | within **48 hours** |
| Initial severity assessment | within **5 business days** |
| Resolution | timeline depends on complexity; we will keep you informed of progress |
| Public disclosure | only after the vulnerability has been acknowledged and resolved |

---

## Scope

In scope:

- **7.Exchange smart contracts** — The Diamond Router contracts are in pre-deployment testing. Vulnerabilities found in these contracts during the bounty period are in scope.
- **Platform security** — Critical vulnerabilities affecting the integrity of quotes, execution payloads, or user data.

### Out of scope

- Third-party bridge or DEX smart contracts (report these to the respective projects)
- UI/UX bugs that do not have a security impact
- Social engineering attacks
- Denial-of-service attacks
- Issues already known or previously reported

---

## Rewards

Rewards are determined based on the severity and impact of the vulnerability. Factors include:

- Potential for fund loss
- Scope of affected users
- Complexity of the exploit
- Quality of the report

Reward amounts are determined at 7.Exchange's discretion and communicated during the assessment phase.

---

## Rules

- Act in good faith. Test only against test environments or your own accounts.
- Do not exploit vulnerabilities beyond what is necessary to demonstrate the issue.
- Do not access, modify, or delete other users' data.
- One report per vulnerability. Duplicate reports are not eligible for rewards.
- Compliance with applicable laws is required.

> Attempting to exploit vulnerabilities on production systems, accessing other users' funds or data, or violating the rules above will disqualify you from the program and may result in legal action.

> This document is a security policy, not a contract or a guarantee of payment, and does not grant permission to act unlawfully or to access third-party systems.

---

## Disclosure

We practice coordinated disclosure. Once a fix is deployed and users are protected, we are happy to publicly credit reporters (with your consent) and, where appropriate, publish a post-mortem.

Thank you for helping keep 7.Exchange and its users safe.
