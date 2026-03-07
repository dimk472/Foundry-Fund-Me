# 🏗️ Foundry Fund Me

![Built with Foundry](https://img.shields.io/badge/built%20with-Foundry-FFDB1C.svg)
![Solidity](https://img.shields.io/badge/Solidity-%5E0.8.18-363636.svg)

A crowd-sourcing Ethereum app that allows you to **create and fund projects** using smart contracts.

👨‍💻 **Created by:** [Dimitris Kazantzis](https://www.linkedin.com/in/dimitris-kazantzis-5b575936a/)  
💻 GitHub: [dimk472](https://github.com/dimk472)

---

## 📋 Table of Contents
1. [Requirements](#-requirements)
2. [Quickstart](#-quickstart)
3. [Usage](#-usage)
4. [Testing](#-testing)
5. [Deployment](#-deployment)
6. [Scripts](#-scripts)
7. [Formatting](#-formatting)
8. [Connect](#-connect)

---

## 🔧 Requirements

- **Git**  
  Verify installation:
  ```bash
  git --version

Foundry
Verify installation:

forge --version

Expected output:

forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)
⚡ Quickstart

Clone the repository and build:

git clone https://github.com/dimk472/Foundry-Fund-Me.git
cd Foundry-Fund-Me
forge build

Optional: Gitpod
If you don't want to run locally, you can use Gitpod
 for an online dev environment.

💻 Usage
Deploy
forge script script/DeployFundMe.s.sol
🧪 Testing

Supported test types:

Unit Tests

Integration Tests

Forked Tests

Staging Tests

Run all tests:

forge test

Run a specific test:

forge test --match-test testFunctionName

Run forked tests:

forge test --fork-url $SEPOLIA_RPC_URL

Test coverage:

forge coverage
🌐 Deployment
Environment Setup

Create a .env file:

PRIVATE_KEY=<Your private key>
SEPOLIA_RPC_URL=<URL from Alchemy or Infura>
ETHERSCAN_API_KEY=<Optional>

⚠️ Warning: Use testnet private keys only, never real funds!

Get Testnet ETH

Use the Chainlink Faucet
 to get test ETH for Sepolia.

Deploy to Sepolia
forge script script/DeployFundMe.s.sol \
--rpc-url $SEPOLIA_RPC_URL \
--private-key $PRIVATE_KEY \
--broadcast \
--verify \
--etherscan-api-key $ETHERSCAN_API_KEY
📜 Scripts
Fund (Send Money)
cast send <CONTRACT_ADDRESS> "fund()" --value 0.1ether --private-key <PRIVATE_KEY>
Withdraw
cast send <CONTRACT_ADDRESS> "withdraw()" --private-key <PRIVATE_KEY>
Estimate Gas
forge snapshot

This will generate a .gas-snapshot file with gas usage info.

✨ Formatting
forge fmt
🔗 Connect with Me

LinkedIn: Dimitris Kazantzis

GitHub: dimk472

Feel free to connect for questions or collaborations! 🚀

⭐ Support

If you like this project, please give it a star on GitHub! 🌟
