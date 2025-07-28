---
cover: ../../.gitbook/assets/tcw-stateless.jpg
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

# Blockchain Stateless

La elección de **Solana** como base tecnológica en **The Corporate Wars** no es casualidad: su diseño arquitectónico resuelve problemas clave para construir un universo persistente, distribuido y asimétrico en el tiempo.

A continuación, detallamos los motivos, ventajas y desafíos de esta integración.

***

### Proof-of-History y Merkle Trees

Solana implementa un sistema de **proof-of-history (PoH)**, donde cada bloque y transacción queda anclado a una secuencia temporal verificable. Esto permite construir un **versionado de estados diferenciados en el tiempo**, donde cada actualización de juego contiene un `hash_root` que actúa como marca temporal única.

Los Merkle trees permiten comprimir y validar estos estados de forma eficiente, sirviendo como un ledger histórico de cambios que puede ser auditado y referenciado en cualquier momento pasado.

En esto se apoya el [modelo de información desfasada](outdated-information-model.md).

***

### Programas stateless y claves derivadas

A diferencia de otros ecosistemas, Solana opera con **programas stateless** y almacenamiento basado en claves derivadas.

Esto permite modelar estructuras complejas mediante nomenclaturas implícitas: una `key` principal, asociada a una `foreign key` derivada, define relaciones de datos **sin necesidad de SQL ni tablas**.

En esencia, se trata de un mapa estructural activo donde las relaciones están codificadas en el diseño de las claves, reduciendo la dependencia de modelos relacionales clásicos.

***

### noNFTs y gobernanza multicapa

Solana no presenta un "estándar ERC", sino un **modelo de programas reusables** que abren un territorio técnico aún poco explorado.

En lugar de adoptar modelos como los pNFT de Metaplex, **The Corporate Wars** implementa un sistema propio de contratos y propiedades entre partes.

Aquí, los llamados "noNFTs" son registros de gobernanza en PDAs asignadas a las _Políticas_, funcionando de manera similar a las **Associated Token Accounts (ATA)**, pero diseñados para manejar:

* colecciones completas, mutables y auditadas,
* transferibles e intercambiables entre actores,
* con capacidad de representar activos dinámicos dentro del juego,
* y minimizando los depósitos en _rent_.

Este enfoque supera las limitaciones de los estándares NFT existentes en Solana, evitando depender de esquemas que imitan ERC-XXX.

En su lugar, aprovechamos la flexibilidad de Solana como ecosistema de programas reusables para modelar relaciones, gobernanza y estructuras dinámicas dentro de un universo persistente.

{% hint style="warning" %}
**¿Qué problema hay con los pNFT y los NFT "normales" de Solana?**

Los **pNFT** (y los NFT tradicionales) no son desarrollados directamente por Solana Labs ni forman parte del **SPL oficial**: son una iniciativa de **Metaplex**, una fundación independiente que controla el sistema de NFT en Solana.

Aunque Solana es un entorno completamente distinto, Metaplex intenta replicar la experiencia de Ethereum: se ha forzado un modelo **incompatible con la filosofía de cuentas ligeras y ejecutables** de Solana, intentando emular ERC-721.

Se ha priorizado el ecosistema visual/comercial (_NFT-as-asset_) en lugar de diseñar **un token no fungible nativo y eficiente para la red Solana**. De hecho, **Token-2022** ofrece mecanismos superiores, pero no se integran completamente con los pNFT.

**En 2025 existe integración parcial, pero no es eficaz ni canónica para Solana como red.**

Metaplex ha adaptado los pNFT a Token-2022 **desde fuera hacia dentro**, mientras que una solución verdaderamente eficiente para juegos o simuladores requeriría:

* usar directamente `spl-token-2022`,
* diseñar lógica sobre extensiones como `TransferHook`, `MintCloseAuthority`, etc.,
* evitar capas externas como `mpl-token-metadata`.
{% endhint %}

***

### ¿Qué almacenamos on-chain?

La blockchain guarda solo **datos deshidratados y ultracomprimidos**; el backend mantiene vivas las sesiones, interpretando, hidratando y cacheando en tiempo real.

Por su parte, los programas desplegados en la red Solana resuelven de forma nativa consultas, gestión y administración, facilitando el acceso tanto para cliente como para backend.

{% hint style="success" %}
Lo macro, estructural, poco mutable y de alcance global, vive **on-chain**;
{% endhint %}

{% hint style="danger" %}
Lo micro, por jugador, dinámico, derivable desde semillas y de interpretación rápida, vive **off-chain**.
{% endhint %}

***

## Problemas que resuelve

Solana resuelve desafíos que colapsarían muchas arquitecturas no-SQL a gran escala:

* **Seguridad de altísimo grado:** gracias al modelo de firmas y cuentas programáticas, cada operación está verificada criptográficamente.
* **Ledger temporal:** todas las transacciones quedan registradas con precisión histórica, permitiendo trazabilidad completa y versiones válidas en el tiempo.
* **Fuente de verdad única:** aunque cada jugador perciba un estado diferente (por latencia), todos comparten una base común e inmutable. Esto asegura coherencia y equilibrio estratégico.
* **Modelado de gobernanza distribuida:** usando firmas múltiples (`multisig`), cuentas autorizadas y validaciones en `accounts`, se pueden implementar desde permisos simples hasta sistemas complejos de toma de decisiones.
*   **Coste radicalmente inferior:**\
    Comparado con servicios en la nube, almacenar y replicar datos en Solana es mucho más barato a largo plazo:

    * Una base de datos cloud con replicación, disponibilidad y rendimiento _equivalentes_ cuesta **300–500 €/mes**, solo en infraestructura.
    * Si además quieres capa de ejecución (triggers, validación, lógica de negocio), el coste sube, o te limitas a bases como MySQL, NoSQL, Tables, sin ejecución activa.
    * A gran escala (ej. 100.000 mundos simulados), el coste por almacenamiento y cómputo se vuelve crítico: pagas por mega, por CPU, por IOPS.
    * En Solana, aunque el _rent_ inicial no es trivial, **se paga una vez**: no hay pagos mensuales continuos.

    Para un juego con un ciclo de vida de 10 años, los costes en la nube rondarían entre **62.000 € y 144.000 €** como mínimo, sin contar la complejidad operativa ni los límites técnicos.

**Solana permite construir estructuras de almacenamiento con relaciones complejas, persistentes y verificables, sin depender de infraestructura externa ni modelos propietarios.**
