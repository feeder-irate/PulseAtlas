# PulseAtlas

Built for Base

PulseAtlas is a Base-native repository created to validate wallet connectivity, RPC consistency, and explorer visibility across Base networks using official Coinbase tooling.

Rather than acting as a full application, PulseAtlas serves as a clean diagnostic layer for Base infrastructure and account abstraction–friendly user flows.

---

## Repository Focus

This project is intentionally scoped to:
- Base Mainnet and Base Sepolia compatibility
- Wallet onboarding via OnchainKit
- Read-only onchain queries through Viem
- Clear Basescan deployment and verification references

---

## Network Targets

Base Sepolia (Testnet)  
- chainId (decimal): 84532  
- Explorer: https://sepolia.basescan.org  
- RPC: https://sepolia.base.org  

Base Mainnet  
- chainId (decimal): 8453  
- Explorer: https://basescan.org  
- RPC: https://mainnet.base.org  

---

## Runtime Behavior

Primary file: `app/pulseAtlas.ts`

During execution, the app:
- Initializes an OnchainKit provider bound to a selected Base chain
- Displays wallet connection UX
- Uses a Viem public client for Base JSON-RPC reads
- Fetches:
  - RPC-reported chainId
  - latest block height
  - native ETH balance for a supplied address
- Outputs direct Basescan explorer references

---

## Project Layout

- app/
  - pulseAtlas.ts  
    React entry file combining wallet UI and Base RPC reads.

Expected auxiliary files:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

---

## Libraries Used

- OnchainKit  
  Wallet UI components and Base-first primitives  
  https://github.com/coinbase/onchainkit  

- Viem  
  EVM client for interacting with Base RPC endpoints  

---

## Setup & Execution

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies via your preferred package manager and start a local dev server using a standard React/Vite or Next.js setup.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

---

## Base Mainnet Deployment

Deployed on Base Mainnet

Network: Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Deployed contract address:  
your_adress  

Basescan deployment and verification links:
- Contract address:  
  https://basescan.org/address/your_adress  
- Contract verification (source code):  
  https://basescan.org/address/your_adress#code  

---

## License

MIT License

---

## Author

GitHub: https://github.com/your-handle  
Public contact (email): your-name@proton.me  
Public contact (X): https://x.com/your-handle  

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
your_adress  

Deployment and verification:
- https://sepolia.basescan.org/address/your_adress  
- https://sepolia.basescan.org/your_adress/0#code  

Contract #2 address (optional):  
your_adress  

Deployment and verification:
- https://sepolia.basescan.org/address/your_adress  
- https://sepolia.basescan.org/your_adress/0#code  

Contract #3 address (optional):  
your_adress  

Deployment and verification:
- https://sepolia.basescan.org/address/your_adress  
- https://sepolia.basescan.org/your_adress/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
