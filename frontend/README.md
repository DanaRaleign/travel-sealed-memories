# TripLock Frontend

The TripLock frontend is a modern Next.js application that provides an encrypted trip planning interface. Users can create, manage, and analyze travel itineraries with complete privacy using Fully Homomorphic Encryption (FHE).

This frontend works alongside the TripLock smart contracts and provides a beautiful, responsive interface for interacting with encrypted trip data on-chain.

## 🚀 Features

- **Encrypted Trip Planning**: Create trips with local AES-GCM encryption
- **Homomorphic Analytics**: View travel style insights computed with FHE
- **Wallet Integration**: Connect MetaMask and other Web3 wallets
- **Responsive Design**: Beautiful UI built with Tailwind CSS
- **Real-time Updates**: Live connection to blockchain state

> [!IMPORTANT]
> This frontend requires the TripLock smart contracts to be deployed. Please follow the installation instructions below.

## Features

- **Fully Homomorphic Encryption**: Privacy-preserving analytics on encrypted data
- **Next.js 14**: Modern React framework with App Router
- **TypeScript**: Type-safe development experience
- **Tailwind CSS**: Utility-first styling for rapid UI development
- **ethers.js**: Ethereum blockchain interaction
- **Web3Modal**: Multi-wallet connection support

## Requirements

- You need to have Metamask browser extension installed on your browser.

## Local Hardhat Network (to add in MetaMask)

Follow the step-by-step guide in the [Hardhat + MetaMask](https://docs.metamask.io/wallet/how-to/run-devnet/) documentation to set up your local devnet using Hardhat and MetaMask.

- Name: Hardhat
- RPC URL: http://127.0.0.1:8545
- Chain ID: 31337
- Currency symbol: ETH

## Install

### Installation

1. Navigate to the frontend directory:

```sh
cd frontend
```

2. Install dependencies:

```sh
npm install
```

3. Ensure the smart contracts are deployed (see root README for deployment instructions).

4. Start the development server:

```sh
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Development

### Prerequisites

- MetaMask or compatible Web3 wallet
- Local Hardhat node running (from project root)
- Smart contracts deployed to local network

### Running the Application

1. Connect MetaMask to local Hardhat network:
   - Network Name: Hardhat
   - RPC URL: http://127.0.0.1:8545
   - Chain ID: 31337
   - Currency Symbol: ETH

2. Start the frontend:

```sh
npm run dev
```

3. Open [http://localhost:3000](http://localhost:3000) and connect your wallet.

## How to fix Hardhat Node + Metamask Errors ?

When using MetaMask as a wallet provider with a development node like Hardhat, you may encounter two common types of errors:

### 1. ⚠️ Nonce Mismatch ❌💥

MetaMask tracks wallet nonces (the number of transactions sent from a wallet). However, if you restart your Hardhat node, the nonce is reset on the dev node, but MetaMask does not update its internal nonce tracking. This discrepancy causes a nonce mismatch error.

### 2. ⚠️ View Function Call Result Mismatch ❌💥

MetaMask caches the results of view function calls. If you restart your Hardhat node, MetaMask may return outdated cached data corresponding to a previous instance of the node, leading to incorrect results.

### ✅ How to Fix Nonce Mismatch:

To fix the nonce mismatch error, simply clear the MetaMask cache:

1. Open the MetaMask browser extension.
2. Select the Hardhat network.
3. Go to Settings > Advanced.
4. Click the "Clear Activity Tab" red button to reset the nonce tracking.

The correct way to do this is also explained [here](https://docs.metamask.io/wallet/how-to/run-devnet/).

### ✅ How to Fix View Function Return Value Mismatch:

To fix the view function result mismatch:

1. Restart the entire browser. MetaMask stores its cache in the extension's memory, which cannot be cleared by simply clearing the browser cache or using MetaMask's built-in cache cleaning options.

By following these steps, you can ensure that MetaMask syncs correctly with your Hardhat node and avoid potential issues related to nonces and cached view function results.

## Project Structure

```
frontend/
├── app/                 # Next.js app router pages
├── components/          # React components
├── fhevm/              # FHEVM integration utilities
├── hooks/              # Custom React hooks
├── lib/                # Utility functions and encryption
├── abi/                # Contract ABIs and addresses
└── public/             # Static assets
```

### Key Components

- **TripBuilder**: Form for creating encrypted trip itineraries
- **TripVault**: Display and manage stored encrypted trips
- **InsightBoard**: View homomorphic analytics on travel styles
- **FHEVM Hooks**: Utilities for encrypted contract interactions

## Documentation

- [Hardhat + MetaMask](https://docs.metamask.io/wallet/how-to/run-devnet/): Set up your local devnet step by step using Hardhat and MetaMask.
- [FHEVM Documentation](https://docs.zama.ai/protocol/solidity-guides/)
- [FHEVM Hardhat](https://docs.zama.ai/protocol/solidity-guides/development-guide/hardhat)
- [@zama-fhe/relayer-sdk Documentation](https://docs.zama.ai/protocol/relayer-sdk-guides/)
- [Setting up MNEMONIC and INFURA_API_KEY](https://docs.zama.ai/protocol/solidity-guides/getting-started/setup#set-up-the-hardhat-configuration-variables-optional)
- [React Documentation](https://reactjs.org/)
- [FHEVM Discord Community](https://discord.com/invite/zama)
- [GitHub Issues](https://github.com/zama-ai/fhevm-react-template/issues)

## License

This project is licensed under the BSD-3-Clause-Clear License - see the LICENSE file for details.
