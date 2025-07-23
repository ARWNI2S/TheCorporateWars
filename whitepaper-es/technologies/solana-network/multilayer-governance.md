---
icon: pencil
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Capas de Governanza

La gobernanza en **The Corporate Wars** no es un sistema monolítico, sino una superposición de capas funcionales que reflejan la complejidad del poder político, económico y operativo en el universo de juego.

En este modelo, cada actor —ya sea una IA, una corporación dirigida por jugadores o una institución transgaláctica— ejerce su agencia dentro de un marco normativo determinado, compatible con el resto del sistema mediante una arquitectura común basada en la red Solana.

Desde imperios milenarios hasta comunas orbitales, todos los niveles de organización se articulan sobre tres grandes capas de gobernanza: global, agregada e individual.

Estas no representan escalones jerárquicos clásicos, sino dimensiones de autoridad que operan de forma simultánea y que definen el alcance y la naturaleza de cada decisión.

La **Capa Global** establece los fundamentos del universo simulado.

Abarca la normativa universal: leyes físicas inmutables, marcos fiscales interestelares, sincronización temporal entre sectores, control de inflación, acceso a recursos finitos o delimitación de rutas.

Esta capa está enteramente bajo control de la IA del juego, y constituye el esqueleto invisible sobre el que se construye el resto de la simulación.

No es negociable ni manipulable, pero sí observable, predecible y utilizable por los jugadores más avanzados.

La **Capa de Agregados de Gobernanza** engloba a todas aquellas entidades colectivas que representan poder institucional, político o doctrinal sobre múltiples actores.

Lealtades como el Tercer Imperio, los Dos Mil Mundos o el Consulado Zhodani; instituciones como ministerios, flotas o clanes ancestrales; alianzas entre corporaciones o movimientos ideológicos transversales: todos ellos constituyen agregados.

En su mayoría, son gobernados por la IA, aunque pueden ser influenciados desde dentro a través de estructuras meritocráticas o por presión externa.

Los agregados modulan y median la acción de las entidades individuales, estableciendo doctrinas, regulaciones y jerarquías de acceso al poder, al conocimiento o al capital.

La **Capa Individual** corresponde a los actores operativos básicos del sistema: gobiernos planetarios, corporaciones, culturas, religiones, partidos o cualquier otra forma de organización autónoma.

Estas entidades —controladas por jugadores o por la IA— toman decisiones locales, gestionan recursos, declaran conflictos, fundan asentamientos y definen sus propias regulaciones internas.

Actúan dentro del marco definido por las capas superiores, pero gozan de suficiente margen para construir estrategias singulares, desarrollar doctrinas únicas o incluso desafiar el orden establecido.

Este modelo distribuido permite una simulación rica, coherente y estratégicamente profunda.

Cada capa contribuye a la dinámica del universo desde una función específica: la global garantiza estabilidad sistémica; los agregados, cohesión y diversidad; lo individual, agencia y conflicto.

Este sistema multicapa permite implementar reglas y excepciones de forma coherente y trazable.

Las decisiones se modelan mediante estructuras nativas de Solana como cuentas firmantes múltiples (multisig), registros en PDA y validación por timestamp, lo que garantiza integridad, transparencia y resistencia a manipulaciones.

## noNFT

Los **noNFTs** representan los activos de gobernanza fundamentales.

A diferencia de los NFTs tradicionales —centrados en la propiedad individual y la transferibilidad comercial—, los noNFTs en *The Corporate Wars* actúan como **tokens estructurales ligados a entidades de gobernanza en el juego** (_Políticas_), con atributos dinámicos y auditables.

Un noNFT no es una imagen ni un coleccionable: es una **representación codificada de poder**, vinculada a una _Política_ (corporación, gobierno, clan, federación, etc.).

Cada uno se almacena en una **PDA derivada del programa de gobernanza**, y su validez depende de:

- la clave pública de la _Política_;
- el tipo de autoridad que representa (legislativa, ejecutiva, operativa, etc.);
- la fecha y el contexto de emisión;
- su estado dentro del marco legal (activo, suspendido, transferido, revocado, etc.).

A nivel técnico, los noNFTs no utilizan el modelo habitual de Solana donde cada NFT requiere su propio mint individual (1:1).

En su lugar, **todo el sistema de noNFTs se apoya en un único mint común**, del cual se derivan las cuentas asociadas a cada *Política*.

Estas cuentas —análogas a una ATA extendida— almacenan los noNFTs correspondientes junto con los metadatos operativos mínimos necesarios para su validación y uso.

Esto permite, por ejemplo:

- delegar permisos de uso de instalaciones;
- conceder licencias de explotación temporales;
- establecer jerarquías de voto interno para elecciones o reformas;
- validar contratos interestelares entre _Políticas_ sin necesidad de oráculos externos.

Técnicamente, cada noNFT se comporta como una **cuenta de metadatos programática**, sin depender de estándares visuales como los NFT tradicionales.

Su diseño aprovecha la arquitectura de Solana para garantizar trazabilidad, compresión y ejecución paralela de decisiones.

Además, al no tratarse de objetos individuales con mercado abierto, los noNFTs **no pueden ser especulados ni revendidos** fuera del juego, lo que refuerza su función como instrumento de gobernanza real, y no como ítem de valor volátil.

Por último, cabe destacar que múltiples noNFTs pueden coexistir dentro de una misma _Política_, reflejando distintas funciones o roles: desde el consejo directivo de una megacorporación hasta los delegados locales de un enclave autónomo.

***

Este modelo permite que la toma de decisiones, las reformas internas y los conflictos legales se resuelvan **dentro del propio universo del juego**, sin intervención externa ni necesidad de sistemas paralelos.

Los noNFTs, en combinación con las capas de gobernanza, hacen posible una simulación rica, coherente y verosímil de un futuro gobernado por humanos, alienígenas... y protocolos.

