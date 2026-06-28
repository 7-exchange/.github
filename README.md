# `.github`

Organization-wide community health files and defaults for **7.Exchange**.

GitHub automatically applies the files in this repository to **every repo in the org that doesn't define its own** equivalent. The org profile page is rendered from `profile/README.md`.

## What's in here

```
.github/                         <- this repository (named ".github")
├── profile/
│   └── README.md                # rendered on github.com/7ExchangeDefi
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.yml
│   │   ├── feature_request.yml
│   │   ├── integration_support.yml
│   │   └── config.yml           # disables blank issues; routes security/support
│   └── PULL_REQUEST_TEMPLATE.md
├── SECURITY.md                  # vulnerability disclosure policy
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SUPPORT.md
├── CODEOWNERS                   # default owners for repos without their own
└── FUNDING.yml                  # optional sponsor button (disabled by default)
```

## Before you publish — replace these placeholders

- [ ] `security@7.exchange` in **SECURITY.md** → your real, monitored security address
- [ ] `conduct@7.exchange` in **CODE_OF_CONDUCT.md** → your real moderation contact
- [ ] Team handles in **CODEOWNERS** (`@7ExchangeDefi/core`, `/contracts`, `/security`, …) → create these teams under **Org Settings → Teams**

## Recommended org settings to pair with these files

These files document policy; the settings below enforce it.

1. **Require 2FA org-wide** (Settings → Authentication security). Prefer hardware/passkeys for maintainers.
2. **Enable Private Vulnerability Reporting** per repo (Settings → Security) so the SECURITY.md flow has a button.
3. **Secret scanning + push protection** on every repo.
4. **Branch protection / rulesets** on `main`: require PR review (2 for contracts), required status checks, no force-push, and "Require review from Code Owners".
5. **Require signed commits** on contract and other sensitive repos.
6. **Harden GitHub Actions**: allow selected actions only, pin third-party actions to a commit SHA, default `GITHUB_TOKEN` to read-only.
7. **Dependabot** alerts + security updates enabled across repos.

> Per-repo `CONTRIBUTING.md`, `CODEOWNERS`, and issue templates override these org defaults — add stack-specific ones (especially in `contracts`) as the org grows.
