Foundry Fund Me 🏗️
https://img.shields.io/badge/built%2520with-Foundry-FFDB1C.svg
https://img.shields.io/badge/Solidity-%255E0.8.18-363636.svg

A crowd-sourcing Ethereum app that allows you to create and fund projects using smart contracts.

👨‍💻 Created by: Dimitris Kazantzis
LinkedIn: https://www.linkedin.com/in/dimitris-kazantzis-5b575936a/

GitHub: https://github.com/dimk472

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
git --version
Foundry
bash
forge --version
Expected output:

text
forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)
⚡ Quickstart
bash
git clone https://github.com/dimk472/Foundry-Fund-Me.git
cd Foundry-Fund-Me
forge build
Optional: Gitpod
If you don't want to run locally, you can use Gitpod.

💻 Usage
Deploy
bash
forge script script/DeployFundMe.s.sol
🧪 Testing
The project supports:

Unit Tests

Integration Tests

Forked Tests

Staging Tests

bash
# Run all tests
forge test

# Run specific test
forge test --match-test testFunctionName

# Run forked tests
forge test --fork-url $SEPOLIA_RPC_URL

# Test coverage
forge coverage
🌐 Deployment
Environment Setup
Create a .env file:

bash
PRIVATE_KEY=<Your private key>
SEPOLIA_RPC_URL=<URL from Alchemy or Infura>
ETHERSCAN_API_KEY=<Optional>
⚠️ Warning: Use testnet private keys only, never use real funds!

Get Testnet ETH
🔗 Chainlink Faucet

Deploy to Sepolia
bash
forge script script/DeployFundMe.s.sol \
--rpc-url $SEPOLIA_RPC_URL \
--private-key $PRIVATE_KEY \
--broadcast \
--verify \
--etherscan-api-key $ETHERSCAN_API_KEY
📜 Scripts
Fund (Send Money)
bash
cast send <CONTRACT_ADDRESS> "fund()" --value 0.1ether --private-key <PRIVATE_KEY>
Withdraw
bash
cast send <CONTRACT_ADDRESS> "withdraw()" --private-key <PRIVATE_KEY>
Estimate Gas
bash
forge snapshot
✨ Formatting
bash
forge fmt
🔗 Connect with Me
LinkedIn: https://www.linkedin.com/in/dimitris-kazantzis-5b575936a/

GitHub: https://github.com/dimk472

Feel free to connect with me for any questions or collaborations! 🚀

⭐ Support
If you like this project, please give it a star on GitHub!
