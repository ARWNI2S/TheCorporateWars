---
icon: user-helmet-safety
cover: ../../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Economía Autosostenible

> **The Corporate Wars** es la primera simulación galáctica en tiempo real cuyo propio modelo económico es parte del gameplay, y está diseñado desde cero para sostenerse sin inversores, sin pre-minados, sin promesas futuras.

El diseño parte de la premisa: la infraestructura necesaria para cualquier juego en línea de calidad es, simplemente, cara y costosa de mantener.

Durante todo el ciclo de vida de un videojuego —salvo quizás en las fases iniciales de diseño y desarrollo básico— se generan gastos, que aumentan proporcionalmente al alcance del proyecto.

**The Corporate Wars** está diseñado como un ecosistema holístico autosuficiente, para poder realizar un desarrollo rápido y mantener su ciclo de vida durante años.

Esto implica que la economía del sistema —tanto en términos de funcionamiento interno del juego, como de operación técnica— debe ser capaz de financiarse a sí misma sin necesidad de métodos especulativos.

### Realidad Económica

Páginas web, servicios de identidad, bases de datos, en internet todo puede ser gratuito mientras _solo lo uses tú_, pero en el momento en el que necesitas _servir a usuarios_, por pocos que sean, las subscripciones gratuitas no son capaces de absorver ni una fracción del tráfico entrante, creando cuellos de botella y fallos de red.

Ademas los servidores de juego requiren de capacidad de respuesta con latencias minimas a (ojalá) miles de usuarios, que al mismo tiempo esperan un funcionamiento **perfecto** del sistema; lo que implica orquestación y replica para evitar caidas, hubs de redirección geografica y un incremento progresivo de servicios integrados al sistema.

Aunque se diseñen mecanismos de automatización con precisión, no existe un _metodo milagroso estandar_ que libere completamente a un sistema de mantenimiento y supervisión humano; administracion y soporte tecnico, seran necesarios para garantizar la calidad del servicio.

Finalmente, cada acción en la red Solana, desde desplegar un programa hasta almacenar el estado de un sistema planetario, incurre en costes: comisiones de red (_fees_) y depósitos de almacenamiento (_rent_).

### El '_Rent_' de las _Narices_.

A diferencia de otras blockchains donde los costes se asumen una vez al desplegar el programa, en Solana cada cuenta debe mantener una cantidad mínima de SOL como "depósito" (_rent_) proporcional a su tamaño, o será eliminada automáticamente de la red.

Si este depósito cubre el coste de 2 años de _rent_, la cuenta se considera _rent-exempt_ y no se elimina.

> Para cada cuenta en Solana —ya sea de usuario, de programa, PDA o cuenta de datos— hay que depositar el _rent_, proporcional al número de bytes ocupados.\
> Cuanto más grande sea el estado, mayor el depósito.

Tambien existe el _cierre_ de cuentas **controlado**, que permite recuperar el _rent_; aunque este mecanismo se tiene que implementar en cada programa de forma especifica.

Esto se vuelve especialmente relevante en un sistema como **The Corporate Wars**, donde pretendemos desplegar estructuras de información complejas: planetas, sectores, rutas comerciales, holdings corporativos...

El almacenamiento sin optimización puede llegar a costar 0.3 SOL por sistema estelar o más, volviendo inviable el escalado a un sector galáctico o una red de 11.000 mundos.

***

## Sostenibilidad económica real

El volumen de requisitos de mantenimiento y operación, no es ni mucho menos infinito, sino cuantificable y escalable: la actividad real de los usuarios determina las necesidades actuales del sistema.

Por otro lado, aunque el proceso de desarrollo espera apoyarse en 'colaboradores altruistas', la realidad es que siguiendo el modelo colaborativo no alcanzaremos ni la calidad ni el ritmo de progresos deseado.

