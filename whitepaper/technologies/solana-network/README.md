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

# Stateless Blockchain

The choice of **Solana** as the technological foundation of **The Corporate Wars** is no coincidence: its architectural design solves key challenges for building a persistent, distributed, and temporally asymmetric universe.

Below, we outline the reasons, advantages, and challenges of this integration.

***

### Proof-of-History and Merkle Trees

Solana implements a **proof-of-history (PoH)** system, where each block and transaction is anchored to a verifiable temporal sequence. This enables the construction of **versioned states differentiated over time**, where each game update contains a `hash_root` acting as a unique timestamp.

Merkle trees allow these states to be compressed and validated efficiently, serving as a historical ledger of changes that can be audited and referenced at any point in the past.

This is the backbone of the [outdated information model](outdated-information-model.md).

***

### Stateless programs and derived keys

Unlike other ecosystems, Solana operates with **stateless programs** and storage based on derived keys.

This enables modeling of complex structures through implicit naming schemes: a main `key`, associated with a derived `foreign key`, defines data relationships **without the need for SQL or tables**.

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

This approach surpasses the limitations of existing NFT standards in Solana, avoiding reliance on schemes that emulate ERC-XXX .

Instead, it leverages Solana’s flexibility as a reusable-program ecosystem to model relationships, governance, and dynamic structures within a persistent universe.

{% hint style="warning" %}
#### What’s the problem with pNFTs and “normal” NFTs on Solana?

**pNFTs** (and traditional NFTs) are not developed directly by Solana Labs nor are they part of the **official SPL**: they are an initiative by **Metaplex**, an independent foundation that controls the NFT system on Solana.

Although Solana is a fundamentally different environment, Metaplex tries to replicate the Ethereum experience: it has forced a model **incompatible with Solana’s philosophy of lightweight and executable accounts**, attempting to emulate ERC-721.

The visual/commercial ecosystem (_NFT-as-asset_) has been prioritized instead of designing **a truly native and efficient non-fungible token standard for the Solana network**. In fact, **Token-2022** offers superior mechanisms, but it is not fully integrated with pNFTs.

**As of 2025, integration is partial — but it remains neither efficient nor canonical for Solana.**

Metaplex has adapted pNFTs to Token-2022 **from the outside in**, whereas a truly efficient solution for games or simulations would require:

* using `spl-token-2022` directly,
* designing logic around extensions like `TransferHook`, `MintCloseAuthority`, etc.,
* avoiding external layers like `mpl-token-metadata`.
{% endhint %}

***

### What do we store on-chain?

The blockchain holds only **dehydrated and ultra-compressed data**; the backend keeps sessions alive, interpreting, hydrating, and caching in real-time.

Meanwhile, programs deployed on the Solana network natively handle queries, management, and administration, facilitating access for both client and backend.

{% hint style="success" %}
The macro, structural, infrequently mutable, and global-scope data lives **on-chain**;
{% endhint %}

{% hint style="danger" %}
The micro, player-specific, dynamic, seed-derivable and fast-to-interpret data lives **off-chain**.
{% endhint %}

***

## Problems It Solves

Solana addresses challenges that would overwhelm many large-scale no-SQL architectures:

- **High-grade security:** thanks to the signature model and programmatic accounts, every operation is cryptographically verified.
- **Temporal ledger:** all transactions are recorded with historical precision, allowing full traceability and valid state versions over time.
- **Single source of truth:** even if each player perceives a different state (due to latency), all share a common, immutable foundation. This ensures coherence and strategic fairness.
- **Distributed governance modeling:** using multisignature (`multisig`), authorized signer accounts, and validations through `accounts`, it’s possible to implement everything from simple permissions to complex decision-making systems.
- **Radically lower cost:**  
  Compared to cloud services, storing and replicating data on Solana is significantly cheaper in the long run:
  
  - A cloud database with _equivalent_ replication, availability, and performance costs **€300–500/month** in infrastructure alone.
  - If you need an execution layer (triggers, validation, business logic), costs increase — or you're limited to systems like MySQL, NoSQL, or Tables, with no active logic.
  - At scale (e.g. simulating 100,000 worlds), storage and compute costs become critical: you pay per megabyte, per CPU, per IOPS.
  - In Solana, although the initial _rent_ isn't trivial, **you pay once** — there are no ongoing monthly costs.
  
  For a game with a 10-year lifecycle, cloud costs would range from **€62,000 to €144,000**, not including operational complexity or technical ceilings.

**Solana enables the construction of complex, persistent, and verifiable simulations — without relying on external infrastructure or proprietary models.**
