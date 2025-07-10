# El Modelo de Información Desfasada

En un Imperio de más de once mil mundos, donde las naves de salto son las arterias que conectan civilizaciones dispersas, la información **nunca** llega de forma instantanea.

Por muy avanzada que sea la tecnología, ninguna civilización del Tercer Imperio —ni de cualquier otra facción conocida— ha encontrado forma de superar una ley fundamental del universo conocido:

> **La información no puede viajar más rápido que la luz.**

Las comunicaciones interestelares dependen de emisarios físicos: mensajeros, cargueros, sondas, naves diplomáticas. Los despachos, las cotizaciones bursátiles, los informes militares y hasta las simples noticias locales cruzan los corredores de salto encapsulados en unidades físicas, sujetas a las mismas limitaciones que cualquier carga material.

Esto introduce **latencias estructurales**:

* Un mensaje del sector Core a los márgenes del Imperio puede tardar semanas o meses.
* Las decisiones se toman con base en datos antiguos.
* Las oportunidades y amenazas pueden haberse desvanecido cuando la información llega.

El modelo de información desfasada no es un fallo del sistema: **es el sistema**. Define las estrategias, condiciona la logística y da forma al propio tejido social, político y económico de la galaxia. Y en _The Corporate Wars_, este modelo no es un detalle de color: es la columna vertebral del diseño técnico que sostiene el ecosistema persistente.

{% hint style="info" %}
A continuación explicamos cómo hemos integrado esta asincronía en el corazón del juego, usando tecnologías distribuidas (como la blockchain Solana) para reflejar un universo donde la sincronización absoluta es inalcanzable.
{% endhint %}

## Latencia estructural

En The Corporate Wars, la información interestelar no fluye en tiempo real ni de forma global. El universo se estructura como un **grafo dirigido de latencia**, donde cada nodo representa un sistema estelar, y cada arista (ruta de tránsito) introduce un retraso concreto determinado por las limitaciones físicas del viaje interestelar.

Cada ruta A → B implica una latencia intrínseca. Aunque las transacciones globales se registran en blockchain, cada nodo solo puede percibir y operar con los bloques correspondientes a su ventana de visibilidad:

* La blockchain guarda las transacciones en ordenados en el tiempo (T, T-1, T-2, ..., T-N).
* El nodo A tiene acceso a las transacciones de B únicamente hasta el bloque **T-(n)**, donde **n** representa el retraso de la ruta.
* Bloques posteriores no son visibles hasta que los datos físicos "llegan" a través de las rutas de tránsito.

Así, la percepción de A sobre B siempre está desfasada y depende de:

* el retraso acumulado por las rutas disponibles,
* el ritmo de actualización,
* y la capacidad logística para transportar datos a través del grafo.

## Desafíos técnicos

Implementar un modelo de información desfasada en un universo distribuido plantea desafíos únicos, especialmente cuando se busca mantener coherencia, auditabilidad y seguridad en un entorno multijugador masivo.

Entre los principales retos encontramos:

* **Gestión de latencia heterogénea:** cada ruta A → B tiene una latencia propia, generando múltiples vistas temporales parciales que deben sincronizarse solo hasta el límite permitido.
* **Integridad de datos:** aunque las transacciones están registradas en blockchain (Solana), los nodos solo deben acceder a los bloques que les corresponden según su posición en el grafo, sin posibilidad de anticipar bloques futuros.
* **Cifrado selectivo:** los datos en blockchain son accesibles públicamente, pero están encriptados. Solo el backend autorizado puede desencriptar la porción específica del snapshot disponible para cada jugador, asegurando fair play y evitando exploits.
* **Reutilización de datos contextuales:** las PDA (percepciones dinámicas asíncronas) de rutas y mundos no solo alimentan la capa de juego, sino que se reutilizan como inputs para instrumentos financieros del ISE (Interstellar Stock Exchange) y para mecanismos de gobernanza multicapa, amplificando el impacto técnico del modelo.
* **Programas Solana especializados:** las soluciones no dependen solo del on-chain, sino de programas (smart contracts) diseñados específicamente para manejar agregación, filtrado, cifrado y entrega de datos, respetando tanto la latencia física como la lógica del ecosistema.

## Ventajas del modelo

Este enfoque no es solo una solución técnica: es un pilar que aporta ventajas diferenciadoras a nivel de diseño y experiencia.

* **Refuerza la asimetría estratégica:** quien tiene mejores rutas o control logístico accede antes a datos clave.
* **Introduce incertidumbre:** no todos los eventos recientes son visibles en todos los nodos, creando decisiones basadas en probabilidades, no certezas.
* **Habilita capas de juego emergente:** desde manipulación informativa hasta corredores de datos y brokers de actualización.
* **Conecta sistemas:** las PDA de rutas y mundos no son datos aislados, sino que alimentan directamente los instrumentos del ISE y las dinámicas de gobernanza multicapa.
* **Seguridad de fair game:** aunque los datos están en blockchain y son accesibles públicamente, solo el backend autorizado puede desencriptar y exponer la información que cada jugador tiene derecho a ver, evitando leaks, minería de datos externos o abusos.

En resumen, el modelo de información desfasada no es solo una mecánica de juego: es un diseño profundamente interconectado que refuerza la coherencia narrativa, la integridad técnica y la riqueza del ecosistema persistente.
