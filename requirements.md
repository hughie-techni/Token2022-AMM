# Token-2022 AMM Integration Guide

## 🧠 Context
Token-2022 is a significant upgrade for the Solana ecosystem, introducing advanced features such as whitelisting, KYC gating, conditional transfers, and programmable behaviors through Transfer Hooks. These capabilities make Token-2022 an ideal foundation for tokenizing real-world assets (RWA) and addressing enterprise use cases. However, major automated market makers (AMMs) like Raydium, Orca, and Meteora do not currently support trading Token-2022 tokens with active Transfer Hooks, which limits its adoption as a DeFi primitive.

## 🎯 Objective
Develop a working solution to enable trading of Token-2022 tokens with Transfer Hooks on a Solana AMM. The project can achieve this by either:

1. **Building a new AMM** that natively supports Token-2022 with Transfer Hooks.
2. **Patching or extending an existing AMM** (e.g., Raydium, Orca, Meteora) to support a whitelisted set of safe Transfer Hook programs.

Support for arbitrary hooks is not required; a whitelisted list of safe hook programs is sufficient.

## ✅ Submission Requirements
The project must include:

- **User Interface (UI)** to:
  - Create a Token-2022 with a Transfer Hook.
  - Create a liquidity pool (e.g., SOL-token pair).
  - Enable trading of the Token-2022.

- **Deliverables**:
  - A video demo showcasing the complete workflow.
  - A live demo deployed on Solana devnet or testnet.
  - Source code for the solution.

### Bonus Points
- Support for multiple Transfer Hooks.
- A permissionless but safe hook approval system.
- Direct integration with existing AMM protocols (Raydium, Orca, Meteora).

## 💡 Inspiration
Potential approaches to consider:
- Implement pre-transfer simulation to validate and approve trades.
- Maintain a whitelist of known-safe Transfer Hook programs.
- Use proxy token wrappers to temporarily bypass restrictions, with hook confirmation.
- Develop a middleware relayer to validate Transfer Hooks.

## 🛠️ Tech Stack
- **Solana Token-2022**: For token creation and Transfer Hook implementation.
- **Anchor and Solana Program Library**: For smart contract development.
- **Raydium / Orca / Metora**: Leverage open-source AMM protocols for integration or extension.
- **TypeScript**: For building the UI and SDK.

## 👩‍⚖️ Judging Criteria
The solution will be evaluated based on:
- **Functionality**: Does the system enable real trading of Token-2022 with Transfer Hooks?
- **Security**: Does it prevent bypassing the Transfer Hook logic?
- **Scalability**: Can it support additional hooks or tokens?
- **Developer UX**: Is the UI and toolchain intuitive and smooth?
- **Documentation & Clarity**: Is the code well-documented, easy to understand, and reusable?
