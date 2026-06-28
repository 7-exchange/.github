# Security Policy

7.Exchange is a non-custodial, cross-chain execution layer that moves real value across multiple networks. We take security extremely seriously and deeply appreciate the work of security researchers who help keep users safe.

This policy explains **how to report a vulnerability**, **what is in scope**, and **the protections we extend to good-faith research**.

---

## Reporting a vulnerability

**Do not open a public GitHub issue, pull request, or Discord/Telegram message for security vulnerabilities.** Public disclosure before a fix is deployed puts user funds at risk.

Report privately through **one** of the following:

- **Email:** `security@7.exchange` *(replace with your verified address before publishing)*
- **GitHub Private Vulnerability Reporting:** use the **"Report a vulnerability"** button under the *Security* tab of the affected repository (enable *Private vulnerability reporting* in each repo's settings first)

> If you are submitting sensitive details, request our PGP key in your first message and we will provide an encrypted channel.

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
| Status updates | at least every **7 days** until resolved |
| Coordinated public disclosure | by mutual agreement, typically after a fix is deployed |

---

## Scope

In scope:

- **Smart contracts** — the Diamond Router (EIP-2535), its facets, and any related on-chain contracts deployed by 7.Exchange. Canonical deployed addresses are published in the `contracts` repository; only those addresses are in scope.
- **Routing & quote engine / API** — `*.7.exchange` API endpoints and the routing/execution backend.
- **Web application** — `https://7.exchange` and its subdomains.
- **TypeScript SDK** and the **embeddable swap widget** published by 7.Exchange.
- **Org infrastructure** — exposed secrets, CI/CD pipeline weaknesses, or supply-chain issues affecting the repositories in this organization.

Examples of issues we especially care about: loss or theft of user funds, unauthorized state changes, broken access control or facet/upgrade authorization in the Diamond, signature/replay flaws, routing manipulation that harms execution, price/slippage bypasses, bridge-message handling flaws, and secret/key exposure.

### Out of scope

- Vulnerabilities in third-party DEXs, bridges, wallets, or liquidity sources we integrate with (report those to the respective projects)
- Findings that require a compromised user device, malicious browser extension, or physical access
- Theoretical issues without a demonstrated security impact, or best-practice suggestions with no exploit path
- Spam, social engineering, phishing, and attacks against our staff or infrastructure providers
- Automated scanner output without validation; missing security headers, SPF/DMARC, or rate-limiting without a concrete impact
- Denial of service through traffic volume, and issues only reproducible on unsupported/outdated software
- Recently disclosed 0-days in dependencies (give us reasonable time to patch)

---

## Severity & rewards

We assess severity using an impact-based model (loss of funds, scope of affected users, exploit complexity), broadly aligned with industry standards for DeFi.

| Severity | Typical example |
|---|---|
| **Critical** | Direct, scalable theft or permanent loss of user funds; unauthorized Diamond upgrade or facet takeover |
| **High** | Theft/loss under specific conditions; significant unauthorized state change |
| **Medium** | Limited fund-at-risk scenarios; meaningful integrity or availability impact |
| **Low** | Minor issues with limited impact; defense-in-depth gaps |

A formal **bug bounty program for the Diamond Router** is on our roadmap. Until it launches with published reward tiers, valid reports are still triaged, fixed, and eligible for discretionary recognition and rewards. When the program goes live (e.g. via a bounty platform), this section will link to the official scope and payout tiers, which will govern reward amounts.

---

## Safe harbor for good-faith research

We will not pursue or support legal action against researchers who, in good faith:

- Make a genuine effort to avoid privacy violations, data destruction, and interruption or degradation of our services
- **Only interact with accounts and funds they own, or with explicit permission** — and use testnets or their own funds rather than other users' assets
- Do **not** exploit a finding beyond the minimum necessary to demonstrate it, and do not withdraw, move, or retain user funds
- Report promptly and give us reasonable time to remediate before any public disclosure
- Do not violate applicable law

If you are unsure whether a specific action is authorized, ask us first at `security@7.exchange`. We will work with you in good faith and consider research conducted consistently with this policy to be authorized.

> This document is a security policy, not a contract or a guarantee of payment, and does not grant permission to act unlawfully or to access third-party systems.

---

## Disclosure

We practice coordinated disclosure. Once a fix is deployed and users are protected, we are happy to publicly credit reporters (with your consent) and, where appropriate, publish a post-mortem.

Thank you for helping keep 7.Exchange and its users safe.
