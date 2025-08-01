---
cover: ../../../../.gitbook/assets/tcw-ru.jpg
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

# Unidades de Recursos

Las **Unidades de Recursos** (RU) son tokens SPL utilizados dentro de **The Corporate Wars** para representar el peso económico estructural de los mundos.

Cada mundo tiene una cantidad determinada de RU asociada, que refleja su riqueza relativa dentro del modelo económico.

Estas unidades no se asignan de forma dinámica, sino que forman parte de la configuración estructural del universo simulado.

Su distribución obedece a un modelo de suma cero: la cantidad total de RU en el sistema es constante, y solo puede redistribuirse —o transformarse— como resultado de eventos internos.

***

### Referencia de Valor Interno

> **Las RU no están pensadas para salir del sistema:** No están diseñadas para circular entre usuarios ni para operar como moneda de intercambio.

{% hint style="success" %}
Están directamente vinculadas a los mundos, y solo pueden ser _instrumentalizadas_ mediante el sistema de juego.
{% endhint %}

Aunque técnicamente son tokens SPL y podrían transferirse, el diseño del juego impone restricciones explícitas: no se comercializan, no se transfieren entre jugadores y no se utilizan en mercados.

{% hint style="danger" %}
**Advertencia**: las RU no tienen ni tendrán liquidez de mercado.\
Cualquier intento de hacerlas circular fuera del sistema, listarlas en DEX o venderlas como si fueran activos transferibles debe considerarse un fraude (_scam_).\
Su aparición en entornos externos indicaría un fallo de seguridad o una manipulación no autorizada.
{% endhint %}

Dentro del sistema, las RU permiten modelar el flujo de riqueza, calcular el impacto económico de acciones políticas o comerciales, y establecer jerarquías entre regiones galácticas según su importancia estructural.

Además, las RU están ancladas a una realidad técnica concreta: **cada unidad está respaldada por el SOL efectivamente depositado como&#x20;**_**rent**_**&#x20;al desplegar los mundos y rutas que la sostienen.**

Durante los eventos de [Despliegue Histórico](../../../../roadmap/deployment/), las aportaciones comunitarias no solo activan mundos y rutas: construyen el universo con una base económica tangible.

> **Cada RU representa una fracción de esa aportación, y su existencia garantiza que, al menos, ese valor técnico se encuentra ahí.**

El sistema reconoce esa huella como un respaldo mínimo real y no permitimos que RU cotice en mercados porque —de forma extrañamente poética— **representa el** _**SOL**_ **que mantiene la galaxia entera encendida.**

***

## Función en la Simulación

> Las RU representan el peso estructural de un mundo dentro del universo simulado.

Emergen directamente de los valores reales del mundo en el sistema de juego: un mundo con perfil _Importante_ vincula —por definición— rutas de salto principales que generan _actividad_.

Esa actividad genera una carga de datos —ATA, PDA, almacenamiento... es decir: _rent_— vinculada a dicho mundo, a sus rutas de salto y a sus _Políticas_ locales; siendo necesaria una mayor cantidad de SOL depositado como '_rent-exempt_' para mantener su existencia.

Ese SOL, aunque no está en _stake_, permanece inmovilizado en la red, y su existencia —y _valor real_— se usa para **respaldar dentro del sistema** las cantidades de RU asignadas al mundo.

Este sistema permite emplear RU para cuantificar una equivalencia mínima garantizada **RU/SOL** que sirve como patrón referencial a diversos sistemas jugables y servicios del juego.

También permite cuantificar el peso económico de regiones enteras, evaluar el impacto estructural de eventos históricos y priorizar procesos como replicación, escaneo, migración o degradación.

Las RU actúan como memoria económica estructural del universo simulado, tanto en la exploración y expansión, como en el colapso y la contracción, permitiendo ciclos regionales de _Larga Noche_: si un mundo se desconecta, sus RU quedan asociadas a su derivación lógica (misma PDA), listas para restaurar su estado cuando vuelva a emerger.

***

## Proporción y Distribución

> El número total de RU es finito y determinado por el propio universo desplegado.

Distribuir —o redistribuir— RU requiere **eventos de escala mayor**: la expansión exploratoria del Tercer Imperio —[Milieu 0](../../../../roadmap/deployment/first-survey/) y [Second Survey](../../../../roadmap/deployment/second-survey.md)— contemplada en el [Despliegue Histórico](../../../../roadmap/deployment/), las mecánicas de exploración de mundos desconocidos basadas en el **Tercer Censo (Third Survey)**, implementación de nuevos contenidos —parches o expansiones— y narrativas jugables de alto nivel —guerras fronterizas, colapsos o reconstrucciones regionales.

Las RU disponibles existen en su totalidad: el número de RU emitidos es el máximo permitido por la red Solana.

