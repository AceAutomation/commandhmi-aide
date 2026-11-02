# Controlador Mitsubishi

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie Melsec FXxn/Q00J/C24N. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie Melsec FXxn/Q00J/Q00U/C24N</p>
<p><strong>1.  Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS422- Melsec-FXxn/FX3U/3G<span id="OLE_LINK1"></span><span id="OLE_LINK3"></span><span id="OLE_LINK2"></span> <span id="OLE_LINK24"></span><span id="OLE_LINK26"></span><span id="OLE_LINK25"></span>(puerto serie, protocolo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Melsec-FXxn</strong></p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>7</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>1</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>2</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/mitsubishi.files/image002.gif" width="145" /><img src="../../drivers/mitsubishi.files/image003.gif" width="280" /><img src="../../drivers/mitsubishi.files/image004.gif" width="130" />

El conector de la pantalla táctil es DB9F y el del PLC Melsec de la serie FXxn es MD8M.

**RS232- Melsec-Q00J/Q00U**

|                                                                                       |     |              |     |
|---------------------------------------------------------------------------------------|-----|--------------|-----|
| **HMI serie HM COM1/COM2** |     | **Q00J CPU** |     |
| **2**                                                                                 | RX  | 2            | TX  |
| **3**                                                                                 | TX  | 1            | RX  |
| **5**                                                                                 | GND | 3            | GND |

<img src="../../drivers/mitsubishi.files/image005.gif" width="146" /><img src="../../drivers/mitsubishi.files/image006.gif" width="280" /><img src="../../drivers/mitsubishi.files/image007.gif" width="130" />

El conector de la pantalla táctil es DB9F y el del PLC Melsec de la serie FXxn es MD8M.

Nota: conexión del Q00U

Q00U: puentear los pines 5 y 6 del conector de 6 pines

Software de programación MITSUBISHI: parámetros &gt; parámetros del PLC -- &gt; ajustes de comunicación serie

Active la función de comunicación serie, elija 115200 baudios, marque la suma de control y marque «Escritura en RUN»

Use el cable de comunicación MITSUBISHI, conectado directamente al HMI

**RS232- módulo Melsec-QC24N**

|                             |     |              |     |
|-----------------------------|-----|--------------|-----|
| **HMI serie HM COM1/COM2** |     | **Q00J CPU** |     |
| **2**                       | RX  | 3            | TX  |
| **3**                       | TX  | 2            | RX  |
| **5**                       | GND | 5            | GND |

<img src="../../drivers/mitsubishi.files/image008.gif" width="130" /><img src="../../drivers/mitsubishi.files/image009.gif" width="290" /><img src="../../drivers/mitsubishi.files/image010.gif" width="130" />

El conector de la pantalla táctil es DB9F y el del módulo Melsec QC24N es MB9M.

**2. Ajustes de software**

Elija MITSUBISHI en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Melsec de la serie FXxn/Q00J/C24N.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Melsec-FX2N                 | Melsec-FX/ FX2N/ FX3U/3G /Q_C24N Q00J        |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 7                           | 7/8                                          |
| **Paridad**              | EVEN                        | EVEN/ODD/NONE                                |
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

Melsec-FXxn/FX3U/3G/ FX3U-Ethernet

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                  |
| **X**             | oooo               | 0~377           | Bit: Bobina de entrada, solo lectura                   |
| **Y**             | oooo               | 0~377           | Bit: Bobina de salida                             |
| **M**             | dddd               | 0~7999          | Bit: Relé intermedio (marca)                      |
| **SM**            | dddd               | 8000~8999       | Bit: Relé intermedio especial              |
| **S**             | dddd               | 0~999           | Bit: Bit de estado                              |
| **T**             | dddd               | 0~256           | Bit: Estado del temporizador                         |
| **C**             | dddd               | 0~256           | Bit: Estado del temporizador                         |
| **D_Bit**         | dddd.dd            | 0.00~7999.15    | Bit: Bit de un registro de 16 bits                  |
| **D**             | dddd               | 0~7999          | Palabra: Registro                               |
| **SD**            | dddd               | 8000~8999       | Palabra: Registro especial                       |
| **TV**            | dddd               | 0~255           | Palabra: Valor actual del temporizador                 |
| **CV**            | dddd               | 0~199           | Palabra: Valor actual del contador               |
| **CV32**          | dddd               | 200~255         | Doble palabra: Valor actual del contador de 32 bits |

FX5U/FX5U-Ethernet

|                   |                    |                               |                                         |
|-------------------|--------------------|-------------------------------|-----------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada**               | **Observaciones**                             |
| **X**             | oooo               | 0~1777                        | Bit: Bobina de entrada, solo lectura              |
| **Y**             | oooo               | 0~1777                        | Bit: Bobina de salida                        |
| **M**             | dddd               | 0~7679                        | Bit: Relé interno (marca)                     |
| **L**             | dddd               | 0~7679                        | Bit: Relé de enclavamiento                     |
| **F**             | ddd                | 0~127                         | Bit: Relé de alarma                        |
| **TS**            | ddd                | 0~511                         | Bit: Contacto de temporizador                      |
| **CS**            | ddd                | 0~255                         | Bit: Contacto de contador                    |
| **S**             | dddd               | 0~4095                        | Bit: Relé de etapa                     |
| **SM**            | dddd               | 0~9999                        | Bit: Relé especial                      |
| **B**             | hh                 | 0-ff (hexadecimal)  | Bit: Bit: relé de enlace                     |
| **D_Bit**         | dddd.dd            | 0.0~7999.15                   | Bit: Bit de un registro de 16 bits             |
| **D**             | dddd               | 0~7999                        | Palabra: Registro                          |
| **R**             | ddddd              | 0~32767                       | Palabra: Valor actual acumulado del temporizador |
| **W**             | hhh                | 0-1ff (hexadecimal) | Palabra: Registro de enlace                     |
| **CN**            | ddd                | 0~255                         | Palabra: Valor actual del registro         |
| **TN**            | ddd                | 0~511                         | Palabra: Valor actual del temporizador            |
| **SD**            | ddddd              | 0~11999                       | Palabra: Registro especial                  |

  Melsec-Q00J/QC24N

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                    |
| **X**             | hhh                | 0~7ff           | Bit: Relé de entrada, solo lectura    |
| **Y**             | hhh                | 0~7ff           | Bit: Relé de salida              |
| **M**             | dddd               | 0~8191          | Bit: Relé interno (marca)            |
| **L**             | dddd               | 0~2047          | Bit: Relé de enclavamiento            |
| **F**             | dddd               | 0~2047          | Bit: Alarma                     |
| **V**             | dddd               | 0~2047          | Bit: Relé de índice            |
| **S**             | dddd               | 0~2047          | Bit: Relé de etapa            |
| **B**             | hhh                | 0~7ff           | Bit: Relé de conversión          |
| **SB**            | hhh                | 0~3ff           | Bit: Relé de enlace especial        |
| **T**             | ddd                | 0~511           | Bit: Estado del temporizador           |
| **C**             | ddd                | 0~511           | Bit: Estado del contador         |
| **D**             | ddddd              | 0~11135         | Palabra: Registro de datos            |
| **W**             | hhh                | 0~7ff           | Palabra: Registro de conversión      |
| **SW**            | hhh                | 0~3ff           | Palabra: Registro de enlace especial    |
| Z                 | d                  | 0~9             | Palabra: Registro de índice           |
| TV                | ddd                | 0~511           | Palabra: Valor actual del temporizador   |
| CV                | ddd                | 0~511           | Palabra: Valor actual del contador |

Q00U

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                    |
| **X**             | hhhh               | 0~1fff          | Bit: Relé de entrada, solo lectura    |
| **Y**             | hhhh               | 0~1fff          | Bit: Relé de salida              |
| **M**             | dddd               | 0~8191          | Bit: Relé interno (marca)            |
| **L**             | dddd               | 0~8191          | Bit: Relé de enclavamiento            |
| **F**             | dddd               | 0~2047          | Bit: Relé de alarma               |
| **V**             | dddd               | 0~2047          | Bit: Relé de índice            |
| **B**             | ffff               | 0~1fff          | Bit: Relé de conversión          |
| **T**             | ddd                | 0~2047          | Bit: Estado del temporizador           |
| **C**             | dddd               | 0~1023          | Bit: Estado del contador         |
| **SB**            | hhh                | 0~7ff           | Bit: Relé de enlace especial        |
| **SM**            | ddd                | 0~2047          | Bit: Relé especial             |
| **D_Bit**         | Dddd.h             | 0.0~12287.f     | Bit: Bit de un registro de 16 bits    |
| **D**             | Dddd               | 0~12287         | Palabra: Registro de datos            |
| **W**             | Hhhh               | 0~1fff          | Palabra: Registro de conversión      |
| **TV**            | Dddd               | 0~2047          | Palabra: Valor actual del temporizador   |
| **CV**            | Dddd               | 0~1023          | Palabra: Valor actual del contador |
| **SW**            | Hhh                | 0~7ff           | Palabra: Registro de enlace especial    |
| **SD**            | Dddd               | 0~2047          | Palabra: Registro especial         |
| **Z**             | Dd                 | 0~19            | Palabra: Registro de índice           |

Melsec-E71

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                    |
| **X**             | hhhh               | 0~1fff          | Bit: Relé de entrada, solo lectura    |
| **Y**             | hhhh               | 0~1fff          | Bit: Relé de salida              |
| **M**             | dddd               | 0~8191          | Bit: Relé interno (marca)            |
| **L**             | dddd               | 0~8191          | Bit: Relé de enclavamiento            |
| **F**             | dddd               | 0~2047          | Bit: Relé de alarma               |
| **V**             | dddd               | 0~2047          | Bit: Relé de índice            |
| **S**             | dddd               | 0~8191          | Bit: Relé de etapa            |
| **B**             | ffff               | 0~1fff          | Bit: Relé de conversión          |
| **T**             | ddd                | 0~2047          | Bit: Estado del temporizador           |
| **C**             | dddd               | 0~1023          | Bit: Estado del contador         |
| **SB**            | hhh                | 0~7ff           | Bit: Relé de enlace especial        |
| **SM**            | ddd                | 0~2047          | Bit: Relé especial             |
| **D_Bit**         | Dddd.h             | 0.0~12287.f     | Bit: Bit de un registro de 16 bits    |
| **D**             | Dddd               | 0~12287         | Palabra: Registro de datos            |
| **W**             | Hhhh               | 0~1fff          | Palabra: Registro de conversión      |
| **TV**            | Dddd               | 0~2047          | Palabra: Valor actual del temporizador   |
| **CV**            | Dddd               | 0~1023          | Palabra: Valor actual del contador |
| **SW**            | Hhh                | 0~7ff           | Palabra: Registro de enlace especial    |
| **SD**            | Dddd               | 0~2047          | Palabra: Registro especial         |
| **Z**             | Dd                 | 0~19            | Palabra: Registro de índice           |

Melsec-LCPU

|                |              |              |                                |
|----------------|--------------|--------------|--------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                       |
| **X**          | hhhh         | 0~1fff       | Bit: Relé de entrada, solo lectura    |
| **Y**          | hhhh         | 0~1fff       | Bit: Relé de salida              |
| **M**          | dddd         | 0~8191       | Bit: Relé interno (marca)            |
| **L**          | dddd         | 0~8191       | Bit: Relé de enclavamiento            |
| **F**          | dddd         | 0~2047       | Bit: Relé de alarma               |
| **V**          | dddd         | 0~2047       | Bit: Relé de índice            |
| **S**          | dddd         | 0~8191       | Bit: Relé de etapa            |
| **B**          | hhhh         | 0~1fff       | Bit: Relé de conversión          |
| **SB**         | hhh          | 0~7ff        | Bit: Relé de enlace especial        |
| **T**          | dddd         | 0~2047       | Bit: Estado del temporizador           |
| **C**          | dddd         | 0~1023       | Bit: Estado del contador         |
| **D-bit**      | ddddd.dd     | 0~45055.15   | Bit: Bit de un registro de 16 bits    |
| **D**          | ddddd        | 0~45055      | Palabra: Registro de datos            |
| **TV**         | dddd         | 0~2047       | Palabra: Valor actual del temporizador   |
| **CV**         | dddd         | 0~1023       | Palabra: Valor actual del contador |
| **W**          | hhhh         | 0~1fff       | Palabra: Registro de conversión      |
| **SW**         | hhh          | 0~7ff        | Palabra: Registro de enlace especial    |
| **SD**         | hhhh         | 0~2047       | Palabra: Registro especial         |
| **Z**          | hh           | 0~19         | Palabra: Registro de índice           |

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

h: hexadecimal, rango de entrada 0-9, a-f;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

**4. Conexión de los HMI de la serie HM con el PLC FX5U de Mitsubishi**

Abra GX Works3 - Nuevo archivo - Serie FX5CPU - Tipo FX5U

<img src="../../drivers/mitsubishi.files/image012.gif" width="384" />

Navegación - Parámetros - Parámetros del módulo - Ethernet

<img src="../../drivers/mitsubishi.files/image013.gif" width="1092" />

Conexión de objetos - Ajustes específicos

<img src="../../drivers/mitsubishi.files/image014.gif" width="1024" />

Software CommandHMI: página «General»

<img src="../../drivers/mitsubishi.files/image015.gif" width="532" />

Conexión - Parámetros

<img src="../../drivers/mitsubishi.files/image016.gif" width="532" />
