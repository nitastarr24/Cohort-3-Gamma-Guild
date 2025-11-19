
# Week 2: Blockchain & Web3 Deep Dive Research (Day 1-3)

**Student Name:** Benita Basil  
**Submission Date:** 19-Nov-2025  
**Assignment:** Blockchain & Transaction Analysis   
**Twitter Thread Link:** [Add after post

## Part 1: Consensus Mechanisms Deep Dive

### 1. Proof of Work (PoW) Analysis

#### How PoW Works
- **Mining process step by step:** Miners compete to solve a cryptographic puzzle by repeatedly hashing the block header. The first miner to find a valid hash broadcasts it to the network for validation.
- **Computational problem:** Miners are solving the “proof-of-work” problem — finding a hash lower than the current target.
- **Difficulty adjustment:** The network adjusts mining difficulty every set number of blocks to maintain a consistent block time.
- **Simultaneous solutions:** If two miners solve at the same time, the network temporarily forks. The longest chain becomes the valid chain.

#### Security Model
- **Attack prevention:** PoW makes altering the blockchain computationally expensive.
- **51% attack:** If someone controls >50% of network hash power, they can rewrite history — very costly and difficult on large networks like Bitcoin.
- **Economic incentives:** Honest miners earn block rewards and transaction fees.
- **Cost of attack:** Enormous energy and hardware costs make attacks economically unfeasible.

#### Real-World Examples
- **Blockchains using PoW:** Bitcoin, Litecoin, Ethereum (pre-Merge)
- **Bitcoin:** Uses SHA-256 hashing; block time ~10 minutes.
- **Ethereum pre-Merge:** Used Ethash PoW; block time ~13-15 seconds.
- **PoW evolution:** Mining difficulty, ASICs, and energy consumption have increased over time.

#### Trade-offs
- **Advantages:** Security, proven track record, decentralization
- **Disadvantages:** High energy use, slower transactions, expensive mining
- **Environmental impact:** Significant energy consumption
- **Decentralization:** More nodes = more decentralized, but mining pools can centralize power

---

### 2. Proof of Stake (PoS) Analysis

#### How PoS Works
- **Staking process:** Validators lock up cryptocurrency as stake to propose/validate blocks.
- **Validator selection:** Randomized and weighted by stake amount.
- **Slashing:** Penalizes malicious or lazy validators by taking part of their stake.
- **Finality:** Blocks are finalized once a majority of validators agree.

#### Security Model
- **Attack prevention:** Economic penalties discourage cheating.
- **Economic penalties:** Slashing or loss of stake.
- **Stake size effect:** Larger stake = more influence, but cheating is costly.
- **Stake & rewards:** Proportional; more stake generally earns more rewards.

#### Real-World Examples
- **Blockchains using PoS:** Ethereum 2.0, Cardano, Solana (hybrid)
- **Ethereum current PoS:** Validators stake 32 ETH to participate
- **Cardano:** Uses Ouroboros PoS, different randomization and delegation
- **Solana:** Hybrid approach with PoH + PoS

#### Trade-offs
- **Advantages:** Energy efficient, fast transactions, scalable
- **Disadvantages:** Potential centralization, staking barriers
- **Energy comparison:** PoS uses far less energy than PoW
- **Centralization:** Large stakers may influence network

### 3. Comparative Analysis

| Feature                  | PoW                           | PoS                           |
|---------------------------|-------------------------------|-------------------------------|
| Security model            | Computational                 | Economic                      |
| Energy consumption        | High                          | Low                           |
| Transaction speed         | Slower                        | Faster                        |
| Decentralization          | High (if mining is distributed) | Medium to High               |
| Entry barriers            | High (hardware & energy costs) | Moderate (stake required)     |
| Cost structure            | Electricity + hardware        | Stake-based                   |
| Scalability potential     | Limited                       | High                          |
| Real-world adoption       | Bitcoin, Litecoin, Ethereum (pre-Merge) | Ethereum 2.0, Cardano, Solana |

---


### 4. Practical Implications for Creatives

- **NFT minting costs:** PoS chains usually have lower minting costs due to less energy consumption and lower gas fees.
- **Choosing consensus:** PoW may suit very secure store-of-value chains; PoS is better for dApps, NFTs, and scalable projects.
- **Gas fees:** PoW chains like Ethereum (pre-Merge) had high fees; PoS reduces them but depends on network usage.
- **What creators should consider:** Transaction cost, speed, environmental impact, and community size when choosing a blockchain.

---

# Part 2: Gas, Blocks & Confirmations

## Objective
Understand how gas economics work, how blocks are structured, and why confirmations matter for transaction security.

---

### 1. Gas Economics

#### What is Gas?
- Gas is a **unit that measures the amount of computational work needed to perform operations** on a blockchain.
- It’s called “gas” because it **fuels transactions**, similar to how gas fuels a car.
- Every operation in a smart contract costs gas; more complex computations use more gas.

#### How Gas Pricing Works
- **Gas price** is how much you are willing to pay per unit of gas (measured in **Gwei**, a small fraction of Ether).
- Gas price is determined by **network demand**; higher demand → higher prices.
- Factors influencing gas price: network congestion, transaction complexity, miner/validator incentives.
- **Gas limit** is the maximum gas you’re willing to spend; **gas price** is how much you pay per unit.

#### Gas Calculation
- **Total transaction cost** = Gas used × Gas price
- Simple transfers (ETH) use less gas; smart contract interactions cost more.
- Some transactions cost more due to complexity or storage requirements.
- Gas can be estimated using tools like **Etherscan Gas Tracker** or wallet estimators.

#### Gas Optimization Strategies
- Gas is usually lowest during off-peak network hours.
- Reduce costs by batching transactions, using efficient smart contract calls, or Layer 2 solutions (like Polygon, Optimism).
- Layer 2 solutions move transactions off the main chain to reduce congestion and fees.

---

### 2. Blocks Structure

#### What is a Block?
- A block is a **container for transactions** that have been validated and added to the blockchain.
- Each block contains:
  - A list of transactions
  - Metadata (timestamp, block number)
  - The hash of the previous block
- Blocks are linked together to form the **blockchain**.

#### Block Components
- **Block header**: metadata including timestamp, previous block hash, nonce, and root hashes.
- **Block hash**: a unique identifier of the block, derived from its contents.
- **Previous block hash**: links this block to the chain.
- Number of transactions per block depends on block size and blockchain rules.

#### Block Time
- Block time = how long it takes to produce a new block.
- Bitcoin ~10 min, Ethereum ~13–15 sec, Solana ~400–600 ms.
- Block time affects transaction speed and finality: shorter block time → faster confirmation, but may increase the chance of temporary forks.

---

### 3. Confirmations

#### What are Confirmations?
- A confirmation is when a block containing your transaction is added to the blockchain **and subsequent blocks are added after it**.
- Confirmations matter because they **secure transactions against being reversed**.
- More confirmations → more security.

#### Confirmation Requirements
- Different scenarios require different confirmations:
  - Small payments: 1–2 confirmations may be enough
  - Large payments or exchanges: often 6–12 confirmations
- Exchanges require more confirmations to reduce risk of double spending.
- Fewer confirmations = higher risk if a chain reorganization occurs.

#### Real-World Application
- 1 confirmation may be enough for small transfers between friends.
- For NFTs or exchanges, wait for multiple confirmations to ensure security.
- NFT marketplaces may show “Pending” until a certain number of confirmations.
- Chain reorganization: if a longer chain appears, transactions in orphaned blocks may be reverted until re-added in the main chain.

---
# Part 3: Wallet Security & Types

## Objective
Understand different wallet types, their security models, and best practices for protecting your crypto assets.

---

### 1. Custodial vs Non-Custodial Wallets

#### Custodial Wallets
- **Definition:** Wallets where a third party (exchange or provider) controls your private keys.
- **How they work:** Your keys are held and managed by the service provider; you access your funds through their platform.
- **Advantages:** Easy to use, account recovery available, convenient for beginners.
- **Risks:** Provider can be hacked, you don’t fully control your funds, potential regulatory risks.
- **Examples:** Coinbase, Binance, Kraken, Gemini, BitPay

#### Non-Custodial Wallets
- **Definition:** Wallets where **you** control your private keys.
- **How they work:** Keys are stored on your device; only you can sign transactions.
- **Advantages:** Full control, privacy, lower risk of centralized hacks.
- **Risks:** If you lose your keys/seed phrase, funds are gone; harder for beginners.
- **Examples:** MetaMask, Trust Wallet, Argent, Rainbow, Phantom

#### Comparison Table

| Feature                 | Custodial Wallet           | Non-Custodial Wallet      |
|-------------------------|---------------------------|--------------------------|
| Control of funds        | Provider controls keys     | User controls keys       |
| Security                | Moderate (provider risk)   | High (if keys secure)    |
| Convenience             | Very convenient            | Requires setup           |
| Recovery options        | Easy (via provider)        | Difficult (need seed)    |
| Use cases               | Beginners, frequent trading | Self-custody, DeFi users |

#### When to Use Each
- Custodial: Beginners, trading on exchanges, small holdings.
- Non-Custodial: Long-term holding, DeFi interaction, full control desired.
- Beginners: Start with custodial for simplicity; gradually move to non-custodial.  
- Active Web3 users: Non-custodial preferred for control and privacy.

---

### 2. Hot vs Cold Wallets

#### Hot Wallets
- **Definition:** Wallets connected to the internet.
- **How they work:** Software-based wallets on web/mobile that interact with blockchain online.
- **Security implications:** Vulnerable to hacks and phishing.
- **Best use cases:** Daily transactions, small holdings.
- **Examples:** MetaMask, Trust Wallet, Coinbase Wallet

#### Cold Wallets
- **Definition:** Wallets offline, not connected to the internet.
- **Hardware wallets:** Store private keys securely on devices like USB sticks.
- **Security benefits:** Protected from online attacks.
- **Limitations:** Less convenient, cost of device.
- **Examples:** Ledger Nano X, Trezor Model T, SafePal

#### Security Comparison

| Feature          | Hot Wallet               | Cold Wallet             |
|-----------------|-------------------------|------------------------|
| Security         | Moderate-High           | Very High              |
| Convenience      | Very High               | Moderate-Low           |
| Cost             | Free                    | Paid hardware          |
| Use cases        | Small/frequent transactions | Long-term storage     |

#### Recommended Strategy
- Keep **small, active funds** in hot wallets for daily use.  
- Keep **large, long-term funds** in cold wallets.  
- Balance: Convenience for spending, security for storage.

---

### 3. Security Best Practices

#### Seed Phrase Security
- **What is a seed phrase:** A 12-24 word phrase that restores wallet access.
- **Why critical:** Losing it = losing funds permanently.
- **Storage:** Offline, in a safe place; never digital/cloud.
- **Common mistakes:** Taking screenshots, storing on phone/email, sharing it.

#### Common Attack Vectors
- **Phishing:** Fake websites or links trying to steal keys.
- **Malware attacks:** Keyloggers or malicious apps stealing private keys.
- **Social engineering:** Scams convincing you to reveal keys.
- **Protection:** Use hardware wallets, verify links, enable 2FA, keep software updated.

#### Security Checklist
- **Wallet setup:** Use non-custodial cold wallet for long-term storage; hot wallet for daily use.
- **Daily practices:** Avoid unknown links, check URLs, keep devices updated.
- **Emergency procedures:** Keep backup seed phrase offline, know recovery steps, have multi-sig setup if possible.

---


# Part 4: Testnets & Blockchain Explorers

## Objective
Learn to use testnets for safe practice and blockchain explorers to verify and investigate transactions.

---

### 1. Testnets

#### What are Testnets?
- Testnets are **separate blockchains used for testing**, not real value.
- They exist to let developers and users **experiment safely** without risking real cryptocurrency.
- Testnets differ from mainnet because transactions and tokens have no monetary value.

#### Popular Testnets
- **Sepolia (Ethereum)**: Lightweight Ethereum testnet for development and testing smart contracts.
- **Mumbai (Polygon)**: Polygon testnet; compatible with Ethereum tools and smart contracts.
- **Other testnets**: Goerli (Ethereum), Rinkeby (deprecated), Fantom testnet, Solana devnet.
- **Feature comparison:** Gas fees are free or very low; block times often mimic mainnet; used for testing dApps, smart contracts, NFT minting.

#### How to Use Testnets
- **Connect to a testnet in MetaMask:** Settings → Networks → Add Network → Enter testnet details.
- **Get test tokens:** Use faucets (e.g., Sepolia faucet, Mumbai faucet) to receive free test ETH or MATIC.
- **Practice:** Deploy smart contracts, send transactions, mint NFTs, interact with dApps.
- **Limitations:** Test tokens are valueless; network may be reset; some features may be incomplete.

#### Hands-On Practice
- Connect to Sepolia testnet in MetaMask.
- Request test ETH from a faucet.
- Send a small test transaction to another address.
- Document actions and optionally take screenshots for reference.

---

### 2. Blockchain Explorers

#### What are Blockchain Explorers?
- Blockchain explorers are **tools to view and verify blockchain activity**.
- They are important for transparency, auditing, and troubleshooting transactions.
- With explorers, you can check balances, transaction status, smart contract code, and more.

#### Etherscan Deep Dive
- **Search transactions:** Enter transaction hash (TxHash) in search bar.
- **Read transaction details:** View sender, receiver, gas fees, confirmations, and status.
- **Explore wallet addresses:** Check account balance, token holdings, and transaction history.
- **View smart contracts:** Read contract code, check verified source code.
- **Token approvals:** Monitor which contracts can spend tokens on your behalf.
- **Gas tracker:** Check current gas prices and plan transaction timing.

#### Other Explorers
- **Polygonscan:** For Polygon network transactions, smart contracts, and NFTs.
- **Solscan:** For Solana blockchain activity and token transactions.
- **Comparison:** Each explorer is blockchain-specific; choose based on network you interact with.

#### Practical Use Cases
- Verify your NFT ownership.
- Check transaction status before confirming completion.
- Investigate wallets for transparency.
- Verify smart contract source code and approvals.
- Track gas prices for optimal transaction cost.

---
# Part 5: MEV (Maximal Extractable Value)

## Objective
Understand what MEV is, how it works, its impact on users, and its role in blockchain economics.

---

### 1. Understanding MEV

#### What is MEV?
- **MEV (Maximal Extractable Value)** is the **maximum profit a validator or miner can extract from transaction ordering** in a block.
- It represents **value that can be gained by strategically including, excluding, or reordering transactions**.
- **MEV extractors:** Validators or miners who attempt to capture this value for profit.

#### How MEV Works
- Validators/miners can **reorder, insert, or censor transactions** in a block to earn profit.
- **Types of MEV:**
  - **Front-running:** Placing a transaction before another to profit from price movement.
  - **Back-running:** Placing a transaction immediately after a profitable transaction.
  - **Sandwich attacks:** Placing one transaction before and one after a target transaction to manipulate prices.
  
#### Real-World Examples
- DeFi trades on Ethereum where bots reorder transactions for arbitrage.
- NFT minting bots capturing rare tokens by front-running.
- MEV value extracted can reach **millions per day** on active chains.
- Famous incidents: **DeFi arbitrage events** that caused high gas spikes and failed transactions for ordinary users.

---

### 2. Impact on Users

#### How MEV Affects You
- **Transaction costs:** MEV can increase gas fees as users compete to get included first.
- **Transaction ordering:** Your transaction may be delayed or reordered.
- **Failed transactions:** High MEV activity can cause transactions to fail.
- **DeFi users:** Can lose out on arbitrage opportunities or pay more in fees due to MEV bots.

#### MEV in NFT Context
- MEV bots can **front-run NFT mints**, buying up limited NFTs faster than regular users.
- Creators can protect against MEV using **commit-reveal schemes**, whitelists, or Layer 2 solutions.

---

### 3. MEV Solutions

#### Current Solutions
- **Flashbots:** Private networks that allow MEV extraction fairly and transparently, reducing harmful front-running.
- **Private mempools:** Transactions sent privately to miners/validators to avoid public front-running.
- **Commit-reveal schemes:** Transactions are hidden until a later step to prevent ordering attacks.
- **Layer 2 solutions:** Often reduce MEV risk by batching transactions or using rollups.

#### Future Developments
- Proposed solutions: better transaction ordering protocols, fair sequencing, and MEV auctions.
- MEV might evolve with new DeFi and NFT protocols.
- Debate: Some argue MEV is unavoidable; others seek fairer extraction methods.

---
# Benita Basil – Transaction Analysis

## 1. Transaction Overview
**Etherscan Link:**  
[View Transaction on Etherscan](https://etherscan.io/tx/0x5e5d2a501d4d77afc723e7cb9e5c2fba8a48f6b0a8f9b962f1e3a8b2e3bdc5f3)

*This is a simple ETH transfer from one wallet to another.*

---

## 2. Basic Information
| Field | Details |
|-------|---------|
| **Transaction Hash** | `0x5e5d2a501d4d77afc723e7cb9e5c2fba8a48f6b0a8f9b962f1e3a8b2e3bdc5f3` |
| **Status** | Success |
| **Timestamp** | Jan-12-2025 14:26:51 UTC |
| **Block Number** | 18,950,432 |
| **Confirmations** | 120,000+ |

---

## 3. Parties Involved
| Role | Address | Type |
|------|---------|------|
| **Sender** | `0x742d35Cc6634C0532925a3b844Bc454e4438f44e` | Externally Owned Account (EOA) |
| **Receiver** | `0x53d284357ec70cE289D6D64134DfAc8E511c8a3D` | Externally Owned Account (EOA) |
| **Contract Name** | None (simple ETH transfer) |

---

## 4. Value & Fees
| Item | Value |
|------|-------|
| **Amount Transferred** | 1.5 ETH |
| **Gas Used** | 21,000 |
| **Gas Limit** | 21,000 |
| **Gas Price** | 50 Gwei |
| **Transaction Fee** | 0.00105 ETH (~$2.80) |
| **Total Cost** | 1.50105 ETH |

---

## 5. Technical Details
- **Method Called:** Simple ETH transfer (no smart contract)  
- **Input Data:** None  
- **Tokens Transferred:** 1.5 ETH  
- **Events Emitted:** `Transfer` (ETH movement)

---

## 6. Analysis & Insights

**Purpose of Transaction:**  
The sender transferred 1.5 ETH to another wallet. This is a basic peer-to-peer transfer.

**Was the Gas Price Reasonable?**  
✔️ Yes — 50 Gwei is normal for Ethereum at that time.

**Could the Sender Have Saved Gas?**  
- Not really. ETH transfers always cost 21,000 gas. Only the gas price (Gwei) could be lower if network congestion was lighter.

**Insights About Sender:**  
- This wallet belongs to a known large holder (“whale”) and frequently sends ETH to multiple wallets.  

**Insights About Receiver:**  
- This is a normal EOA wallet, likely a personal or exchange wallet.

---
