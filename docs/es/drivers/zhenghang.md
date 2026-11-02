# Controlador ZhengHang

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC ZhengHang de la serie A5. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

Cómo establecer la conexión con un PLC ZhengHang de la serie A5

**1. Conexión de hardware**

Cable de conexión:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

|                           |     |                    |     |
|---------------------------|-----|--------------------|-----|
| **HMI HM COM1/COM2** |     | **ZhengHang A5　** |     |
| 2                         | RX  | 2                  | TX  |
| 3                         | TX  | 3                  | RX  |
| 5                         | GND | 5                  | GND |

<img src="../../drivers/zhenghang.files/image002.gif" width="130" /><img src="../../drivers/zhenghang.files/image003.gif" width="290" /><img src="../../drivers/zhenghang.files/image004.gif" width="130" />

El conector del HMI es DB9F y el del PLC ZhengHang de la serie A5 es DB9M.

**2. Ajustes de software**

Elija ZhengHang Electronics en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC ZhengHang de la serie A5.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie A5                   | Serie A5                                    |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**                  | NONE                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión**  | Sí                         |
| **Simulación en línea**   | Sí                         |
| **Modo extendido**       | Sí                         |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                                                           |
|-------------------|--------------------|-----------------|---------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                               |
| **I**             | dd.o               | 0.0 a 15.7     | Bit: Imagen de entradas, solo lectura                                      |
| **Q**             | dd.o               | 0.0 a 15.7     | Bit: Imagen de salidas                                                |
| **M**             | dddd.o             | 0.0 a 4095.7   | Bit: Memoria de bits (marcas)                                                           |
| **VW**            | dddd               | 0 a 1998       | Palabra: Memoria de variables, registro de 8 bits, cada palabra ocupa dos direcciones |
| **AIW**           | d                  | 0 a 9          | Palabra: Entrada analógica, solo lectura                                             |
| **AQW**           | d                  | 0 a 9          | Palabra: Salida analógica, solo escritura                                           |

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />
