# Oscires NFT Smart Contract

![ERC1155](https://img.shields.io/badge/ERC-1155-blue) ![MIT](https://img.shields.io/badge/License-MIT-green) ![Solidity](https://img.shields.io/badge/Solidity-%5E0.8.22-lightgrey) ![Allowlist](https://img.shields.io/badge/Feature-Allowlist-orange) ![Supply](https://img.shields.io/badge/Feature-Supply%20Tracking-purple)

## Overview 🚀
The **Oscires** smart contract is a powerful implementation of an NFT minting platform using the ERC1155 standard. It includes features such as payment splitting, pausing functionality, and separate minting windows for public and allowlist participants.

### Key Features ✨
- **ERC1155 Standard**: Supports multi-token functionality.
- **Minting Windows**: Flexible public and allowlist minting periods.
- **Supply Tracking**: Enforces maximum supply and wallet limits.
- **Dynamic Metadata**: Supports IPFS-based metadata with adjustable URI.
- **Payment Splitting**: Built-in `PaymentSplitter` for revenue sharing.
- **Pausable**: Pausing and unpausing functionality for security.

---

## Features 🛠️

### Core Features 🧩

![Key Features](https://img.shields.io/badge/Core-Features-blue)

1. **Dynamic Minting**: Supports both allowlist and public minting with adjustable pricing.
2. **Metadata Management**: Fully compatible with IPFS for decentralized metadata storage.
3. **Supply Control**: Implements strict total supply and per-wallet limits to ensure fair distribution.
4. **Pause and Unpause**: Includes pausing functionality to secure the contract during emergencies.
5. **Payment Splitting**: Automates revenue distribution among multiple stakeholders.
6. **Batch Minting**: Enables batch minting for efficient token distribution.

### Advanced Features 💡

![Advanced Features](https://img.shields.io/badge/Advanced-Features-green)

- **Allowlist Verification**: Ensures exclusive access to minting for pre-approved users.
- **Token URI Customization**: Dynamically adjusts metadata URI for enhanced flexibility.
- **On-Chain Security**: Protects against unauthorized access with ownership-based controls.

---

## Setup 🛠️

### Prerequisites 📋
- Install [Node.js](https://nodejs.org/).
- Install [Hardhat](https://hardhat.org/) or [Truffle](https://trufflesuite.com/) for contract deployment.
- Ensure you have an Ethereum wallet like [MetaMask](https://metamask.io/).

### Deployment 🚀
1. Clone this repository.
   ```bash
   git clone https://github.com/your-repo/oscires-nft.git
   cd oscires-nft
   ```
2. Install dependencies.
   ```bash
   npm install
   ```
3. Deploy the contract using Hardhat or Truffle.
   ```bash
   npx hardhat run scripts/deploy.js --network goerli
   ```

---

## Functions ⚙️

### Admin Functions 👩‍💼
| Function                   | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| `setAllowList(address[])` | Adds addresses to the allowlist.                                            |
| `editMintWindows()`       | Configures the minting windows for public and allowlist.                     |
| `setURI(string)`          | Updates the base URI for token metadata.                                    |
| `pause()` / `unpause()`   | Pauses/unpauses the contract for security.                                   |
| `mintBatch()`             | Allows batch minting of NFTs by the owner.                                  |

### Minting Functions 🪙
| Function                 | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| `allowListMint()`        | Mints tokens for allowlist participants.                                   |
| `publicMint()`           | Mints tokens during the public mint window.                                 |

### Helper Functions 🛠️
| Function                 | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| `mint()`                 | Internal helper to validate and mint tokens.                               |
| `uri(uint256)`           | Returns metadata URI for a specific token ID.                              |

---

## Minting Workflow 🖌️

### Allowlist Minting 🌟
1. Ensure the minting window is open (`allowListMintOpen`).
2. Confirm the user is on the allowlist.
3. Execute the `allowListMint` function with the desired token ID and quantity.
4. Payment for the transaction must match `allowListPrice * amount`.

### Public Minting 🌍
1. Ensure the public minting window is open (`publicMintOpen`).
2. Execute the `publicMint` function with the desired token ID and quantity.
3. Payment for the transaction must match `publicPrice * amount`.

---

## Metadata 📦
Metadata is hosted on IPFS. The token URI follows the format:
```
ipfs://<base-uri>/<token-id>.json
```
Ensure metadata JSON files are structured according to the ERC1155 metadata standard.

---

## Security 🔐
- **Mint Restrictions**: Enforces maximum per-wallet and total supply limits.
- **Allowlist Verification**: Ensures only allowlisted addresses can participate during the allowlist mint window.
- **Pausable**: Allows pausing of contract in case of vulnerabilities.

---

## Contribution 🤝
We welcome contributions to enhance the **Oscires** smart contract. Please follow the steps below:
1. Fork the repository.
2. Create a feature branch.
3. Submit a pull request with detailed descriptions of your changes.

---

## License 📜
This project is licensed under the MIT License. See the LICENSE file for details.

---

### Contact 📧
For questions or issues, reach out to:
- **Email**: abhi8994ty@gmail.com

![Ethereum](https://img.shields.io/badge/Ethereum-NFT-black) ![IPFS](https://img.shields.io/badge/IPFS-Storage-blue) ![Hardhat](https://img.shields.io/badge/Hardhat-Deployment-yellow)

