---
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# The Outdated Information Model

In an Empire of over eleven thousand worlds, where jump ships are the arteries connecting scattered civilizations, information **never** arrives instantly.

No matter how advanced the technology, no civilization of the Third Imperium —nor any other _Allegiance_— has found a way to overcome a fundamental law of Charted Space:

> **Information cannot travel faster than light.**

Interstellar communications depend on physical couriers: messengers, freighters, probes, diplomatic ships. Dispatches, stock quotes, military reports, and even local news cross the jump corridors encapsulated in physical units, subject to the same constraints as any cargo.

This introduces **structural latencies**:

- A message from the Core Sector to the edge of the Imperium may take weeks or months.
- Decisions are made based on outdated data.
- Opportunities and threats may have vanished by the time the information arrives.

The outdated information model is not a system failure: **it is the system**. It defines strategy, constrains logistics, and shapes the social, political, and economic fabric of the galaxy. In **The Corporate Wars**, this model is not a flavor detail: it is the backbone of the technical design supporting the persistent ecosystem.

{% hint style="info" %}
Below we explain how we’ve integrated this asynchrony at the heart of the game, using distributed technologies (like the Solana blockchain) to reflect a universe where perfect synchronization is impossible.
{% endhint %}

***

## Structural Latency

In **The Corporate Wars**, interstellar information does not flow in real time or globally. The universe is structured as a **directed latency graph**, where each node represents a star system, and each edge (transit route) introduces a specific delay determined by the physical constraints of interstellar travel.

Each route A → B implies intrinsic latency. Although global transactions are recorded on-chain, each node can only perceive and operate with **deltas applied to its own local state**, within its visibility window:

- Deltas are stored in time-ordered sequence: $$(T, T-1, T-2, ..., T-N)$$.
- Node A has access to changes from B only up to version $$(T-t_{route})$$, where $$t_{route}$$ is the route delay.
- Later changes remain invisible until data "arrives" physically via the transit routes.

Thus, A’s perception of B is always outdated and depends on:

- the cumulative delay from available routes,
- the update frequency,
- and the logistical capacity to transport data across the graph.

***

## Technical Challenges

Implementing an outdated information model in a distributed, blockchain-supported universe (Solana) introduces real engineering challenges — not just gameplay concerns, but deep system-level problems:

- **Efficient storage and crawling of differential versions:** nodes must access only the deltas relevant to their window $$(T-t_{route})$$, avoiding full-chain scans.\
  This requires performant algorithms to filter, index, and serve partial versions at scale.
- **Asymmetric bidirectionality of the graph:** routes A → B are not always time- or capacity-symmetric with B → A. This causes divergent update and latency paths, dynamically affecting topology and visible snapshot calculations.
- **Context-based access limitation:** while data is public on-chain, it must only be decrypted and exposed to the backend based on player permissions, context, and position. This demands granular encryption and key management beyond the on-chain layer.
- **Efficient reuse of PDAs across multiple systems:** PDA accounts serve not just players, but also secondary systems like the Interstellar Stock Exchange (ISE) and multilayer governance. This requires well-designed data pipelines serving multiple domains without inconsistency or overload.
- **Scalability of programs in Solana:** programs handling aggregation, filtering, and data delivery must scale across tens of thousands of players and nodes, managing SOL costs, throughput limits, and minimal latencies.
- **Soft synchronization of local nodes:** with no instant global state, local nodes need reconciliation and eventual correction mechanisms to prevent error accumulation or long-term state divergence.

These challenges are neither trivial nor theoretical: they define how a system like **The Corporate Wars** can grow and operate at real scale.

***

## Model Advantages

This approach is not just a technical solution: it’s a foundational pillar offering unique design and gameplay benefits.

- **Reinforces strategic asymmetry:** players with better routes or logistical control access key data faster.
- **Introduces uncertainty:** recent events are not visible everywhere, forcing decisions based on probability, not certainty.
- **Enables emergent gameplay layers:** from information manipulation to data couriers and update brokers.
- **Connects systems:** route and world PDAs are not isolated data, but directly fuel ISE instruments and multilayer governance dynamics.
- **Ensures fair play security:** although blockchain data is public, only the authorized backend can decrypt and expose information players are entitled to, preventing leaks, data mining, or abuse.

In short, the outdated information model is not just a game mechanic: it’s a deeply interconnected design strengthening narrative coherence, technical integrity, and the richness of a persistent ecosystem.
