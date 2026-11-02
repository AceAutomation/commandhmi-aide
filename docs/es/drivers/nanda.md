# Controlador Nanda

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie Nanda NA-200/400. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie Nanda NA-200/400</p>
<p><strong>1.  Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Nanda NA-200/400</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>2</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/nanda.files/image002.gif" width="130" /><img src="../../drivers/nanda.files/image003.gif" width="290" /><img src="../../drivers/nanda.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

El conector del HMI es DB9F y el del PLC Nanda de la serie NA-200/400 es DB9M.

**2. Ajustes de software**

Elija Nanda Auto Technology en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Nanda de la serie NA-200/400.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Nanda NA-200                | Nanda NA-200/400                             |
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

**3. Registros accesibles y rangos de direcciones**

Nanda NA-200

|                   |                    |                 |                                                                                                                               |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                                                                   |
| **I**             | ddd                | 1~128           | Bit: Entrada digital, solo lectura |
| **Q**             | ddd                | 1~128           | Bit: Salida digital                                                                                                  |
| **M**             | dddd               | 1~1024          | Bit: Registro de bits                                                                                                             |
| **S**             | ddd                | 1~256           | Bit: Registro de bits del sistema                                                                                                      |
| **N**             | ddd                | 1~256           | Bit: Registro de bits remanente (protegido ante cortes)                                                                                |
| **IW**            | dd                 | 1~32            | Palabra: Entrada analógica                                                                                                   |
| **QW**            | dd                 | 1~32            | Palabra: Salida analógica                                                                                                  |
| **MW**            | dddd               | 1~1024          | Palabra: Registro de palabras                                                                                                           |
| **SW**            | ddd                | 1~256           | Palabra: Registro de palabras del sistema                                                                                                    |
| **NW**            | ddd                | 1~256           | Palabra: Registro de palabras remanente (protegido ante cortes)                                                                              |

Nanda NA-400

|                   |                    |                 |                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                      |
| **I**             | ddd                | 1~2048          | Bit: Entrada digital, solo lectura           |
| **Q**             | ddd                | 1~2048          | Bit: Salida digital                     |
| **M**             | dddd               | 1~8192          | Bit: Registro de bits                                |
| **S**             | ddd                | 1~4096          | Bit: Registro de bits del sistema                         |
| **N**             | ddd                | 1~2048          | Bit: Registro de bits remanente (protegido ante cortes)   |
| **IW**            | dd                 | 1~512           | Palabra: Entrada analógica                      |
| **QW**            | dd                 | 1~512           | Palabra: Salida analógica                     |
| **MW**            | dddd               | 1~8192          | Palabra: Registro de palabras                              |
| **SW**            | ddd                | 1~2048          | Palabra: Registro de palabras del sistema                       |
| **NW**            | ddd                | 1~2048          | Palabra: Registro de palabras remanente (protegido ante cortes) |

<img src="../../drivers/nanda.files/image005.gif" width="596" />

Nota:

d: decimal, rango de entrada 0-9;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/nanda.files/image006.gif" width="595" />
