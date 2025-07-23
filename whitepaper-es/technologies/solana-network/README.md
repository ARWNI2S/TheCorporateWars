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

### Proof-of-History y Merkle Trees

Solana implementa un sistema de **proof-of-history (PoH)**, donde cada bloque y transacción queda anclado a una secuencia temporal verificable. Esto permite construir un **versionado de estados diferenciados en el tiempo**, donde cada actualización de juego contiene un `hash_root` que actúa como marca temporal única.

Los Merkle trees permiten comprimir y validar estos estados de forma eficiente, sirviendo como un ledger histórico de cambios que puede ser auditado y referenciado en cualquier momento pasado.

### Programas stateless y claves derivadas

A diferencia de otros ecosistemas, Solana opera con **programas stateless** y almacenamiento basado en claves derivadas.

Esto permite modelar estructuras complejas mediante nomenclaturas implícitas.\
Una `key` principal, asociada a una `foreign key`, define relaciones de datos **sin necesidad de SQL ni tablas**.

En esencia, se trata de un mapa estructural activo donde las relaciones están codificadas en el diseño de las claves, reduciendo la dependencia de modelos relacionales clásicos.

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

### ¿Qué almacenamos on-chain?

Solo lo mínimo necesario:

* lo macro, estructural, poco mutable y de alcance global, vive **on-chain**;
* lo micro, por jugador, dinámico, derivable desde semillas y de interpretación rápida, vive **off-chain**.

La blockchain guarda solo **datos deshidratados y ultracomprimidos**; el backend mantiene vivas las sesiones, interpretando, hidratando y cacheando en tiempo real.

Por su parte, los programas desplegados en la red Solana resuelven de forma nativa consultas, gestión y administración, facilitando el acceso tanto para cliente como para backend.

***

## Problemas que resuelve

Solana resuelve desafíos que tradicionalmente colapsarían bases de datos no-SQL a gran escala:

* Seguridad de altísimo grado.
* Ledger de versiones en el tiempo, garantizando trazabilidad.
* Fuente de verdad única: aunque la información esté desfasada, es correcta en algún punto temporal para **todos los jugadores** (clave para mantener coherencia e igualdad estratégica).
* Complejidad de gobernanza: usando multisig nativo, cuentas firmantes variadas y contextos de `accounts`, es posible modelar desde simples permisos hasta sistemas de decisión distribuidos.
