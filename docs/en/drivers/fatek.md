# Fatek device driver

The device driver is used for HM series HMI to read and write the data or state of <span id="OLE_LINK158"></span><span id="OLE_LINK159"></span>Fatek FB series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Fatek FB series PLC, so as to operate Fatek FB series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Fatek FB series PLC.

**How to establish connection with Fatek device**

**1.Hardware connection**

Connecting cable:

RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (serial port RS232 protocol)

|                         |     |                 |     |
|-------------------------|-----|-----------------|-----|
| HM series HMI COM1/COM2 |     | Fatek FB series |     |
| 2                       | RX  | 1               | TX  |
| 3                       | TX  | 2               | RX  |
| 5                       | GND | 4               | GND |

|     |                                                    |     |                                                    |     |                                                    |
|-----|----------------------------------------------------|-----|----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     | <img src="fatek.files/image006.gif" width="146" /> |
|     | <img src="fatek.files/image007.gif" width="129" /> |     |                                                    |     |                                                    |
|     |                                                    |     | <img src="fatek.files/image008.gif" width="280" /> |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |

Terminal of HM series HMI is DB9F, and that of Fatek FB series PLC is MD4M.

**2. Software settings**

Select Fatek Automation Corp. in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Fatek FB series PLC.

Default connection parameters of HMI series touch screen

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Fatek FB Series             | Fatek FB Series                              |
| **Communication port type** | RS232                       | RS232                                        |
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

**3.Operational register and address range**

|                   |                    |                 |                                                   |
|-------------------|--------------------|-----------------|---------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                       |
| X                 | dddd               | 0~9999          | Bit: input connection point, read only            |
| Y                 | dddd               | 0~9999          | Bit: output relay                                 |
| M                 | dddd               | 0~9999          | Bit: internal relay                               |
| S                 | dddd               | 0~9999          | Bit: stepping relay                               |
| T                 | dddd               | 0~9999          | Bit: timer status                                 |
| C                 | dddd               | 0~9999          | Bit: counter status                               |
| R                 | dddd               | 0~9999          | <span id="OLE_LINK198"></span>Word: data register |
| D                 | dddd               | 0~9999          | Word: data register                               |
| TR                | dddd               | 0~9999          | Word: current value of timer                      |
| CR                | dddd               | 0~9999          | Word: current value of counter                    |
| F                 | dddd               | 0~9999          | Word: file register                               |
| DRC               | ddd                | 200~255         | Double word: current value of 32-bit counter      |

<img src="fatek.files/image009.gif" width="600" />

Note:

d represents decimal system, input range is 0-9;

o represents octal system, input range is 0-7;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

Double-word in the remarks: represents that the data type of the register in configuration must be 32-bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="fatek.files/image009.gif" width="600" />
