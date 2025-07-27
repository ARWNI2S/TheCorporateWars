---
cover: ../../.gitbook/assets/tcw-stateless.jpg
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: full
  title:
    visible: false
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Blockchain Stateless

The choice of **Solana** as the technological foundation of **The Corporate Wars** is no coincidence: its architectural design solves key challenges for building a persistent, distributed, and temporally asymmetric universe.

Below, we outline the reasons, advantages, and challenges of this integration.

***

### Proof-of-History and Merkle Trees

Solana implements a **proof-of-history (PoH)** system, where each block and transaction is anchored to a verifiable temporal sequence. This enables the construction of **versioned states differentiated over time**, where each game update contains a `hash_root` acting as a unique timestamp.

Merkle trees allow these states to be compressed and validated efficiently, serving as a historical ledger of changes that can be audited and referenced at any point in the past.

***

### Stateless programs and derived keys

Unlike other ecosystems, Solana operates with **stateless programs** and storage based on derived keys.

This enables modeling of complex structures through implicit naming schemes.\
A main `key`, associated with a `foreign key`, defines data relationships **without the need for SQL or tables**.

Essentially, it's an active structural map where relationships are encoded in the key design itself, reducing dependence on traditional relational models.

***

### noNFTs and multilayer governance

Solana doesn’t follow an "ERC-style standard", but rather a **model of reusable programs** that opens up a still-uncharted technical territory.

Instead of adopting models like Metaplex’s pNFTs, **The Corporate Wars** implements its own system of contracts and ownership between parties.

Here, the so-called "noNFTs" are governance records within PDAs assigned to specific _Allegiances_, functioning similarly to **Associated Token Accounts (ATA)**, but designed to handle:

* complete, mutable, and auditable collections,
* transferable and exchangeable between actors,
* capable of representing dynamic in-game assets,
* while minimizing _rent_ deposits.

This approach surpasses the limitations of existing NFT standards in Solana, avoiding reliance on schemes that emulate ERC-XXX.

Instead, it leverages Solana’s flexibility as a reusable-program ecosystem to model relationships, governance, and dynamic structures within a persistent universe.

***

### What do we store on-chain?

Only what’s strictly necessary:

* the macro, structural, infrequently mutable, and global-scope data lives **on-chain**;
* the micro, player-specific, dynamic, seed-derivable and fast-to-interpret data lives **off-chain**.

The blockchain holds only **dehydrated and ultra-compressed data**; the backend keeps sessions alive, interpreting, hydrating, and caching in real-time.

Meanwhile, programs deployed on the Solana network natively handle queries, management, and administration, facilitating access for both client and backend.

***

## Problems it solves

Solana addresses challenges that would traditionally collapse large-scale non-SQL databases:

* Extremely high-grade security.
* Versioned ledger over time, ensuring traceability.
* Single source of truth: even if information is outdated, it’s correct at some point in time for **all players** (critical for maintaining coherence and strategic equality).
* Governance complexity: using native multisig, varied signer accounts, and `accounts` contexts, it’s possible to model everything from basic permissions to distributed decision systems.
