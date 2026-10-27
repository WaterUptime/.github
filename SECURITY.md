# Security Policy

## Project status

WaterUptime is an experimental prototype. It is **not** approved for production water-service operations, personal data, or real funds. Only Stellar testnet deployments exist.

## Reporting a vulnerability

**Please do not open a public issue for security problems.**

Report privately using GitHub's private vulnerability reporting:

1. Open the affected repository (for example [WaterUptime-SmartContract](https://github.com/WaterUptime/WaterUptime-SmartContract)).
2. Go to the **Security** tab and choose **Report a vulnerability**.
3. Include the affected component, steps to reproduce, the impact, and any suggested fix.

Only maintainers can see these reports. Please don't include real personal data in a report.

We aim to acknowledge reports within **5 working days** and will keep you updated as we investigate. With your permission, we're happy to credit you once a fix is published.

## Scope

In scope:

- The Soroban contract: authorisation bypass, invalid state transitions, role-separation failures, storage or event issues.
- The web app: anything that could sign on the wrong network, leak data, or mislead users about what was recorded on-chain.
- Leaked secrets or keys in any repository.

Out of scope: issues that only affect the synthetic demo data in your own browser, and testnet funding or availability problems.

## Security assumptions

- All on-chain state and events are public and may be permanent.
- A hash is not encryption; predictable data can be guessed from its hash, which is why fingerprints are salted.
- An on-chain record shows what an authorised account submitted. It does not independently prove a physical repair or water quality.
- Contract bugs, compromised keys, collusion, false evidence, connectivity problems and weak governance remain possible.

## Before any real-world pilot

An independent contract and security review, a documented role and key-management model, a data-protection review, clear governance and incident handling, human verification procedures, and an accountable implementation partner are all required. No mainnet deployment or real-money workflow is authorised.
