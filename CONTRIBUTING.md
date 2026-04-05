# Contributing to TrustAgent

Contributions are welcome. The project is early-stage and there is meaningful work to do across all layers.

## Where to contribute

The most impactful areas right now:

- **Naryo integration** — event-driven pipeline replacing the manual /feedback trigger. Naryo listens to giveFeedback() across chains and broadcasts to the backend in real time.
- **ERC-8004 multi-chain** — deploy the existing Solidity contracts on additional EVM chains (Hedera, Base, Arbitrum) and configure the TEE to aggregate them.
- **SDK** — wrap register, feedback, resolve, and verify into a standalone npm package with clean TypeScript types and minimal dependencies.
- **Score model** — the current model (reliability + seniority) is intentionally simple. Better weighting, additional dimensions, and a formal spec are open questions.
- **Production TEE attestation** — replace the local mode flag with full GCP enclave attestation and a verifiable code hash.

## How to contribute

1. Fork the repo and create a branch from `main`
2. Make your changes with clear, minimal commits
3. Open a pull request describing what you changed and why
4. For significant changes, open an issue first to align on direction

## Standards

- TypeScript throughout, strict mode
- No new dependencies without a clear justification
- Backend changes must not break the ENS update flow or the TEE signature format
- Any change to the score model must preserve the ecrecover verification path
