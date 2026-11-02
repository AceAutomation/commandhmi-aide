# Controlador HollySys

Este controlador permite a las pantallas táctiles leer y escribir datos o estados de los registros de los PLC HollySys de la serie LM. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

**Cómo establecer la conexión con un PLC de la serie HOLLYSYS**

**1.  Conexión de hardware**

Cable de conexión:

RS232 (puerto serie, protocolo RS232)

|                             |     |                        |     |
|-----------------------------|-----|------------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Serie HollySys LM** |     |
| 2                           | RX  | 3                      | TX  |
| 3                           | TX  | 2                      | RX  |
| 5                           | GND | 5                      | GND |

<img src="../../drivers/hollysys.files/image002.gif" width="130" /><img src="../../drivers/hollysys.files/image003.gif" width="290" /><img src="../../drivers/hollysys.files/image004.gif" width="130" />

El conector del HMI de la serie HM es DB9F y el del PLC HollySys de la serie LM es DB9M.

**2. Ajustes de software**

Elija HollySys Group en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC HollySys de la serie LM.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie HollySys LM          | Serie HollySys LM                           |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 38400                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**              | NONE                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 51                          | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | No                          |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                                                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                                           |
| **IX**            | ddd.o              | 0.0~511.7       | Bit: Área de memoria I, solo lectura                                                                        |
| **QX**            | ddd.o              | 0.0~511.7       | Bit: Área de memoria Q                                                                                   |
| **MX**            | dddd.o             | 0.0~7816.7      | Bit: Área de memoria M                                                                                   |
| **IW**            | ddd                | 0~510           | Palabra: Área de memoria I, registro de 8 bits, cada palabra ocupa dos direcciones |
| **QW**            | ddd                | 0~510           | Palabra: Área de memoria Q, registro de 8 bits, cada palabra ocupa dos direcciones |
| **MW**            | dddd               | 0~8190          | Palabra: Área de memoria M, registro de 8 bits, cada palabra ocupa dos direcciones                               |

<img src="../../drivers/hollysys.files/image005.gif" width="600" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Registro de 8 bits en las observaciones: la separación entre dos palabras consecutivas del registro es 2;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/hollysys.files/image005.gif" width="600" />
