# Controlador GE

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC GE Fanuc. La comunicación serie se establece entre el puerto serie del HMI y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

**1. Conexión de hardware**

Cable de conexión:

RS232 (puerto serie, protocolo RS232)

|                             |     |                     |     |
|-----------------------------|-----|---------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Serie GE Fanuc** |     |
| 2                           | RX  | 4                   | TX  |
| 3                           | TX  | 3                   | RX  |
| 5                           | GND | 8                   | GND |

|     |                                                 |     |                                                 |     |                                                |
|-----|-------------------------------------------------|-----|-------------------------------------------------|-----|------------------------------------------------|
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     | <img src="../../drivers/ge.files/image002.gif" width="97" /> |
|     | <img src="../../drivers/ge.files/image003.gif" width="130" /> |     |                                                 |     |                                                |
|     |                                                 |     | <img src="../../drivers/ge.files/image004.gif" width="278" /> |     |                                                |
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     |                                                |

El conector del HMI de la serie HM es DB9F y el del PLC GE Fanuc es RJ45.

**2. Ajustes de software**

Elija GE Corporation en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC GE Fanuc.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | GE Fanuc SNP-X              | GE Fanuc SNP-X/ GE Fanuc CCM                 |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**              | ODD                         | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 0                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | No                          |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                            |
|-------------------|--------------------|-----------------|----------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                |
| **%I**            | ddddd              | 1~10000         | Bit: Entrada digital        |
| **%Q**            | ddddd              | 1~10000         | Bit: Salida digital       |
| **%M**            | ddddd              | 1~10000         | Bit: Uso interno          |
| **%S**            | ddd                | 1~128           | Bit: Uso del sistema, solo lectura |
| **%SA**           | ddd                | 1~128           | Bit: Uso del sistema, solo lectura |
| **%SB**           | ddd                | 1~128           | Bit: Uso del sistema, solo lectura |
| **%SC**           | ddd                | 1~128           | Bit: Uso del sistema, solo lectura |
| **%T**            | ddd                | 1~256           | Bit: Estado temporal      |
| **%G**            | dddd               | 1~7680          | Bit: Genius Global        |
| **%AI**           | ddddd              | 1~10000         | Palabra: Entrada analógica         |
| **%AQ**           | ddddd              | 1~10000         | Palabra: Salida analógica        |
| **%R**            | ddddd              | 1~32640         | Palabra: Memoria de registros      |

 <img src="../../drivers/ge.files/image005.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Bit en las observaciones: el registro solo puede usarse como bit;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.

<img src="../../drivers/ge.files/image005.gif" width="595" />
