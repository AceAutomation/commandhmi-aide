# Fuji device driver

The device driver is used for HM series HMI to read and write the data or state of Fuji NB series PLC register. The serial communication connection is established through the HMI serial port and the serial port of Fuji NB series PLC, so as to operate Fuji NB series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Fuji NB series PLC.

**How to establish connection with Fuji device**

**1. Hardware connection**

Connecting cable:

RS422<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (serial port RS422 protocol)

|                         |     |                |     |
|-------------------------|-----|----------------|-----|
| HM series HMI COM1/COM2 |     | Fuji NB series |     |
| 6                       | RX- | 4              | TX- |
| 7                       | RX+ | 3              | TX+ |
| 8                       | TX- | 6              | RX- |
| 9                       | TX+ | 5              | RX+ |

|     |                                                   |     |                                                   |     |                                                  |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|--------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     | <img src="fuji.files/image002.gif" width="95" /> |
|     | <img src="fuji.files/image003.gif" width="130" /> |     |                                                   |     |                                                  |
|     |                                                   |     | <img src="fuji.files/image004.gif" width="278" /> |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |

Terminal of HM series HMI is DB9F, and that of Fuji NB series PLC is RJ45.

**2. Software settings**

Select Fuji Electric Corporation in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the Fuji NB series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Fuji NB Series              | Fuji NB Series                               |
| **Communication port type** | RS422                       | RS422                                        |
| **Baud rate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity bit**              | ODD                         | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 0                           | 0~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Off-line simulation** | Yes                         |
| **On-line simulation**  | Yes                         |
| **Extended mode**       | Yes                         |

**3. Operational register and address range**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                            |
| **X**             | hhh                | 0~7ff           | Bit: input connection point, read only |
| **Y**             | hhh                | 0~7ff           | Bit: output connection point           |
| **M**             | hhhh               | 0~7fff          | Bit: internal relay                    |
| **SM**            | hhhh               | 8000~81ff       | Bit: internal relay                    |
| **L**             | hhh                | 0~5ff           | Bit: Lockout relay                     |
| **S**             | hh                 | 0~ff            | Bit: Stepping relay                    |
| **T**             | hhh                | 0~1ff           | Bit: Status of timer                   |
| **C**             | hh                 | 0~ff            | Bit: Status of counter                 |
| **D**             | hhhh               | 0~7fff          | Word: Temporary data storage           |
| **SD**            | hhhh               | 8000~80ff       | Word: Temporary data storage           |
| **TV**            | hhh                | 0~1ff           | Word: Current value of timer           |
| **CV**            | hh                 | 0~ff            | Word: Current value of counter         |

<img src="fuji.files/image005.gif" width="595" />

Note:

h represents hexadecimal system, input range is 0-9, a-f;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device.

<img src="fuji.files/image005.gif" width="595" />
