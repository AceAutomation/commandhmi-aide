# Nanda device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of Nanda NA-200/400 series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Nanda NA-200/400 series PLC, so as to operate Nanda NA-200/400 series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Nanda NA-200/400 series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with Nanda NA-200/400 series PLC</p>
<p><strong>1.  Hardware connection</strong></p>
<p>Connecting cable:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>HM series HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Nanda NA-200/400</strong></p></td>
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
<p><img src="nanda.files/image002.gif" width="130" /><img src="nanda.files/image003.gif" width="290" /><img src="nanda.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Terminal of HMI is DB9F, and that of Nanda NA-200/400 series PLC is DB9M.

**2. Software settings**

Select Nanda Auto Technology in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Nanda NA-200/400 series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Nanda NA-200                | Nanda NA-200/400                             |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
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

Nanda NA-200

|                   |                    |                 |                                                                                                                               |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                                                                                                   |
| **I**             | ddd                | 1~128           | Bit: <span id="OLE_LINK54"></span><span id="OLE_LINK55"></span><span id="OLE_LINK56"></span>digital quantity input, read only |
| **Q**             | ddd                | 1~128           | Bit: digital quantity output                                                                                                  |
| **M**             | dddd               | 1~1024          | Bit: bit register                                                                                                             |
| **S**             | ddd                | 1~256           | Bit: system bit register                                                                                                      |
| **N**             | ddd                | 1~256           | Bit: bit register for power failure protection                                                                                |
| **IW**            | dd                 | 1~32            | Word: analog quantity input                                                                                                   |
| **QW**            | dd                 | 1~32            | Word: analog quantity output                                                                                                  |
| **MW**            | dddd               | 1~1024          | Word: word register                                                                                                           |
| **SW**            | ddd                | 1~256           | Word: system word register                                                                                                    |
| **NW**            | ddd                | 1~256           | Word: word register for power failure protection                                                                              |

Nanda NA-400

|                   |                    |                 |                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                      |
| **I**             | ddd                | 1~2048          | Bit: digital quantity input, read only           |
| **Q**             | ddd                | 1~2048          | Bit: digital quantity output                     |
| **M**             | dddd               | 1~8192          | Bit: bit register                                |
| **S**             | ddd                | 1~4096          | Bit: system bit register                         |
| **N**             | ddd                | 1~2048          | Bit: bit register for power failure protection   |
| **IW**            | dd                 | 1~512           | Word: analog quantity input                      |
| **QW**            | dd                 | 1~512           | Word: analog quantity output                     |
| **MW**            | dddd               | 1~8192          | Word: word register                              |
| **SW**            | ddd                | 1~2048          | Word: system word register                       |
| **NW**            | ddd                | 1~2048          | Word: word register for power failure protection |

<img src="nanda.files/image005.gif" width="596" />

Note:

d represents decimal system, input range is 0-9;

Word in the remarks: represents the register can only be used as word;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="nanda.files/image006.gif" width="595" />
