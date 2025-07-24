---
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Servicios Solana

Dentro de la arquitectura del sistema distribuido, existe una capa específica de interacción con la red Solana cuya función es coordinar el acceso, la transformación y la sincronización de datos persistentes asociados a la simulación estelar.

Esta capa, que denominamos **Servicios Solana**, actúa como puente entre los procesos de simulación y el ecosistema descentralizado de la blockchain.

Uno de los conceptos clave en este entorno es el de **simulación latente**: se refiere a todos aquellos sistemas, entidades o eventos que no requieren ser ejecutados activamente en el motor de simulación, sino que pueden resolverse de forma puramente algorítmica a partir de su estado deshidratado.

> Esta capa latente corresponde, en términos de nivel de detalle, a lo que podríamos considerar un [**LOD 0**](ai-lod.md#ai-lod-en-la-simulacion-distribuida).

***

Los datos deshidratados representan una forma compacta, determinista y verificable de describir el estado de un sistema sin necesidad de mantenerlo activamente simulado.

Al ser deshidratables y rehidratables, estos datos permiten trasladar regiones completas de la simulación a un estado pasivo sin perder la capacidad de reconstrucción posterior.

El papel de los **Servicios Solana** es precisamente gestionar este ciclo de hidratación y deshidratación, operando de forma periódica y selectiva según la necesidad de resolución.

Esta gestión incluye:

* Identificar qué sistemas estelares o regiones del universo deben mantenerse activas en la [simulación distribuida](distributed-simulation.md) (LOD > 0).
* Consultar y almacenar de forma eficiente los datos persistentes en programas desplegados sobre Solana.
* Rehidratar dinámicamente los sistemas cuando se acercan a eventos relevantes, zonas de interés o proximidad de actores interactivos.
* Deshidratar de nuevo aquellas regiones que puedan resolverse mediante lógica latente, liberando recursos de simulación activa.

La función de esta capa de servicios, por tanto, no es re-implementar la lógica on-chain, sino orquestar su acceso desde los nodos de simulación, respetando las reglas de consistencia, periodicidad y eficiencia de red.

***

Gracias a esta división clara entre simulación activa y simulación latente, y al aprovechamiento de las capacidades descentralizadas de Solana, el sistema puede escalar a gran escala sin necesidad de mantener toda la complejidad del universo simulado en memoria o ejecución continua.

{% hint style="success" %}
La capa de Servicios Solana garantiza que los datos estén disponibles, actualizados y sincronizados en el momento en que deban cobrar vida dentro de la simulación distribuida.
{% endhint %}
