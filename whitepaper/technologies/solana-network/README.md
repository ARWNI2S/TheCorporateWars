---
icon: user-helmet-safety
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

# Stateless Blockchain

The choice of Solana as the technological foundation of **The Corporate Wars** is no coincidence: its architectural design addresses key challenges in building a persistent, distributed, and temporally asymmetric universe.

Below, we outline the reasons, advantages, and challenges of this integration.

### Proof-of-History and Merkle Trees

Solana implements a **proof-of-history (PoH)** system, where each block and transaction is anchored to a verifiable temporal sequence. This enables the construction of **state versioning** _differentiated_ by time, where each game update contains a `hash_root` corresponding to its timestamp.

Merkle trees allow these states to be efficiently compressed and validated, serving as a historical ledger of changes that can be audited and referenced at any past point.

### Stateless programs and derived keys

Unlike other ecosystems, Solana operates with **stateless programs** and storage based on derived keys.

This enables the modeling of complex structures through implicit naming.\
A main `key`, associated with a `foreign key`, defines data relationships **without the need for SQL or tables**.

It is, in essence, an active structural map, where relationships are encoded in key design, reducing dependence on classic relational models.

### noNFTs and multilayer governance

Solana does not offer an "ERC standard" but rather a **model of reusable programs** that opens a technical territory still largely unexplored.

Instead of adopting models like Metaplex's pNFTs, **The Corporate Wars** implements its own system of contracts and shared assets between parties.

Here, the so-called "noNFTs" are governance records in PDAs assigned to _Polities_, functioning similarly to **Associated Token Accounts (ATA)**, but designed to handle:

* complete, mutable, and audited collections,
* transferable and exchangeable between actors,
* with the capacity to represent dynamic in-game assets,
* with minimal _rent_ overhead.

This approach surpasses the limitations of existing NFT standards on Solana, avoiding reliance on schemes that mimic ERC-XXX.

Instead, we leverage Solana’s flexibility as an ecosystem of reusable programs to model relationships, governance, and dynamic structures within a persistent universe.

### What do we store on-chain?

Only what is strictly necessary:

* macro-level, structural, low-mutability, global-scope data lives **on-chain**;
* micro-level, per-player, dynamic data, derivable from seeds and fast to interpret, lives **off-chain**.

The blockchain stores only **dehydrated and ultracompressed data**; the backend keeps sessions alive, interpreting, hydrating, and caching in real time.

Meanwhile, the programs deployed on the Solana network natively handle queries, management, and administration, facilitating access for both client and backend.

***

## Problems it solves

Solana addresses challenges that would traditionally overwhelm large-scale NoSQL databases:

* Extremely high-level security.
* Time-versioned ledgers ensuring traceability.
* A single source of truth: even if information is delayed, it remains correct at some temporal point for **all players** (key to maintaining strategic coherence and fairness).
* Governance complexity: using native multisig, varied signing accounts, and `account` contexts, it is possible to model everything from simple permissions to distributed decision systems.
