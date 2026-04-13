# My App

A Web3 dApp composed with [[N]skills](https://www.nskills.xyz).

## Blueprint: selected nodes

These components were included in this generation:

- **ERC-721 Stylus NFT** — Deploy and interact with ERC-721 NFTs on Arbitrum Stylus
- **Chain Data** — Token/NFT data fetching with Moralis or Alchemy Enhanced APIs

## Project structure

```
my-app/
├── package.json                # Workspace root
├── contracts/                  # Rust/Stylus smart contracts
│   └── erc721/
├── docs/                       # Documentation
├── scripts/                     # Deploy / utility scripts (if generated)
├── .gitignore
└── README.md
```

## Quick start

### Prerequisites

- **Node.js** 18+ and **npm** (comes with Node.js)
- **Rust** toolchain and **cargo-stylus** for building/deploying Stylus contracts (see `docs/` and [Stylus SDK](https://github.com/OffchainLabs/stylus-sdk-rs))

### Step-by-step

1. **Clone and enter the project**

   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
   ```

   ![Clone and enter the project](https://raw.githubusercontent.com/Cradle-app/NSkills/main/apps/web/public/clone-and-enter.png)

2. **Install dependencies** (workspace root):

   ```bash
   npm install
   ```

   This installs all workspace packages (including `apps/web` when present).

   ![Install dependencies](https://raw.githubusercontent.com/Cradle-app/NSkills/main/apps/web/public/install-dep.png)

3. **Environment variables**

   ```bash
   cp .env.example .env
   ```

   Edit `.env` and set:

   - `NEXT_PUBLIC_ALCHEMY_API_KEY`: Alchemy API key for data fetching

   ![Environment variables](https://raw.githubusercontent.com/Cradle-app/NSkills/main/apps/web/public/env-var.png)

### ERC-721 Integration

Add the `ERC721InteractionPanel` to `apps/web/src/app/page.tsx`:

```tsx
import { WalletButton } from '@/components/wallet-button';
import { ERC721InteractionPanel } from '@/lib/erc721-stylus/src';

export default function Home() {
  return (
    <main className="flex min-h-screen flex-col items-center justify-center p-24">
      <div className="max-w-5xl w-full text-center">
        <h1 className="text-4xl font-bold mb-8">
          My DApp
        </h1>
        <p className="text-lg text-gray-600 dark:text-gray-400 mb-12">
          A Web3 application built with Cradle
        </p>

        <div className="flex justify-center">
          <WalletButton />
        </div>

        <ERC721InteractionPanel />
      </div>
    </main>
  );
}
```



## Documentation

Check the `docs/` folder for guides that match your blueprint (e.g. frontend setup, contract deployment, API routes).

## License

MIT

---

Generated with [[N]skills](https://www.nskills.xyz)
