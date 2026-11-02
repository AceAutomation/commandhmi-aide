# Controlador HaiWell

|                                                                                                                                                                                                                                                                                                                                                                                                                                                     |     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC Haiwell de la serie E/S/H. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC. |     |

<span id="OLE_LINK217"></span><span id="OLE_LINK218"></span><span id="OLE_LINK219"></span>Cómo establecer la conexión con el equipo HAIWELL<span id="OLE_LINK221"></span>

<span id="OLE_LINK222"></span><span id="OLE_LINK223"></span><span id="OLE_LINK224"></span>**1. Conexión de hardware**

<span id="OLE_LINK225"></span><span id="OLE_LINK226"></span><span id="OLE_LINK227"></span>Cable de conexión:

RS232 (puerto serie, protocolo RS232)

|                                                                                                                       |     |                          |     |
|-----------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Serie HaiWell E/S/H** |     |
| 2                                                                                                                     | RX  | 2                        | TX  |
| 3                                                                                                                     | TX  | 1                        | RX  |
| 5                                                                                                                     | GND | 3                        | GND |

|     |                                                      |     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                      |
|     | <img src="../../drivers/haiwell.files/image002.gif" width="129" /> |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     | <img src="../../drivers/haiwell.files/image003.gif" width="140" /> |
|     |                                                      |     | <img src="../../drivers/haiwell.files/image004.gif" width="280" /> |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |

<span id="OLE_LINK231"></span>El conector del HMI de la serie HM es DB9F y el del PLC Haiwell de la serie E/S/H es MD4M.

<span id="OLE_LINK237"></span>**2. Ajustes de software**

Elija Haiwell Technology Corp. en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Haiwell de la serie E/S/H.

<span id="OLE_LINK242"></span>Parámetros de conexión por defecto de la pantalla táctil

|                             |                             |                             |                                              |     |
|-----------------------------|-----------------------------|-----------------------------|----------------------------------------------|-----|
| **Parámetro**            | **Valor por defecto** |                             | **Rango de ajuste**                            |     |
| **Tipo de puerto** | RS232                       |                             | RS232/RS422/RS485                            |     |
| **Velocidad (baudios)**               | 19200                       |                             | 1200/2400/4800/9600/19200/38400/57600/115200 |     |
| **Bits de datos**         | 8                           |                             | 7/8                                          |     |
| **Paridad**              | NONE                        |                             | EVEN/ODD/NONE                                |     |
| **Bits de parada**         | 2                           |                             | 1/2                                          |     |
| **Número de estación del PLC**      | 1                           |                             | 1~31                                         |     |
| **Número de estación del HMI**      | 0                           |                             | 0~255                                        |     |
| **Función**     |                             | **Compatible** |                                              |     |
| **Simulación sin conexión**     |                             | Sí                         |                                              |     |
| **Simulación en línea**      |                             | Sí                         |                                              |     |
| **Modo extendido**           |                             | Sí                         |                                              |     |
|                             |                             |                             |                                              |     |

3\. **Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                |
| X                 | ddd                | 0~1023          | Bit: Entrada digital externa                                 |
| Y                 | ddd                | 0~1023          | Bit: Salida digital externa                                |
| M                 | ddd                | 0~12287         | Bit: Relé interno (marca)                                        |
| SM                | ddd                | 0~215           | Bit: Estado del sistema           |
| S                 | ddd                | 0~2047          | Bit: Estado de etapa                                           |
| T                 | ddd                | 0~1023          | Bit: Estado del temporizador                                          |
| C                 | ddd                | 0~255           | Bit: Estado del contador                                        |
| AI                | ddd                | 0~255           | Palabra: Registro de entrada analógica                                |
| AQ                | ddd                | 0~255           | Palabra: Registro de salida analógica                               |
| V                 | ddd                | 0~14847         | Palabra: Registro interno                                    |
| TCV               | ddd                | 0~1023          | Palabra: Valor actual del temporizador |
| CCV               | ddd                | 0~47, 80~255    | Palabra: Valor actual del contador                             |
| SV                | ddd                | 0~154           | Palabra: Registro del sistema                                      |
| CCV32             | ddd                | 0~31            | Doble palabra: Valor actual del contador                      |

<img src="../../drivers/haiwell.files/image010.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

Bit en las observaciones: el registro solo puede usarse como bit;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.

<img src="../../drivers/haiwell.files/image011.gif" width="595" />
