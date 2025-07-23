---
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Servicios Solana

Dentro de la arquitectura del sistema distribuido, existe una capa espec�fica de interacci�n con la red Solana cuya funci�n es coordinar el acceso, la transformaci�n y la sincronizaci�n de datos persistentes asociados a la simulaci�n estelar.

Esta capa, que denominamos **Servicios Solana**, act�a como puente entre los procesos de simulaci�n y el ecosistema descentralizado de la blockchain.

Uno de los conceptos clave en este entorno es el de **simulaci�n latente**: se refiere a todos aquellos sistemas, entidades o eventos que no requieren ser ejecutados activamente en el motor de simulaci�n, sino que pueden resolverse de forma puramente algor�tmica a partir de su estado deshidratado.

Esta capa latente corresponde, en t�rminos de nivel de detalle, a lo que podr�amos considerar un **LOD 0**.

***

Los datos deshidratados representan una forma compacta, determinista y verificable de describir el estado de un sistema sin necesidad de mantenerlo activamente simulado.

Al ser deshidratables y rehidratables, estos datos permiten trasladar regiones completas de la simulaci�n a un estado pasivo sin perder la capacidad de reconstrucci�n posterior.

El papel de los **Servicios Solana** es precisamente gestionar este ciclo de hidrataci�n y deshidrataci�n, operando de forma peri�dica y selectiva seg�n la necesidad de resoluci�n.

Esta gesti�n incluye:

- Identificar qu� sistemas estelares o regiones del universo deben mantenerse activas en la simulaci�n distribuida (LOD > 0).
- Consultar y almacenar de forma eficiente los datos persistentes en programas desplegados sobre Solana.
- Rehidratar din�micamente los sistemas cuando se acercan a eventos relevantes, zonas de inter�s o proximidad de actores interactivos.
- Deshidratar de nuevo aquellas regiones que puedan resolverse mediante l�gica latente, liberando recursos de simulaci�n activa.

La funci�n de esta capa de servicios, por tanto, no es reimplementar la l�gica on-chain, sino orquestar su acceso desde los nodos de simulaci�n, respetando las reglas de consistencia, periodicidad y eficiencia de red.

Gracias a esta divisi�n clara entre simulaci�n activa y simulaci�n latente, y al aprovechamiento de las capacidades descentralizadas de Solana, el sistema puede escalar a gran escala sin necesidad de mantener toda la complejidad del universo simulado en memoria o ejecuci�n continua.

La capa de Servicios Solana garantiza que los datos est�n disponibles, actualizados y sincronizados en el momento en que deban cobrar vida dentro de la simulaci�n distribuida.
