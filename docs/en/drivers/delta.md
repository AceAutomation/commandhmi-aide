# Delta device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of <span id="OLE_LINK42"></span><span id="OLE_LINK43"></span>Delta DVP series PLC register. The serial communication connection is established through the serial port of HMI and the serial port of Delta DVP series PLC, so as to operate Delta DVP series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Delta DVP series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with Delta DVP series PLC</p>
<p><strong>1.  Hardware connection</strong></p>
<p>Connecting cable:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK53"></span><span id="OLE_LINK2"></span> (serial port RS232 protocol)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HM series HMI  COM1/COM2</p></td>
<td colspan="2"><p>Delta DVP series</p></td>
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
<p><img src="delta.files/image008.gif" width="281" /><img src="delta.files/image009.gif" width="146" /><img src="delta.files/image010.gif" width="130" />  </p>
<p><span id="OLE_LINK54"></span>Terminal of HM series HMI is DB9F; that of Delta DVP series PLC is MD8M.</p>
<p>RS485 (serial port RS485 protocol)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HM series HMI COM1/COM2</p></td>
<td><p>Delta DVP series</p></td>
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
<p><img src="delta.files/image011.gif" width="130" /><img src="delta.files/image012.gif" width="156" /></p>
<p>Terminal of HM series is DB9F, and that of Delta DVP series PLC is two-wire terminal.</p></td>
</tr>
</tbody>
</table>

**2. Software settings**

ü Select Delta Corporation in connection device service.

ü Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

ü Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

ü For settings of the PLC, refer to the technical documents of the Delta DVP series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Delta DVP Series            | Delta DVP Series                             |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity bit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 1                           | 0~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Off-line simulation** | Yes                         |
| **On-line simulation**  | Yes                         |
| **Extended mode**       | Yes                         |

**3. Operational register and address range**

|                   |                    |                 |                                               |
|-------------------|--------------------|-----------------|-----------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                   |
| **X**             | ooo                | 0~377           | Bit: input connection point, read only        |
| **Y**             | ooo                | 0~377           | Bit: output connection point                  |
| **M**             | dddd               | 0~4095          | Bit: auxiliary relay                          |
| **S**             | dddd               | 0~1023          | Bit: internal relay                           |
| **T**             | ddd                | 0~255           | Bit: timer status                             |
| **C**             | ddd                | 0~255           | Bit: counter status                           |
| **D**             | dddd               | 0~9999          | Word: temporary data storage                  |
| **TV**            | ddd                | 0~255           | Word: current value of timer                  |
| **CV**            | ddd                | 0~199           | Word: current value of counter                |
| **CV32**          | ddd                | 200~255         | Double words: current value of 32-bit counter |

<img src="delta.files/image013.gif" width="595" />

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Note:</p>
<p>d represents decimal system, input range is 0-9;</p>
<p>o represents octal system, input range is 0-7;</p>
<p>Bit in the remarks: represents the register can only used as bit;</p>
<p>Word in the remarks: represents the register can only used as word;</p>
<p>Double-word in the remarks: represents that the data type of the register in configuration must be 32-bit;</p>
<p>Read only in the remarks represents that the register can only be read but not be written;</p>
<p>The names of the registers supported by different equipment model may be different, and the scopes may also be different.</p>
<p>For detailed name and scope, please consult related technical document of the connected device.</p></td>
</tr>
</tbody>
</table>
