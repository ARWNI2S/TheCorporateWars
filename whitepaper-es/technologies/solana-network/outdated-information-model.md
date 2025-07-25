---
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# El Modelo de Información Desfasada

En un Imperio de más de once mil mundos, donde las naves de salto son las arterias que conectan civilizaciones dispersas, la información **nunca** llega de forma instantanea.

Por muy avanzada que sea la tecnología, ninguna civilización del Tercer Imperio —ni de cualquier otra _lealtad_— ha encontrado forma de superar una ley fundamental del espacio conocido:

> **La información no puede viajar más rápido que la luz.**

Las comunicaciones interestelares dependen de emisarios físicos: mensajeros, cargueros, sondas, naves diplomáticas. Los despachos, las cotizaciones bursátiles, los informes militares y hasta las simples noticias locales cruzan los corredores de salto encapsulados en unidades físicas, sujetas a las mismas limitaciones que cualquier carga material.

Esto introduce **latencias estructurales**:

- Un mensaje del sector Core a los márgenes del Imperio puede tardar semanas o meses.
- Las decisiones se toman con base en datos antiguos.
- Las oportunidades y amenazas pueden haberse desvanecido cuando la información llega.

El modelo de información desfasada no es un fallo del sistema: **es el sistema**. Define las estrategias, condiciona la logística y da forma al propio tejido social, político y económico de la galaxia. Y en **The Corporate Wars**, este modelo no es un detalle de color: es la columna vertebral del diseño técnico que sostiene el ecosistema persistente.

{% hint style="info" %}
A continuación explicamos cómo hemos integrado esta asincronía en el corazón del juego, usando tecnologías distribuidas (como la blockchain Solana) para reflejar un universo donde la sincronización absoluta es inalcanzable.
{% endhint %}

***

## Latencia estructural

En **The Corporate Wars**, la información interestelar no fluye en tiempo real ni de forma global. El universo se estructura como un **grafo dirigido de latencia**, donde cada nodo representa un sistema estelar, y cada arista (ruta de tránsito) introduce un retraso concreto determinado por las limitaciones físicas del viaje interestelar.

Cada ruta A → B implica una latencia intrínseca. Aunque las transacciones globales se registran en blockchain, cada nodo solo puede percibir y operar con las **diferencias aplicadas sobre su propio estado local**, correspondientes a su ventana de visibilidad:

- Las diferencias se almacenan ordenadas en el tiempo $$(T, T-1, T-2, ..., T-N)$$.
- El nodo A tiene acceso a las diferencias procedentes de B únicamente hasta la versión $$(T-t_{ruta})$$, donde $$t_{ruta}$$ representa el retraso de la ruta.
- Cambios posteriores no son visibles hasta que los datos físicos "llegan" a través de las rutas de tránsito.

Así, la percepción de A sobre B siempre está desfasada y depende de:

- el retraso acumulado por las rutas disponibles,
- el ritmo de actualización,
- y la capacidad logística para transportar datos a través del grafo.

***

## Desafíos técnicos

Implementar un modelo de información desfasada en un universo distribuido, apoyado en blockchain (Solana), plantea retos técnicos reales que no son simples problemas jugables, sino desafíos de ingeniería profunda:

- **Almacenamiento y crawling eficiente de versiones diferenciales:** los nodos deben acceder solo a los deltas relevantes para su ventana temporal $$(T-t_{ruta})$$, evitando recorrer toda la cadena completa.\
  Esto requiere algoritmos eficientes para filtrar, indexar y servir versiones parciales a escala masiva.
- **Bidireccionalidad asimétrica del grafo:** las rutas A → B no siempre son simétricas en tiempo ni en capacidad con B → A. Esto genera caminos de actualización y latencia divergentes que deben ser modelados dinámicamente, afectando tanto a la topología como al cálculo de snapshots visibles.
- **Limitación de acceso contextual:** aunque los datos están públicos en blockchain, solo deben ser desencriptados y expuestos al backend según los permisos, contexto y posición de cada jugador. Esto exige una capa adicional de cifrado granular y gestión de claves que no depende solo del on-chain.
- **Reuso eficiente de PDA en sistemas múltiples:** las cuentas PDA no solo sirven al jugador, sino que alimentan sistemas secundarios como el Interstellar Stock Exchange (ISE) y la gobernanza multicapa. Esto obliga a diseñar pipelines de datos que puedan servir múltiples dominios sin inconsistencias ni sobrecarga.
- **Escalabilidad de programas en Solana:** los programas encargados de manejar agregación, filtrado y entrega de datos deben ser capaces de escalar en un entorno con decenas de miles de jugadores y nodos, respetando costes computacionales (SOL), límites de throughput y latencias mínimas.
- **Sincronización blanda de nodos locales:** como no existe estado global instantáneo, los nodos locales necesitan mecanismos de reconciliación y corrección eventual para evitar acumulación de errores o derivaciones prolongadas del estado base.

Estos desafíos no son triviales ni teóricos: son limitaciones presentes que definen cómo puede crecer y operar un sistema como **The Corporate Wars** a escala real.

***

## Ventajas del modelo

Este enfoque no es solo una solución técnica: es un pilar que aporta ventajas diferenciadoras a nivel de diseño y experiencia.

- **Refuerza la asimetría estratégica:** quien tiene mejores rutas o control logístico accede antes a datos clave.
- **Introduce incertidumbre:** no todos los eventos recientes son visibles en todos los nodos, creando decisiones basadas en probabilidades, no certezas.
- **Habilita capas de juego emergente:** desde manipulación informativa hasta corredores de datos y brokers de actualización.
- **Conecta sistemas:** las PDA de rutas y mundos no son datos aislados, sino que alimentan directamente los instrumentos del ISE y las dinámicas de gobernanza multicapa.
- **Seguridad de fair game:** aunque los datos están en blockchain y son accesibles públicamente, solo el backend autorizado puede desencriptar y exponer la información que cada jugador tiene derecho a ver, evitando leaks, minería de datos externos o abusos.

En resumen, el modelo de información desfasada no es solo una mecánica de juego: es un diseño profundamente interconectado que refuerza la coherencia narrativa, la integridad técnica y la riqueza del ecosistema persistente.
