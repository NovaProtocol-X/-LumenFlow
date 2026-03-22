LumenFlow

Automated On-Chain Billing Engine for Stellar

Description
LumenFlow is an automated on-chain billing engine built for the Stellar network. It enables decentralized recurring payments by allowing users to authorize time-bound asset transfers using a non-custodial Vault-Allowance model. Built with Soroban (Rust), it removes the need for centralized payment processors while keeping Stellar’s low transaction costs.

Key Features
Recurring decentralized payments
Non-custodial vault allowance system
Soroban smart contracts (Rust)
Low-cost automated billing

Installation

# Install Stellar CLI (required)

# Build contracts
stellar contract build

# Setup frontend
cd web
npm install

# Deploy contract
stellar contract deploy \
--wasm target/wasm32-unknown-unknown/release/lumenflow.wasm \
--source admin \
--network testnet

Contributing
We use Wave Program sprint cycles. See CONTRIBUTING.md for scoped issues and contribution guidelines.

License:
This project is licensed under the MIT License - see the LICENSE file for details.
