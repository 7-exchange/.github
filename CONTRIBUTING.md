# Contributing to 7.Exchange

Thanks for your interest in contributing! This guide applies across the 7.Exchange organization. Individual repositories may add their own `CONTRIBUTING.md` or `README` with stack-specific setup — when they do, that repo's instructions take precedence over the general guidance here.

By participating, you agree to abide by our [Code of Conduct](./CODE_OF_CONDUCT.md).

> [!IMPORTANT]
> **Never report security vulnerabilities through public issues or pull requests.** Follow our [Security Policy](./SECURITY.md) instead.

---

## Ways to contribute

- **Report bugs** — open an issue using the bug report template
- **Request features** — open an issue using the feature request template
- **Improve docs** — corrections and clarifications are always welcome
- **Submit code** — fixes, tests, and integrations via pull request
- **Build integrations** — using the [API](https://docs.7.exchange/developers/api-reference), [SDK](https://docs.7.exchange/developers), or [widget](https://docs.7.exchange/developers/widget)

## Before you start

For anything beyond a small fix, **open an issue first** to discuss the approach. This avoids duplicated effort and makes sure the change fits the roadmap — especially for contract or routing changes, where design and security review matter most.

## Development workflow

1. **Fork** the repository (external contributors) or create a branch (members).
2. **Branch** from `main` using a descriptive name: `feat/limit-order-ui`, `fix/quote-rounding`, `docs/sdk-readme`.
3. **Commit** using [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`, etc. This keeps history readable and drives changelogs for the SDK and widget.
4. **Sign your commits.** Contract and other security-sensitive repos require signed commits (`git commit -S`). See [GitHub's commit signing guide](https://docs.github.com/authentication/managing-commit-signature-verification).
5. **Test.** Add or update tests for your change and make sure the full suite and linters pass locally.
6. **Open a pull request** against `main`, fill out the PR template completely, and link the related issue.

## Pull request expectations

- Keep PRs focused — one logical change per PR is far easier to review.
- All required CI checks (build, lint, tests, and security scans) must pass.
- PRs require review before merge: **at least one** maintainer approval for most repos, and **two** approvals for smart-contract changes.
- Reviews are dismissed when you push new commits; re-request review after addressing feedback.
- Maintainers may request changes for security, correctness, or consistency reasons.

### Documentation contributions

Docs live in [7-exchange/docs](https://github.com/7-exchange/docs) and publish to
[docs.7.exchange](https://docs.7.exchange).

- Typo fixes, broken links, and clarifications don't need an issue first — open the
  PR directly.
- New pages or restructuring: open an issue first so placement and sidebar
  structure can be agreed before you write.
- Docs PRs require one maintainer approval.
- When you change a public interface — API, SDK, or widget — update the docs in the
  same PR as the behaviour change, not a follow-up.
- Stack-specific setup, MDX components, and writing conventions are in the repo's
  `AUTHORING.md`.
  
### Smart contract contributions

Contract changes carry the highest risk and the highest bar:

- Include comprehensive unit tests and, where relevant, fuzz/invariant tests.
- Run static analysis (e.g. Slither) and address findings or justify exceptions.
- Document any change to facets, storage layout, or upgrade authorization explicitly in the PR — storage layout mistakes in a Diamond can be catastrophic.
- Do not include deployment keys, mnemonics, or `.env` files. Push protection and secret scanning are enabled; treat any leaked secret as compromised and rotate it.

## Style & quality

- Follow the existing conventions of the repo you're working in (formatter and linter configs are committed).
- Write clear comments for non-obvious logic, especially around routing, slippage, and cross-chain message handling.
- Update documentation when behavior or public interfaces change.

## Licensing

Unless a repository states otherwise, contributions are accepted under that repository's `LICENSE`. By submitting a contribution, you confirm you have the right to do so and agree to license it under those terms.

## Questions?

Ask in [Discord](https://discord.com/invite/8aujTp5znT) or open a discussion/issue. For anything sensitive, see [SUPPORT.md](./SUPPORT.md) and [SECURITY.md](./SECURITY.md).
