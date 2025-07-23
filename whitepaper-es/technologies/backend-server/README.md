---
icon: pencil
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Servicios Propios

A pesar de utilizar motores de juego y plataformas en la nube de nivel profesional (AAA), es importante se�alar que ning�n sistema se encuentra completamente preparado para su uso inmediato con el comportamiento espec�fico que se requiere.

Si bien estas tecnolog�as permiten la incorporaci�n de m�ltiples capas de componentes, no resulta eficiente estructurar los servicios como programas independientes, ya que esto introduce redundancias y penalizaciones en el rendimiento.

***

La estrategia adecuada consiste en dise�ar una arquitectura compatible con la infraestructura empleada. En nuestro caso, se trata de un servidor de juego basado en nodos distribuidos, que ejecuta un sistema de simulaci�n igualmente distribuido. El balance de carga de este sistema se ajusta din�micamente en funci�n del nivel de detalle necesario, dependiendo del n�mero de usuarios activos.

Este enfoque permite operar mundos virtuales de gran escala y complejidad, manteniendo una carga de sistema proporcional a la actividad real de los usuarios, y no al tama�o absoluto del entorno simulado.

Estas tecnologias, aunque  son experimentales, han sido desarrolladas durante a�os por el proyecto NI2S y se van a poner a prueba en un entorno real.