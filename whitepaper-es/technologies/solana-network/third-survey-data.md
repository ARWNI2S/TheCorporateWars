---
icon: pencil
cover: ../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Base de Datos del Tercer Censo

El Tercer Censo es el n�cleo estructural del universo simulado en **The Corporate Wars**.

No se trata de un simple cat�logo de planetas ni de un mapa de rutas, sino de una base de datos activa, descentralizada y asincr�nica, que modela los elementos f�sicos y l�gicos del espacio conocido.

Define qu� existe, qu� est� conectado y qui�n puede ejercer autoridad sobre qu�.

La informaci�n no es est�tica: evoluciona con el tiempo, se transmite de forma parcial y presenta retardo seg�n el flujo de informaci�n real.

Este comportamiento no es un artificio narrativo, sino una consecuencia directa del modelo: mundos, rutas y estructuras de poder se almacenan, procesan y actualizan dentro de cuentas program�ticas derivadas (PDA), ancladas a programas espec�ficos.

## Mundos como nodos din�micos

Cada mundo es una cuenta program�tica derivada (PDA), cuyo contenido est� comprimido en un Merkle Tree que representa un **perfil deshidratado** del planeta: datos esenciales codificados de forma eficiente y verificable.

Esto incluye poblaci�n, nivel tecnol�gico, r�gimen jur�dico, PIB estimado, tipo de gobierno, clima y otros atributos clave.

Adem�s, cada mundo mantiene un **historial de versiones**. En lugar de sobrescribir su estado, cada cambio se almacena como una diferencia (_diff_) sobre la versi�n anterior, permitiendo reconstruir su evoluci�n con precisi�n en cualquier momento del pasado.

Estos mundos no existen en aislamiento: est�n enlazados por rutas que determinan no solo el tr�nsito f�sico, sino tambi�n el acceso a informaci�n actualizada, �rdenes v�lidas y autoridad aplicable.

## Rutas, visibilidad y gobernanza

Las **rutas de salto** son cuentas program�ticas derivadas que representan _todas las conexiones funcionales entre mundos_. Registran su latencia, volumen de tr�fico, condiciones operativas y restricciones.

Son entidades t�cnicas, pero tambi�n pol�ticas: permiten o bloquean la transmisi�n de �rdenes, mercanc�as, datos y poder.

El sistema simula un universo **asincr�nico y parcialmente visible**. Cada mundo ve solo lo que ha sido transmitido a trav�s de sus rutas activas.

No existe una verdad global instant�nea: dos mundos pueden mantener versiones distintas del mismo hecho, dependiendo de su posici�n en el grafo topol�gico y del retardo en la propagaci�n de informaci�n.

Esta l�gica reproduce con fidelidad los l�mites f�sicos de la comunicaci�n interestelar.

***

Sobre este entramado operan las _Pol�ticas_, las entidades de gobernanza del sistema.

Ninguna puede aplicar autoridad en abstracto: necesitan **mundos bajo control** y **rutas operativas** que las conecten.

Sin esa infraestructura validada por el sistema, su capacidad de acci�n es nula o simb�lica. La autoridad depende de la topolog�a: no se gobierna donde no se alcanza.

El conjunto es, adem�s, una estructura viva. Los mundos pueden fundarse, cambiar de manos, ser terraformados, abandonados o destruidos.

Las rutas pueden cerrarse, degradarse o abrirse por decisi�n diplom�tica, eventos sist�micos o cambios tecnol�gicos.

Todo ello queda registrado y reflejado en las cuentas program�ticas del Tercer Censo.

***

En resumen, el Tercer Censo no solo describe el universo: lo define.\
Es la fuente ontol�gica del juego.\
Lo que no est� en el Tercer Censo, no existe.\
Y lo que no est� actualizado, es incierto.
