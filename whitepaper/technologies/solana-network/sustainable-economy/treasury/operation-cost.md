---
cover: ../../../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Operational Costs

The operating cost represents the set of resources required for **The Corporate Wars** to function continuously, both in its deployment on the Solana network and in the technical infrastructure that supports it off-chain.

At the _blockchain level_, it includes maintaining active accounts and programs, paying _rent_ proportional to state size, and the _fees_ for each operation executed, whether by players or internal system processes.

But beyond the Solana network, the system requires a permanent technical base: cloud servers, databases, auxiliary storage, authentication services, web servers, APIs, event processing, orchestration tools, monitoring, security, backups, and more.

{% hint style="success" %}
Without this operational layer, the universe would not be accessible, stable, or functional.
{% endhint %}

***

### Economic Reality

> Websites, identity services, databases —everything can be free as long as _you're the only user_, but once you need to _serve users_, even a few, free subscriptions can't handle a fraction of the incoming traffic, creating bottlenecks and network failures.

Game servers require low-latency responsiveness for thousands of users —hopefully— who expect **perfect** system operation. This implies orchestration and replication to prevent downtime, geographic redirection hubs, and a progressive increase in services integrated into the system.

Even with precise automation mechanisms, there is no _standard miracle method_ that completely frees a system from human maintenance and oversight; administration and technical support will be necessary to guarantee service quality.

Therefore, a real AAA system also requires a real human team, who should be gratefully compensated for their invaluable contributions and services.

***

### The '_Damn Rent_'

Unlike other blockchains where costs are paid once at deployment, in Solana each account must maintain a minimum amount of SOL as a —deposit— (_rent_) proportional to its size, or it will be automatically deleted from the network.

If the deposit covers 2 years of _rent_, the account is considered _rent-exempt_ and is not removed.

> For each account on Solana —whether user, program, PDA, or data account— rent must be deposited, proportional to the number of occupied bytes.\
> The larger the state, the higher the deposit.

{% hint style="success" %}
There is also **controlled** account _closure_, which allows recovering the _rent_; but this mechanism must be implemented in each program explicitly.
{% endhint %}

This becomes especially relevant in a system like **The Corporate Wars**, where we intend to deploy complex information structures: planets, sectors, trade routes, corporate holdings...

{% hint style="danger" %}
Unoptimized storage can cost 0.3 SOL per star system or more, making scaling to a galactic sector or a network of 11,000 worlds unfeasible without a solid deployment plan.
{% endhint %}

***

All these elements have a real and sustained cost, which must be regularly covered.

The Treasury is designed to continuously support this structural expense, channeling part of the received funds into infrastructure maintenance and general operations.

> If the universe keeps running when no one is playing, it's because there's a real system keeping it on.

***

### Simulated Recession

In _Long Night_ scenarios, whether total or partial, disconnected planetary systems stop operating actively: the PDAs associated with those worlds can be **closed in a controlled manner**, recovering the corresponding _rent_ and freeing technical resources.

This capacity for economic and technical retreat allows the universe to **degrade without collapsing**: abandoned routes shut down, systems fall silent, and only traces remain in the _lore_ and the block history.

When a new _Allegiance_ regains control or a region is reactivated, the same worlds and routes can be recreated from the same PDA derivation, restoring their logical and narrative identity even if the previous state was dismantled.

> This mechanism allows the **structural memory of the universe** to persist even when the data has been wiped:\
> **same key, new cycle —another milieu.**
