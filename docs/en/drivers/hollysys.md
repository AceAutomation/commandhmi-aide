# HollySys device driver

The device driver is used for HMI-TOOLS series touch screen to read and write the data or state of HollySys LM series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of HollySys LM series PLC, so as to operate HollySys LM series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and HollySys LM series PLC.

**How to establish connection with HOLLYSYS series PLC**

**1.  Hardware connection**

Connecting cable:

RS232 (serial port RS232 protocol)

|                             |     |                        |     |
|-----------------------------|-----|------------------------|-----|
| **HM series HMI COM1/COM2** |     | **HollySys LM series** |     |
| 2                           | RX  | 3                      | TX  |
| 3                           | TX  | 2                      | RX  |
| 5                           | GND | 5                      | GND |

<img src="hollysys.files/image002.gif" width="130" /><img src="hollysys.files/image003.gif" width="290" /><img src="hollysys.files/image004.gif" width="130" />

Terminal of HM series HMI is DB9F, and that of HollySys LM series PLC is DB9M.

**2. Software settings**

Select HollySys Group in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the HollySys LM series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | HollySys LM Series          | HollySys LM Series                           |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 38400                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity bit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 51                          | 0~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Off-line simulation** | Yes                         |
| **On-line simulation**  | Yes                         |
| **Extended mode**       | No                          |

**3. Operational register and address range**

|                   |                    |                 |                                                                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                                                                                           |
| **IX**            | ddd.o              | 0.0~511.7       | Bit: I storage area, read only                                                                        |
| **QX**            | ddd.o              | 0.0~511.7       | Bit: Q storage area                                                                                   |
| **MX**            | dddd.o             | 0.0~7816.7      | Bit: M storage area                                                                                   |
| **IW**            | ddd                | 0~510           | Word:<span id="OLE_LINK284"></span> I storage area, 8-bit register, each word occupying two addresses |
| **QW**            | ddd                | 0~510           | Word: <span id="OLE_LINK285"></span>Q storage area, 8-bit register, each word occupying two addresses |
| **MW**            | dddd               | 0~8190          | Word: M storage area, 8-bit register, each word occupying two addresses                               |

<img src="hollysys.files/image005.gif" width="600" />

Note:

d represents decimal system, input range is 0-9;

o represents octal system, input range is 0-7;

Word in the remarks: represents the register can only used as word;

Bit in the remarks: represents the register can only used as bit;

8-bit register in the remarks: represents the address spacing between two adjacent words in the register is 2;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="hollysys.files/image005.gif" width="600" />
