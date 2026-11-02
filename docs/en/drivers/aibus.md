# AIBUS device driver

The device driver is used for HM series HMI to read and write the data or state of AIBUS device via AIBUS protocols. The serial communication connection is established through the serial port of the HMI and the serial port of AIBUS device, so as to operate AIBUS device. Prior to use of the driver, please carefully read this chapter and the related technical specifications of the AIBUS device.

**1.  Hardware connection**

Connecting cable:

RS232 (serial port RS232 protocol)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HM series HMI COM1/COM2** |     | **AIBUS device**  |     |
| 2                           | RX  | User-defined pins | TX  |
| 3                           | TX  | User-defined pins | RX  |
| 5                           | GND | User-defined pins | GND |

<img src="aibus.files/image002.gif" width="157" /><img src="aibus.files/image003.gif" width="130" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>HMI series touch screen port is a 9P trapezoidal female connector. Definitions of AIBUS device pins depend on particular AIBUS device.</p>
<p><strong>RS422 (Serial port RS422 protocol)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HM series HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>AIBUS device</strong></p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>User-defined pins</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>User-defined pins</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>User-defined pins</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>User-defined pins</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table>
<table>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><img src="aibus.files/image004.gif" width="280" /></td>
</tr>
</tbody>
</table>
 &#10;<br />
&#10;<p>HMI series touch screen port is a 9P trapezoidal female connector. Definitions of AIBUS device pins depend on particular AIBUS device.</p>
<p><strong>RS485 (Serial port RS485 protocol)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI series touch screen COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>AIBUS device</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>D-</p></td>
<td><p>User-defined pins</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>D+</p></td>
<td><p>User-defined pins</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p>HMI series touch screen port is a 9P trapezoidal female connector. Definitions of AIBUS device pins depend on particular AIBUS device.</p></td>
</tr>
</tbody>
</table>

**2. Software settings**

ü Select AIBUS Protocol in connection device service.

ü Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

ü Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the AIBUS device.

ü For settings of the AIBUS device, refer to the technical documents of the AIBUS device.

Default connection parameters of HMI series touch screen

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | AIBUS Protocol              | AIBUS Protocol                               |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity bit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 1                           | 1~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Off-line simulation** | Yes                         |
| **On-line simulation**  | Yes                         |
| **Extended mode**       | Yes                         |

**3. Operational register and address range**

|                   |                    |                 |                      |
|-------------------|--------------------|-----------------|----------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**          |
| **Parameter**     | ddd                | 0~255           | Word: parameter item |
| **PV**            | d                  | 0               | Word: Output value   |
| **SV**            | d                  | 0               | Word: Set value      |
| **MV**            | d                  | 0               | Word: State value    |
| **Status**        | d                  | 0               | Word: State value    |

<img src="aibus.files/image005.gif" width="595" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Note: </p>
<p>• ·d represents decimal system, input range is 0-9;</p>
<p>• ·”Word” in the remarks: represents that the register can only be used as word;</p>
<p>• The names of the registers supported by different equipment model may be different, and the scopes may also be different.</p>
<p>For detailed name and scope, please consult related technical document of the connected device.</p></td>
</tr>
</tbody>
</table>

<img src="aibus.files/image006.gif" width="595" />
