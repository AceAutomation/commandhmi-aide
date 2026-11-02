# Hitachi device driver

The device driver is used for HM series HMI to read and write the data or state of Hitachi E/EH series PLC register. The serial communication connection is established through the HMI serial port and that of Hitachi E/EH series PLC, so as to operate Hitachi E/EH series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Hitachi E/EH series PLC.

**1. Hardware connection**

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
<td colspan="3"><p><strong>Hitachi E/EH series</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td colspan="2"><p>SD</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>6</p></td>
<td colspan="2"><p>RD</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>1</p></td>
<td colspan="2"><p>SG</p></td>
</tr>
<tr class="odd">
<td colspan="2" rowspan="2"></td>
<td><p>4</p></td>
<td><p>PHL</p></td>
<td rowspan="2"><p>4-7</p>
<p>Short circuit</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>DR</p></td>
</tr>
</tbody>
</table>

|     |                                                      |     |                                                      |     |                                                     |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|-----------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     | <img src="hitachi.files/image002.gif" width="91" /> |
|     | <img src="hitachi.files/image003.gif" width="130" /> |     |                                                      |     |                                                     |
|     |                                                      |     | <img src="hitachi.files/image004.gif" width="278" /> |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |

Terminal of HM series HMI is DB9F, and that of AB device is RJ45.

**2. Software settings**

Select Hitachi Industrial in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Hitachi E/EH series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Hitachi E/EH Series         | Hitachi E/EH Series                          |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Extended mode**       | Yes                         |

**3. Operational register and address range**

|                   |                    |                 |                                                                    |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                                        |
| **X**             | hhhh               | 0~ffff          | Bit: external switch quantity input, read only                     |
| **Y**             | hhhh               | 0~ffff          | Bit: <span id="OLE_LINK247"></span>external switch quantity output |
| **M**             | hhhh               | 0~ffff          | Bit: internal relay                                                |
| **R**             | hhhh               | 0~ffff          | Bit: internal register                                             |
| **T**             | hhhh               | 0~ffff          | Bit: status of timer                                               |
| **L**             | hhhh               | 0~ffff          | Bit: link relay                                                    |
| **WX**            | hhhh               | 0~ffff          | Word: external switch quantity input                               |
| **WY**            | hhhh               | 0~ffff          | Word: external switch quantity output                              |
| **WM**            | hhhh               | 0~ffff          | Word: internal relay                                               |
| **WR**            | hhhh               | 0~ffff          | Word: internal register                                            |
| **WL**            | hhhh               | 0~ffff          | Word: link relay                                                   |
| **TC**            | hhhh               | 0~ffff          | Word: current value of timer/counter                               |

<img src="hitachi.files/image005.gif" width="595" />

Note：

h represents hexadecimal system, input range is 0-9, a-f;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device.

<img src="hitachi.files/image006.gif" width="595" />
