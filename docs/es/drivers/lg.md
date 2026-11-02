# Controlador LG

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC LG de la serie Master-K. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

Cómo establecer la conexión con un PLC LG de la serie Master-K

**1. Conexión de hardware**

Cable de conexión:

RS232 con protocolo CNet<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> (puerto serie, protocolo RS232)

|                                                                                                                    |     |                 |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-----------------|-----|
| **HMI serie HM COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                                                  | RX  | 7               | TX  |
| 3                                                                                                                  | TX  | 4               | RX  |
| 5                                                                                                                  | GND | 5               | GND |

<img src="../../drivers/lg.files/image002.gif" width="130" /><img src="../../drivers/lg.files/image003.gif" width="291" /><img src="../../drivers/lg.files/image004.gif" width="130" />

El conector del HMI es DB9F y el del PLC LG de la serie Master-K es DB9M.

RS232 con protocolo KLoader

|                                                                                       |     |                 |     |
|---------------------------------------------------------------------------------------|-----|-----------------|-----|
| **HMI serie HM COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                     | RX  | 3               | TX  |
| 3                                                                                     | TX  | 2               | RX  |
| 5                                                                                     | GND | 5               | GND |

<img src="../../drivers/lg.files/image005.gif" width="291" /><img src="../../drivers/lg.files/image006.gif" width="130" /><img src="../../drivers/lg.files/image007.gif" width="130" />

El conector del HMI es DB9F y el del PLC LG de la serie Master-K es DB9M.

RS<span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>485

|                                                          |     |                 |
|----------------------------------------------------------|-----|-----------------|
| **HMI serie HM COM1/COM2** |     | **LG Master-K** |
| 8                                                        | D-  | B               |
| 9                                                        | D+  | A               |

 <img src="../../drivers/lg.files/image008.gif" width="157" /><img src="../../drivers/lg.files/image009.gif" width="130" />

El conector del HMI es DB9F y el del PLC LG de la serie Master-K es un borne de dos hilos.

RS232-K10S1

|                             |     |                 |     |
|-----------------------------|-----|-----------------|-----|
| **HMI serie HM COM1/COM2** |     | **LG Master-K** |     |
| 2                           | RX  | 4               | TX  |
| 3                           | TX  | 1               | RX  |
| 5                           | GND | 6               | GND |

El conector del HMI es DB9F y el del PLC LG de la serie Master-K es MD6M.

|     |                                                 |     |                                                 |
|-----|-------------------------------------------------|-----|-------------------------------------------------|
|     |                                                 |     |                                                 |
|     |                                                 |     | <img src="../../drivers/lg.files/image010.gif" width="146" /> |
|     | <img src="../../drivers/lg.files/image011.gif" width="401" /> |     |                                                 |
|     |                                                 |     |                                                 |

**2. Ajustes de software**

Elija LG Industrial Systems en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC LG de la serie Master-K.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | LG Master-K Cnet            | LG Master-K Cnet/K Loader/K10s1              |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**              | NONE                        | EVEN/ODD/NONE                                |
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

Rango de direcciones accesibles de los PLC de la serie Kxxx:

|               |                |             |                                |
|---------------|----------------|-------------|--------------------------------|
| Nombre del registro | Formato de dirección | Rango de entrada | Observaciones                        |
| P_Bit         | dddh           | 0~255f      | Bit: Área de entradas/salidas         |
| M_Bit         | dddh           | 0~255f      | Bit: Relé auxiliar (marca)           |
| K_Bit         | dddh           | 0~255f      | Bit: Relé de protección (remanente)          |
| L_Bit         | dddh           | 0~255f      | Bit: Relé de enlace                |
| F_Bit         | dddh           | 0~255f      | Bit: Relé especial             |
| P             | dddh           | 0~255f      | Palabra: Área de entradas/salidas        |
| M             | dddh           | 0~255f      | Palabra: Relé auxiliar (marca)          |
| K             | dddh           | 0~255f      | Palabra: Relé de protección (remanente)         |
| L             | dddh           | 0~255f      | Palabra: Relé de enlace               |
| F             | dddh           | 0~255f      | Palabra: Relé especial            |
| T             | ddd            | 0~255       | Bit: Relé de temporizador               |
| C             | ddd            | 0~255       | Bit: Relé de contador             |
| S             | dddd           | 0~9999      | Palabra: Registro de etapas        |
| D             | dddd           | 0~9999      | Palabra: Registro de datos            |
| TV            | ddd            | 0~255       | Palabra: Valor actual del temporizador   |
| CV            | ddd            | 0~255       | Palabra: Valor actual del contador |

