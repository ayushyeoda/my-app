# Chain Data

| Field | Value |
|-------|-------|
| Type | `chain-data` |
| ID | `63058cff` |
| Category | app |
| Tags | data, alchemy, moralis, tokens, nfts |
| Description | Token/NFT data with Alchemy/Moralis |

## Configuration

| Setting | Value |
|---------|-------|
| Provider | alchemy |
| Features | token-balances, nft-data |
| Cache Enabled | Enabled |
| Cache Duration | 60000 |

## Environment Variables

| Key | Description | Required | Secret | Default |
|-----|-------------|----------|--------|---------|
| `NEXT_PUBLIC_ALCHEMY_API_KEY` | Alchemy API key for data fetching | Yes | No |  |

## Documentation

### Chain Data

# Chain Data

On-chain data fetching using Alchemy Enhanced APIs.

## Features

- **token-balances**: Enabled
- **nft-data**: Enabled

## Usage

```tsx
import { useTokenBalances, useNFTs, useTransactionHistory } from '@/hooks/useChainData';

function Portfolio() {
  const { data: tokens } = useTokenBalances();
  const { data: nfts } = useNFTs();
  
  return (
    <div>
      <TokenList tokens={tokens} />
      <NFTGallery nfts={nfts} />
    </div>
  );
}
```


## File Structure

This component would generate the following files:

- `data-client.ts` (frontend-lib)
- `useChainData.ts` (frontend-hooks)
- `TokenList.tsx` (frontend-components)
- `NFTGallery.tsx` (frontend-components)

## Integration Points

**Depends on:**
- Erc721-stylus (`ac4e3cdc`)

