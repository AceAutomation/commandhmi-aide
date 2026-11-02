# Propiedades del puerto de comunicación

Aquí se definen los parámetros de comunicación entre el HMI y los equipos conectados.

Haga doble clic en «Conexión» (Link) y después en Conexión 1, como en la figura 7-1:

<img src="../../setting/com.files/image004.jpg" width="532" />

Figura 7-1      Cuadro de diálogo Propiedades de COM1

En la página «Conexión» hay muchas marcas y modelos de PLC disponibles, además del «Nombre de la conexión» y el «Intervalo de direcciones continuas del PLC»

Haga clic en la pestaña «Parámetros», como en la figura 7-2:

<img src="../../setting/com.files/image005.jpg" width="532" />

Figura 7-2      Parámetros del puerto de comunicación COM1

**Parámetros:**

Servicio de equipo: fabricante, marca de PLC y modelo de CPU.

Puerto: RS232 / 485/ 422

Velocidad: 1200/2400/4800/9600/19200/38400/57600/115200 / 187.5k

Paridad: Odd / Even / None

Bits de datos: 7/8

Bits de parada: 1/2

Modelo: modelo de PLC

Número de estación del HMI: número de estación del HMI

Tiempo de comunicación: el HMI envía datos al PLC y recibe su respuesta; no puede volver a enviar hasta que transcurra este tiempo.

Tiempo de espera 1 y tiempo de espera 2: el tiempo de espera se calcula a partir de ambos; en la figura anterior es de 200 ms. Si el HMI no recibe respuesta 200 ms después de enviar, se produce un tiempo de espera agotado.

Número de reintentos: número de reenvíos tras un tiempo de espera agotado

Modo de direccionamiento: ① Modo estándar: un puerto serie con un PLC; ② Modo extendido: un puerto serie con varios PLC del mismo tipo

Intervalo de direcciones continuas del PLC: número máximo de palabras que el PLC puede leer de una vez
