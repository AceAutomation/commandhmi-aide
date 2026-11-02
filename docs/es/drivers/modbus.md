# Controlador Modbus

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los <span id="OLE_LINK37"></span><span id="OLE_LINK38"></span>dispositivos MODBUS. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del dispositivo MODBUS. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del dispositivo MODBUS.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un dispositivo MODBUS</p>
<p><strong>1.</strong> <strong>Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS232<span id="OLE_LINK24"></span><span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK62"></span><span id="OLE_LINK63"></span><span id="OLE_LINK64"></span><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Dispositivo Modbus</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modbus.files/image002.gif" width="157" /><img src="../../drivers/modbus.files/image003.gif" width="130" />

El conector del HMI es DB9F. La asignación de pines del dispositivo Modbus depende de cada dispositivo.

**RS422**

|                                                                                                                    |     |                   |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Modbus device** |     |
| 6                                                                                                                  | RX- | Pin definido por el usuario | TX- |
| 7                                                                                                                  | RX+ | Pin definido por el usuario | TX+ |
| 8                                                                                                                  | TX- | Pin definido por el usuario | RX- |
| 9                                                                                                                  | TX+ | Pin definido por el usuario | RX+ |

<img src="../../drivers/modbus.files/image004.gif" width="157" /><img src="../../drivers/modbus.files/image005.gif" width="130" />

El conector del HMI es DB9F. La asignación de pines del dispositivo Modbus depende de cada dispositivo.

**RS485**

|                                                                                       |     |                   |     |
|---------------------------------------------------------------------------------------|-----|-------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Modbus device** |     |
| 8                                                                                     | D-  | Pin definido por el usuario | B   |
| 9                                                                                     | D+  | Pin definido por el usuario | A   |

<img src="../../drivers/modbus.files/image006.gif" width="157" /><img src="../../drivers/modbus.files/image007.gif" width="130" />

El conector del HMI es un conector hembra Sub-D de 9 pines. La asignación de pines del dispositivo Modbus depende de cada dispositivo.

**TCP/IP (conexión directa RJ45)**

|                                                                                                                    |      |                   |      |
|--------------------------------------------------------------------------------------------------------------------|------|-------------------|------|
| **HMI serie HM COM1/COM2** |      | **Modbus device** |      |
| 1                                                                                                                  | TX+  | 3                 | RX+  |
| 2                                                                                                                  | TX-  | 6                 | RX-  |
| 3                                                                                                                  | RX+  | 1                 | TX+  |
| 4                                                                                                                  | BD4+ | 4                 | BD4+ |
| 5                                                                                                                  | BD4- | 5                 | BD4- |
| 6                                                                                                                  | RX-  | 2                 | TX-  |
| 7                                                                                                                  | BD3+ | 7                 | BD3+ |
| 8                                                                                                                  | BD3- | 8                 | BD3- |

|     |                                                    |     |                                                     |     |                                                    |
|-----|----------------------------------------------------|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                     |     |                                                    |
|     | <img src="../../drivers/modbus.files/image008.gif" width="95" /> |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     | <img src="../../drivers/modbus.files/image009.gif" width="95" /> |
|     |                                                    |     | <img src="../../drivers/modbus.files/image010.gif" width="267" /> |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |

<span id="OLE_LINK68"></span><span id="OLE_LINK69"></span><span id="OLE_LINK70"></span>

El conector del HMI es RJ45 y el del dispositivo Modbus es RJ45.

**TCP/IP (conexión RJ45 a través de router)**

|                       |      |               |      |
|-----------------------|------|---------------|------|
| **HMI HM COM1/COM2** |      | Modbus device |      |
| 1                     | TX+  | 3             | RX+  |
| 2                     | TX-  | 6             | RX-  |
| 3                     | RX+  | 1             | TX+  |
| 4                     | BD4+ | 4             | BD4+ |
| 5                     | BD4- | 5             | BD4- |
| 6                     | RX-  | 2             | TX-  |
| 7                     | BD3+ | 7             | BD3+ |
| 8                     | BD3- | 8             | BD3- |

<img src="../../drivers/modbus.files/image011.gif" width="95" />

|     |                                                     |     |                                                    |
|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                     |     |                                                    |
|     |                                                     |     | <img src="../../drivers/modbus.files/image012.gif" width="95" /> |
|     | <img src="../../drivers/modbus.files/image013.gif" width="267" /> |     |                                                    |
|     |                                                     |     |                                                    |

El conector del HMI es RJ45 y el del dispositivo Modbus es RJ45.

**2. Ajustes de software**

Elija Modbus en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del equipo conectado, consulte la documentación técnica del dispositivo Modbus.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | RTU Master                  | RTU/RTU_S/ASCII/ASCII_S Master               |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**              | NONE                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | Sí                         |

<img src="../../drivers/modbus.files/image014.gif" width="595" />

Nota: en RTU_S y ASCII_S, la escritura de datos usa el código de función 0x10 (sea cual sea la longitud de los datos escritos);

·Si el número de estación del PLC es 0, el sistema funciona en modo difusión (broadcast).

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                                                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                                      |
| 0x                | ddddd              | 0~65535         | Bit: Bobina de entrada                                                                                  |
| 1x                | ddddd              | 0~65536         | Bit: Bobina de entrada, solo lectura                                                                       |
| 3x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit: Bit de un registro de entrada de 16 bits, solo lectura                       |
| 4x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit: Bit de un registro de salida de 16 bits                                                               |
| 3x                | ddddd              | 0~65535         | Palabra: Registro de entrada de 16 bits, solo lectura                                                           |
| 4x                | ddddd              | 0~65535         | Palabra: Registro de salida de 16 bits                                                                     |
| 3x_D              | ddddd              | 0~65535         | Doble palabra: Registro de entrada, con los 16 bits altos y bajos de la doble palabra 3x invertidos, solo lectura |
| 4x_D              | ddddd              | 0~65535         | Doble palabra: Registro de salida, con los 16 bits altos y bajos de la doble palabra 4x invertidos           |

Modbus Slave

|                       |                             |                 |                                                                |
|-----------------------|-----------------------------|-----------------|----------------------------------------------------------------|
| **Registro interno** | **Código de función admitido** | **Rango de entrada** | **Observación**                                                     |
| LB                    | 01/02/05/15                 | 0~59999         | Bit：Leer y escribir la dirección interna de la pantalla táctil (LB) |
| LW                    | 03/04/06/16                 | 0~59999         | Palabra：Leer y escribir la dirección interna de la pantalla táctil  |

<img src="../../drivers/modbus.files/image015.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

DD: 16 bits, rango de entrada 0-15;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/modbus.files/image016.gif" width="595" />
