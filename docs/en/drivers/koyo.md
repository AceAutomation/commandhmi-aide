# Koyo device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of Koyo SN series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Koyo SN series PLC, so as to operate Koyo SN series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Koyo SN series PLC.</p></td>
</tr>
<tr class="even">
<td><p> How to establish connection with Koyo SN series PLC</p>
<p><strong>1.</strong> <strong>Hardware connection</strong></p>
<p>Connecting cable:</p>
<p>RS232 (serial port RS232 protocol)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HM HMI COM1/COM2</p></td>
<td colspan="2"><p>Koyo SN series</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>4</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="koyo.files/image006.gif" width="278" /><img src="koyo.files/image007.gif" width="130" /><img src="koyo.files/image008.gif" width="90" />

Terminal of HMI is DB9F, and that of Koyo SN series PLC is 6-pin registered jack.

**2.Software settings**

Select Koyo Electronics in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Koyo SN series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Koyo SN Series              | Koyo SN Series                               |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity bit**              | ODD                         | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 1                           | 0~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Off-line simulation** | Yes                         |
| **On-line simulation**  | Yes                         |
| **Extended mode**       | Yes                         |

**3.Koyo SN Series**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                    |
| **I**             | ooo                | 0~377           | Bit: input relay, read only    |
| **O**             | ooo                | 0~377           | Bit: output relay              |
| **M**             | oooo               | 0~1177          | Bit: auxiliary relay           |
| **SP**            | ooo                | 0~777           | Bit: special auxiliary relay   |
| **S**             | ooo                | 0~177           | Bit: stepping relay            |
| **T**             | ooo                | 0~177           | Bit: timer                     |
| **C**             | ooo                | 0~177           | Bit: counter                   |
| **R**             | ooooo              | 0~13777         | Word: data register            |
| **TR**            | ooooo              | 0~13777         | Word: current value of timer   |
| **CR**            | ooooo              | 0~13777         | Word: current value of counter |
| **SR**            | ooooo              | 0~13777         | Word: special data register    |

**4.Koyo DIRECT Series**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                    |
| **X**             | ooo                | 0~3777          | Bit: input relay, read only    |
| **Y**             | ooo                | 0~3777          | Bit: output relay              |
| **GX**            | oooo               | 0~7777          | Bit: input relay, read only    |
| **GY**            | oooo               | 0~7777          | Bit: output relay              |
| **C**             | oooo               | 0~7777          | Bit: counter                   |
| **S**             | oooo               | 0~1777          | Bit: stepping relay            |
| **SP**            | oooo               | 0~1777          | Bit: special auxiliary relay   |
| **CT**            | ooo                | 0~777           | Bit: counter                   |
| **T**             | ooo                | 0~777           | Bit: timer                     |
| **V**             | oooo               | 0~77777         | Word: special data register    |
| **TV**            | ooo                | 0~777           | Word: current value of timer   |
| **CV**            | ooo                | 0~777           | Word: current value of counter |

KV-Nano

|                |              |              |                                            |
|----------------|--------------|--------------|--------------------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                                   |
| **R**          | ddddd        | 0~59915      | Position: relay                            |
| **B**          | DDDD         | 0~1FFF       | Position: Link Relay                       |
| **MR**         | ddddd        | 0~59915      | Position：Internal auxiliary relay         |
| **LR**         | ddddd        | 0~19915      | Position: Latching relay                   |
| **CR**         | dddd         | 0~8915       | Position: control relay                    |
| **VB**         | DDDD         | 0~1FFF       | Position: work relay                       |
| **T**          | ddd          | 0~511        | Position: timer                            |
| **C**          | ddd          | 0~255        | Position: counter                          |
| **DM**         | dddd         | 0~32767      | Word：Data storage                         |
| **W**          | DDDD         | 0~3FFF       | Word：Link register                        |
| **TM**         | dddd         | 0~511        | Word：Temporary data storage               |
| **Z**          | dddd         | 1~12         | Word：Index register                       |
| **TC**         | dddd         | 0~511        | Double word：Timer (current value)         |
| **TS**         | dddd         | 0~511        | Double word：Timer (setting value)         |
| **CC**         | ddd          | 0~255        | Double word：Counter (current value)       |
| **CS**         | ddd          | 0~255        | Double word：Counter (setting value)       |
| **CTH**        | d            | 0~3          | Double word：High-speed counter            |
| **CTC**        | d            | 0~7          | Double word：High speed counter comparator |
| **CM**         | dddd         | 0~8999       | word：Control storage                      |
| **VM**         | dddd         | 0~9999       | word：Working memory                       |

<img src="koyo.files/image009.gif" width="595" />

Note:

o represents octal system, input range is 0-7;

Word in the remarks: represents the register can only be used as word;

Double-word in the remarks: represents that the data type of the register in configuration must be 32-bit;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="koyo.files/image010.gif" width="595" />
