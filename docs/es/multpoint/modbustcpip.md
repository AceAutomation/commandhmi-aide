# Modbus TCP/IP

Mediante MODBUS TCP se puede comunicar con el HMI y controlarlo a distancia.

**Ajustes** con el HMI como maestro:

Tras crear el proyecto, haga doble clic en «Conexión 1», como abajo:

<img src="../../multpoint/modbustcpip.files/modbustcpip209.png" width="248" />

Se abre el cuadro de diálogo «Propiedades del puerto de comunicación» (abajo).

<img src="../../multpoint/modbustcpip.files/modbustcpip286.png" width="590" />

Haga clic en «Parámetros» en el cuadro de diálogo de propiedades del puerto para definir la dirección IP y el puerto (los del equipo supervisado). Elija el modo de direccionamiento estándar y haga clic en «Aceptar».

<img src="../../multpoint/modbustcpip.files/modbustcpip544.png" width="588" />

Si elige «Modo extendido» como modo de direccionamiento, la IP y el puerto definidos aquí no se usan: se definen con la función «Configuración IP de los esclavos» de un botón de función.

Con el proyecto en marcha, haga clic en el botón para abrir la ventana de número de estación; introdúzcalo y se abre la ventana de ajuste de la IP y el puerto del esclavo, como en la figura siguiente:

<img src="../../multpoint/modbustcpip.files/modbustcpip985.png" width="445" />

Tras estos ajustes, descargue el proyecto al HMI y conecte el maestro y el esclavo directamente o mediante un router para la supervisión y el control.

**Ajustes del esclavo:**

**1. Definir la IP**

Primero, use los interruptores DIP 1 y 3 para definir la dirección IP del HMI en la ventana de ajuste de IP. En este ejemplo, la IP del esclavo es 192.168.1.31.

**2. Crear la conexión**

Tras crear el proyecto, haga doble clic en «Conexión 1», como abajo:

<img src="../../multpoint/modbustcpip.files/modbustcpip1527.png" width="229" />

Se abre el cuadro de diálogo «Propiedades del puerto de comunicación» (abajo).

<img src="../../multpoint/modbustcpip.files/modbustcpip1604.png" width="588" />

En el cuadro de diálogo anterior, haga estos ajustes:

\* Puerto de conexión: «Ethernet» (como en la figura).

<img src="../../multpoint/modbustcpip.files/modbustcpip1711.png" width="543" />

\* Ubicación del HMI: «Local» (como en la figura).

<img src="../../multpoint/modbustcpip.files/modbustcpip1752.png" width="163" />

\* Servicio de conexión: «Modbus» - «Modbus Slave TCP / IP» (como en la figura).

<img src="../../multpoint/modbustcpip.files/modbustcpip1830.png" width="531" />

Haga clic en «Parámetros» en el cuadro de diálogo de propiedades del puerto para definir la dirección IP (la del esclavo) y el puerto. Haga clic en «Aceptar».

<img src="../../multpoint/modbustcpip.files/modbustcpip2039.png" width="589" />

Descargue el proyecto al HMI y conecte el maestro y el esclavo directamente o mediante un router para la supervisión y el control.

<img src="../../multpoint/modbustcpip.files/modbustcpip2198.png" width="130" />

Con el HMI como esclavo, las direcciones son direcciones internas.
