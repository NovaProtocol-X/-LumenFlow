# LumenFlow

> Automated on-chain recurring billing engine for the Stellar Network

---

## Overview

LumenFlow is an **automated on-chain billing engine** for the Stellar Network. It enables decentralized, recurring payments by allowing users to authorize time-bound asset transfers through a non-custodial **Vault-Allowance** model — built with Soroban smart contracts in Rust.

LumenFlow eliminates the need for centralized payment processors entirely, while maintaining Stellar's ultra-low transaction costs. Subscriptions, payroll, and any recurring payment flow can now live fully on-chain.

---

## Features

- **Recurring Payments** — Fully automated, on-chain billing at configurable time intervals
- **Vault-Allowance Model** — Non-custodial authorization; users stay in control of their assets
- **Time-Bound Transfers** — Payments are scoped to specific windows, preventing unauthorized pulls
- **No Centralized Processor** — Protocol-native billing with zero third-party dependencies
- **Ultra-Low Costs** — Inherits Stellar's near-zero transaction fee structure
- **Soroban-Powered** — Secure, auditable smart contract logic written in Rust

---

## Getting Started

### Prerequisites

- [Stellar CLI](https://developers.stellar.org/docs/tools/developer-tools)
- [Rust](https://www.rust-lang.org/tools/install) with `wasm32-unknown-unknown` target
- [Node.js](https://nodejs.org/) (for the web frontend)

### Installation

**1. Build the smart contract:**
```bash
stellar contract build
```

**2. Set up the frontend:**
```bash
cd web && npm install
```

**3. Deploy to Testnet:**
```bash
stellar contract deploy \
  --wasm target/wasm32-unknown-unknown/release/lumenflow.wasm \
  --source admin \
  --network testnet
```

---

## Project Structure

```
lumenflow/
├── src/                # Soroban smart contract source (Rust)
├── target/             # Compiled WASM artifacts (generated)
├── web/                # Frontend interface
├── tests/              # Contract and integration tests
└── CONTRIBUTING.md     # Contribution guidelines
```

---

## How It Works

1. A user **authorizes** a Vault-Allowance, granting the protocol permission to pull a specified asset amount within a defined time window
2. LumenFlow's contract **executes transfers** automatically at each billing interval
3. The user's funds remain **non-custodial** at all times — only the authorized allowance is accessible
4. Allowances can be **revoked** by the user at any point, stopping future billing immediately

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests. Contributions are managed through **Wave Program** sprint cycles.

---

## License

This project is licensed under the [MIT License](./LICENSE).