Rango de direcciones accesibles de los PLC de la serie XGB CPU (comunicación por el puerto de descarga RS232 del PLC):

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                          |
| P_Bit          | ddddh        | 0-1023f      | Bit: Área de entradas/salidas            |
| M_Bit          | ddddh        | 0-1023f      | Bit: Relé auxiliar (marca)              |
| F_Bit          | ddddh        | 0-1023f      | Bit: Relé especial                |
| L_Bit          | ddddh        | 0-2047f      | Bit: Relé de enlace                   |
| K_Bit          | ddddh        | 0-4095f      | Bit: Relé de protección (remanente)             |
| D_Bit          | ddddh        | 0-10239f     |                                   |
| T              | dddd         | 0-1023       | Bit: Relé de temporizador                  |
| C              | dddd         | 0-1023       | Bit: Relé de contador                |
| TV             | dddd         | 0-1023       | Palabra: Valor actual del temporizador      |
| CV             | dddd         | 0-1023       | Palabra: Valor actual del contador    |
| P              | dddd         | 0-1023       | Palabra: Área de entradas/salidas           |
| M              | dddd         | 0-1023       | Palabra: Relé auxiliar (marca)             |
| F              | dddd         | 0-1023       | Palabra: Relé especial (solo lectura) |
| L              | dddd         | 0-2047       | Palabra: Relé de enlace                  |
| K              | dddd         | 0-4095       | Palabra: Relé de protección (remanente)            |
| D              | dddd         | 0-10239      | Palabra: Registro de datos               |
| R              | dddd         | 0-10239      | Palabra: Registro de etapas           |
| ZR             | dddd         | 0-10239      | Palabra:                             |
| S              | ddd          | 0-127        | Palabra: Registro de etapas           |
| Z              | ddd          | 0-127        | Palabra:                             |
| U              | dd.dd        | 0.0-10.31    | Palabra：(solo lectura)               |

Rango de direcciones accesibles de los PLC de la serie XGB CNET:

|               |                |             |                         |
|---------------|----------------|-------------|-------------------------|
| Nombre del registro | Formato de dirección | Rango de entrada | Observaciones                 |
| P             | dddh           | 0~127f      | Palabra: Área de entradas/salidas |
| M             | dddh           | 0~255f      | Palabra: Relé auxiliar (marca)   |
| K             | dddh           | 0~2559f     | Palabra: Relé de protección (remanente)  |
| L             | dddh           | 0~1279f     | Palabra: Relé de enlace        |
| F             | dddh           | 0~255f      | Palabra: Relé especial     |
| T             | ddd            | 0~255       | Bit: Relé de temporizador        |
| C             | ddd            | 0~255       | Bit: Relé de contador      |
| S             | ddd            | 0~127.99    | Palabra: Registro de etapas |
| D             | dddd           | 0~5119      | Palabra: Registro de datos     |
| N             | dddd           | 0~3935      |                         |
| Z             | ddd            | 0~127       |                         |
| ZR            | dddd           | 0~1023      |                         |
| U             | d              | 0~7.31      |                         |

XGB TCP/IP

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                          |
| P_Bit          | ddddh        | 0-2047f      | Bit: Área de entradas/salidas            |
| M_Bit          | ddddh        | 0-2047f      | Bit: Relé auxiliar (marca)              |
| F_Bit          | ddddh        | 0-2047f      | Bit: Relé especial                |
| L_Bit          | ddddh        | 0-4095f      | Bit: Relé de enlace                   |
| K_Bit          | ddddh        | 0-8191f      | Bit: Relé de protección (remanente)             |
| T              | dddd         | 0-2047       | Bit: Relé de temporizador                  |
| C              | dddd         | 0-2047       | Bit: Relé de contador                |
| TV             | dddd         | 0-2047       | Palabra: Valor actual del temporizador      |
| CV             | dddd         | 0-2047       | Palabra: Valor actual del contador    |
| P              | dddd         | 0-2047       | Palabra: Área de entradas/salidas           |
| M              | dddd         | 0-2047       | Palabra: Relé auxiliar (marca)             |
| F              | dddd         | 0-2047       | Palabra: Relé especial (solo lectura) |
| L              | dddd         | 0-4095       | Palabra: Relé de enlace                  |
| K              | dddd         | 0-8191       | Palabra: Relé de protección (remanente)            |
| D              | ddddd        | 0-19999      | Palabra: Registro de datos               |
| R              | ddddd        | 0-16383      |                                   |
| S              | ddd          | 0-127        | Palabra: Registro de etapas           |
| Z              | ddd          | 0-127        |                                   |
| U              | dd.dd        | 0.0-11.31    |                                   |
| N              | ddddd        | 0-10239      | Palabra：(solo lectura)               |

<img src="../../drivers/lg.files/image012.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

h: hexadecimal, rango de entrada 0-9, a-f;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/lg.files/image013.gif" width="595" />
