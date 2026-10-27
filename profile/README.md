# WaterUptime

**Open-source maintenance and verification infrastructure for community water systems.**

When a community water point breaks, the fault report, the repair, the evidence and the sign-off often live in different places. WaterUptime is exploring whether one shared, verifiable workflow can help water committees, technicians, independent verifiers and programme partners agree on what was repaired, who checked it, and when service was restored.

> **Status: early prototype.** Synthetic data and Stellar testnet only. The problem hypothesis still needs validation with water-service stakeholders. No government, NGO or UNDP partnership is claimed.

## How it works

```text
Reported ─▶ Assigned ─▶ Repair submitted ─▶ Verified ─▶ Closed
                ▲               │
                └── Rework ◀────┘        (mistaken reports can be cancelled)
```

1. An authorised **reporter** logs a fault for a registered water point.
2. The **coordinator** assigns a technician and a *different* verifier.
3. The **technician** submits a fingerprint of the repair evidence.
4. The **verifier** approves the repair or returns it for rework.
5. The **coordinator** closes the job. Every step stays in the audit history.

A [Soroban](https://developers.stellar.org/docs/build/smart-contracts/overview) smart contract on Stellar enforces who may do what, and in which order. Names, photos, coordinates and documents stay off-chain; only opaque IDs and salted fingerprints are recorded. The record shows what an authorised person submitted; it does not by itself prove a repair physically happened.

## Repositories

| Repository | What's inside |
|---|---|
| [WaterUptime-SmartContract](https://github.com/WaterUptime/WaterUptime-SmartContract) | Soroban contract (Rust), tests, testnet deployment and demo script |
| [WaterUptime-Frontend](https://github.com/WaterUptime/WaterUptime-Frontend) | React + TypeScript web app with an interactive demo and a read-only testnet view |
| [WaterUptime](https://github.com/WaterUptime/WaterUptime) | Product spec, architecture and project docs |

## Not in scope for v0

Real funds or payments, mainnet deployment, AI or token features, public storage of personal data, or replacing existing public-sector WASH systems.

## Contributing

Scoped issues with acceptance criteria are open in each repository. Look for **`good first issue`** to get started. Changes labelled **`security-sensitive`** (authorisation, signing, personal data) get extra review.

- Read the [contributing guide](https://github.com/WaterUptime/.github/blob/main/CONTRIBUTING.md) and our [Code of Conduct](https://github.com/WaterUptime/.github/blob/main/CODE_OF_CONDUCT.md).
- Report vulnerabilities privately; see the [security policy](https://github.com/WaterUptime/.github/blob/main/SECURITY.md).

Licensed under MIT.
