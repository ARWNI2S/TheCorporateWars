---
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Solana Services

Within the architecture of the distributed system, there is a dedicated layer responsible for interacting with the Solana network. Its purpose is to coordinate access to, transformation of, and synchronization with persistent data associated with the stellar simulation.

This layer, known as **Solana Services**, acts as a bridge between the simulation processes and the decentralized blockchain ecosystem.

One of the key concepts in this context is **latent simulation**: this refers to systems, entities, or events that do not need to be actively executed by the simulation engine, as they can be resolved algorithmically from their dehydrated state.

> This latent layer corresponds, in terms of level of detail, to what we might consider **LOD 0**.

***

Dehydrated data represents a compact, deterministic, and verifiable way to describe the state of a system without requiring it to be actively simulated.

Because this data can be dehydrated and rehydrated, entire regions of the simulation can be moved into a passive state without losing the ability to reconstruct them later.

The role of **Solana Services** is precisely to manage this hydration—dehydration cycle, operating periodically and selectively according to the required level of resolution.

This management includes:

* Identifying which stellar systems or regions of the universe must remain active in the distributed simulation (LOD > 0).
* Efficiently querying and storing persistent data via programs deployed on Solana.
* Dynamically rehydrating systems when they approach relevant events, points of interest, or the proximity of interactive actors.
* Dehydrating again those regions that can be resolved using latent logic, thus freeing up resources from the active simulation.

The function of this service layer is not to reimplement the on-chain logic, but to orchestrate its access from the simulation nodes, while respecting rules of consistency, periodicity, and network efficiency.

***

Thanks to this clear separation between active and latent simulation —and by leveraging Solana's decentralized capabilities— the system can scale massively without needing to keep the full complexity of the simulated universe in memory or in continuous execution.

{% hint style="success" %}
The Solana Services layer ensures that data is available, up to date, and synchronized at the precise moment it needs to come alive within the distributed simulation.
{% endhint %}
