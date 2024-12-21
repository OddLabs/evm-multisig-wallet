# 🔐 EVM MultiSig Wallet

A Foundry implementation of a MultiSig wallet compatible with EVM (Ethereum Virtual Machine). This wallet enables secure storage of tokens and cryptocurrencies, requiring approval from the majority of owners to execute transactions.

## 📋 Features

- Support for ETH and ERC-20/ERC-721/ERC-1155 tokens
- Requires simple majority approval from owners to execute transactions
- Compatible with all EVM networks (Ethereum, Polygon, BSC, etc.)
- Developed and tested with Foundry
- Transaction proposal and execution system
- Owner management interface

## 🔧 Requirements

- [Foundry](https://book.getfoundry.sh/getting-started/installation.html)
- Solidity ^0.8.0

## ⚙️ Installation

1. Clone the repository:
```bash
git clone https://github.com/OddLabs/evm-multisig-wallet.git
cd evm-multisig-wallet
```

2. Install dependencies:
```bash
forge install
```

3. Compile contracts:
```bash
forge build
```

## 🧪 Testing

Run tests with:

```bash
forge test
```

For coverage testing:

```bash
forge coverage
```

## 📝 Usage

### Deployment

1. Set up your environment variables:
```bash
cp .env.example .env
# Edit .env with your private keys and settings
```

2. Deploy the contract:
```bash
forge script script/Deploy.s.sol --rpc-url <your-network> --broadcast
```

### Interacting with the Wallet

1. Propose a transaction:
```solidity
function proposeTransaction(
    address target,
    uint256 value,
    bytes memory data
) public returns (uint256 transactionId);
```

2. Approve a transaction:
```solidity
function approveTransaction(uint256 transactionId) public;
```

3. Execute an approved transaction:
```solidity
function executeTransaction(uint256 transactionId) public;
```

## 🏗️ Architecture

The project consists of three main contracts:

1. `MultiSigWallet.sol`: Main contract managing transactions and approvals
2. `MultiSigFactory.sol`: Factory for creating new wallet instances
3. `MultiSigStorage.sol`: State management and storage

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add: amazing new feature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Security Notice

This project is under development. A full audit is recommended before production use.

## 📞 Contact

Your Name - [@your-twitter](https://twitter.com/your-username)

Project Link: [https://github.com/OddLabs/evm-multisig-wallet](https://github.com/OddLabs/evm-multisig-wallet)