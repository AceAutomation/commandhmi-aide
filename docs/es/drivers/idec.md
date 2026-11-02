# Controlador IDEC

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC Macro Smart de la serie FC4A/FC5A/FC6A. La comunicación serie se establece entre el puerto serie del HMI y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

**Cómo establecer la conexión con la serie Macro Smart FC4A/FC5A**

1\. Conexión de hardware

Cable de conexión:

RS232 (puerto serie, protocolo RS232)

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="3"><p><strong>Macro Smart FC4A/FC5A</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td colspan="2"><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td colspan="2"><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>6</p></td>
<td><p>GND</p></td>
<td rowspan="2"><p>6-7</p>
<p>Cortocircuito</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>

|     |                                                   |     |                                                   |     |                                                   |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|---------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     | <img src="../../drivers/idec.files/image002.gif" width="146" /> |
|     | <img src="../../drivers/idec.files/image003.gif" width="129" /> |     |                                                   |     |                                                   |
|     |                                                   |     | <img src="../../drivers/idec.files/image004.gif" width="280" /> |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |

El conector del HMI es DB9F y el del PLC Macro Smart de la serie FC4A/FC5A es MD8M.

**2. Ajustes de software**

Elija IDEC en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Macro Smart de la serie FC4A/FC5A/FC6A.

Parámetros de conexión por defecto del HMI HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Macro Smart FC4A            | Macro Smart FC4A/ Macro Smart FC5A           |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
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

Macro Smart FC4A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                    |
| **I**             | ddd                | 0~255           | Bit: Entrada digital externa, solo lectura |
| **Q**             | ddd                | 0~255           | Bit: Salida digital externa           |
| **M**             | dddd               | 0~1023          | Bit: Relé interno (marca)                            |
| **SM**            | ddd                | 0~215           | Bit: Registro interno                         |
| **R**             | ddd                | 0~255           | Palabra: Registro de desplazamiento                           |
| **D**             | ddd                | 0~1299          | Palabra: Registro de datos                            |
| **TV**            | ddd                | 0~127           | Palabra: Valor actual del temporizador                   |
| **CV**            | ddd                | 0~127           | Palabra: Valor actual del contador                 |

Macro Smart FC5A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                    |
| **I**             | ddd                | 0~255           | Bit: Entrada digital externa, solo lectura |
| **Q**             | ddd                | 0~255           | Bit: Salida digital externa           |
| **M**             | dddd               | 0~2047          | Bit: Relé interno (marca)                            |
| **SM**            | ddd                | 0~215           | Bit: Registro interno                         |
| **R**             | ddd                | 0~255           | Palabra: Registro de desplazamiento                           |
| **D**             | ddd                | 0~42000         | Palabra: Registro de datos                            |
| **TV**            | ddd                | 0~255           | Palabra: Valor actual del temporizador                   |
| **CV**            | ddd                | 0~255           | Palabra: Valor actual del contador                 |

Macro Smart FC6A TCP/IP

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Nombre del registro</strong></p></td>
<td><p><strong>Formato de dirección</strong></p></td>
<td><p><strong>Rango de entrada</strong></p></td>
<td><p><strong>Observaciones</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>I</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit: entrada digital externa, solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Q</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit：Bit: salida digital externa</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>Dddo</p></td>
<td><p>0~7997</p>
<p>8000~8317</p>
<p>10000~17497</p></td>
<td><p>Bit：relé interno (marca)</p></td>
</tr>
<tr class="odd">
<td><p><strong>R</strong></p></td>
<td><p>Ddd</p></td>
<td><p>0~255</p></td>
<td><p>Bit：registro de desplazamiento</p></td>
</tr>
<tr class="even">
<td><p><strong>T</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Bit: estado del temporizador (solo lectura)</p></td>
</tr>
<tr class="odd">
<td><p><strong>C</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~511</p></td>
<td><p>Bit: estado del contador (solo lectura)</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>ddddd</p></td>
<td><p>0~8499</p>
<p>10000~55999</p></td>
<td><p>Palabra: registro</p></td>
</tr>
<tr class="odd">
<td><p><strong>TV</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Palabra: valor actual del temporizador (solo lectura)</p></td>
</tr>
<tr class="even">
<td><p><strong>CV</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Palabra: valor actual del contador (solo lectura)</p></td>
</tr>
<tr class="odd">
<td><p><strong>TS</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>• Palabra: consigna del temporizador (solo lectura)</p></td>
</tr>
<tr class="even">
<td><p><strong>CS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Palabra: consigna del contador (solo lectura)</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/idec.files/image009.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

Bit en las observaciones: el registro solo puede usarse como bit;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.

<img src="../../drivers/idec.files/image010.gif" width="595" />
