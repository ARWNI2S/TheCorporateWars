---
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Governance Layers

Governance in **The Corporate Wars** is not a monolithic system, but a superposition of functional layers that reflect the complexity of political, economic, and operational power within the game universe.

In this model, each actor�whether an AI, a player-run corporation, or a transgalactic institution�exerts its agency within a defined regulatory framework, compatible with the rest of the system through a shared architecture based on the Solana network.

> From millennia-old empires to orbital communes, all levels of organization are structured across three main layers of governance: global, aggregate, and individual.

{% hint style="info" %}
These do not represent classical hierarchical steps, but rather dimensions of authority that operate simultaneously and define both the scope and the nature of each decision.
{% endhint %}

### The **Global Layer**

Establishes the foundations of the simulated universe.

It encompasses universal regulation: immutable physical laws, interstellar fiscal frameworks, sector synchronization, inflation control, access to finite resources, and route delimitation.

This layer is entirely controlled by the game�s AI and constitutes the invisible skeleton upon which the rest of the simulation is built.

It is not negotiable or manipulable, but it is observable, predictable, and usable by the most advanced players.

### The **Aggregate Governance Layer**

Encompasses all collective entities that exercise institutional, political, or doctrinal power over multiple actors.

> Allegiances such as the Third Imperium, the Two Thousand Worlds, or the Zhodani Consulate; institutions like ministries, fleets, or ancestral clans; alliances between corporations or ideological movements�all of these constitute aggregates.

Most of them are governed by AI, although they may be influenced from within through meritocratic structures or external pressure.

These aggregates shape and mediate the actions of individual entities, establishing doctrines, regulations, and access hierarchies for power, knowledge, or capital.

### The **Individual Layer**

Corresponds to the system�s core operational actors: planetary governments, corporations, cultures, religions, political parties, or any other form of autonomous organization.

These entities�controlled by players or AI�make local decisions, manage resources, declare conflicts, establish settlements, and define their own internal regulations.

They operate within the framework defined by the upper layers, but enjoy sufficient autonomy to craft singular strategies, develop unique doctrines, or even challenge the established order.

***

> This distributed model allows for a simulation that is rich, coherent, and strategically deep.
>
> Each layer contributes to the universe�s dynamics through a specific function: the global layer ensures systemic stability; the aggregates, cohesion and diversity; the individual, agency and conflict.

> This multilayered system allows rules and exceptions to be implemented in a coherent and traceable manner.
>
> Decisions are modeled through Solana-native structures such as multisig accounts, PDA records, and timestamp validation, ensuring integrity, transparency, and resistance to tampering.

***

## noNFT

{% hint style="success" %}
**noNFTs** represent the fundamental governance assets.
{% endhint %}

Unlike traditional NFTs�focused on individual ownership and commercial transferability�noNFTs in _The Corporate Wars_ function as **structural tokens linked to in-game governance entities** (_Polities_), with dynamic and auditable attributes.

A noNFT is neither an image nor a collectible: it is a **codified representation of power**, bound to a _Polity_ (corporation, government, clan, federation, etc.).

Each noNFT is stored in a **PDA derived from the governance program**, and its validity depends on:

* the public key of the _Polity_;
* the type of authority it represents (legislative, executive, operational, etc.);
* its date and context of issuance;
* its status within the legal framework (active, suspended, transferred, revoked, etc.).

At a technical level, noNFTs do not use Solana�s usual model, where each NFT requires its own individual mint (1:1).\
Instead, **the entire noNFT system relies on a single shared mint**, from which accounts are derived for each _Polity_.

These accounts�functionally similar to extended ATAs�store the associated noNFTs along with the minimal operational metadata required for validation and execution.

This enables, for example:

* delegating access rights to facilities;
* granting temporary exploitation licenses;
* establishing internal voting hierarchies for elections or reforms;
* validating interstellar contracts between _Polities_ without external oracles.

Technically, each noNFT behaves as a **programmable metadata account**, without depending on visual standards like traditional NFTs.

Its design leverages Solana�s architecture to ensure traceability, compression, and parallel execution of decisions, while eliminating the overhead associated with individual mint proliferation.

Furthermore, since they are not market-traded individual objects, noNFTs **cannot be speculated on or resold** outside the game, reinforcing their function as real governance instruments rather than volatile-value items.

Lastly, it is worth noting that multiple noNFTs can coexist within the same _Polity_, representing different roles or functions�from the executive board of a megacorporation to the local delegates of an autonomous enclave.

***

> This model allows decision-making, internal reforms, and legal conflicts to be resolved **within the game universe itself**, without external intervention or the need for parallel systems.

{% hint style="warning" %}
noNFTs, combined with the governance layers, make possible a rich, coherent, and believable simulation of a future ruled by humans, aliens... and protocols.
{% endhint %}
