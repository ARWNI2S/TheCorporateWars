---
icon: user-helmet-safety
cover: ../../../../.gitbook/assets/tcw-ru.jpg
coverY: 0
---

# Unidades de Recursos

Las **Unidades de Recursos** (RU) son tokens SPL utilizados dentro de **The Corporate Wars** para representar el peso económico estructural de los mundos.

Cada mundo tiene una cantidad determinada de RU asociada, que refleja su riqueza relativa dentro del modelo económico.

Estas unidades no se asignan de forma dinámica, sino que forman parte de la configuración estructural del universo simulado.

Su distribución obedece a un modelo de suma cero: la cantidad total de RU en el sistema es constante, y solo puede redistribuirse —o transformarse— como resultado de eventos internos.

### Referencia de Valor Interno

Las RU no están pensadas para salir del sistema.

> No están diseñadas para circular entre usuarios ni para operar como moneda de intercambio.

Aunque técnicamente son tokens SPL y podrían transferirse, el diseño del juego impone restricciones explícitas: no se comercializan, no se transfieren entre jugadores y no se utilizan en mercados.

Están directamente vinculadas a los mundos, y solo pueden ser instrumentalizados mediante el sistema financiero del juego.

{% hint style="danger" %}
**Advertencia**: las RU no tienen ni tendrán liquidez de mercado.\
Cualquier intento de hacerlas circular fuera del sistema, listarlas en DEX o venderlas como si fueran activos transferibles debe considerarse un fraude (_scam_).\
Su aparición en entornos externos indicaría un fallo de seguridad o una manipulación no autorizada.
{% endhint %}

Dentro del sistema, las RU permiten modelar el flujo de riqueza, calcular el impacto económico de acciones políticas o comerciales, y establecer jerarquías entre regiones galácticas según su importancia estructural.

Además, las RU están ancladas a una realidad técnica concreta: **cada unidad está respaldada por el SOL efectivamente depositado como _rent_ al desplegar los mundos y rutas que la sostienen.**

Durante los eventos de Despliegue Histórico, las aportaciones comunitarias no solo activan mundos y rutas: construyen el universo con una base económica tangible.

> **Cada RU representa una fracción de esa inversión, y su existencia garantiza que, al menos, ese valor técnico se encuentra ahí.**

El sistema reconoce esa huella como un respaldo mínimo real y no permitimos que RU cotize en mercados porque —de forma extrañamente poética— **representa el** _**SOL**_ **que mantiene la galaxia entera encendida.**

***

## Función en la simulación

Las RU dispnibles existen en su totalidad: el numero de RU emitidos es el máximo permitido por la red Solana.

`u64::MAX = 18,446,744,073,709,551,615`

Ese es el total de RU disponibles en la galáxia.

Los calculos actuales estiman una poblacion estelar en la via lactea con cifras de entre:

`100,000,000,000` y `400,000,000,000`

Lo cual nos proporciona una media de:

$$\frac{18,\!446,\!744,\!073,\!709,\!551,\!615\ \text{RU}}{400,\!000,\!000,\!000\ \text{estrellas}} \approx 46,\!116\ \text{RU por estrella}$$

18,446,744,073,709,551,615 RU ÷ 400,000,000,000 estrellas
≈ 46,116 RU por estrella

Las RU permiten cuantificar de forma abstracta el peso económico de cada región, el valor objetivo de ciertos eventos históricos y la prioridad relativa en procesos de replicación, escaneo, migración o degradación planetaria.

También sirven como **memoria estructural** en escenarios de _Larga Noche_: si un mundo se desconecta, sus RU siguen existiendo y pueden ser reactivadas al restaurar su estado desde la misma derivación lógica (misma PDA).

> El número total de RU es finito y determinado por el propio universo desplegado.\
> Redistribuir RU requiere **eventos de escala mayor**, como guerras económicas, absorciones, colapsos o reconstrucciones regionales.

