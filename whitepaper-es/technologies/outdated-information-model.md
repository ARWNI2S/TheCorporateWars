# El Modelo de Información Desfasada

En un Imperio de más de once mil mundos, donde las naves de salto son las arterias que conectan civilizaciones dispersas, la información **nunca** llega de forma instantanea.

Por muy avanzada que sea la tecnología, ninguna civilización del Tercer Imperio —ni de cualquier otra facción conocida— ha encontrado forma de superar una ley fundamental del universo conocido:

> **La información no puede viajar más rápido que la luz.**

Las comunicaciones interestelares dependen de emisarios físicos: mensajeros, cargueros, sondas, naves diplomáticas. Los despachos, las cotizaciones bursátiles, los informes militares y hasta las simples noticias locales cruzan los corredores de salto encapsulados en unidades físicas, sujetas a las mismas limitaciones que cualquier carga material.

Esto introduce **latencias estructurales**:
- Un mensaje de Core a los márgenes puede tardar semanas o meses.
- Las decisiones se toman con base en datos antiguos.
- Las oportunidades y amenazas pueden haberse desvanecido cuando la información llega.

El modelo de información desfasada no es un fallo del sistema: **es el sistema**.
Define las estrategias, condiciona la logística y da forma al propio tejido social, político y económico de la galaxia.
Y en *The Corporate Wars*, este modelo no es un detalle de color: es la columna vertebral del diseño técnico que sostiene el ecosistema persistente.

{% hint style="info" %}
A continuación explicamos cómo hemos integrado esta asincronía en el corazón del juego, usando tecnologías distribuidas (como la blockchain Solana) para reflejar un universo donde la sincronización absoluta es inalcanzable.
{% endhint %}

## Latencia estructural

En The Corporate Wars, la información interestelar no fluye en tiempo real ni de forma global. El universo se estructura como un **grafo dirigido de latencia**, donde cada nodo representa un mundo, estación o enclave, y cada arista (ruta de tránsito) introduce un retardo concreto determinado por las limitaciones físicas del viaje interestelar.

Cada ruta A → B implica un retraso intrínseco. Aunque las transacciones globales se registran en blockchain, cada nodo solo puede percibir y operar con los bloques correspondientes a su ventana de visibilidad.

En concreto:
- La blockchain guarda las transacciones en bloques ordenados en el tiempo (T, T-1, T-2, ..., T-N).
- El nodo A tiene acceso a las transacciones de B únicamente hasta el bloque **T-(n)**, donde **n = route_lag(A-B)**.
- Bloques posteriores (T-(n+1), T-(n+2), ...) no son visibles hasta que los datos físicos (updates) llegan a través de las rutas de tránsito.

Así, la percepción de A sobre B siempre está desfasada y depende de:
- el retraso acumulado por las rutas disponibles,
- el ritmo de actualización,
- y la capacidad logística para transportar datos a través del grafo.

## Diseño técnico

Este modelo combina:
- **Blockchain Solana**: guarda las transacciones (updates) agregadas, con sellado temporal y trazabilidad.
- **Rutas físicas (salto interestelar)**: transportan las actualizaciones efectivas entre nodos.
- **Snapshots locales parciales**: cada nodo mantiene una colección de transacciones visibles hasta su frontera temporal según latencia.

No existe un “estado global instantáneo”:  
Cada actor toma decisiones y opera con información limitada por las condiciones reales del universo.

## Implicaciones en el juego

Este diseño:
- Refuerza la asimetría estratégica: quien tiene mejores rutas o control logístico accede antes a datos clave.
- Introduce incertidumbre: no todos los eventos recientes son visibles en todos los nodos.
- Añade capas de juego emergente: manipulación informativa, corredores de datos, brokers de actualización.

En resumen, en The Corporate Wars la asincronía no es solo un detalle narrativo: es la base del ecosistema técnico y jugable.
