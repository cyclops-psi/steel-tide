# Steel Tide (Built for Base)

Steel Tide is a lightweight, read-only onchain tool designed to work with Base Mainnet and Base Sepolia. It allows users to validate Base network identity, retrieve blockchain data, inspect balances, and interact with deployed contracts, using Coinbase Wallet SDK and direct verification through Basescan.

## Project Structure

- **app/steel-tide.ts**  
  The primary script that connects to Coinbase Wallet and performs read-only queries using Base RPC.

- **config/base.networks.json**  
  Contains static configuration data for Base networks, including RPC endpoints, explorers, and chain IDs for Base Mainnet and Base Sepolia.

- **scripts/sample-addresses.json**  
  Example addresses for conducting repeatable checks and inspections.

- **contracts/**  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - `imports.sol` — a contract that uses import statements to include other Solidity contracts, libraries, or interfaces
  - `ERC721.sol` — represents non-fungible tokens (NFTs), where each token is unique
  - `control.sol` — deals with access control and permissions for controlling who can perform certain actions in a smart contract

- **package.json**  
  Contains the project’s dependencies, referencing Base and Coinbase SDKs and libraries.

- **README.md**  
  This document, providing all the necessary information to use and set up the repository.

## Features

- **Coinbase Wallet SDK integration** for secure wallet connection via EIP-1193  
- **Validation of Base chain IDs** for Mainnet (8453) and Sepolia (84532)  
- **Network snapshot functionality** to fetch block details, gas price, and usage statistics  
- **Address inspection** to check balances, transaction counts, and bytecode presence  
- **ERC-20 token inspection** to retrieve token metadata, total supply, and holder balances  
- **Basescan verification links** for easy and independent cross-checking  

## Supported Networks

- **Base Sepolia**  
  ChainId (decimal): 84532  
  Explorer: [sepolia.basescan.org](https://sepolia.basescan.org)

- **Base Mainnet**  
  ChainId (decimal): 8453  
  Explorer: [basescan.org](https://basescan.org)

## Tooling and Ecosystem

This repository utilizes the following tools and SDKs from Coinbase and Base:
- **Coinbase Wallet SDK** for wallet connectivity  
- **OnchainKit** for seamless interaction with Base’s native primitives  
- **Viem** for efficient, typed communication with Base’s RPC  
- Direct dependencies to various Base and Coinbase GitHub repositories  

## License

MIT License

Copyright (c) 2025 YOUR_NAME

## Author

GitHub: [https://github.com/cyclops-psi](https://github.com/cyclops-psi) 

Email: cyclops.psi-0b@icloud.com

X: [https://x.com/manathis63](https://x.com/manathis63)  

## Testnet Deployment (Base Sepolia)

In preparation for production deployment, the following contracts have been deployed to Base Sepolia to confirm correct behavior and tooling compatibility:

**Network**: Base Sepolia  
**ChainId (decimal)**: 84532  
**Explorer**: [sepolia.basescan.org](https://sepolia.basescan.org)

**Contract imports.sol address**:  
0x29F184704E63de8dcB1C194dE8d5A2d465B276c2 

**Deployment and verification**:
- [Deployment link](https://sepolia.basescan.org/address/0x29F184704E63de8dcB1C194dE8d5A2d465B276c2)
- [Code verification](https://sepolia.basescan.org/0x29F184704E63de8dcB1C194dE8d5A2d465B276c2/0#code)

**Contract ERC721.sol address**:  
0x17D5F460750db734C1A7E0BFC38370Bedcb6e807 

**Deployment and verification**:
- [Deployment link](https://sepolia.basescan.org/address/0x17D5F460750db734C1A7E0BFC38370Bedcb6e807)
- [Code verification](https://sepolia.basescan.org/0x17D5F460750db734C1A7E0BFC38370Bedcb6e807/0#code)

**Contract control.sol address**:  
0x4714601d1cD6D371Ee005FAc5f502BA3b731f6a9 

**Deployment and verification**:
- [Deployment link](https://sepolia.basescan.org/address/0x4714601d1cD6D371Ee005FAc5f502BA3b731f6a9)
- [Code verification](https://sepolia.basescan.org/0x4714601d1cD6D371Ee005FAc5f502BA3b731f6a9/0#code)

These deployments serve to validate the functionality and ensure compatibility with Base tooling before full deployment to Mainnet.

