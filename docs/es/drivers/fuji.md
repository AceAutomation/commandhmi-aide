# Controlador Fuji

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC Fuji de la serie NB. La comunicación serie se establece entre el puerto serie del HMI y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

**Cómo establecer la conexión con el equipo Fuji**

**1. Conexión de hardware**

Cable de conexión:

RS422<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (puerto serie, protocolo RS422)

|                         |     |                |     |
|-------------------------|-----|----------------|-----|
| HMI serie HM COM1/COM2 |     | Serie Fuji NB |     |
| 6                       | RX- | 4              | TX- |
| 7                       | RX+ | 3              | TX+ |
| 8                       | TX- | 6              | RX- |
| 9                       | TX+ | 5              | RX+ |

|     |                                                   |     |                                                   |     |                                                  |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|--------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     | <img src="../../drivers/fuji.files/image002.gif" width="95" /> |
|     | <img src="../../drivers/fuji.files/image003.gif" width="130" /> |     |                                                   |     |                                                  |
|     |                                                   |     | <img src="../../drivers/fuji.files/image004.gif" width="278" /> |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |

El conector del HMI de la serie HM es DB9F y el del PLC Fuji de la serie NB es RJ45.

**2. Ajustes de software**

Elija Fuji Electric Corporation en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Fuji de la serie NB.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie Fuji NB              | Serie Fuji NB                               |
| **Tipo de puerto** | RS422                       | RS422                                        |
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
| **Modo extendido**       | Sí                         |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                            |
| **X**             | hhh                | 0~7ff           | Bit: Entrada, solo lectura |
| **Y**             | hhh                | 0~7ff           | Bit: Salida           |
| **M**             | hhhh               | 0~7fff          | Bit: Relé interno (marca)                    |
| **SM**            | hhhh               | 8000~81ff       | Bit: Relé interno (marca)                    |
| **L**             | hhh                | 0~5ff           | Bit: Relé de bloqueo                     |
| **S**             | hh                 | 0~ff            | Bit: Relé de etapa                    |
| **T**             | hhh                | 0~1ff           | Bit: Estado del temporizador                   |
| **C**             | hh                 | 0~ff            | Bit: Estado del contador                 |
| **D**             | hhhh               | 0~7fff          | Palabra: Memoria de datos temporal           |
| **SD**            | hhhh               | 8000~80ff       | Palabra: Memoria de datos temporal           |
| **TV**            | hhh                | 0~1ff           | Palabra: Valor actual del temporizador           |
| **CV**            | hh                 | 0~ff            | Palabra: Valor actual del contador         |

<img src="../../drivers/fuji.files/image005.gif" width="595" />

Nota:

h: hexadecimal, rango de entrada 0-9, a-f;

Bit en las observaciones: el registro solo puede usarse como bit;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.

<img src="../../drivers/fuji.files/image005.gif" width="595" />
