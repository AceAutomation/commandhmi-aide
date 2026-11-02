# HaiWell device driver

|                                                                                                                                                                                                                                                                                                                                                                                                                                                     |     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| The device driver is used for HM series HMI to read and write the data or state of Haiwell E/S/H series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Haiwell E/S/H series PLC, so as to operate Haiwell E/S/H series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Haiwell E/S/H series PLC. |     |

<span id="OLE_LINK217"></span><span id="OLE_LINK218"></span><span id="OLE_LINK219"></span>How to establish connection with HAIWELL device<span id="OLE_LINK221"></span>

<span id="OLE_LINK222"></span><span id="OLE_LINK223"></span><span id="OLE_LINK224"></span>**1. Hardware connection**

<span id="OLE_LINK225"></span><span id="OLE_LINK226"></span><span id="OLE_LINK227"></span>Connecting cable:

RS232 (serial port RS232 protocol)

|                                                                                                                       |     |                          |     |
|-----------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| <span id="OLE_LINK228"></span><span id="OLE_LINK229"></span><span id="OLE_LINK230"></span>**HM series HMI COM1/COM2** |     | **HaiWell E/S/H series** |     |
| 2                                                                                                                     | RX  | 2                        | TX  |
| 3                                                                                                                     | TX  | 1                        | RX  |
| 5                                                                                                                     | GND | 3                        | GND |

|     |                                                      |     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                      |
|     | <img src="haiwell.files/image002.gif" width="129" /> |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     | <img src="haiwell.files/image003.gif" width="140" /> |
|     |                                                      |     | <img src="haiwell.files/image004.gif" width="280" /> |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |

<span id="OLE_LINK231"></span>Terminal of HM series HMI is DB9F, and that of Haiwell E/S/H series PLC is MD4M.

<span id="OLE_LINK237"></span>**2. Software settings**

Select Haiwell Technology Corp. in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Haiwell E/S/H series PLC.

<span id="OLE_LINK242"></span>Default connection parameters of HMI series touch screen

|                             |                             |                             |                                              |     |
|-----------------------------|-----------------------------|-----------------------------|----------------------------------------------|-----|
| **Setting item**            | **Default parameter value** |                             | **Setting scope**                            |     |
| **Communication port type** | RS232                       |                             | RS232/RS422/RS485                            |     |
| **Baud rate**               | 19200                       |                             | 1200/2400/4800/9600/19200/38400/57600/115200 |     |
| **Data bit length**         | 8                           |                             | 7/8                                          |     |
| **Parity bit**              | NONE                        |                             | EVEN/ODD/NONE                                |     |
| **Stop bit length**         | 2                           |                             | 1/2                                          |     |
| **PLC station number**      | 1                           |                             | 1~31                                         |     |
| **HMI station number**      | 0                           |                             | 0~255                                        |     |
| **Supporting function**     |                             | **Whether it is supported** |                                              |     |
| **Off-line simulation**     |                             | Yes                         |                                              |     |
| **On-line simulation**      |                             | Yes                         |                                              |     |
| **Extended mode**           |                             | Yes                         |                                              |     |
|                             |                             |                             |                                              |     |

3\. **Operational register and address range**

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                                |
| X                 | ddd                | 0~1023          | Bit: External switch input                                 |
| Y                 | ddd                | 0~1023          | Bit: External switch output                                |
| M                 | ddd                | 0~12287         | Bit: Internal relay                                        |
| SM                | ddd                | 0~215           | Bit:<span id="OLE_LINK153"></span> System status           |
| S                 | ddd                | 0~2047          | Bit: Step status                                           |
| T                 | ddd                | 0~1023          | Bit: Timer status                                          |
| C                 | ddd                | 0~255           | Bit: Counter status                                        |
| AI                | ddd                | 0~255           | Word: Analog input register                                |
| AQ                | ddd                | 0~255           | Word: Analog output register                               |
| V                 | ddd                | 0~14847         | Word: Internal register                                    |
| TCV               | ddd                | 0~1023          | Word: <span id="OLE_LINK154"></span>current value of Timer |
| CCV               | ddd                | 0~47, 80~255    | Word: Current value of counter                             |
| SV                | ddd                | 0~154           | Word: System register                                      |
| CCV32             | ddd                | 0~31            | Double word: Current value of counter                      |

<img src="haiwell.files/image010.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device.

<img src="haiwell.files/image011.gif" width="595" />
