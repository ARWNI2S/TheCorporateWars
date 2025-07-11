# Solana Blockchain

The choice of Solana as the technological foundation in The Corporate Wars is no coincidence: its architectural design solves key challenges in building a persistent, distributed, and temporally asymmetric universe.

Below, we detail the reasons, advantages, and challenges of this integration.

### Proof-of-History and Merkle Trees

Solana implements a **proof-of-history (PoH)** system, where each block and transaction is anchored to a verifiable temporal sequence. This enables the construction of a **versioned state system across time**, where each game update contains a `hash_root` corresponding to its timestamp.

Merkle trees allow these states to be compressed and validated efficiently, serving as a historical ledger of changes that can be audited and referenced at any past moment.

### Stateless programs and derived keys

Unlike other ecosystems, Solana operates with **stateless programs** and storage based on derived keys.

This allows for modeling complex structures through implicit naming:

* a primary `key`,
* associated with a `foreign key`,
* defines a data relationship **without the need for SQL or tables**.

In essence, it creates a live structural map, where relationships are encoded in the key design, reducing dependency on traditional relational models.

### Programmable NFTs and multilayer governance

Solana enables the use of **programmable NFTs** that go beyond simple assets, allowing for the construction of:

* customizable contracts between parties,
* conditional multilayer governance,
* and even the modeling of legality and illegality layers within the game.

This model surpasses the `Metaplex` ERC-XXX-like standard, which once dominated the ecosystem but has fallen out of favor in light of more advanced and less design-limited models.

Solana does not offer a "fixed ERC standard" but rather a **set of reusable programs** and a novel infrastructure, still largely unexplored in terms of its full potential.

### What do we store on-chain?

Only what's strictly necessary:

* Macro, structural, slow-changing, globally relevant data lives **on-chain**;
* Micro, per-player, dynamic, seed-derived, and fast-interpreted data lives **off-chain**.

In summary, the blockchain stores **ultracompressed, dehydrated data**, while the backend maintains live sessions, interpreting, hydrating, and caching what's needed in real time.

## Problems it solves

Solana addresses challenges that would traditionally overwhelm large-scale non-SQL databases:

* Very high-grade security.
* Time-versioned ledger, ensuring traceability.
* Single source of truth: even though information is delayed, it is correct at some point in time for **all players** (key to maintaining coherence and strategic fairness).
* Governance complexity: using native multisig, varied signing accounts, and `account` contexts, it�s possible to model everything from simple permissions to distributed decision systems.

## Practical integration with backend and client

{% hint style="info" %}
The megacorporation **Helion Dynamics** operates in the systems **Ergo (Massilia.Keum.0414)**, **Abarre (Massilia.Keum.0415)**, **Shigi (Massilia.Keum.0314)**, and **Uson (Massilia.Keum.0616)**.

* **Ergo:** central administrative and financial headquarters.
* **Abarre** and **Shigi:** industrial colonies with local administrators.
* **Uson:** critical trade hub with high traffic but no resident Helion Dynamics administrator.
{% endhint %}

In the game's graphical environment, the player sees a combined perspective of the data available from Ergo, Abarre, and Shigi. Orders can be issued to Uson, but with key limitations:

* Orders toward **Uson** are recorded but not **effective** until the next "mail run" (interstellar update synchronized via blockchain).
* From **Abarre**, analysts detect an oversupply of Lanthanum at low prices in **Makinen (Massilia.Keum.0719)**.
* The player decides to send freighters:
  * If departing from **Abarre**, the action is immediate because the information is locally available.
  * If attempting to mobilize freighters from **Ergo**, they must account for:
    * transit latency,
    * and the fact that the order, while valid, relies on data Ergo knows only through delayed updates.

This is where blockchain becomes essential:

* Authorization to execute orders depends on context, timestamp, and the instantaneous snapshot of visible data.
* The game backend hydrates only the information valid per node and game session, maintaining:
  * coherence,
  * traceability,
  * and fair play.

The result: even though the galactic map shows an integrated whole, strategic decisions critically depend on:

* which worlds have real-time data and which do not,
* which routes are optimized for information flow,
* and what logistical capacities each enclave has.

{% hint style="success" %}
This reflects the real complexity of interstellar trade —and that's why we turn to blockchain: because its native properties inherently solve latency, signature, consensus, and traceability constraints.
{% endhint %}
