# Matsushita device driver

The device driver is used for HM series HMI to read and write the data or state of Matsushita FP series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Matsushita FP series PLC, so as to operate Matsushita FP series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Matsushita FP series PLC.

How to establish connection with Matsushita FP series PLC

**1.  Hardware connection**

Connecting cable:

RS232-FP0/FP2/FP2SH/FPM

|                                                                                                                                                 |     |                          |     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| <span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span>**HM series HMI COM1/COM2** |     | **Matsushita FP series** |     |
| 2                                                                                                                                               | RX  | 3                        | TX  |
| 3                                                                                                                                               | TX  | 2                        | RX  |
| 5                                                                                                                                               | GND | 1                        | GND |

<img src="matsushita.files/image002.gif" width="280" /><img src="matsushita.files/image003.gif" width="129" /><img src="matsushita.files/image004.gif" width="145" />

Terminal of HMI is DB9F, and that of Matsushita FP series PLC is MD5M.

RS422-FP1

|                             |     |                      |     |
|-----------------------------|-----|----------------------|-----|
| **HM series HMI COM1/COM2** |     | Matsushita FP series |     |
| 6                           | RX- | 2                    | TX- |
| 7                           | RX+ | 5                    | TX+ |
| 8                           | TX- | 3                    | RX- |
| 9                           | TX+ | 6                    | RX+ |

<img src="matsushita.files/image005.gif" width="140" /><img src="matsushita.files/image006.gif" width="129" /><img src="matsushita.files/image007.gif" width="280" />

Terminal of HMI is DB9F, and that of Matsushita FP series PLC is MD8M.

**2. Software settings**

Select MATSUSHITA in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of connecting PLC, please refer to the technical documents of the Matsushita FP series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | FP Series                   | FP Series                                    |
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
| **Extended mode**       | No                          |

**3. Operational register and address range**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                            |
| **X**             | ddddh              | 0~9999f         | Bit: external input, read only         |
| **Y**             | ddddh              | 0~9999f         | Bit: external output                   |
| **R**             | ddddh              | 0~9999f         | Bit: internal relay                    |
| **L**             | ddddh              | 0~9999f         | Bit: link relay                        |
| **T**             | dddd               | 0~9999          | Bit: status of timer, read only        |
| **C**             | dddd               | 0~9999          | Bit: status of counter, read only      |
| **WX**            | dddd               | 0~9999          | Word: external input, read only        |
| **WY**            | dddd               | 0~9999          | Word: external output                  |
| **WR**            | dddd               | 0~9999          | Word: internal relay                   |
| **WL**            | dddd               | 0~9999          | Word: link relay                       |
| **DT**            | ddddd              | 0~99999         | Word: data register                    |
| **LD**            | ddddd              | 0~99999         | Word: link register                    |
| **FL**            | ddddd              | 0~99999         | Word: file register                    |
| **SV**            | dddd               | 0~9999          | Word: timer/counter set value area     |
| **EV**            | dddd               | 0~9999          | Word: timer/counter process value area |

<img src="matsushita.files/image008.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

h represents hexadecimal system, input range is 0-9, a-f;

Word in the remarks: represents the register can only be used as word;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="matsushita.files/image009.gif" width="595" />
