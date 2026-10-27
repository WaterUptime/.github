# Contributing to WaterUptime

Thank you for considering a contribution. WaterUptime is an early-stage open-source experiment: the problem hypothesis and architecture may change after stakeholder research.

This guide applies to every repository in the organisation unless a repository has its own `CONTRIBUTING.md`, which then takes precedence.

## Before you start

- Read the repository's `README.md` and the relevant docs.
- Pick an open issue, or open one describing the problem before starting larger work.
- Comment on the issue to say you're working on it, so effort isn't duplicated.
- For anything beyond a small fix, agree the approach in the issue first.

## Making a change

1. Fork the repository and create a branch from `main` (e.g. `fix/assign-validation`).
2. Keep the change focused on one issue. Small, complete PRs are reviewed fastest.
3. Add or update tests:
   - **Contract:** positive *and* negative tests for every state transition or authorisation rule you touch.
   - **Frontend:** keep `src/domain/workflow.ts` and its tests in sync with the contract.
4. Update docs when interfaces, error codes, events or assumptions change.
5. Run the repository's checks locally before pushing:
   - Contract: `cargo fmt --all -- --check`, `cargo clippy --all-targets -- -D warnings`, `cargo test`
   - Frontend: `npm run typecheck`, `npm test`, `npm run build`

## Pull requests

Each PR should:

- link the issue it resolves (`Closes #123`);
- explain what changed and why;
- list the commands you ran and whether they passed;
- contain no personal data, secrets, private keys or unapproved third-party datasets.

CI must pass before review. Maintainers may ask for changes; that's a normal part of review.

## Data and privacy rules

- Never put names, phone numbers, photos, exact household or GPS locations, or raw reports on-chain or in test fixtures.
- Use synthetic data and Stellar **testnet** only. Never use real funds or mainnet.
- Don't claim or imply partnerships or endorsements (government, NGO, UNDP, Stellar Development Foundation or others).

## Security-sensitive changes

Changes to authorisation, role separation, state transitions, signing, evidence handling or personal data carry the `security-sensitive` label. They need careful review and are never merged just because the happy path works. To report a vulnerability, follow [SECURITY.md](SECURITY.md); don't open a public issue.

## Scope

Please don't add AI, tokens, payments or new integrations without an agreed issue describing the problem, the user need and the design.

## Funded contribution programmes

Some issues may be listed in programmes such as Drips Wave. Rewards follow that programme's official rules only; maintainers never promise payment outside them.

## Conduct

Everyone taking part is expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md).
