# Emerson device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of <span id="OLE_LINK120"></span><span id="OLE_LINK121"></span>Emerson EC series PLC register. The serial communication connection is established through the serial port of HMI and the serial port of Emerson EC series PLC, so as to operate Emerson EC series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Emerson EC series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with Emerson EC series PLC</p>
<p>1.  Hardware connection</p>
<p>Connecting cable:</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HM series HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Emerson EC</strong></p></td>
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
<td><p>3</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="emerson.files/image002.gif" width="146" /><img src="emerson.files/image003.gif" width="281" /><img src="emerson.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Terminal of HMI is DB9F, and that of Emerson EC series PLC is MD8M.

**2. Software settings**

Select Emerson Network Power in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Emerson EC series PLC.

Default connection parameters of HMI series touch screen

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | EC Series (RTU)             | EC Series (RTU)                              |
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

**3. Operational register and address range**

|                   |                    |                 |                                             |
|-------------------|--------------------|-----------------|---------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                 |
| X                 | ooo                | 0~377           | Bit: input connection point, read only      |
| Y                 | ooo                | 0~377           | Bit: output connection point                |
| M                 | dddd               | 0~7999          | Bit: internal relay                         |
| SM                | ddd                | 0~255           | Bit: special internal relay                 |
| S                 | ddd                | 0~999           | Bit: Stepping relay                         |
| T                 | ddd                | 0~255           | Bit: timer status                           |
| C                 | ddd                | 0~255           | Bit: counter status                         |
| D                 | dddd               | 0~7999          | Word: temporary data storage                |
| SD                | ddd                | 0~255           | Word: special temporary data storage        |
| TV                | ddd                | 0~255           | Word: current value of timer                |
| CV                | ddd                | 0~255           | Word: current value of counter              |
| Z                 | dd                 | 0~15            | Word: indexed addressing register           |
| D_Double          | dddd               | 0~7999          | Double word: temporary data storage         |
| CV_Double         | ddd                | 200~255         | Double word: current value of counter       |
| SD_Double         | ddd                | 0~255           | Double word: special temporary data storage |

<img src="emerson.files/image005.gif" width="600" />

Note:

d represents decimal system, input range is 0-9;

o represents octal system, input range is 0-7;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

Double-word in the remarks: represents that the data type of the register in configuration must be 32-bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device.

<img src="emerson.files/image006.gif" width="600" />
