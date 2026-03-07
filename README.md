Foundry Fund Me 🏗️


https://img.shields.io/badge/built%2520with-Foundry-FFDB1C.svg

https://img.shields.io/badge/Solidity-%255E0.8.18-363636.svg

https://img.shields.io/badge/license-MIT-blue.svg

A crowd-sourcing Ethereum app that allows you to create and fund projects using smart contracts.

👨‍💻 Created by: Dimitris Kazantzis
https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white
https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white

📋 Table of Contents
Requirements

Quickstart

Usage

Testing

Deployment

Scripts

Formatting

Connect

🔧 Requirements
Git
bash
# Verify installation
git --version
Foundry
bash
# Verify installation
forge --version
You should see something like:

text
forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)
⚡ Quickstart
bash
git clone https://github.com/dimk472/Foundry-Fund-Me.git
cd Foundry-Fund-Me
forge build
Optional: Gitpod
If you cannot or do not want to run locally, you can use Gitpod to work online.

💻 Usage
Deploy
bash
forge script script/DeployFundMe.s.sol
🧪 Testing
The project supports multiple test tiers:

Unit

Integration

Forked

Staging

This repository covers Unit and Forked tests:

bash
# Run all tests
forge test

# Run specific test functions
forge test --match-test testFunctionName

# Run with forked testnet
forge test --fork-url $SEPOLIA_RPC_URL

# Test coverage
forge coverage
🌐 Deployment to Testnet or Mainnet
Environment Setup
Create a .env file and add:

bash
PRIVATE_KEY=<Your MetaMask private key>
SEPOLIA_RPC_URL=<URL of Sepolia node, e.g., from Alchemy>
ETHERSCAN_API_KEY=<Optional, for contract verification on Etherscan>
⚠️ Warning: Use testnet private keys only, do not use real funds.

Get Testnet ETH
Visit Chainlink Faucet to receive test ETH for your MetaMask wallet.

Deploy to Sepolia
bash
forge script script/DeployFundMe.s.sol \
--rpc-url $SEPOLIA_RPC_URL \
--private-key $PRIVATE_KEY \
--broadcast \
--verify \
--etherscan-api-key $ETHERSCAN_API_KEY
📜 Scripts
Fund Contract
bash
cast send <FUNDME_CONTRACT_ADDRESS> "fund()" --value 0.1ether --private-key <PRIVATE_KEY>
Or using forge script:

bash
forge script script/Interactions.s.sol --rpc-url sepolia --private-key $PRIVATE_KEY --broadcast
Withdraw
bash
cast send <FUNDME_CONTRACT_ADDRESS> "withdraw()" --private-key <PRIVATE_KEY>
Estimate Gas
bash
forge snapshot
This will create a .gas-snapshot file with results.

✨ Formatting
bash
forge fmt
🤝 Connect
If you enjoyed this project, feel free to connect with me!

https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white

https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white

⭐ Support
If you like this project, please give it a star on GitHub!
