---
cover: ../../.gitbook/assets/tcw-survey3-db.jpg
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

# Base de Datos del Tercer Censo

El Tercer Censo es el núcleo estructural del universo simulado en **The Corporate Wars**. No se trata de un simple catálogo de planetas ni de un mapa de rutas, sino de una base de datos activa, descentralizada y asincrónica, que modela los elementos físicos y lógicos del espacio conocido.

{% hint style="info" %}
Define qué existe, qué está conectado y quién puede ejercer autoridad sobre qué.
{% endhint %}

> La información no es estática: evoluciona con el tiempo, se transmite de forma parcial y presenta retardo según el flujo de información real.

Este comportamiento no es un artificio narrativo, sino una consecuencia directa del modelo: mundos, rutas y estructuras de poder se almacenan, procesan y actualizan dentro de cuentas programáticas derivadas (PDA), ancladas a programas específicos.

***

## Mundos como nodos dinámicos

Cada mundo es una cuenta programática derivada (PDA), cuyo contenido está comprimido en un Merkle Tree que representa un **perfil deshidratado** del planeta: datos esenciales codificados de forma eficiente y verificable.

Esto incluye población, nivel tecnológico, régimen jurídico, PIB estimado, tipo de gobierno, clima y otros atributos clave.

Además, cada mundo mantiene un **historial de versiones**. En lugar de sobrescribir su estado, cada cambio se almacena como una diferencia (_diff_) sobre la versión anterior, permitiendo reconstruir su evolución con precisión en cualquier momento del pasado.

Estos mundos no existen en aislamiento: están enlazados por rutas que determinan no solo el tránsito físico, sino también el acceso a información actualizada, órdenes válidas y autoridad aplicable.

***

## Rutas, visibilidad y gobernanza

Las **rutas de salto** son cuentas programáticas derivadas que representan _todas las conexiones funcionales entre mundos_. Registran su latencia, volumen de tráfico, condiciones operativas y restricciones.

Son entidades técnicas, pero también políticas: permiten o bloquean la transmisión de órdenes, mercancías, datos y poder.

El sistema simula un universo **asincrónico y parcialmente visible**. Cada mundo ve solo lo que ha sido transmitido a través de sus rutas activas.

> No existe una verdad global instantánea: dos mundos pueden mantener versiones distintas del mismo hecho, dependiendo de su posición en el grafo topológico y del retardo en la propagación de información.

{% hint style="success" %}
Esta lógica reproduce con fidelidad los límites físicos de la comunicación interestelar.
{% endhint %}

***

> Sobre este entramado operan las _Políticas_, las entidades de gobernanza del sistema.
>
> Ninguna puede aplicar autoridad en abstracto: necesitan **mundos bajo control** y **rutas operativas** que las conecten.
>
> Sin esa infraestructura validada por el sistema, su capacidad de acción es nula o simbólica. La autoridad depende de la topología: no se gobierna donde no se alcanza.
>
> El conjunto es, además, una estructura viva. Los mundos pueden fundarse, cambiar de manos, ser terraformados, abandonados o destruidos.
>
> Las rutas pueden cerrarse, degradarse o abrirse por decisión diplomática, eventos sistémicos o cambios tecnológicos.
>
> Todo ello queda registrado y reflejado en las cuentas programáticas del Tercer Censo.

***

{% hint style="warning" %}
En resumen, el Tercer Censo no solo describe el universo: lo define.\
Es la fuente ontológica del juego.\
Lo que no está en el Tercer Censo, no existe.\
Y lo que no está actualizado, es incierto.
{% endhint %}
