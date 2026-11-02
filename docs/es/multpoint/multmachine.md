# Conexión «un HMI, varios equipos»

Además de la conexión «un equipo, varios HMI», los HMI de la serie permiten la conexión «un HMI, varios equipos» con PLC mediante MODBUS. Una pantalla táctil accede directamente a los registros de varios PLC conectados, siempre que admitan MODBUS. En los ajustes, elija Modbus RTU en «Servicio de equipo» de la página «General» y a la derecha Modbus RTU Master: la pantalla es maestra y todos los PLC son esclavos. La pantalla puede acceder entonces a los registros de los PLC, cuyos nombres corresponden a los del protocolo MODBUS.

<img src="../../multpoint/multmachine.files/multmachine744.png" width="506" />

Figura 8-8      Conexión «un HMI, varios equipos»

<img src="../../multpoint/multmachine.files/multmachine805.png" width="590" />

Figura 8-9      Pantalla táctil como maestra

<img src="../../multpoint/multmachine.files/multmachine857.png" width="588" />

Figura 8-10    Con la pantalla táctil como maestra, se necesita el modo extendido

Tras este ajuste, las direcciones de PLC de las propiedades del puerto ya no se usan. Al introducir la dirección de un objeto aparece el campo de dirección de la figura 8-11. A la derecha del nombre del registro hay una lista desplegable en la que se elige la dirección de esclavo del PLC.

<img src="../../multpoint/multmachine.files/multmachine1294.png" width="251" />

Figura 8-11    Campo de introducción de dirección

<img src="../../multpoint/multmachine.files/multmachine1326.png" width="130" />

**Direcciones de activación de la comunicación por estación en modo extendido:**

Cada puerto serie tiene asignadas 16 palabras para activar los números de estación, es decir, hasta 256 estaciones; la dirección base es LW59000

COM1 corresponde a 59010~59025: LW59010 a las estaciones 0~15, LW59011 a las estaciones 16~31, etc.

COM2 corresponde a 59026~59041: LW59026 a las estaciones 0~15, LW59027 a las estaciones 16~31, etc.

Ethernet corresponde a 59026~59041: LW59026 a las estaciones 0~15, LW59027 a las estaciones 16~31, etc.

Al arrancar el HMI todo está activado; un script puede activar o desactivar cada estación mediante su bit.

<img src="../../multpoint/multmachine.files/multmachine1993.png" width="130" />

Nota: como RS232 no admite conexiones multipunto, si el PLC de la conexión «un HMI, varios equipos» no tiene puerto RS485, hace falta un convertidor RS485/RS232.
