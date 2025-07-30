---
cover: ../.gitbook/assets/tcw-roadmap.jpg
coverY: 0
---

# Hoja de Ruta

El desarrollo de **The Corporate Wars** sigue una hoja de ruta centrada en la integración progresiva y ortogonal de sistemas complejos que conforman el núcleo de la experiencia de juego.

### Prioridades

La prioridad es desplegar un prototipo funcional del **tercer censo**, que servirá como controlador principal de una base de datos basada en derivación de direcciones de mundos y rutas.

Esta estructura soporta tanto al [Modelo de Información Desfasada](../technologies/solana-network/outdated-information-model.md) como a las [Capas de Gobernanza](../technologies/solana-network/multilayer-governance.md), los actores principales del sistema.

- Esta primera etapa permitirá validar los flujos de información y las interacciones de gobernanza.

### Desarrollo

El siguiente paso lógico es integrar estos sistemas con los procesos de backend, lo cual requiere una arquitectura ortogonal por etapas.

Los nodos de [Simulación Distribuida](../technologies/backend-server/distributed-simulation.md) ejecutan contextos por sesión basados en [AI LOD](../technologies/backend-server/ai-lod.md), que toma como origen de datos un conjunto de [Servicios Solana](../technologies/backend-server/solana-rpc.md).

- El desarrollo de estos sistemas no es una etapa, sino un proceso acumulativo de implementación de servicios y subsistemas.

Los principios fundamentales para el diseño de la simulación y sus interacciones quedan determinados por la teoría de [sistemas complejos](https://es.wikipedia.org/wiki/Sistema_complejo) y la [Economía Autosostenible](technologies/solana-network/sustainable-economy/README.md), basada en [Estabilización Algorítmica](technologies/solana-network/sustainable-economy/hayek-money.md).

A partir de esta base sólida, el proyecto avanzará en la incorporación gradual de sistemas de juego:

- Visualización 3D del mapa del Espacio Conocido, con LOD de alta densidad y level streaming dinámico.
- Superdetallado de superficies planetarias e instalaciones.
- Sistemas de diseño de productos en general, arquitectura naval, fabricación, I+D.
- Modos de edición para interiores.
- Personajes y control.
- Autoridad y gobernanza.

Y otros tantos sistemas clave que completarán la experiencia de juego, con especial atención a la interacción estratégica, la construcción de infraestructuras y el control de rutas comerciales.

La integración del cliente sobre Unreal Engine 5 permitirá escalar la complejidad visual y táctica del gameplay, mientras los sistemas de backend gestionan la persistencia y las transacciones de forma transparente para el jugador.

Cada sistema añadido será funcional y completo por sí mismo, evitando dependencias parciales y facilitando el ajuste iterativo sobre mecánicas y balance.

## Despliegue

**The Corporate Wars** presenta dos entornos de despliegue bien diferenciados: la Red Solana y el backend distribuido.

El backend se encuentra desplegado permanentemente, mantenido por los desarrolladores. Las máquinas virtuales permiten escalar vertical y horizontalmente según las necesidades y carga del sistema.

El despliegue en la red Solana pasará por etapas de testeo en devnet antes de su implementación en mainnet beta.

Tanto la simulación distribuida como los servicios de la red Solana están alineados con la economía autosostenible desde el principio, pues es la base fundamental de todo el sistema de juego.

El despliegue público del gameplay se realizará una vez que la economía, la gobernanza y las primeras interacciones estratégicas estén plenamente operativas y equilibradas.

Desde ese momento, **The Corporate Wars** evolucionará como un universo vivo donde la competencia por el control económico, político y territorial será el motor principal de la experiencia.

La expansión posterior incorporará nuevas capas de complejidad y posibilidades emergentes, manteniendo siempre la coherencia y solidez del sistema sobre el que se sostiene la guerra corporativa interestelar.
