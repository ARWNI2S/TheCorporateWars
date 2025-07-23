---
icon: pencil
cover: ../../.gitbook/assets/tcw-custom.jpg
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

# Servicios Propios

A pesar de utilizar motores de juego y plataformas en la nube de nivel profesional (AAA), es importante señalar que ningún sistema se encuentra completamente preparado para su uso inmediato con el comportamiento específico que se requiere.

Si bien estas tecnologías permiten la incorporación de múltiples capas de componentes, no resulta eficiente estructurar los servicios como programas independientes, ya que esto introduce redundancias y penalizaciones en el rendimiento.

***

La estrategia adecuada consiste en diseñar una arquitectura compatible con la infraestructura empleada. En nuestro caso, se trata de un servidor de juego basado en nodos distribuidos, que ejecuta un sistema de simulación igualmente distribuido. El balance de carga de este sistema se ajusta dinámicamente en función del nivel de detalle necesario, dependiendo del número de usuarios activos.

Este enfoque permite operar mundos virtuales de gran escala y complejidad, manteniendo una carga de sistema proporcional a la actividad real de los usuarios, y no al tamaño absoluto del entorno simulado.

{% hint style="danger" %}
Estas tecnologías, aunque son experimentales, han sido desarrolladas durante años por el proyecto NI2S y se van a poner a prueba en un entorno real.
{% endhint %}
