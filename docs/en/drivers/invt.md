# Invt device

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of <span id="OLE_LINK121"></span>Invt series PLC register. The serial communication connection is established through the serial port of HMI and the serial port of Invt series PLC, so as to operate Invt series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Invt series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with Invt  series PLC</p>
<p>1.  Hardware connection</p>
<p>Connecting cable:</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HM series HMI COM1/COM2</strong></p></td>
<td colspan="2"><p>Invt</p></td>
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
<p><img src="invt.files/image005.gif" width="145" /><img src="invt.files/image006.gif" width="281" /><img src="invt.files/image007.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Terminal of HMI is DB9F, and that of Invt series PLC is MD8M.

**2. Software settings**

Select Invt  Network Power in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Invt  series PLC.

Default connection parameters of HMI series touch screen

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | IVC1,IVC1L,IVCIS,IVC2L,IVC3 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                  |
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

**3. (IVC1,IVC1L,IVCIS,IVC2L,IVC3,IVC3 TCP)Operational register and address range**

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
| CV_Double         | ddd                | 0~255           | Double word: current value of counter       |
| SD_Double         | ddd                | 0~255           | Double word: special temporary data storage |
| R                 | ddd                | 0~32767         | Word: 16 bit register                       |
| RD                | ddd                | 32766           | Double word: 32 bit R register              |
|                   |                    |                 |                                             |
| D_Bit             | dddd.dd            | 0.0~7999.15     | Bit:D digit register                        |
| SD_Bit            | ddd.dd             | 0.0~255.15      | Bit:SD digit register                       |
| Z_Bit             | dd.dd              | 0.0~15.15       | Bit:Z digit register                        |
| R_Bit             | dddd.dd            | 0.0~32767.15    | Bit:R digit register                        |

AX70 RTU/AX70 TCP

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                                |
| **IX**            | ddd.o              | 0.0~511.7       | Bit：I area Bit representation (read-only)                 |
| **QX**            | ddd.o              | 0.0~511.7       | Bit：Q area Bit representation                             |
| **MX**            | ddd.o              | 0.0~7566.7      | Bit：M area Bit representation                             |
| **IB**            | ddd                | 0~511           | Byte ：I area Byte representation (read-only)              |
| **QB**            | ddd                | 0~511           | Byte ：Q area Byte representation                          |
| **MB**            | dddd               | 0~7566          | Byte ：M area Byte representation                          |
| **IW**            | ddd                | 0~511           | Word ：I area Word representation (read-only)              |
| **QW**            | ddd                | 0~511           | Word：Q area Word representation                           |
| **MW**            | dddd               | 0~3783          | Word：M area Word representation                           |
| **ID**            | ddd                | 0~127           | Double Word：I area Double Word representation (read-only) |
| **QD**            | ddd                | 0~127           | Double Word：Q area Double Word representation             |
| **MD**            | dddd               | 0~1891          | Double Word：M area Double Word representation             |

<img src="invt.files/image004.gif" width="600" />

Note:

d represents decimal system, input range is 0-9;

o represents octal system, input range is 0-7;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

Double-word in the remarks: represents that the data type of the register in configuration must be 32-bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device.

<img src="invt.files/image004.gif" width="600" />
