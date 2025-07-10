# La Blockchain Solana

La elección de Solana como base tecnológica en The Corporate Wars no es casualidad: su diseño arquitectónico resuelve problemas clave para construir un universo persistente, distribuido y asimétrico en el tiempo.

A continuación, detallamos los motivos, ventajas y desafíos de esta integración.

### Proof-of-History y Merkle Trees

Solana implementa un sistema de **proof-of-history (PoH)**, donde cada bloque y transacción queda anclado a una secuencia temporal verificable. Esto permite construir un **versionado de estados diferenciados en el tiempo**, donde cada update de juego contiene un `hash_root` correspondiente a su timestamp.

Los Merkle trees permiten comprimir y validar estos estados de forma eficiente, sirviendo como un ledger histórico de cambios que puede ser auditado y referenciado a cualquier momento pasado.

### Programas stateless y claves derivadas

A diferencia de otros ecosistemas, Solana opera con **programas stateless** y almacenamiento basado en claves derivadas.

Esto permite modelar estructuras complejas mediante nomenclaturas implícitas:
- una `key` principal,
- asociada a una `foreign key`,
- define una relación de datos **sin necesidad de SQL ni tablas**.

Es, en esencia, un mapa estructural vivo, donde las relaciones están codificadas en el diseño de las claves, reduciendo dependencia de modelos relacionales clásicos.

### NFTs programables y gobernanza multicapa

Solana permite usar **NFTs programables**, que no se limitan a representar activos simples, sino que permiten construir:
- contratos personalizables entre partes,
- gobernanza multicapa condicional,
- e incluso modelar capas de legalidad e ilegalidad dentro del juego.

Este modelo supera al estándar `Metaplex` tipo ERC-XXX, que, aunque en su momento dominó el ecosistema, ha caído en desuso frente a modelos más avanzados y menos limitados por diseño.

Solana no presenta un "ERC estándar" sino un **conjunto de programas reusables** y una infraestructura novedosa, todavía poco explorada en cuanto a sus verdaderas posibilidades.

### ¿Qué almacenamos on-chain?

Solo lo mínimo necesario:
- lo macro, estructural, poco mutable y de alcance global, vive **on-chain**;
- lo micro, por jugador, dinámico, derivable desde seeds y de interpretación rápida, vive **off-chain**.

En resumen, la blockchain guarda **datos deshidratados y ultracomprimidos**, mientras que el backend mantiene las sesiones vivas, interpretando, hidratando y cacheando lo necesario en tiempo real.

## Problemas que resuelve

Solana resuelve desafíos que tradicionalmente colapsarían bases de datos no-SQL a gran escala:

* Seguridad de altísimo grado.
* Ledger de versiones en el tiempo, garantizando trazabilidad.
* Fuente de verdad única: aunque la información esté desfasada, es correcta en algún punto temporal para **todos los jugadores** (clave para mantener coherencia e igualdad estratégica).
* Complejidad de gobernanza: usando multisig nativo, cuentas firmantes variadas, y contextos de `accounts`, es posible modelar desde simples permisos hasta sistemas de decisión distribuidos.

## Integración práctica con backend y cliente

Ejemplo práctico:

La corporación X tiene presencia en los mundos A, B, C y D.
- A aloja la sede.
- C y D tienen administradores activos.
- B tiene instalaciones, pero no observadores activos.

El entorno gráfico (ej. Unreal Engine) muestra una perspectiva combinada de A, C y D, pero las órdenes sobre B están limitadas:
- se pueden emitir,
- pero no serán efectivas hasta el próximo “correo” o ciclo de sincronización.

Así, aunque se vea el precio óptimo en E desde D, si se envían cargueros desde A, habrá semanas de retraso; solo usando cargueros de D se logra una acción “instantánea”. Además, la orden debe emitirse desde D (con acceso directo a la información de E), aunque el transporte salga físicamente de A.

Esta es la complejidad real del comercio interestelar — y por eso recurrimos a blockchain:
porque el propio modelo de transacciones, con contexto, firmas y timestamps, refleja de forma nativa las restricciones y oportunidades del ecosistema.
