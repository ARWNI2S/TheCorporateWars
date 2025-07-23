# Milieu 0

Históricamente Milieu 0 representa el punto de inicio de la expansión del Tercer Imperio.

> Es el periodo inmediatamente posterior a su fundación, cuando Cleon Zhunastu, el Primer Emperador, unifica los mundos heredados de un Ziru Sirka 'reunificado' y comienza a consolidar poder real sobre una galaxia fragmentada.

Es una época de exploración, diplomacia, construcci�n de infraestructura, establecimiento de rutas de comunicaci�n y negociaci�n de lealtades con sectores y mundos perif�ricos, marcando las bases sobre las que el Imperio crecer� durante los siguientes mil a�os.

### Despliegue Inicial

En un principio el sistema presenta requisitos de infraestructura básicos:

* servidores de backend,
* sitios web,
* nodos rpc
* y programas en la red Solana.

Todos ellos pueden implementarse en entornos de pruebas, en la nube o localmente, y con los programas stateless en '_Devnet_'.

Baterías de test validan la efectividad del código, y pruebas cerradas de experiencia de usuario validan la puesta en producción de la primera etapa del despliegue.

Para ello disponemos de un MVP que contiene lo siguiente sistemas:

* gestión administrativa del mapa de la galaxia,
* tesorería del sistema económico,
* la estructura de gobernanza multicapa,
* las _Políticas_ como entidades de juego y gobernanza,
* el sistema financiero interestelar.

## Participación de la Comunidad

En esta etapa temprana de desarrollo no existe un cliente de juego funcional, pero si disponemos de programas en la red solana completamente desarrollados que permiten definir las estructuras principales del sistema de juego.

Los participantes en esta etapa aportan SOL a la tesorería de sistema a cambio de un paquetes de MCr y RU que van destinados al sistema economico del juego a traves del sistema financiero interestelar ya implementado.

La **tesorería** del sistema está destinada a:

* permitir el _mint_ de **MCr** y **RU**,
* cubrir los depósitos de _rent_ de toda las _PDA_ del sistema,
* mantener los costes operativos del sistema,
* recompensar la participación de desarrolladores y artistas,
* y establecer la posible liquidez futura del **MCr** en mercados externos,

En esta etapa el sistema financiero interestelar simula:

* las participaciones en _megacorporaciones_, _corporaciones_ y otras _Políticas_.
* los grandes depósitos de la _Banca Imperial_,
* las _Opciones de Ruta_ del _Mercado de Valores Interestelar_
* las grandes fortunas de la _Nobiliti_.

{% hint style="danger" %}
Esto no es una propuesta de inversión, sino de participación en un sistema de juego funcional y emergente, en una etapa temprana de su desarrollo.
{% endhint %}

### _Políticas_ de Milieu 0

El sistema de _Políticas_, ya estructurado, permite:

* la creación de las _Lealtades_ principales y _Políticas_ interestelares,
* la creación de _gobiernos_ afiliadas a _Lealtades_,
* la creación de _megacorporaciones_ como agregados de _Políticas_,
* y la creación de _corporaciones_ individuales.

Estas _Políticas_ persistirán como entidades de juego historicas, fuera del control directo de los jugadores, pero con un impacto directo en las mecanicas relacionadas con _lealtades_, _gobiernos_, _leyes_ y _economía_ de grandes territorios.

### Exploración y Expansión

Los diversos aportes al sistema económico construyen una red de mundos y rutas de salto alrededor de Sylea.

Los RU se distribuyen en el sistema de forma equilibrada, acumulándose en los mundos de forma progresiva.

Las primeras etapas están destinadas únicamente a Sylea, reforzando su posición como Capital del Imperio.

Las RU acumuladas implican SOL en tesorería, lo cual permite el despliegue de rutas como PDA, pero para desplegar la ruta primero necesitamos un destino, por lo que es responsabilidad del "stack syleano" pagar los rent de las pda de los mundos y turas a su alrededor.

Esto nos permite sentar las bases del proceso de exploración de nevos sectores de la galaxia y simular la expansión del imperio y las rutas interestelares.

Cada mundo representa un nodo y cada ruta una arista en una red neural asimétrica bidireccional.
