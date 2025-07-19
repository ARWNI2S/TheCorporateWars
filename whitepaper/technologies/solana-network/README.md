---
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Stateless Blockchain

The choice of Solana as the technological foundation of **The Corporate Wars** is no coincidence: its architectural design addresses key challenges in building a persistent, distributed, and temporally asymmetric universe.

Below, we outline the reasons, advantages, and challenges of this integration.

### Proof-of-History and Merkle Trees

Solana implements a **proof-of-history (PoH)** system, where each block and transaction is anchored to a verifiable temporal sequence. This enables the construction of **time-differentiated state versioning**, where each game update contains a `hash_root` corresponding to its timestamp.

Merkle trees allow these states to be efficiently compressed and validated, serving as a historical ledger of changes that can be audited and referenced at any past point.

### Stateless programs and derived keys

Unlike other ecosystems, Solana operates with **stateless programs** and storage based on derived keys.

This enables the modeling of complex structures through implicit naming.  
A main `key`, associated with a `foreign key`, defines data relationships **without the need for SQL or tables**.

It is, in essence, a living structural map, where relationships are encoded in key design, reducing dependence on classic relational models.

### noNFTs and multilayer governance

Solana does not offer an "ERC standard" but rather a **set of reusable programs** that opens a technical territory still largely unexplored.

Instead of adopting models like Metaplex's pNFTs, **The Corporate Wars** implements its own system of contracts and ownership between parties.

Here, the so-called "noNFTs" are records in PDAs assigned to governance _polities_, functioning similarly to **Associated Token Accounts (ATA)**, but designed to handle:

* complete, mutable, and audited collections,
* transferable and exchangeable between actors,
* with the capacity to represent dynamic in-game assets,
* while minimizing '_rent_' deposits.

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

***

## Practical integration with backend and client

{% hint style="info" %}
The megacorporation **Helion Dynamics** operates in the systems **Ergo (Massilia.Keum.0414)**, **Abarre (Massilia.Keum.0415)**, **Shigi (Massilia.Keum.0314)**, and **Uson (Massilia.Keum.0616)**.

* **Ergo:** central administrative and financial headquarters.
* **Abarre** and **Shigi:** industrial colonies with local administrators.
* **Uson:** critical commercial hub with high traffic but no resident Helion Dynamics administrator.
{% endhint %}

In the game’s graphical environment, the player sees a combined perspective of data available from Ergo, Abarre, and Shigi. Orders toward Uson can be issued, but with key limitations:

* Orders to **Uson** are registered but not **effective** until the next “mail run” (interstellar update synchronized via blockchain).
* From **Abarre**, analysts detect an oversupply of lanthanum at low prices in **Makinen (Massilia.Keum.0719)**.
* The player decides to send freighters:
  * If departing from **Abarre**, the action is immediate since the information is locally available.
  * If attempting to move freighters from **Ergo**, they must account for:
    * transit latency,
    * and that the order, while valid, relies on data Ergo knows only through delayed updates.

This is where the blockchain becomes essential:

* Authorization to execute orders depends on context, timestamp, and visible data snapshot.
* The game’s backend hydrates only the valid information per node and game session, maintaining:
  * coherence,
  * traceability,
  * and fair play.

The result: although the galactic map displays an integrated whole, strategic decisions depend on:

* which worlds have real-time data and which do not,
* which routes are optimized to the flow of information,
* and what logistical capacities each enclave has.

{% hint style="success" %}
This reproduces the real complexity of interstellar trade — and that is why we turn to blockchain: its inherent properties natively resolve latency, signature, consensus, and traceability constraints.
{% endhint %}
