# GreenSignals

A decentralized prediction market platform built on the **Terra Classic (LUNC)** blockchain. GreenSignals lets you create and trade on binary YES/NO prediction markets, powered by LMSR (Logarithmic Market Scoring Rule) pricing and secured by CosmWasm smart contracts - all from a browser-based interface using the Keplr wallet extension.

---

## Features at a Glance

- **Browse Markets** - Discover open, resolved, and cancelled prediction markets across 11 categories
- **Trade Shares** - Buy and sell YES/NO shares with LMSR-based dynamic pricing
- **Create Markets** - Launch your own binary prediction market with a title, category, and resolution date
- **Portfolio** - Track all your open positions and claimable winnings
- **Payout Distribution** - See the full ranked payout table for resolved markets
- **Keplr Integration** - One-click wallet connect with auto chain suggestion for Columbus-5
- **Category Filters** - Filter markets by topic: Politics, Crypto, Sports, Finance, and more

---

## Pages

### Home
Market discovery and browsing:
- Grid of market cards showing title, category, probability bar, volume, and status
- Filter by category pill or search by keyword
- Pagination with "Load more" support
- Links to individual market detail pages

### Market Detail
Full trading interface for a single market:
- Live YES/NO probability bar powered by on-chain LMSR state
- Trade panel - buy or sell YES/NO shares, with estimated cost/return shown before signing
- Fee breakdown (1% on buys and sells)
- Resolved markets show the DistributionTable: ranked winner/loser payout list with "Load more" pagination
- Claimed positions show a "Claimed" badge; winners highlighted

### Create Market
Form for launching a new prediction market:
- Title, description, resolution date
- Category selector (all 11 categories available)
- Submits a transaction via Keplr

### Portfolio
Personal position overview:
- Lists all markets where the connected wallet holds shares
- Shows YES shares, NO shares, current value, and claimable amount (net of 0.25% claim fee)
- One-click claim winnings and refund position actions

---

## Smart Contract

A single CosmWasm contract handles all on-chain prediction market logic.

**Pricing model:** LMSR (Logarithmic Market Scoring Rule) - continuous AMM pricing for binary YES/NO shares.

### Fee Structure

| Action | Fee | Recipient |
|---|---|---|
| BuyShares | 1% of collateral sent | Protocol fee accumulator |
| SellShares | 1% of gross return | Protocol fee accumulator |
| ClaimWinnings | 0.25% of gross payout | Protocol fee accumulator |

---

## Architecture

```
React Components -> Custom Hooks -> Services -> Zustand Stores
                                             -> Blockchain (CosmJS) / LCD API (Axios)
---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 19 + TypeScript |
| Build tool | Vite 5 |
| State management | Zustand 4 |
| Routing | React Router 6 |
| Blockchain client | CosmJS 0.32 |
| Wallet | Keplr browser extension |
| HTTP client | Axios |
| Charts / UI | Recharts, Lucide React |
| Smart contracts | Rust / CosmWasm 1.5 |
| Linting | ESLint |

---

## Market Categories

| Key | Label |
|---|---|
| sustainability | Sustainability |
| politics | Politics |
| crypto | Crypto |
| sports | Sports |
| finance | Finance |
| geopolitics | Geopolitics |
| tech | Tech |
| culture | Culture |
| elections | Elections |
| economy | Economy |
| weather | Weather |

---

## Network

| Network | Chain ID | LCD Endpoint | RPC Endpoint |
|---|---|---|---|
| Mainnet (Columbus-5) | columbus-5 | terra-classic-lcd.publicnode.com | terra-classic-rpc.publicnode.com |

**Deployed contract address:**
```
terra1z53x88dh2s6sj9uvknwpmhd9scs9tczhkne5emnwu9kflrdpmyfqg3rnwr
```

---

## Donations & Support

Want to support the sustainability of **GreenSignals**?

Donate LUNC to:
```
terra1l9q4guus5vjxl84d5qea068vcen32l04jmc55w
```

---

## License

This project is open-source under the **MIT License**.

## Contributing

We welcome contributions! Feel free to fork, create pull requests, or report issues.

## Contact & Community

- [Twitter](https://twitter.com/GreenFrndLabs)
- [Website](https://www.greenfriendlylabs.com/)

---

Together, let's build a sustainable **LUNC** future! 🌿🚀
