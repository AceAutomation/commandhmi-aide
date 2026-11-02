# IDEC device driver

The device driver is used for HM series HMI to read and write the data or state of Macro Smart FC4A/FC5A/FC6A series PLC register. The serial communication connection is established through the serial port of HMI and that of Macro Smart FC4A/FC5A/FC6A series PLC, so as to operate Macro Smart FC4A/FC5A series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Macro Smart FC4A/FC5A/FC6A series PLC.

**How to establish connection with Macro Smart FC4A/FC5A series**

1\. Hardware connection

Connecting cable:

RS232 (serial port RS232 protocol)

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
<td colspan="2"><p><strong>HM series HMI COM1/COM2</strong></p></td>
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
<p>Short circuit</p></td>
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
|     |                                                   |     |                                                   |     | <img src="idec.files/image002.gif" width="146" /> |
|     | <img src="idec.files/image003.gif" width="129" /> |     |                                                   |     |                                                   |
|     |                                                   |     | <img src="idec.files/image004.gif" width="280" /> |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |

Terminal of  HMI is DB9F, and that of Macro Smart FC4A/FC5A series PLC is MD8M.

**2.Software settings**

Select Allen-Bradley in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the relevant technical documents of the Macro Smart FC4A/FC5A/FC6A series PLC.

Default connection parameters of HM  HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Macro Smart FC4A            | Macro Smart FC4A/ Macro Smart FC5A           |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 7                           | 7/8                                          |
| **Parity bit**              | EVEN                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 1                           | 0~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Off-line simulation** | Yes                         |
| **On-line simulation**  | Yes                         |
| **Extended mode**       | Yes                         |

**3.Operational register and address range**

Macro Smart FC4A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                    |
| **I**             | ddd                | 0~255           | Bit: external switch quantity input, read only |
| **Q**             | ddd                | 0~255           | Bit: external switch quantity output           |
| **M**             | dddd               | 0~1023          | Bit: internal relay                            |
| **SM**            | ddd                | 0~215           | Bit: internal register                         |
| **R**             | ddd                | 0~255           | Word: shift register                           |
| **D**             | ddd                | 0~1299          | Word: data register                            |
| **TV**            | ddd                | 0~127           | Word: current value of timer                   |
| **CV**            | ddd                | 0~127           | Word: current value of counter                 |

Macro Smart FC5A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                    |
| **I**             | ddd                | 0~255           | Bit: external switch quantity input, read only |
| **Q**             | ddd                | 0~255           | Bit: external switch quantity output           |
| **M**             | dddd               | 0~2047          | Bit: internal relay                            |
| **SM**            | ddd                | 0~215           | Bit: internal register                         |
| **R**             | ddd                | 0~255           | Word: shift register                           |
| **D**             | ddd                | 0~42000         | Word: data register                            |
| **TV**            | ddd                | 0~255           | Word: current value of timer                   |
| **CV**            | ddd                | 0~255           | Word: current value of counter                 |

Macro Smart FC6A Tcp/IP

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Register name</strong></p></td>
<td><p><strong>Address format</strong></p></td>
<td><p><strong>Input range</strong></p></td>
<td><p><strong>Remarks</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>I</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit: external switch quantity input, read only</p></td>
</tr>
<tr class="odd">
<td><p><strong>Q</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit：Bit: external switch quantity output</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>Dddo</p></td>
<td><p>0~7997</p>
<p>8000~8317</p>
<p>10000~17497</p></td>
<td><p>Bit：internal relay</p></td>
</tr>
<tr class="odd">
<td><p><strong>R</strong></p></td>
<td><p>Ddd</p></td>
<td><p>0~255</p></td>
<td><p>Bit：shift register</p></td>
</tr>
<tr class="even">
<td><p><strong>T</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Bit: status of timer (read only)</p></td>
</tr>
<tr class="odd">
<td><p><strong>C</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~511</p></td>
<td><p>Bit: Status of counter(read only)</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>ddddd</p></td>
<td><p>0~8499</p>
<p>10000~55999</p></td>
<td><p>Word: register</p></td>
</tr>
<tr class="odd">
<td><p><strong>TV</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Word: current value of timer (read only)</p></td>
</tr>
<tr class="even">
<td><p><strong>CV</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Word: current value of counter (read only)</p></td>
</tr>
<tr class="odd">
<td><p><strong>TS</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>• Word: timer set value(read only)</p></td>
</tr>
<tr class="even">
<td><p><strong>CS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Word: counter set value (read only)</p></td>
</tr>
</tbody>
</table>

<img src="idec.files/image009.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device.

<img src="idec.files/image010.gif" width="595" />
