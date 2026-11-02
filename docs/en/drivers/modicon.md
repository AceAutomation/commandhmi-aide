# Modicon device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of Modicon NEZA/TWIDO/M218 series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Modicon NEZA/TWIDO/M218 series PLC, so as to operate Modicon NEZA/TWIDO/M218 series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Modicon NEZA/TWIDO/M218 series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with Modicon NEZA/TWIDO/M218 series PLC</p>
<p><strong>1.  Hardware connection</strong></p>
<p><span id="OLE_LINK19"></span><span id="OLE_LINK20"></span>Connecting cable:</p>
<p>RS<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>485</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><span id="OLE_LINK60"></span><strong>HM series HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Modicon NEZA/TWIDO/M218</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="modicon.files/image002.gif" width="281" /><img src="modicon.files/image003.gif" width="130" /><img src="modicon.files/image004.gif" width="145" />

Terminal of HMI is DB9F, and that of Modicon NEZA/TWIDO/M218 series PLC is MD8M.

**2. Software settings**

Select Modicon Corp. in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Modicon NEZA/TWIDO/M218 series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | NEZA Series                 | NEZA/TWIDO/M218 Series                       |
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

**3. Operational register and address range**

NEZA Series

|                   |                    |                 |                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                           |
| **%MW**           | ddddd              | 0~65535         | Word: <span id="OLE_LINK50"></span>word data register |

TWIDO Series

|                   |                    |                 |                                                                                    |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                                                        |
| **%M**            | ddddd              | 0~65535         | Bit: <span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>bit data register   |
| **%MW**           | ddddd              | 0~65535         | Word: <span id="OLE_LINK53"></span><span id="OLE_LINK54"></span>word data register |

M218 Series

|                   |                    |                 |                          |
|-------------------|--------------------|-----------------|--------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**              |
| **%MX**           | ddddd.o            | 0~131071.7      | Bit: bit data register   |
| **%MW**           | ddddd              | 0~65535         | Word: word data register |

<img src="modicon.files/image005.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

o represents octal system, input range is 0-7;

Word in the remarks: represents the register can only be used as word;

Bit in the remarks: represents the register can only be used as bit;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="modicon.files/image006.gif" width="595" />
