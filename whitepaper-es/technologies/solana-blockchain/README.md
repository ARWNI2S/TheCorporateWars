# La Blockchain Solana

La elección de Solana como base tecnológica en The Corporate Wars no es casualidad: su diseño arquitectónico resuelve problemas clave para construir un universo persistente, distribuido y asimétrico en el tiempo.

A continuación, detallamos los motivos, ventajas y desafíos de esta integración.

### Proof-of-History y Merkle Trees

Solana implementa un sistema de **proof-of-history (PoH)**, donde cada bloque y transacción queda anclado a una secuencia temporal verificable. Esto permite construir un **versionado de estados diferenciados en el tiempo**, donde cada actualización de juego contiene un `hash_root` correspondiente a su marca de tiempo.

Los Merkle trees permiten comprimir y validar estos estados de forma eficiente, sirviendo como un ledger histórico de cambios que puede ser auditado y referenciado a cualquier momento pasado.

### Programas stateless y claves derivadas

A diferencia de otros ecosistemas, Solana opera con **programas stateless** y almacenamiento basado en claves derivadas.

Esto permite modelar estructuras complejas mediante nomenclaturas implícitas:

* una `key` principal,
* asociada a una `foreign key`,
* define una relación de datos **sin necesidad de SQL ni tablas**.

Es, en esencia, un mapa estructural vivo, donde las relaciones están codificadas en el diseño de las claves, reduciendo dependencia de modelos relacionales clásicos.

### NFTs programables y gobernanza multicapa

Solana permite usar **NFTs programables**, que no se limitan a representar activos simples, sino que permiten construir:

* contratos personalizables entre partes,
* gobernanza multicapa condicional,
* e incluso modelar capas de legalidad e ilegalidad dentro del juego.

Este modelo supera al estándar `Metaplex` tipo ERC-XXX, que, aunque en su momento dominó el ecosistema, ha caído en desuso frente a modelos más avanzados y menos limitados por diseño.

Solana no presenta un "ERC estándar" sino un **conjunto de programas reusables** y una infraestructura novedosa, todavía poco explorada en cuanto a sus verdaderas posibilidades.

### ¿Qué almacenamos on-chain?

Solo lo mínimo necesario:

* lo macro, estructural, poco mutable y de alcance global, vive **on-chain**;
* lo micro, por jugador, dinámico, derivable desde seeds y de interpretación rápida, vive **off-chain**.

En resumen, la blockchain guarda **datos deshidratados y ultracomprimidos**, mientras que el backend mantiene las sesiones vivas, interpretando, hidratando y cacheando lo necesario en tiempo real.

## Problemas que resuelve

Solana resuelve desafíos que tradicionalmente colapsarían bases de datos no-SQL a gran escala:

* Seguridad de altísimo grado.
* Ledger de versiones en el tiempo, garantizando trazabilidad.
* Fuente de verdad única: aunque la información está desfasada, es correcta en algún punto temporal para **todos los jugadores** (clave para mantener coherencia e igualdad estratégica).
* Complejidad de gobernanza: usando multisig nativo, cuentas firmantes variadas, y contextos de `accounts`, es posible modelar desde simples permisos hasta sistemas de decisión distribuidos.

## Integración práctica con backend y cliente

{% hint style="info" %}
La megacorporación **Helion Dynamics** opera en los sistemas **Ergo (Massilia.Keum.0414)**, **Abarre (Massilia.Keum.0415)**, **Shigi (Massilia.Keum.0314)** y **Uson (Massilia.Keum.0616)**.

* **Ergo:** sede central administrativa y financiera.
* **Abarre** y **Shigi:** colonias industriales con administradores locales.
* **Uson:** hub comercial crítico con alto tráfico pero sin administrador residente de Helion Dynamics.
{% endhint %}

En el entorno gráfico del juego, el jugador ve una perspectiva combinada de los datos disponibles desde Ergo, Abarre y Shigi. Las órdenes hacia Uson pueden emitirse, pero con limitaciones clave:

* Las órdenes hacia **Uson** se registran pero no son **efectivas** hasta que llegue el próximo “correo” (actualización interestelar sincronizado vía blockchain).
* Desde **Abarre**, los analistas detectan que en **Makinen (Massilia.Keum.0719)** hay una sobreoferta de Lantano a precio bajo.
* El jugador decide enviar cargueros:
  * Si parte de **Abarre**, la acción es inmediata porque la información está disponible localmente.
  * Si intenta mover cargueros desde **Ergo**, debe asumir:
    * la latencia del trayecto,
    * y que la orden, aunque válida, depende de datos que Ergo conoce solo por actualizaciones retrasadas.

Aquí es donde la blockchain es esencial:

* La autorización para ejecutar ordenes depende contexto, maca de tiempo, e instantanea de datos visibles.
* El backend del juego hidrata solo la información válida por nodo y sesión de juego, manteniendo:
  * coherencia,
  * trazabilidad,
  * y fair play.

El resultado: aunque el mapa galáctico muestre un todo integrado, las decisiones estratégicas dependen de:

* qué mundos tienen datos en tiempo real, y cuales no,
* qué rutas están optimizadas al flujo de información,
* y qué capacidades logísticas tiene cada enclave.

{% hint style="success" %}
Esto reproduce la complejidad real del comercio interestelar — y por eso recurrimos a blockchain, porque sus propias propiedades resuelven de forma nativa restricciones de latencia, firmas, consenso y trazabilidad.
{% endhint %}