`u64::MAX = 18,446,744,073,709,551,615` → es el total de RU disponibles en la galaxia.

Los cálculos actuales estiman una población estelar en la Vía Láctea con cifras de entre:

`100,000,000,000` y `400,000,000,000` estrellas.

Lo cual nos proporciona una media de:

$$
\frac{18,\!446,\!744,\!073,\!709,\!551,\!615\ \text{RU}}{400,\!000,\!000,\!000\ \text{estrellas}} \approx 46,\!116\ \text{RU/estrella}
$$

Tomando ese número de $$46,\!116\ \text{RU/estrella}$$ y asumimos una media aproximada de entre `5` y `8` planetas $$\approx 6.5 \text{planetas/estrella}$$

$$
\frac{46,\!116\ \text{RU/estrella}}{6.5\ \text{planetas/estrella}} \approx 7,\!094\ \text{RU/planeta}
$$

> **CASUALMENTE:** Un resultado muy aproximado a los 'máximos relativos' que se dan en la versión de Marc Miller's Traveller™ —5ª Edición.\
> —...y sí, de un modo u otro, todo el material de Traveller™ ha servido de inspiración para cada una de las etapas del diseño de **The Corporate Wars**

{% hint style="success" %}
Este número de RU 'por planeta' nos garantiza que cada **mundo** —abstracción de sistema estelar— de la galaxia dispone de suficientes RU —$$\approx 46,\!116\ RU/mundo$$— como para ser explotado intensivamente en Niveles Tecnológicos muy superiores —_anillos y esferas Dyson_—, sin sobrepasar el límite permitido por la red.
{% endhint %}

***

### Distribución Real

> Los cálculos efectuados representan los _límites_ del sistema, pero no son las cifras reales que el sistema va a manejar.

Aunque solo podemos aproximar una cifra, el Espacio Cartografiado en el año 1201 del Tercer Imperio abarca alrededor de `80,000` mundos repartidos en unos 1.000 Sectores.

Esto representa una reserva —orientativa— de RU máximos asignables:

$$
46,\!116\ RU/mundo \times 80,\!000\ mundos = 3,\!689,\!280,\!000\ RU_{asignables}
$$

Lo cual implica una mínima fracción del total:

$$
\frac{3,\!689,\!280,\!000 RU_{asignables}}{18,\!446,\!744,\!073,\!709,\!551,\!615 RU_{max}} \times 100 \approx 0.00002\% \text{ del total}
$$

Esto refuerza la enorme escala de una galaxia aún inexplorada, y es proporcional a los recursos aún disponibles en la simulación y el universo de juego.

No todos los mundos estarán cartografiados exhaustivamente, ni todos habrán sido registrados por una única _Institución_ o _Lealtad_, pero todos ellos _existen_ en la simulación y, junto a las rutas de salto que los conectan, son _actores estructurales_ del **juego económico de suma cero**.

***

### "_Minería_ de RU"

Explorar las fronteras del Espacio Cartografiado implica el descubrimiento de nuevos mundos, el primer contacto con civilizaciones y otros elementos jugables.

Internamente, el sistema despliega procesos jugables que consumen MCr —directa o indirectamente— con el objetivo de establecer los **mínimos necesarios** para el registro del mundo descubierto en el **Tercer Censo (Third Survey)**.

Este proceso permite redestinar SOL de la tesorería a los depósitos de _rent_ necesarios para incluir el nuevo mundo en la economía interestelar, basándose en el índice SOL/RU, consumiendo MCr del sistema en el corto plazo —equipos de exploración, combustible, balizas, información privilegiada—, a cambio de recompensas estructurales —concesiones, licencias, tasas reducidas...— en el medio plazo.

Estos depósitos de _rent_ respaldan los RU del nuevo mundo y se aplican de forma progresiva a medida que se progresa con el ciclo jugable de la narrativa exploratoria, permitiendo escenarios de **colaboración competitiva**.

Finalmente —después de varias exploraciones y contactos— el nuevo mundo quedaría integrado en la sociedad interestelar, en la misma medida que los RU aportados:

Mundos con civilizaciones nativas complejas requieren de mayor aporte estructural, lo cual aportará también una mayor dimensión de jugabilidad —nuevos sofontes, _lealtades_ menores—, justificando los costes y recompensas —reales y simulados— de exploración, comercio y contacto.

Por otro lado, mundos deshabitados, con dinamicas simples, de extraccion de recusos y colonizacion a futuros, requieren de menores despliegues estrucutrales —menos _rent_ y RU.

Este funcionamiento emerge organicamente integrando _de forma natural_ la "_minería_ de RU" con la exploración interestelar y el escenario temático del **Tercer Censo (Third Survey)**.
