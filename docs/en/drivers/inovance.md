# Inovance device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of Inovance H1u/H2u series PLC register. The serial communication connection is established through the serial port of HMI and the serial port of Inovance H1u/H2u series PLC, so as to operate Inovance H1u/H2u series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Inovance H1u/H2u series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with Inovance H1u/H2u series PLC</p>
<p><strong>1.  Hardware connection</strong></p>
<p>Connecting cable:</p>
<p>RS232 (serial port RS232 protocol)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HM　HMI COM1/COM2</p></td>
<td colspan="2"><p>Inovance H1u/H2u series</p></td>
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

<img src="inovance.files/image002.gif" width="281" /><img src="inovance.files/image003.gif" width="130" /><img src="inovance.files/image004.gif" width="145" />

Terminal of HMI is DB9F, and that of Inovance H1u/H2u series PLC is DB9M.

**2. Software settings**

Select Inovance Technology Corp. in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Inovance H1u/H2u series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | H1u/H2u                     | H1u/H2u                                      |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 7                           | 7/8                                          |
| **Parity bit**              | EVEN                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 0                           | 0~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Off-line simulation** | Yes                         |
| **On-line simulation**  | Yes                         |
| **Extended mode**       | No                          |

**3. Operational register and address range**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                  |
| **X**             | oooo               | 0~377           | Bit: input coil, read only                   |
| **Y**             | oooo               | 0~377           | Bit: output coil                             |
| **M**             | dddd               | 0~7999          | Bit: intermediate relay                      |
| **SM**            | dddd               | 8000~8999       | Bit: special intermediate relay              |
| **S**             | dddd               | 0~999           | Bit: status bit                              |
| **T**             | dddd               | 0~256           | Bit: status of timer                         |
| **C**             | dddd               | 0~256           | Bit: Status of counter                       |
| **D**             | dddd               | 0~7999          | Word: register                               |
| **SD**            | dddd               | 8000~8999       | Word: special register                       |
| **TV**            | dddd               | 0~255           | Word: current value of timer                 |
| **CV**            | dddd               | 0~199           | Word: current value of counter               |
| **CV32**          | dddd               | 200~255         | Double word: current value of 32-bit counter |

<img src="inovance.files/image005.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

o represents octal system, input range is 0-7;

Word in the remarks: represents the register can only be used as word;

Double-word in the remarks: represents that the data type of the register in configuration must be 32-bit;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="inovance.files/image006.gif" width="595" />
