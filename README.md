Foundry Fund Me

A crowd-sourcing Ethereum app that allows you to create and fund projects using smart contracts.

Created by: Dimitris Kazantzis
LinkedIn: https://www.linkedin.com/in/dimitris-kazantzis-5b575936a/

---

Requirements:

- Git
  Verify installation:
    git --version

- Foundry
  Verify installation:
    forge --version
  You should see something like:
    forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)

---

Quickstart:

git clone https://github.com/dimk472/Foundry-Fund-Me.git
cd Foundry-Fund-Me
forge build

Optional: Gitpod
If you cannot or do not want to run locally, you can use Gitpod (https://gitpod.io) to work online.

---

Usage:

Deploy:

forge script script/DeployFundMe.s.sol

Testing:
The project supports multiple test tiers:
1. Unit
2. Integration
3. Forked
4. Staging

This repository covers Unit and Forked tests:

forge test

To run specific test functions:

forge test --match-test testFunctionName

With forked testnet:

forge test --fork-url $SEPOLIA_RPC_URL

Test Coverage:

forge coverage

---

Deployment to Testnet or Mainnet:

Environment Setup:
Create a .env file and add:

PRIVATE_KEY=<Your MetaMask private key>
SEPOLIA_RPC_URL=<URL of Sepolia node, e.g., from Alchemy>
ETHERSCAN_API_KEY=<Optional, for contract verification on Etherscan>

Warning: Use testnet private keys only, do not use real funds.

Get Testnet ETH:
Visit Chainlink Faucet (https://faucets.chain.link/sepolia) to receive test ETH for your MetaMask wallet.

Deploy to Sepolia:

forge script script/DeployFundMe.s.sol \
--rpc-url $SEPOLIA_RPC_URL \
--private-key $PRIVATE_KEY \
--broadcast \
--verify \
--etherscan-api-key $ETHERSCAN_API_KEY

---

Scripts:

Fund Contract:

cast send <FUNDME_CONTRACT_ADDRESS> "fund()" --value 0.1ether --private-key <PRIVATE_KEY>

or

forge script script/Interactions.s.sol --rpc-url sepolia --private-key $PRIVATE_KEY --broadcast

Withdraw:

cast send <FUNDME_CONTRACT_ADDRESS> "withdraw()" --private-key <PRIVATE_KEY>

Estimate Gas:

forge snapshot

This will create a .gas-snapshot file with results.

---

Formatting:

forge fmt

---

Acknowledgements:

If you enjoyed this project, feel free to connect with me on LinkedIn:
https://www.linkedin.com/in/dimitris-kazantzis-5b575936a/
