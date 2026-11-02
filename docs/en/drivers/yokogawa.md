# Yokogawa device driver

The device driver is used for HM series HMI to read and write the data or state of Yokogawa FA-M3 series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Yokogawa FA-M3 series PLC, so as to operate Yokogawa FA-M3 series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Yokogawa FA-M3 series PLC.

How to establishment connection with Yokogawa FA-M3 series PLC 

**1.Hardware connection**

Connecting cable:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

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
<td colspan="2"><p>HM series COM1/COM2</p></td>
<td colspan="3"><p><strong>Yokogawa FA-M3 series</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>5</strong></p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>SG</p></td>
<td rowspan="2"><p>4-5 short-circuited</p>
<p>220Ω resistor in series</p></td>
</tr>
<tr class="odd">
<td><p><strong>6</strong></p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>SDB</p></td>
</tr>
<tr class="even">
<td><p><strong>7</strong></p></td>
<td><p>RX+</p></td>
<td><p>3</p></td>
<td><p>SDA</p></td>
<td rowspan="2"><p>2-3 short-circuited</p>
<p>220Ω resistor in series</p></td>
</tr>
<tr class="odd">
<td><p><strong>8</strong></p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>RDB</p></td>
</tr>
<tr class="even">
<td><p><strong>9</strong></p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td colspan="2"><p>RDA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>6</p></td>
<td><p>CSA</p></td>
<td rowspan="2"><p>6-7 short-circuited</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>ERA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>8</p></td>
<td><p>CSB</p></td>
<td rowspan="2"><p>8-9 short-circuited</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>9</p></td>
<td><p>ERB</p></td>
</tr>
</tbody>
</table>

Terminal of HMI is DB9F, and that of Yokogawa FA-M3 series PLC is SIO.

**2.Software settings**

Select Yokogawa Electric Corp. in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Guarantee that communication parameters in touch screen connection parameters and PLC station number are consistent with the connected PLC.

For settings of the connected PLC, please consult related technical documents of Yokogawa FA-M3 series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Yokogawa FA-M3              | Yokogawa FA-M3                               |
| **Communication port type** | RS422                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 1                           | 0 to 255                                     |
| **HMI station number**      | 0                           | 0 to 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Offline simulation**  | Yes                         |
| **Online simulation**   | Yes                         |
| **Extended mode**       | No                          |

**3.Operational register and address scope**

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Register name** | **Address format** | **Input scope** | **Remarks**                                               |
| **X**             | ddddd              | 0 to 71664      | Bit: input, discontinuous, determined by the slot number  |
| **Y**             | ddddd              | 0 to 71664      | Bit: output, discontinuous, determined by the slot number |
| **M**             | ddddd              | 0 to 16384      | Bit: special relay                                        |
| **I**             | ddddd              | 0 to 71024      | Bit: internal relay                                       |
| **L**             | ddddd              | 0 to 9984       | Bit: link relay, discontinuous                            |
| **D**             | ddddd              | 0 to 8192       | Word: data register                                       |
| **B**             | ddddd              | 0 to 32768      | Word: file register                                       |
| **V**             | ddddd              | 0 to 64         | Word: external switching value output                     |
| **W**             | ddddd              | 0 to 71024      | Word: link register, discontinuous                        |
| **Z**             | ddddd              | 0 to 512        | Word: special register                                    |

<img src="yokogawa.files/image002.gif" width="595" />

Note:

d represents decimal system, input scope is 0-9;

Word in the remarks: represents the register can only be used as word;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="yokogawa.files/image002.gif" width="595" />
