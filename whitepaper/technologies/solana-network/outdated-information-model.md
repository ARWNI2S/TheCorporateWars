---
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# The Outdated Information Model

In an Imperium of over eleven thousand worlds, where jump ships serve as arteries connecting scattered civilizations, information **never** arrives instantly.

No matter how advanced the technology, no civilization within the Third Imperium —or any other _Allegiance_— has found a way to overcome a fundamental law of the known universe:

> **Information cannot travel faster than light.**

Interstellar communications rely on physical emissaries: messengers, freighters, probes, diplomatic vessels. Dispatches, stock prices, military reports, and even local news travel through jump corridors encapsulated in physical units, subject to the same limitations as any other type of cargo.

This introduces **structural latency**:

- A message from the Core sector to the outer fringes of the Imperium may take weeks or months.
- Decisions are made based on outdated data.
- Opportunities and threats may have already disappeared by the time information arrives.

The outdated information model is not a system flaw: **it is the system**. It defines strategies, constrains logistics, and shapes the social, political, and economic fabric of the galaxy. In _**The Corporate Wars**_, this model is not just flavor — it is the backbone of the technical design that supports the persistent ecosystem.

{% hint style="info" %}
What follows is an explanation of how this asynchrony is integrated into the heart of the game, using distributed technologies (such as the Solana blockchain) to simulate a universe where absolute synchronization is unattainable.
{% endhint %}

***

## Structural latency

In **The Corporate Wars**, interstellar information does not flow in real time or in a global fashion. The universe is structured as a **directed latency graph**, where each node represents a star system and each edge (transit route) introduces a specific delay determined by the physical limitations of interstellar travel.

Each route A → B implies intrinsic latency. While global transactions are recorded on the blockchain, each node can only perceive and operate with the **differential changes applied to its own local state**, according to its visibility window:

- Differences are stored in chronological order: $$(T, T-1, T-2, ..., T-N)$$.
- Node A has access to differences from B only up to version $$(T - t_{route})$$, where $$t_{route}$$ represents the route's delay.
- Later changes remain invisible until the physical data "arrives" via transit routes.

Thus, A’s perception of B is always outdated and depends on:

- the accumulated delay of available routes,
- the update frequency,
- and the logistical capacity to transport data through the graph.

***

## Technical challenges

Implementing an outdated information model in a distributed universe supported by blockchain (Solana) presents real technical challenges. These are not just gameplay mechanics — they are problems of deep systems engineering:

- **Efficient storage and crawling of differential versions:** Nodes must access only the relevant deltas within their temporal window $$(T - t_{route})$$, without traversing the entire chain.\
  This requires efficient algorithms to filter, index, and serve partial versions at large scale.
- **Asymmetric bidirectionality of the graph:** Routes A → B are not always symmetric in time or capacity compared to B → A. This generates diverging update and latency paths that must be modeled dynamically, affecting both topology and visible snapshot computation.
- **Contextual access limitation:** While data is public on-chain, it must only be decrypted and exposed to the backend based on permissions, context, and player position. This demands an additional layer of granular encryption and key management, not handled solely on-chain.
- **Efficient reuse of PDAs across multiple systems:** PDA accounts are not only used by the player but also serve secondary systems like the Interstellar Stock Exchange (ISE) and multilayered governance. This requires designing data pipelines that can support multiple domains without inconsistency or overload.
- **Solana program scalability:** The programs responsible for aggregation, filtering, and data delivery must scale across an environment with tens of thousands of players and nodes, while respecting compute budgets (SOL), throughput limits, and latency constraints.
- **Soft synchronization of local nodes:** Since no instant global state exists, local nodes require reconciliation and eventual correction mechanisms to avoid error accumulation or prolonged drift from baseline.

These challenges are neither trivial nor theoretical — they are active constraints that define how a system like **The Corporate Wars** can grow and operate at real scale.

***

## Model advantages

This approach is not just a technical solution: it is a foundation that brings unique advantages at both design and gameplay levels.

- **Reinforces strategic asymmetry:** those with better routes or logistical control gain earlier access to key data.
- **Introduces uncertainty:** not all recent events are visible across all nodes, forcing decisions based on probability, not certainty.
- **Enables emergent gameplay layers:** from information manipulation to data couriers and update brokers.
- **Connects systems:** PDAs for routes and worlds are not isolated — they directly power instruments like the ISE and the multilayered governance dynamics.
- **Fair game security:** although blockchain data is publicly accessible, only authorized backends can decrypt and expose information each player is entitled to, preventing leaks, external data mining, or abuse.

In short, the outdated information model is not just a game mechanic: it is a deeply interwoven design that strengthens narrative coherence, technical integrity, and the richness of the persistent ecosystem.
