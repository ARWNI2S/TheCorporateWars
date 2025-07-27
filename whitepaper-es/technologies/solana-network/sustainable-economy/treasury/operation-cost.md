---
cover: ../../../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Coste Operativo

El coste operativo representa el conjunto de recursos necesarios para que **The Corporate Wars** funcione de forma continua, tanto en su despliegue sobre la red Solana como en la infraestructura técnica que lo sostiene fuera de ella.

A _nivel blockchain_, incluye el mantenimiento de cuentas y programas activos, el pago de _rent_ proporcional al tamaño  del estado, y las comisiones (_fees_) por cada operación ejecutada, ya sea por los jugadores o por procesos internos del sistema.

Pero más allá de la red Solana, el sistema requiere una base técnica permanente: servidores en la nube, bases de datos, almacenamiento auxiliar, servicios de autenticación, servidores web, APIs, procesamiento de eventos, herramientas de orquestación, monitorización, seguridad, backups y más.

Sin esta capa operativa, el universo no sería accesible, estable ni funcional.

### Realidad Económica

> Páginas web, servicios de identidad, bases de datos, en internet todo puede ser gratuito mientras _solo lo uses tú_, pero en el momento en el que necesitas _servir a usuarios_, por pocos que sean, las subscripciones gratuitas no son capaces de absorver ni una fracción del tráfico entrante, creando cuellos de botella y fallos de red.

Los servidores de juego requiren de capacidad de respuesta con latencias minimas a miles de usuarios —ojalá—, que al mismo tiempo esperan un funcionamiento **perfecto** del sistema; lo que implica orquestación y replica para evitar caidas, hubs de redirección geografica y un incremento progresivo de servicios integrados al sistema.

Aunque se diseñen mecanismos de automatización con precisión, no existe un _metodo milagroso estandar_ que libere completamente a un sistema de mantenimiento y supervisión humano; administracion y soporte tecnico, seran necesarios para garantizar la calidad del servicio.

Por lo que un sistema real AAA tambien requiere de un equipo humano real, al que se le compense agradecidamente por sus inestimables aportaciones y servicios.

***

### El '_Rent_' de las _Narices_.

A diferencia de otras blockchains donde los costes se asumen una vez al desplegar el programa, en Solana cada cuenta debe mantener una cantidad mínima de SOL como "depósito" (_rent_) proporcional a su tamaño, o será eliminada automáticamente de la red.

Si este depósito cubre el coste de 2 años de _rent_, la cuenta se considera _rent-exempt_ y no se elimina.

> Para cada cuenta en Solana —ya sea de usuario, de programa, PDA o cuenta de datos— hay que depositar el _rent_, proporcional al número de bytes ocupados.\
> Cuanto más grande sea el estado, mayor el depósito.

Tambien existe el _cierre_ de cuentas **controlado**, que permite recuperar el _rent_; aunque este mecanismo se tiene que implementar en cada programa de forma especifica.

Esto se vuelve especialmente relevante en un sistema como **The Corporate Wars**, donde pretendemos desplegar estructuras de información complejas: planetas, sectores, rutas comerciales, holdings corporativos...

El almacenamiento sin optimización puede llegar a costar 0.3 SOL por sistema estelar o más, volviendo inviable el escalado a un sector galáctico o una red de 11.000 mundos.

***

Todos estos elementos tienen un coste real y sostenido, que debe cubrirse con regularidad.

La Tesorería está diseñada para sostener este gasto estructural de forma continua, canalizando parte de los fondos recibidos hacia el mantenimiento de la infraestructura y la operativa general.

> Si el universo sigue funcionando cuando nadie está jugando, es porque hay un sistema real manteniéndolo encendido.

### Recesión Simulada

En escenarios de _Larga Noche_, totales o parciales, los sistemas planetarios desconectados dejan de operar activamente: las PDA asociadas a estos mundos pueden ser **cerradas de forma controlada**, recuperando el _rent_ correspondiente y liberando recursos técnicos.

Esta capacidad de repliegue —económica y técnica— permite que el universo **se degrade sin colapsar**: las rutas abandonadas se apagan, los sistemas caen en silencio, y solo quedan trazas en el _lore_ y en el historial de bloques.

Cuando una nueva _Lealtad_ retoma el control o se reactiva una región, los mismos mundos y rutas pueden ser recreados desde la misma derivación PDA, restaurando su identidad lógica y narrativa aunque el estado anterior haya sido desmantelado.

> Este mecanismo permite que la **memoria estructural del universo** persista incluso cuando los datos han sido limpiados:  
> **misma clave, nuevo ciclo —otro milieu.**
