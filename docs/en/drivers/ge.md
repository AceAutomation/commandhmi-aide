# GE device driver

The device driver is used for HM series HMI to read and write the data or state of GE Fanuc series PLC register. The serial communication connection is established through the HMI serial port that of GE Fanuc series PLC, so as to operate GE Fanuc series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and GE Fanuc series PLC.

**1. Hardware connection**

Connecting cable:

RS232 (serial port RS232 protocol)

|                             |     |                     |     |
|-----------------------------|-----|---------------------|-----|
| **HM series HMI COM1/COM2** |     | **GE Fanuc series** |     |
| 2                           | RX  | 4                   | TX  |
| 3                           | TX  | 3                   | RX  |
| 5                           | GND | 8                   | GND |

|     |                                                 |     |                                                 |     |                                                |
|-----|-------------------------------------------------|-----|-------------------------------------------------|-----|------------------------------------------------|
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     | <img src="ge.files/image002.gif" width="97" /> |
|     | <img src="ge.files/image003.gif" width="130" /> |     |                                                 |     |                                                |
|     |                                                 |     | <img src="ge.files/image004.gif" width="278" /> |     |                                                |
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     |                                                |

Terminal of HM series HMI is DB9F, and that of GE Fanuc series PLC is RJ45.

**2. Software settings**

Select GE Corporation in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the GE Fanuc series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | GE Fanuc SNP-X              | GE Fanuc SNP-X/ GE Fanuc CCM                 |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
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
| **Extended mode**       | No                          |

**3. Operational register and address range**

|                   |                    |                 |                            |
|-------------------|--------------------|-----------------|----------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                |
| **%I**            | ddddd              | 1~10000         | Bit: Discrete Input        |
| **%Q**            | ddddd              | 1~10000         | Bit: Discrete Output       |
| **%M**            | ddddd              | 1~10000         | Bit: Internal Use          |
| **%S**            | ddd                | 1~128           | Bit: System Use, Read only |
| **%SA**           | ddd                | 1~128           | Bit: System Use, Read only |
| **%SB**           | ddd                | 1~128           | Bit: System Use, Read only |
| **%SC**           | ddd                | 1~128           | Bit: System Use, Read only |
| **%T**            | ddd                | 1~256           | Bit: Temporary Status      |
| **%G**            | dddd               | 1~7680          | Bit: Genius? Global        |
| **%AI**           | ddddd              | 1~10000         | Word: Analog Input         |
| **%AQ**           | ddddd              | 1~10000         | Word: Analog Output        |
| **%R**            | ddddd              | 1~32640         | Word: Register memory      |

 <img src="ge.files/image005.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

o represents octal system, input range is 0-7;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device.

<img src="ge.files/image005.gif" width="595" />
