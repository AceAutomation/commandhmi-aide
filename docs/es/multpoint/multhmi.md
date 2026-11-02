# Conexión «un equipo, varios HMI»

Las pantallas táctiles CommandHMI permiten la conexión «un equipo, varios HMI» con un PLC mediante el protocolo MODBUS. Las pantallas se conectan una tras otra y la primera se conecta al PLC. Primera opción: todas las pantallas son esclavas y el PLC es maestro. Haga doble clic en «Conexión COM1» en el gestor de proyecto; se abre la ventana de propiedades del puerto de comunicación. En «Servicio de equipo» de la página «General», elija Modbus RTU y a la derecha Modbus RTU Slave. Segunda opción: la primera pantalla, conectada al PLC, es maestra y el PLC y las demás pantallas son esclavos. En ese caso, para la primera pantalla elija Modbus RTU en «Servicio de equipo» de la página «General» y a la derecha Modbus RTU Master, active el modo extendido en la página «Parámetros» y asigne las direcciones de las pantallas. Las pantallas esclavas se comunican así con el PLC a través de la primera. En ambos casos, solo el maestro se comunica con los esclavos; los esclavos no se comunican entre sí.

Con el PLC como maestro y todas las pantallas como esclavas:

1. El puerto de comunicación del PLC es RS232; el cableado y los ajustes se muestran en las figuras 8-1, 8-2 y 8-3:

<img src="../../multpoint/multhmi.files/multhmi1428.png" width="577" />

Figura 8-1  Esquema «un equipo, varios HMI» con el PLC (RS232) como maestro

<img src="../../multpoint/multhmi.files/multhmi1528.png" width="589" />

Figura 8-2 Elección del protocolo MODBUS como esclavo

<img src="../../multpoint/multhmi.files/multhmi1593.png" width="588" />

Figura 8-3 Asignación de la dirección de estación del HMI

2. El puerto de comunicación del PLC es RS485; el cableado se muestra en la figura 8-4:

<img src="../../multpoint/multhmi.files/multhmi1744.png" width="598" />

Figura 8-4  Esquema «un equipo, varios HMI» con el PLC (RS485) como maestro

Con el PLC en RS485 y todas las pantallas como esclavas, los ajustes son los mismos que con RS232. Véanse las figuras 8-2 y 8-3.

Con todos los HMI como esclavos, pueden conectarse hasta 255 HMI. Pero cuantas más pantallas, más lenta es la respuesta.

 Con la primera pantalla como maestra y el PLC y los demás HMI como esclavos:

1. El puerto de comunicación del PLC es RS232; el cableado y los ajustes se muestran en las figuras 8-5, 8-6 y 8-7:

<img src="../../multpoint/multhmi.files/multhmi2462.png" width="579" />

Figura 8-5   Esquema «un equipo, varios HMI» con el PLC (RS232) como esclavo

<img src="../../multpoint/multhmi.files/multhmi2563.png" width="588" />

Figura 8-6 Elección del protocolo MODBUS como maestro para la primera pantalla

<img src="../../multpoint/multhmi.files/multhmi2650.png" width="590" />

Figura 8-7 Con la primera pantalla como maestra, se necesita el modo extendido

Los ajustes de las pantallas esclavas son similares a los de las figuras 8-2 y 8-3.

<img src="../../multpoint/multhmi.files/multhmi2852.png" width="130" />

Nota: como RS232 no admite conexiones multipunto, si el PLC de la conexión «un equipo, varios HMI» no tiene puerto RS485, hace falta un convertidor RS485/RS232.

Nota: si una pantalla de la serie es maestra en la conexión «un equipo, varios HMI», su modo de direccionamiento debe ser multiprotocolo.

Con Modbus como maestro pueden añadirse en principio hasta 255 esclavos; cuantos más esclavos, más lenta es la comunicación.
