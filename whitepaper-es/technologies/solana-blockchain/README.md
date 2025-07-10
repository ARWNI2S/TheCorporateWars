# La Blockchain Solana

La elecci�n de Solana como base tecnol�gica en The Corporate Wars no es casualidad: su dise�o arquitect�nico resuelve problemas clave para construir un universo persistente, distribuido y asim�trico en el tiempo.

A continuaci�n, detallamos los motivos, ventajas y desaf�os de esta integraci�n.

### Proof-of-History y Merkle Trees

Solana implementa un sistema de **proof-of-history (PoH)**, donde cada bloque y transacci�n queda anclado a una secuencia temporal verificable. Esto permite construir un **versionado de estados diferenciados en el tiempo**, donde cada update de juego contiene un `hash_root` correspondiente a su timestamp.

Los Merkle trees permiten comprimir y validar estos estados de forma eficiente, sirviendo como un ledger hist�rico de cambios que puede ser auditado y referenciado a cualquier momento pasado.

### Programas stateless y claves derivadas

A diferencia de otros ecosistemas, Solana opera con **programas stateless** y almacenamiento basado en claves derivadas.

Esto permite modelar estructuras complejas mediante nomenclaturas impl�citas:
- una `key` principal,
- asociada a una `foreign key`,
- define una relaci�n de datos **sin necesidad de SQL ni tablas**.

Es, en esencia, un mapa estructural vivo, donde las relaciones est�n codificadas en el dise�o de las claves, reduciendo dependencia de modelos relacionales cl�sicos.

### NFTs programables y gobernanza multicapa

Solana permite usar **NFTs programables**, que no se limitan a representar activos simples, sino que permiten construir:
- contratos personalizables entre partes,
- gobernanza multicapa condicional,
- e incluso modelar capas de legalidad e ilegalidad dentro del juego.

Este modelo supera al est�ndar `Metaplex` tipo ERC-XXX, que, aunque en su momento domin� el ecosistema, ha ca�do en desuso frente a modelos m�s avanzados y menos limitados por dise�o.

Solana no presenta un "ERC est�ndar" sino un **conjunto de programas reusables** y una infraestructura novedosa, todav�a poco explorada en cuanto a sus verdaderas posibilidades.

### �Qu� almacenamos on-chain?

Solo lo m�nimo necesario:
- lo macro, estructural, poco mutable y de alcance global, vive **on-chain**;
- lo micro, por jugador, din�mico, derivable desde seeds y de interpretaci�n r�pida, vive **off-chain**.

En resumen, la blockchain guarda **datos deshidratados y ultracomprimidos**, mientras que el backend mantiene las sesiones vivas, interpretando, hidratando y cacheando lo necesario en tiempo real.

## Problemas que resuelve

Solana resuelve desaf�os que tradicionalmente colapsar�an bases de datos no-SQL a gran escala:

* Seguridad de alt�simo grado.
* Ledger de versiones en el tiempo, garantizando trazabilidad.
* Fuente de verdad �nica: aunque la informaci�n est� desfasada, es correcta en alg�n punto temporal para **todos los jugadores** (clave para mantener coherencia e igualdad estrat�gica).
* Complejidad de gobernanza: usando multisig nativo, cuentas firmantes variadas, y contextos de `accounts`, es posible modelar desde simples permisos hasta sistemas de decisi�n distribuidos.

## Integraci�n pr�ctica con backend y cliente

Ejemplo pr�ctico:

La corporaci�n X tiene presencia en los mundos A, B, C y D.
- A aloja la sede.
- C y D tienen administradores activos.
- B tiene instalaciones, pero no observadores activos.

El entorno gr�fico (ej. Unreal Engine) muestra una perspectiva combinada de A, C y D, pero las �rdenes sobre B est�n limitadas:
- se pueden emitir,
- pero no ser�n efectivas hasta el pr�ximo �correo� o ciclo de sincronizaci�n.

As�, aunque se vea el precio �ptimo en E desde D, si se env�an cargueros desde A, habr� semanas de retraso; solo usando cargueros de D se logra una acci�n �instant�nea�. Adem�s, la orden debe emitirse desde D (con acceso directo a la informaci�n de E), aunque el transporte salga f�sicamente de A.

Esta es la complejidad real del comercio interestelar � y por eso recurrimos a blockchain:
porque el propio modelo de transacciones, con contexto, firmas y timestamps, refleja de forma nativa las restricciones y oportunidades del ecosistema.
