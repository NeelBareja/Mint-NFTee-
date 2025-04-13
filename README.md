# 🎓 NFTee – Built with LearnWeb3.io | Fun, Easy & Detailed Web3 Learning

This project is part of a **free course from [LearnWeb3.io](https://learnweb3.io)** — a platform that makes learning Web3 **fun, easy, and incredibly detailed**. Whether you're just starting out or sharpening your blockchain dev skills, this project will walk you through deploying an NFT on Sepolia using Foundry step-by-step.

---



# 🎨 NFTee – Mint Your First NFT on Sepolia with Foundry
This project demonstrates how to deploy a simple ERC-721 (NFT) contract using Foundry. It's designed for Ethereum's Sepolia testnet and includes minting functionality out of the box.'



## 🚀 Getting Started

### 1. 📦 Install Foundry
If you haven't already installed Foundry:

`curl -L https://foundry.paradigm.xyz | bash
foundryup
`

### 2. 🛠 Initialize the Project
`forge init foundry-app
cd foundry-app
`

### 3. 📁 Locate the Contract
The main smart contract is located at:
`src/NFTee.sol
`
This contract handles the NFT minting logic.

### 4. 🔐 Setup Environment Variables
Create a .env file in the root of the project with the following content:
`PRIVATE_KEY`=your_private_key_here
`RPC_URL=https:`//sepolia.infura.io/v3/your_project_id

✅ Make sure to rename the file from example.env to .env and replace the placeholders with your actual private key and Sepolia RPC URL (e.g., from Infura or Alchemy).

⚠️ Ensure the wallet corresponding to your private key has Sepolia ETH to cover transaction fees.

### 5. 🧱 Compile the Contract
Run the following to compile the contract:
`forge build
`

### 6. 🚢 Deploy the Contract
`forge script script/Deploy.s.sol:DeployNFTee --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast
`

After deployment, Foundry will output the deployed contract address.

### 7. 🔍 Verify Deployment on Sepolia
- Go to (https://sepolia.etherscan.io/).

- Search for your deployed contract address.

- Check the latest transaction — it should show an NFT being minted and transferred to your wallet address.

### 📄 Project Structure
```
foundry-app/
├── src/
│   └── NFTee.sol          # Main NFT contract
├── script/
│   └── Deploy.s.sol       # Deployment script
├── test/                  # Optional test files
├── .env                   # Environment variables (not committed)
```

## 🧪 Requirements
- Foundry

- Node Provider (e.g., Infura, Alchemy)

- Sepolia ETH (can be claimed from faucets)
