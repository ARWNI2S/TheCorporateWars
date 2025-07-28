---
cover: ../../../../.gitbook/assets/tcw-ru.jpg
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

# Resource Units

**Resource Units** (RU) are SPL tokens used within **The Corporate Wars** to represent the structural economic weight of worlds.

Each world has a specific number of RU assigned to it, reflecting its relative wealth within the economic model.

These units are not dynamically assigned — they are part of the structural configuration of the simulated universe.

Their distribution follows a zero-sum model: the total amount of RU in the system is constant and can only be redistributed —or transformed— as a result of internal events.

***

### Internal Value Reference

> **RUs are not intended to leave the system:** They are not designed to circulate among users or operate as a medium of exchange.

{% hint style="success" %}
They are directly linked to worlds and can only be _instrumentalized_ through the gameplay system.
{% endhint %}

While technically they are SPL tokens and could be transferred, the game design enforces strict restrictions: they are not traded, not transferred between players, and not used in markets.

{% hint style="danger" %}
**Warning**: RUs have no —and will not have— market liquidity.\
Any attempt to circulate them outside the system, list them on a DEX, or sell them as transferable assets should be considered a scam.\
Their appearance in external environments would indicate a security breach or unauthorized manipulation.
{% endhint %}

Within the system, RUs are used to model the flow of wealth, calculate the economic impact of political or commercial actions, and establish hierarchies among galactic regions based on structural importance.

Additionally, RUs are anchored to a concrete technical reality: **each unit is backed by SOL effectively deposited as&#x20;**_**rent**_**&#x20;during the deployment of the worlds and routes that support it.**

During [Historical Deployment](../../../../roadmap/deployment/) events, community contributions not only activate worlds and routes —they build the universe with a tangible economic foundation.

> **Each RU represents a fraction of that contribution, and its existence guarantees that, at the very least, this technical value is in place.**

The system recognizes this footprint as a real minimum backing and we do not allow RUs to be listed in markets because —in a strangely poetic way— they **represent the** _**SOL**_ **that keeps the entire galaxy lit.**

***

## Role in the Simulation

> RUs represent the structural weight of a world within the simulated universe.

They emerge directly from the in-game values of the world: an _Important_ world —by definition— links to main jump routes that generate _activity_.

That activity generates a data load —ATA, PDA, storage… in other words: _rent_— associated with that world, its jump routes, and its local _Allegiances_; requiring a greater amount of SOL to be deposited as _rent-exempt_ to maintain its existence.

That SOL, although not staked, remains immobilized on the network, and its existence —and _real value_— is used **within the system** to support the amount of RU assigned to the world.

This allows the system to define a minimum guaranteed **RU/SOL** ratio that serves as a reference standard across various gameplay systems and services.

It also allows the weight of entire regions to be evaluated, the structural impact of historical events to be measured, and processes like replication, scanning, migration, or degradation to be prioritized.

RUs act as the structural economic memory of the simulated universe, supporting both exploration and expansion —and collapse and contraction— enabling regional cycles of _Long Night_: if a world disconnects, its RU remains tied to its logical derivation (same PDA), ready to restore its state when it reemerges.

***

## Proportion and Distribution

> The total number of RUs is finite and determined by the deployed universe itself.

Distributing —or redistributing— RU requires **large-scale events**: the exploratory expansion of the Third Imperium —[Milieu 0](../../../../roadmap/deployment/first-survey/) and [Second Survey](../../../../roadmap/deployment/second-survey.md)— as laid out in the [Historical Deployment](../../../../roadmap/deployment/), exploration mechanics for unknown worlds via the **Third Survey**, the implementation of new content —patches or expansions— and high-level narrative mechanics —border wars, collapses, or regional reconstruction.

The available RUs exist in full: the number of RU issued is the maximum allowed by the Solana network.

`u64::MAX = 18,446,744,073,709,551,615` → total RU available across the galaxy.

Current estimates for stellar population in the Milky Way range between:

`100,000,000,000` and `400,000,000,000` stars.

This gives an average of:

$$
\frac{18,\!446,\!744,\!073,\!709,\!551,\!615\ RU}{400,\!000,\!000,\!000\ stars} \approx 46,\!116\ RU/star
$$

Assuming \~6.5 planets per star:

$$
\frac{46,\!116\ RU/star}{6.5\ planets/star} \approx 7,\!094\ RU/planet
$$

> **COINCIDENTALLY:** This is very close to the ‘relative maximums’ defined in Marc Miller’s Traveller™ —5th Edition.\
> —And yes, one way or another, all Traveller™ material has inspired each stage of **The Corporate Wars** design.

{% hint style="success" %}
This number of RU per planet ensures that each **world** —as a star system abstraction— in the galaxy holds enough RU —$$\approx 46,\!116\ RU/world$$— to support intensive exploitation at higher Tech Levels —Dyson spheres and orbital rings— without exceeding system limits.
{% endhint %}

***

### Real Distribution

> The calculations above represent system _limits_, not real figures the system will use.

The Charted Space of the year 1201 Imperial covers about `80,000` worlds spread across \~1,000 Sectors.

This gives an assignable RU reserve of:

$$
46,\!116\ RU/world \times 80,\!000\ worlds = 3,\!689,\!280,\!000\ RU_{assignable}
$$

Which is a tiny fraction of the total:

$$
\frac{3,\!689,\!280,\!000 RU_{assignable}}{18,\!446,\!744,\!073,\!709,\!551,\!615 RU_{max}} \times 100 \approx 0.00002\% \text{ from total}
$$

This reinforces the enormous scale of the unexplored galaxy and reflects the vast resources still available within the simulation and game universe.

Not all worlds will be fully charted, nor registered by a single _Institution_ or _Allegiance_, but all of them _exist_ in the simulation and —alongside their jump routes— are structural agents of the **zero-sum economic game**.

***

### RU “Mining”

Exploring the frontier of Charted Space implies discovering new worlds, establishing first contact with civilizations, and triggering other gameplay elements.

Internally, the system unfolds gameplay processes that consume MCr —directly or indirectly— to establish the **minimums required** to register a discovered world in the **Third Survey**.

This process reassigns SOL from the Treasury to _rent_ deposits needed to include the new world in the interstellar economy, based on the RU/SOL index, consuming MCr in the short term —exploration teams, fuel, beacons, privileged information— in exchange for structural rewards —land grants, licenses, reduced fees...— in the mid term.

These _rent_ deposits back the new world’s RU and are progressively applied as exploration progresses —allowing **competitive collaboration**.

Finally —after several explorations and contacts— the new world becomes integrated into interstellar society in proportion to its contributed RU:

Worlds with complex native civilizations require greater structural input —and provide greater gameplay— including new sophonts, minor _Allegiances_… fully justifying the cost —both real and simulated.

Conversely, uninhabited worlds with simpler extraction and future colonization potential require lower structural deployments —less _rent_, less RU.

This behavior emerges organically, naturally integrating RU “mining” with interstellar exploration and the thematic scenario of the **Third Survey**.
