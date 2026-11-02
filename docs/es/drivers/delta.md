# Controlador Delta

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los <span id="OLE_LINK42"></span><span id="OLE_LINK43"></span>Registros de los PLC de la serie Delta DVP. La comunicación serie se establece entre el puerto serie del HMI y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie Delta DVP</p>
<p><strong>1.  Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK53"></span><span id="OLE_LINK2"></span> (puerto serie, protocolo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI serie HM COM1/COM2</p></td>
<td colspan="2"><p>Serie Delta DVP</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/delta.files/image008.gif" width="281" /><img src="../../drivers/delta.files/image009.gif" width="146" /><img src="../../drivers/delta.files/image010.gif" width="130" />  </p>
<p><span id="OLE_LINK54"></span>El conector del HMI de la serie HM es DB9F; el del PLC Delta DVP es MD8M.</p>
<p>RS485 (puerto serie, protocolo RS485)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI serie HM COM1/COM2</p></td>
<td><p>Serie Delta DVP</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/delta.files/image011.gif" width="130" /><img src="../../drivers/delta.files/image012.gif" width="156" /></p>
<p>El conector de la serie HM es DB9F; el del PLC Delta DVP es un borne de dos hilos.</p></td>
</tr>
</tbody>
</table>

**2. Ajustes de software**

ü Elija Delta Corporation en el servicio de equipo de la conexión.

ü Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

ü Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

ü Para la configuración del PLC, consulte la documentación técnica de los PLC Delta de la serie DVP.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Delta DVP Series            | Delta DVP Series                             |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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

|                   |                    |                 |                                               |
|-------------------|--------------------|-----------------|-----------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                   |
| **X**             | ooo                | 0~377           | Bit: Entrada, solo lectura        |
| **Y**             | ooo                | 0~377           | Bit: Salida                  |
| **M**             | dddd               | 0~4095          | Bit: Relé auxiliar (marca)                          |
| **S**             | dddd               | 0~1023          | Bit: Relé interno (marca)                           |
| **T**             | ddd                | 0~255           | Bit: Estado del temporizador                             |
| **C**             | ddd                | 0~255           | Bit: Estado del contador                           |
| **D**             | dddd               | 0~9999          | Palabra: Memoria de datos temporal                  |
| **TV**            | ddd                | 0~255           | Palabra: Valor actual del temporizador                  |
| **CV**            | ddd                | 0~199           | Palabra: Valor actual del contador                |
| **CV32**          | ddd                | 200~255         | Doble palabra: Valor actual del contador de 32 bits |

<img src="../../drivers/delta.files/image013.gif" width="595" />

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Nota:</p>
<p>d: decimal, rango de entrada 0-9;</p>
<p>o: octal, rango de entrada 0-7;</p>
<p>Bit en las observaciones: el registro solo puede usarse como bit;</p>
<p>Palabra en las observaciones: el registro solo puede usarse como palabra;</p>
<p>Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;</p>
<p>Solo lectura en las observaciones: el registro puede leerse pero no escribirse;</p>
<p>Los nombres y rangos de los registros pueden variar según el modelo de equipo.</p>
<p>Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.</p></td>
</tr>
</tbody>
</table>
