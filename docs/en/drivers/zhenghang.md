# ZhengHang device driver

The device driver is used for HM series HMI to read and write the data or state of ZhengHang A5 series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Yokogawa FA-M3 series PLC, so as to operate ZhengHang A5series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and ZhengHang A5 series PLC.

How to establishment connection with ZhengHang A5 series PLC 

**1.Hardware connection**

Connecting cable:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

|                           |     |                    |     |
|---------------------------|-----|--------------------|-----|
| **HM　ＨＭＩ　COM1/COM2** |     | **ZhengHang A5　** |     |
| 2                         | RX  | 2                  | TX  |
| 3                         | TX  | 3                  | RX  |
| 5                         | GND | 5                  | GND |

<img src="zhenghang.files/image002.gif" width="130" /><img src="zhenghang.files/image003.gif" width="290" /><img src="zhenghang.files/image004.gif" width="130" />

Terminal of HMI is DB9F, and that of ZhengHang A5 series PLC is DB9M.

**2.Software settings**

Select ZhengHang Electronics in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Guarantee that communication parameters in touch screen connection parameters and PLC station number are consistent with the connected PLC.

For settings of the connected PLC, please consult related technical documents of ZhengHang A5 series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | A5 Series                   | A5 Series                                    |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity**                  | NONE                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 1                           | 0~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Offline simulation**  | Yes                         |
| **Online simulation**   | Yes                         |
| **Extended mode**       | Yes                         |

**3.Operational register and address scope**

|                   |                    |                 |                                                                           |
|-------------------|--------------------|-----------------|---------------------------------------------------------------------------|
| **Register name** | **Address format** | **Input scope** | **Remarks**                                                               |
| **I**             | dd.o               | 0.0 to 15.7     | Bit: input image register, read only                                      |
| **Q**             | dd.o               | 0.0 to 15.7     | Bit: output image register                                                |
| **M**             | dddd.o             | 0.0 to 4095.7   | Bit: bit memory                                                           |
| **VW**            | dddd               | 0 to 1998       | Word: variable memory, 8-digit register, each word occupies two addresses |
| **AIW**           | d                  | 0 to 9          | Word: analog input, read only                                             |
| **AQW**           | d                  | 0 to 9          | Word: analog output, write only                                           |

<img src="zhenghang.files/image005.gif" width="595" />

Note:

d represents decimal system, input scope is 0-9;

o represents octal system, input scope is 0-7;

Word in the remarks: represents the register can only be used as word;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="zhenghang.files/image005.gif" width="595" />
