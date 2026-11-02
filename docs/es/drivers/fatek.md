# Controlador Fatek

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC <span id="OLE_LINK158"></span><span id="OLE_LINK159"></span>Fatek de la serie FB. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

**Cómo establecer la conexión con el equipo Fatek**

**1. Conexión de hardware**

Cable de conexión:

RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (puerto serie, protocolo RS232)

|                         |     |                 |     |
|-------------------------|-----|-----------------|-----|
| HMI serie HM COM1/COM2 |     | Serie Fatek FB |     |
| 2                       | RX  | 1               | TX  |
| 3                       | TX  | 2               | RX  |
| 5                       | GND | 4               | GND |

|     |                                                    |     |                                                    |     |                                                    |
|-----|----------------------------------------------------|-----|----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     | <img src="../../drivers/fatek.files/image006.gif" width="146" /> |
|     | <img src="../../drivers/fatek.files/image007.gif" width="129" /> |     |                                                    |     |                                                    |
|     |                                                    |     | <img src="../../drivers/fatek.files/image008.gif" width="280" /> |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |

El conector del HMI de la serie HM es DB9F y el del PLC Fatek de la serie FB es MD4M.

**2. Ajustes de software**

Elija Fatek Automation Corp. en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Fatek de la serie FB.

Parámetros de conexión por defecto de la pantalla táctil

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie Fatek FB             | Serie Fatek FB                              |
| **Tipo de puerto** | RS232                       | RS232                                        |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 7                           | 7/8                                          |
| **Paridad**              | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | Sí                         |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                                   |
|-------------------|--------------------|-----------------|---------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                       |
| X                 | dddd               | 0~9999          | Bit: Entrada, solo lectura            |
| Y                 | dddd               | 0~9999          | Bit: Relé de salida                                 |
| M                 | dddd               | 0~9999          | Bit: Relé interno (marca)                               |
| S                 | dddd               | 0~9999          | Bit: Relé de etapa                               |
| T                 | dddd               | 0~9999          | Bit: Estado del temporizador                                 |
| C                 | dddd               | 0~9999          | Bit: Estado del contador                               |
| R                 | dddd               | 0~9999          | Palabra: Registro de datos |
| D                 | dddd               | 0~9999          | Palabra: Registro de datos                               |
| TR                | dddd               | 0~9999          | Palabra: Valor actual del temporizador                      |
| CR                | dddd               | 0~9999          | Palabra: Valor actual del contador                    |
| F                 | dddd               | 0~9999          | Palabra: Registro de archivo                               |
| DRC               | ddd                | 200~255         | Doble palabra: Valor actual del contador de 32 bits      |

<img src="../../drivers/fatek.files/image009.gif" width="600" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Bit en las observaciones: el registro solo puede usarse como bit;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/fatek.files/image009.gif" width="600" />
