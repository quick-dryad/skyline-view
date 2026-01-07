# Skyline View (Built for Base)

Skyline View is a lightweight, read-only utility designed for developers who need to inspect and validate the Base Sepolia network. The tool is easy to use, allowing quick verification of wallet balances, network status, contract deployments, and more—all without modifying the blockchain state.

---

## Features

Skyline View provides a simple way to:
- **Connect to Base Sepolia**: Ensure your connection to the Base network (chainId: 84532).
- **Inspect Wallet Balances**: Quickly check the balance of any wallet without sending transactions.
- **Verify Contract Deployments**: Use verified explorer links from Basescan for contract validation.
- **Review Network Status**: Check recent block information, gas usage, and other network details.
- **Read-Only Mode**: All interactions are non-invasive, ensuring no blockchain state changes.

Skyline View is perfect for developers who need a quick, reliable tool for Base Sepolia network validation and exploration.

---

## How It Works

Skyline View connects to Coinbase Wallet using the Coinbase Wallet SDK. It then queries Base Sepolia using the `viem` library for blockchain information, including wallet balances, transaction counts, contract bytecodes, and gas prices. It fetches all this data securely in read-only mode, ensuring that no transactions are signed or broadcast to the network.

### Workflow:
1. **Connect to Coinbase Wallet**: Uses the Coinbase Wallet SDK to request access to the connected wallet.
2. **Query the Base Sepolia Network**: Retrieves wallet balances and other relevant blockchain data via the `viem` library.
3. **Return the Data**: Outputs the results to the console, including links to Basescan for easy verification.

No transactions are signed or sent on-chain, making it safe for users to inspect their network status without any risk of affecting their blockchain state.

---

## Repository Structure

- **app/skyline-view.ts**  
  This is the main script that integrates Coinbase Wallet SDK and Base Sepolia data fetching using the `viem` library.

- **contracts/**  
  Contains Solidity contracts deployed to Base Sepolia for testing and validation:
  - `contract.sol`  
  - `ERC20.sol`  
  - `minimaltoken.sol`  


- **package.json**  
  Contains the dependencies required to run the project, including `Coinbase Wallet SDK` and `viem`.

- **README.md**  
  This file, which contains an overview of the project, usage instructions, and more.

---

## Supported Networks

- **Base Sepolia**  
  - **ChainId (decimal)**: 84532  
  - **Explorer**: [Base Sepolia Explorer](https://sepolia.basescan.org)

- **Base Mainnet (future)**  
  - **ChainId (decimal)**: 8453 (subject to change)  
  - **Explorer**: [Base Explorer](https://basescan.org)

---

## Usage

To use Skyline View, simply install the dependencies, compile the TypeScript code, and run the main script.

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-handle/skyline-view.git
    cd skyline-view
    ```

2. **Install dependencies:**
    ```bash
    npm install
    ```

3. **Run the script:**
    ```bash
    ts-node app.skyline-view.ts
    ```

This will connect to Base Sepolia, fetch your wallet balance, display the most recent block details, and provide direct explorer links for validation.

---

## Dependencies

Skyline View relies on the following dependencies:
- **Coinbase Wallet SDK**: A JavaScript library for interacting with Coinbase Wallet.
- **Viem**: A TypeScript library for interacting with Ethereum-based RPC endpoints.
- **Axios**: Used for making HTTP requests.

Additional useful libraries:
- **Ethers.js**: Optional library for enhanced Ethereum protocol interaction.
- **Web3.js**: Another optional library for wallet interaction.

---

## License

MIT License  
Copyright (c) 2025 YOUR_NAME

---

## Author

GitHub: [quick-dryad](https://github.com/quick-dryad)  

Email: quick_dryad_0v@icloud.com

---

## Testnet Deployment (Base Sepolia)

The following contracts have been deployed on Base Sepolia for validation purposes:

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: [sepolia.basescan.org](https://sepolia.basescan.org)

Contract contract.sol address:  
0x7273cC5bb7F012e6336F779782691A95008bF556

Deployment and verification:
- [Deployment Link](https://sepolia.basescan.org/address/0x7273cC5bb7F012e6336F779782691A95008bF556)
- [Code Verification](https://sepolia.basescan.org/0x7273cC5bb7F012e6336F779782691A95008bF556/0#code)

Contract ERC20.sol address:  
0xec886A4eb1Cb1212199628d4B4c7d4Af26d26611 

Deployment and verification:
- [Deployment Link](https://sepolia.basescan.org/address/0xec886A4eb1Cb1212199628d4B4c7d4Af26d26611)
- [Code Verification](https://sepolia.basescan.org/0xec886A4eb1Cb1212199628d4B4c7d4Af26d26611/0#code)

Contract minimaltoken.sol address:  
0x3ED8e701dB12E3Ab322e36324dB562ef8e560852 

Deployment and verification:
- [Deployment Link](https://sepolia.basescan.org/address/0x3ED8e701dB12E3Ab322e36324dB562ef8e560852)
- [Code Verification](https://sepolia.basescan.org/0x3ED8e701dB12E3Ab322e36324dB562ef8e560852/0#code)

These testnet deployments are used to ensure that the Base Sepolia network and tools are functioning as expected before mainnet deployment.
