# Controlador de dispositivos AIBUS

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de dispositivos AIBUS mediante el protocolo AIBUS. La comunicación serie se establece entre el puerto serie del HMI y el del dispositivo AIBUS. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del dispositivo AIBUS.

**1.  Conexión de hardware**

Cable de conexión:

RS232 (puerto serie, protocolo RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Dispositivo AIBUS**  |     |
| 2                           | RX  | Pin definido por el usuario | TX  |
| 3                           | TX  | Pin definido por el usuario | RX  |
| 5                           | GND | Pin definido por el usuario | GND |

<img src="../../drivers/aibus.files/image002.gif" width="157" /><img src="../../drivers/aibus.files/image003.gif" width="130" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>El puerto de la pantalla táctil es un conector hembra Sub-D de 9 pines. La asignación de pines del dispositivo AIBUS depende de cada dispositivo.</p>
<p><strong>RS422 (puerto serie, protocolo RS422)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Dispositivo AIBUS</strong></p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table>
<table>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><img src="../../drivers/aibus.files/image004.gif" width="280" /></td>
</tr>
</tbody>
</table>
 &#10;<br />
&#10;<p>El puerto de la pantalla táctil es un conector hembra Sub-D de 9 pines. La asignación de pines del dispositivo AIBUS depende de cada dispositivo.</p>
<p><strong>RS485 (puerto serie, protocolo RS485)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Pantalla táctil COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Dispositivo AIBUS</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>D-</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>D+</p></td>
<td><p>Pin definido por el usuario</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p>El puerto de la pantalla táctil es un conector hembra Sub-D de 9 pines. La asignación de pines del dispositivo AIBUS depende de cada dispositivo.</p></td>
</tr>
</tbody>
</table>

**2. Ajustes de software**

ü Elija AIBUS Protocol en el servicio de equipo de la conexión.

ü Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

ü Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del dispositivo AIBUS.

ü Para la configuración del dispositivo AIBUS, consulte su documentación técnica.

Parámetros de conexión por defecto de la pantalla táctil

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | AIBUS Protocol              | AIBUS Protocol                               |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**              | NONE                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 1~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | Sí                         |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                      |
|-------------------|--------------------|-----------------|----------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**          |
| **Parameter**     | ddd                | 0~255           | Palabra: parámetro |
| **PV**            | d                  | 0               | Palabra: valor de salida   |
| **SV**            | d                  | 0               | Palabra: consigna      |
| **MV**            | d                  | 0               | Palabra: valor de estado    |
| **Status**        | d                  | 0               | Palabra: valor de estado    |

<img src="../../drivers/aibus.files/image005.gif" width="595" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Nota: </p>
<p>• ·d: decimal, rango de entrada 0-9;</p>
<p>• ·«Palabra» en las observaciones: el registro solo puede usarse como palabra;</p>
<p>• Los nombres y rangos de los registros pueden variar según el modelo de equipo.</p>
<p>Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/aibus.files/image006.gif" width="595" />
