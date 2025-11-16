# TripLock - Encrypted Trip Planner

A fully encrypted trip planning application built with FHEVM (Fully Homomorphic Encryption Virtual Machine) and Next.js. Plan and analyze private travel itineraries without exposing your data.

## 🚀 Features

- **Privacy-First**: All trip data is encrypted locally using AES-GCM before being stored on-chain
- **Homomorphic Analytics**: Travel style insights are computed using fully homomorphic encryption
- **Decentralized Storage**: Encrypted trip data is stored permanently on the blockchain
- **Multi-Network Support**: Deployable to Ethereum mainnet, testnets, and local development networks

## 📦 Tech Stack

- **Smart Contracts**: Solidity with FHEVM for encrypted computations
- **Frontend**: Next.js 14 with TypeScript and Tailwind CSS
- **Blockchain**: Ethereum-compatible networks with FHE support
- **Encryption**: AES-GCM for client-side encryption + FHE for on-chain analytics

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Next.js App   │    │   Smart Contract │    │   FHEVM Oracle  │
│                 │    │                 │    │                 │
│ • Trip Builder  │───▶│ • EncryptedTrip │───▶│ • Decryption    │
│ • Trip Vault    │    │   Planner       │    │   Services      │
│ • Style Insights│    │ • FHECounter    │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🚀 Quick Start

### Prerequisites

- Node.js 18+
- npm or yarn
- Git

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd travel-sealed-memories

# Install dependencies
npm install

# Install frontend dependencies
cd frontend && npm install && cd ..
```

### Development

```bash
# Start local Hardhat node with FHEVM
npm run node

# Deploy contracts to local network
npm run deploy

# Start frontend development server
cd frontend && npm run dev
```

### Testing

```bash
# Run contract tests
npm test

# Run frontend tests
cd frontend && npm test
```

## 📚 Documentation

For detailed documentation, please refer to:
- [FHEVM Documentation](https://docs.zama.ai/fhevm)
- [Hardhat Documentation](https://hardhat.org/docs)
- [Next.js Documentation](https://nextjs.org/docs)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