> Muchos proyectos colaborativos han arrancado con fuerza, pero sus progresos son lentos, tardando en algunos casos más de una decada en el proceso de produccion.

La arquitectura financiera del proyecto se plantea como un modelo participativo, pensado para garantizar la autosostenibilidad técnica al margen de beneficios especulativos y garantías de inversión:

Toda entrada de **SOL** al sistema (participación de jugadores, donaciones, inversión externa, etc.) se canaliza hacia tesorerías programáticas y se considera parte de la simulacion, integrándose a la experiencia del juego.

Estas tesorerías financian:

- el mantenimiento de las cuentas activas ('_rent_'),
- las comisiones por uso de red del backend,
- los costes derivados de desarrollo y mantenimiento,
- y la operación general del sistema (infraestructura, cómputo, validación de datos, etc...).

Esta sostenibilidad no solo garantiza la continuidad técnica del sistema, sino que refuerza la premisa central de The Corporate Wars: un universo persistente, dinámico y auténticamente simulado.

***

## Economía y Jugabilidad

El diseño económico de *The Corporate Wars* no es un _método de financiación_, no es _p2e_, ni ningun constructo _crypto_: **es el propio sistema de juego**, que tiene en cuenta los costes operativos reales y que adopta la experiencia de usuario de los métodos de monetización habituales en los videojuegos, como una interfaz de aprovisionamiento.

Reconsideramos el concepto de _game marketplace_, integrándolo con la causalidad, persistencia y escala del universo de juego, donde se adquieren elementos integrados al _lore_ y a las mecánicas economicas participativas del sistema.

El modelo autosostenible no solo garantiza la viabilidad técnica del universo persistente, sino que **modula directamente la experiencia de juego**:

- La entrada masiva de jugadores o fondos provoca un aumento de liquidez: los **pools de financiación se expanden**, se activan nuevas cuentas, se despliegan programas latentes, y los sistemas estelares antes abandonados se reactivan.
  > Con el tiempo esto puede desencadenar una **bonanza galáctica**, acompañada de eventos visibles, mejores condiciones financieras en el juego, etc... 
- Por el contrario, si una facción pierde influencia, si un holding se retira o si se produce una fuga de _stakes_ de megacréditos, el sistema puede responder: recortando automáticamente _rent_ asignado, consolidando cuentas, o cancelando inactivos.
  > Este deterioro provoca una **contracción económica** visible desde el gameplay.

La situación económica global afecta al sistema con dinamicas efectivas a:

- A las decisiones estratégicas de los actores controlados por la IA (_Leatadaes_, _Instituciones_, _megacorporaciones_).
- Al poder adquisitivo de las divisas simuladas.
- A la **capacidad de expansión territorial o tecnológica**.
- Al acceso a servicios, licencias, o concesiones.
- Al valor relativo de los Tokens SPL del sistema.
 
El sistema reacciona con lógica interna: no hay magia, son hechos.

- Si nadie sostiene el _rent_ de una cuenta, se perderán los datos.
- Si una _Política_ retira sus _stakes_, perderá poder.
- Si una _Política_ se sobreexpone, puede quebrar.
- Si una _Política_ se queda sin fondos, colapsará.
- Si el conjunto colapsa, podemos caer en un escenario de _Larga Noche_.

Pero el sistema, aun sin recursos operativos, debería poder mantenerse jugable para los jugadores, desconectados del resto de la galaxia, sin acceso a rutas interestelares (servidores), hasta que una nueva _Lealtad_ emerja, unificando rutas y mundos en un sistema estructurado y... haga contacto.

Así, los jugadores no solo compiten por puntos, territorios o por continuidad narrativa, sino por **sostener un ecosistema vivo y frágil**, donde cada crédito, cada contrato y cada ciclo económico tiene un impacto real con consecuencias sistémicas.

***

> Bienvenido a la primera simulacion masiva en tiempo real de una economía interestelar programada sobre un modelo blockchain stateless autosostenible.
