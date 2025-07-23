---
icon: pencil
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Custom Services

Despite employing AAA-grade game engines and cloud platforms, it is important to note that no system is immediately ready for use with the specific behavior required.

While these technologies support the integration of multiple layers of components, structuring services as independent programs is not efficient, as it introduces redundancy and performance overhead.

***

The appropriate strategy is to design an architecture compatible with the underlying infrastructure. In our case, this consists of a game server based on distributed nodes, executing a likewise distributed simulation system. The system’s load balancing adjusts dynamically according to the required level of detail, which in turn depends on the number of active users.

This approach enables the operation of large-scale, complex virtual worlds, while maintaining system load proportional to user activity rather than the absolute size of the simulated environment.

These technologies, although experimental, have been developed over several years by the NI2S project and are now set to be tested in a real-world environment.