# TaiLing device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of TaiLing DX series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of TaiLing DX series PLC, so as to operate TaiLing DX series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and TaiLing DX series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with TaiLing DX series PLC</p>
<p><strong>1.  Hardware connection</strong></p>
<p>Connecting cable:</p>
<p>RS232 <span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>(serial port RS232 protocol)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HM series HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>TaiLing</strong> <strong>DX series</strong></p></td>
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
<p><img src="tailing.files/image002.gif" width="130" /><img src="tailing.files/image003.gif" width="290" /><img src="tailing.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Terminal of HMI is DB9F, and that of TaiLing DX series PLC is DB9M.

**2. Software settings**

Select TaiLing Electric in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Guarantee that communication parameters in touch screen connection parameters and PLC station number are consistent with the connected PLC.

For setting of the connected PLC, please consult related technical documents of Siemens TaiLing DX series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | DX Series                   | DX Series                                    |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity**                  | NONE                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 1                           | 1 to 31                                      |
| **HMI station number**      | 0                           | 0 to 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Offline simulation**  | Yes                         |
| **Online simulation**   | Yes                         |
| **Extended mode**       | No                          |

**3. Operational register and address scope**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Register name** | **Address format** | **Input scope** | **Remarks**                                  |
| **X**             | oooo               | 0 to 377        | Bit: input coil, read only                   |
| **Y**             | oooo               | 0 to 377        | Bit: output coil                             |
| **M**             | dddd               | 0 to 7999       | Bit: intermediate relay                      |
| **SM**            | dddd               | 8000 to 8999    | Bit: special intermediate relay              |
| **S**             | dddd               | 0 to 999        | Bit: state bit                               |
| **T**             | dddd               | 0 to 256        | Bit: timer state                             |
| **C**             | dddd               | 0 to 256        | Bit: counter state                           |
| **D**             | dddd               | 0 to 7999       | Word: register                               |
| **SD**            | dddd               | 8000 to 8999    | Word: special register                       |
| **TV**            | dddd               | 0 to 255        | Word: current value of the timer             |
| **CV**            | dddd               | 0 to 199        | Word: current value of the counter           |
| **CV32**          | dddd               | 200 to 255      | Double-word: current value of 32-bit counter |

<img src="tailing.files/image005.gif" width="595" />

Note：

d represents decimal system, input scope is 0-9;

o represents octal system, input scope is 0-7;

Word in the remarks: represents the register can only be used as word;

Double-word in the remarks: represents that the data type of the register in configuration must be 32-bit;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different;

For detailed name and scope, please consult related technical document of the connected device.

<img src="tailing.files/image005.gif" width="595" />
