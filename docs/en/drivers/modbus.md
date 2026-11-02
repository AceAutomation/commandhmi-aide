# Modbus device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of <span id="OLE_LINK37"></span><span id="OLE_LINK38"></span>MODBUS device. The serial communication connection is established through the serial port of the HMI series touch screen and the serial port of MODBUS device, so as to operate MODBUS device. Prior to use of the driver, please carefully read this chapter and the related technical specifications of the MODBUS series PLC device.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with MODBUS series PLC</p>
<p><strong>1.</strong> <strong>Hardware connection</strong></p>
<p>Connecting cable:</p>
<p>RS232<span id="OLE_LINK24"></span><span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK62"></span><span id="OLE_LINK63"></span><span id="OLE_LINK64"></span><strong>HM series HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Modbus device</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>User-defined pins</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>User-defined pins</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>User-defined pins</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="modbus.files/image002.gif" width="157" /><img src="modbus.files/image003.gif" width="130" />

Terminal of HMI is DB9F. Definitions of Modbus device pins depend on particular Modbus device.

**RS422**

|                                                                                                                    |     |                   |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-------------------|-----|
| <span id="OLE_LINK72"></span><span id="OLE_LINK73"></span><span id="OLE_LINK74"></span>**HM series HMI COM1/COM2** |     | **Modbus device** |     |
| 6                                                                                                                  | RX- | User-defined pins | TX- |
| 7                                                                                                                  | RX+ | User-defined pins | TX+ |
| 8                                                                                                                  | TX- | User-defined pins | RX- |
| 9                                                                                                                  | TX+ | User-defined pins | RX+ |

<img src="modbus.files/image004.gif" width="157" /><img src="modbus.files/image005.gif" width="130" />

Terminal of HMI is DB9F. Definitions of Modbus device pins depend on particular Modbus device.

**RS485**

|                                                                                       |     |                   |     |
|---------------------------------------------------------------------------------------|-----|-------------------|-----|
| <span id="OLE_LINK78"></span><span id="OLE_LINK79"></span>**HM series HMI COM1/COM2** |     | **Modbus device** |     |
| 8                                                                                     | D-  | User-defined pins | B   |
| 9                                                                                     | D+  | User-defined pins | A   |

<img src="modbus.files/image006.gif" width="157" /><img src="modbus.files/image007.gif" width="130" />

Terminal of HMI is a 9P trapezoidal female connector. Definitions of Modbus device pins depend on particular AIBUS device.

**TCP/IP (RJ45 direct connection)**

|                                                                                                                    |      |                   |      |
|--------------------------------------------------------------------------------------------------------------------|------|-------------------|------|
| <span id="OLE_LINK82"></span><span id="OLE_LINK83"></span><span id="OLE_LINK84"></span>**HM series HMI COM1/COM2** |      | **Modbus device** |      |
| 1                                                                                                                  | TX+  | 3                 | RX+  |
| 2                                                                                                                  | TX-  | 6                 | RX-  |
| 3                                                                                                                  | RX+  | 1                 | TX+  |
| 4                                                                                                                  | BD4+ | 4                 | BD4+ |
| 5                                                                                                                  | BD4- | 5                 | BD4- |
| 6                                                                                                                  | RX-  | 2                 | TX-  |
| 7                                                                                                                  | BD3+ | 7                 | BD3+ |
| 8                                                                                                                  | BD3- | 8                 | BD3- |

|     |                                                    |     |                                                     |     |                                                    |
|-----|----------------------------------------------------|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                     |     |                                                    |
|     | <img src="modbus.files/image008.gif" width="95" /> |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     | <img src="modbus.files/image009.gif" width="95" /> |
|     |                                                    |     | <img src="modbus.files/image010.gif" width="267" /> |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |

<span id="OLE_LINK68"></span><span id="OLE_LINK69"></span><span id="OLE_LINK70"></span>

Terminal of HMI is RJ45, and that of Modbus device is RJ45.

**TCP/IP (RJ45 connection via router)**

|                       |      |               |      |
|-----------------------|------|---------------|------|
| **HM　HMI COM1/COM2** |      | Modbus device |      |
| 1                     | TX+  | 3             | RX+  |
| 2                     | TX-  | 6             | RX-  |
| 3                     | RX+  | 1             | TX+  |
| 4                     | BD4+ | 4             | BD4+ |
| 5                     | BD4- | 5             | BD4- |
| 6                     | RX-  | 2             | TX-  |
| 7                     | BD3+ | 7             | BD3+ |
| 8                     | BD3- | 8             | BD3- |

<img src="modbus.files/image011.gif" width="95" />

|     |                                                     |     |                                                    |
|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                     |     |                                                    |
|     |                                                     |     | <img src="modbus.files/image012.gif" width="95" /> |
|     | <img src="modbus.files/image013.gif" width="267" /> |     |                                                    |
|     |                                                     |     |                                                    |

Terminal of HMI is RJ45, and that of Modbus device is RJ45.

**2.Software settings**

Select Modbus in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Modbus device.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | RTU Master                  | RTU/RTU_S/ASCII/ASCII_S Master               |
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

<img src="modbus.files/image014.gif" width="595" />

Note: The function code used in RTU_S and ASCII_S for data writing is 0x10 (regardless of length of the data written);

·If 0 is chosen for PLC station number, then the system is in broadcasting mode.

**3.Operational register and address range**

|                   |                    |                 |                                                                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                                                                      |
| 0x                | ddddd              | 0~65535         | Bit: input coil                                                                                  |
| 1x                | ddddd              | 0~65536         | Bit: input coil, read only                                                                       |
| 3x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit: <span id="OLE_LINK100"></span>bit of 16-bit input register, read only                       |
| 4x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit: bit of 16-bit output register                                                               |
| 3x                | ddddd              | 0~65535         | Word: 16-bit input register, read only                                                           |
| 4x                | ddddd              | 0~65535         | Word: 16-bit output register                                                                     |
| 3x_D              | ddddd              | 0~65535         | Double word: input register, reversing the higher and lower 16 bits of 3x double word, read only |
| 4x_D              | ddddd              | 0~65535         | Double word: output register, reversing the higher and lower 16 bits of 4x double word           |

Modbus Slave

|                       |                             |                 |                                                                |
|-----------------------|-----------------------------|-----------------|----------------------------------------------------------------|
| **Internal register** | **Supported function code** | **Input range** | **remark**                                                     |
| LB                    | 01/02/05/15                 | 0~59999         | Bit：Read and write the internal address of the touch screenLB |
| LW                    | 03/04/06/16                 | 0~59999         | Word：Read and write the internal address of the touch screen  |

<img src="modbus.files/image015.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

DD represents 16 bits, input range is 0-15;

Word in the remarks: represents the register can only be used as word;

Double-word in the remarks: represents that the data type of the register in configuration must be 32-bit;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment models may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="modbus.files/image016.gif" width="595" />
