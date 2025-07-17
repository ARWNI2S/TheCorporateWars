# The Outdated Information Model

In an Imperium of over eleven thousand worlds, where jump ships are the arteries connecting scattered civilizations, information **never** arrives instantly.

No matter how advanced the technology, no civilization of the Third Imperium — nor any known faction — has found a way to overcome one fundamental law of the known universe:

> **Information cannot travel faster than light.**

Interstellar communications rely on physical couriers: messengers, freighters, probes, diplomatic vessels. Dispatches, stock prices, military reports, and even simple local news traverse the jump corridors encapsulated in physical units, subject to the same limitations as any material cargo.

This introduces **structural latencies**:

* A message from the Core sector to the margins of the Imperium can take weeks or months.
* Decisions are made based on outdated data.
* Opportunities and threats may have already vanished by the time the information arrives.

The outdated information model is not a system flaw: **it is the system**. It defines strategies, conditions logistics, and shapes the very social, polítical, and economic fabric of the galaxy. And in _**The Corporate Wars**_, this model is not just flavor — it is the backbone of the technical design that sustains the persistent ecosystem.

{% hint style="info" %}
Below, we explain how we have integrated this asynchrony at the heart of the game, using distributed technologies (like the Solana blockchain) to reflect a universe where absolute synchronization is unattainable.
{% endhint %}

***

## Structural latency

In **The Corporate Wars**, interstellar information does not flow in real-time nor globally. The universe is structured as a **directed latency graph**, where each node represents a star system, and each edge (transit route) introduces a concrete delay determined by the physical limitations of interstellar travel.

Each route A → B implies an intrinsic latency. Although global transactions are registered on blockchain, each node can only perceive and operate with the blocks corresponding to its visibility window:

* The blockchain stores transactions ordered over time (T, T-1, T-2, ..., T-N).
* Node A only has access to B’s transactions up to block **T-(n)**, where **n** represents the route delay.
* Subsequent blocks remain invisible until the physical data “arrives” via transit routes.

Thus, A's perception of B is always outdated and depends on:

* the accumulated delay of available routes,
* the update rhythm,
* and the logistical capacity to transport data through the graph.

***

## Technical challenges

Implementing an outdated information model in a distributed universe backed by blockchain (Solana) introduces real technical challenges that go far beyond gameplay mechanics — they are deep engineering hurdles:

* **Efficient storage and crawling of historical blocks:** nodes must access only the blocks relevant to their temporal window (T-(n)), avoiding full-chain traversal. This requires efficient algorithms to filter, index, and serve historical data at massive scale.
* **Asymmetric bidirectionality in the graph:** routes A → B are not always symmetric in time or capacity with B → A. This generates divergent update paths and latencies that must be modeled dynamically, affecting both topology and snapshot calculations.
* **Contextual access limitation:** although data is publicly available on blockchain, it must only be decrypted and exposed by the backend according to each player’s permissions, context, and node position. This demands an additional layer of granular encryption and key management beyond the on-chain layer.
* **Efficient reuse of PDA across systems:** dynamic asynchronous perceptions (PDA) not only serve players but also feed secondary systems like the Interstellar Stock Exchange (ISE) and multilayer governance. This requires designing data pipelines that serve multiple domains without inconsistencies or overload.
* **Scalability of Solana programs:** the smart contracts handling data aggregation, filtering, and delivery must scale in an environment with tens of thousands of players and nodes, respecting computational costs (gas), throughput limits, and minimum latencies.
* **Soft synchronization of local nodes:** since no global instant state exists, local nodes need reconciliation and eventual correction mechanisms to avoid cumulative errors or prolonged state drift.

These challenges are neither trivial nor theoretical — they are present-day limitations that define how a system like **The Corporate Wars** can grow and operate at real-world scale.

***

## Model advantages

This approach is not just a technical solution — it is a pillar that brings distinctive advantages in terms of design and experience.

* **Strengthens authentic strategic asymmetry:** not all players access the same data at the same time; those who manage their routes and logistical networks better gain real advantages.
* **Introduces tactical uncertainty:** decisions are made based on partial, outdated information, creating an ecosystem where risk and interpretation are central.
* **Enables deep emergent gameplay:** the model allows phenomena such as information manipulation, data brokers, update corridors, and parallel intelligence markets.
* **Connects systems:** route and world PDAs are not isolated data points — they directly feed financial instruments (ISE) and multilayer governance dynamics, multiplying their relevance.
* **Fair game security:** although data is on-chain and publicly accessible, only the authorized backend can decrypt and expose the information each player is entitled to, preventing leaks, unauthorized data mining, or abuse.

In summary, the outdated information model is not just a gameplay mechanic — it is a deeply interconnected design that reinforces narrative coherence, technical integrity, and the richness of the persistent ecosystem.
