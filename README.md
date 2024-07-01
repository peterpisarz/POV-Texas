# POV You Moved to Texas

This is my first independent NFT project I created using my own photography. At the end of 2020 I moved to Texas and these photos capture the essence of my journey. I decided to turn them into an NFT "drop" for the experience of creating this type of project.

Originally I deployed this on the Rinkeby testnet. Since that has been depricated, I recently redeployed on mainnet Sepolia.

Network: sepolia (id: 11155111)
  Migrations: 0xD3F98dc44164e30FF5eb94BE4ad3bf2f51388BbC
  POVTexas: 0x6CA79A7e3d60582E36AE6C04bFd0fe1a26FE0399

## Technology Stack & Tools

- Solidity (Writing Smart Contract)
- Javascript (React & Testing)
- [Web3](https://web3js.readthedocs.io/en/v1.5.2/) (Blockchain Interaction)
- [Truffle](https://www.trufflesuite.com/docs/truffle/overview) (Development Framework)
- [Ganache](https://www.trufflesuite.com/ganache) (For Local Blockchain)
- [Infura.io](https://infura.io/) (For copying the Ethereum mainnet)
- [MetaMask](https://metamask.io/) (Ethereum Wallet)
- [Git](https://git-scm.com/)/[GitHub](https://github.com) (Commit our code)
- [Fleek](https://fleek.co/) (Website Deployment)

## Requirements For Initial Setup
- Install [NodeJS](https://nodejs.org/en/), Recommended version is 14.16.0
- Install [Truffle](https://www.trufflesuite.com/docs/truffle/overview), In your terminal, you can check to see if you have truffle by running `truffle --version`. To install truffle run `npm i -g truffle`.
- Install [Ganache](https://www.trufflesuite.com/ganache).
- Install [MetaMask](https://metamask.io/) in your browser.

## Setting Up
### 1. Clone/Download the Repository

### 2. Install Dependencies:
`$ npm install `

### 3. Setup .env File
Create a .env file or rename the .env.example file, and update the values. The API & IPFS keys are technically optional for local testing, if you plan to deploy to the testnet or mainnet, you'll need to update those values.

### 4. Start Ganache

### 5. Migrate Smart Contracts
`$ truffle migrate --reset`

### 6. Run Frontend Application
In a separate CMD prompt/terminal run:
`$ npm start`

### 7. (Optional) Test Smart Contracts
`$ truffle test`

### 1. Setup your .env file
Create a .env file in the root directory of your project, and fill in the following:
- DEPLOYER_PRIVATE_KEY="YOUR_PRIVATE_KEY"
- INFURA_API_KEY="PROJECT_ID"
- ETHERSCAN_API_KEY="API_TOKEN"

- PROJECT_NAME="YOUR_PROJECT_NAME"
- PROJECT_SYMBOL="YOUR_PROJECT_SYMBOL"
- MINT_COST=0
- MAX_SUPPLY=16

- IPFS_IMAGE_METADATA_CID="IPFS_CID"
- IPFS_HIDDEN_IMAGE_METADATA_CID="IPFS_CID"
- NFT_MINT_DATE="Oct 27, 2024 20:00:00"

### 2. Run your migrations
- For Rinkeby testnet: `truffle migrate --reset --network rinkeby`
- For Sepolia testnet: `truffle migrate --reset --network sepolia`
- For Polygon Mainnet: `truffle migrate --reset --network matic`

### 3. Verify your contracts
- For Rinkeby testnet: `truffle run verify POVTexas --network rinkeby`
- For Sepolia testnet: `truffle run verify POVTexas --network sepolia`
- For Polygon Mainnet: `truffle run verify POVTexas --network matic`