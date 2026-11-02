# Xinje device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of Thinget XC/XCM/XD series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of Thinget XC/XCM/XD series PLC, so as to operate Thinget XC/XCM/XD series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Thinget XC/XCM/XD series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with Thinget XC/XCM/XD series PLC</p>
<p><strong>1.  Hardware connection</strong></p>
<p>Connecting cable:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI series touch screen COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Thinget XC/XCM/XD series</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="xinje.files/image006.gif" width="130" /><img src="xinje.files/image007.gif" width="280" /><img src="xinje.files/image008.gif" width="146" /></p></td>
</tr>
</tbody>
</table>

Terminal of HMI is DB9F, and that of Thinget XC/XCM/XD series PLC is MD8M.

**2. Software settings**

Select Xinje Electronic in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Guarantee that communication parameters in touch screen connection parameters and PLC station number are consistent with the connected PLC.

For settings of the connected PLC, please consult related technical documents of Thinget XC/XCM/XD series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | Thinget XC Series           | Thinget XC/XCM/XD Series                     |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 1                           | 0 to 255                                     |
| **HMI station number**      | 0                           | 0 to 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Offline simulation**  | Yes                         |
| **Online simulation**   | Yes                         |
| **Extended mode**       | Yes                         |

**3. Operational register and address scope**

Thinget XC/XCM Series

|                   |                    |                 |                                    |
|-------------------|--------------------|-----------------|------------------------------------|
| **Register name** | **Address format** | **Input scope** | **Remarks**                        |
| **X**             | dddd               | 0 to 1037       | Bit: input coil                    |
| **Y**             | dddd               | 0 to 1037       | Bit: output coil                   |
| **M**             | dddd               | 0 to 8767       | Bit: internal coil                 |
| **S**             | dddd               | 0 to 1023       | Bit: process                       |
| **T**             | ddd                | 0 to 639        | Bit: timer state                   |
| **C**             | ddd                | 0 to 639        | Bit: counter state                 |
| **D**             | dddd               | 0 to 9023       | Word: data register                |
| **TD**            | ddd                | 0 to 639        | Word: current value of the timer   |
| **CD**            | ddd                | 0 to 639        | Word: current value of the counter |
| **FD**            | dddd               | 0 to 9023       | Word: FlashROM register            |
| **ED**            | ddddd              | 0 to 16383      | Word: extended internal register   |

Thinget XD2 Series

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Register name</strong></p></td>
<td><p><strong>Address format</strong></p></td>
<td><p><strong>Input scope</strong></p></td>
<td><p><strong>Remarks</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>X</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Input coil</p></td>
</tr>
<tr class="odd">
<td><p><strong>Y</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Output coil</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Internal relay</p></td>
</tr>
<tr class="odd">
<td><p><strong>HM</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~959</p></td>
<td><p>Internal relay</p></td>
</tr>
<tr class="even">
<td><p><strong>SM</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Special internal relay</p></td>
</tr>
<tr class="odd">
<td><p><strong>S</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Technological process</p></td>
</tr>
<tr class="even">
<td><p><strong>HS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~127</p></td>
<td><p>Technological process</p></td>
</tr>
<tr class="odd">
<td><p><strong>T</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>timer</p></td>
</tr>
<tr class="even">
<td><p><strong>TD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Timer current value</p></td>
</tr>
<tr class="odd">
<td><p><strong>HT</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>timer</p></td>
</tr>
<tr class="even">
<td><p><strong>ET</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Precision timer</p></td>
</tr>
<tr class="odd">
<td><p><strong>ETD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~31</p></td>
<td><p>Extended internal register</p></td>
</tr>
<tr class="even">
<td><p><strong>C</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Counter</p></td>
</tr>
<tr class="odd">
<td><p><strong>CD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Counter current value</p></td>
</tr>
<tr class="even">
<td><p><strong>HC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Counter</p></td>
</tr>
<tr class="odd">
<td><p><strong> HSC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>High-speed counter</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Data register</p></td>
</tr>
<tr class="odd">
<td><p><strong>HD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~999</p></td>
<td><p>Data register</p></td>
</tr>
<tr class="even">
<td><p><strong>SD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Special data register</p></td>
</tr>
<tr class="odd">
<td><p><strong>HSD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~499</p></td>
<td><p>Special data register</p></td>
</tr>
<tr class="even">
<td><p><strong>FD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~4095</p></td>
<td><p>FlashROMregister</p></td>
</tr>
<tr class="odd">
<td><p><strong>SFD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1999</p></td>
<td><p>FlashROMregister</p></td>
</tr>
<tr class="even">
<td><p><strong>FS</strong></p></td>
<td><p>dd</p></td>
<td><p>0~47</p></td>
<td><p>Special security register</p></td>
</tr>
<tr class="odd">
<td><p><strong>SEM</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Sequential function block WAIT<br />
Command coil</p></td>
</tr>
</tbody>
</table>

Thinget XD3 Series

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Register name** | **Address format** | **Input scope** | **Remarks**                                                                                                      |
| **X**             | ooooo              | 0~20077         | Input coil (X10000~X11177 belongs to extended module) (X20000~X20277 belongs to extended BD module)              |
| **Y**             | ooooo              | 0~20077         | The output coil (Y10000~Y11177 belongs to the extended module) (Y20000~Y20277 belongs to the extended BD module) |
| **M**             | dddd               | 0~7999          | Internal relay                                                                                                   |
| **HM**            | ddd                | 0~959           | Internal relay                                                                                                   |
| **SM**            | dddd               | 0~2047          | Special internal relay                                                                                           |
| **S**             | dddd               | 0~1023          | Technological process                                                                                            |
| **HS**            | ddd                | 0~127           | Technological process                                                                                            |
| **T**             | ddd                | 0~575           | timer                                                                                                            |
| **TD**            | ddd                | 0~575           | Timer current value                                                                                              |
| **HT**            | dd                 | 0~95            | timer                                                                                                            |
| **ET**            | dd                 | 0~31            | Precision timer                                                                                                  |
| **ETD**           | ddd                | 0~31            | Extended internal register                                                                                       |
| **C**             | ddd                | 0~575           | Counter                                                                                                          |
| **CD**            | ddd                | 0~575           | Counter current value                                                                                            |
| **HC**            | dd                 | 0~95            | Counter                                                                                                          |
| **HSC**          | dd                 | 0~31            | High-speed counter                                                                                               |
| **D**             | dddd               | 0~7999          | Data register                                                                                                    |
| **HD**            | ddd                | 0~999           | Data register                                                                                                    |
| **SD**            | dddd               | 0~2047          | Special data register                                                                                            |
| **HSD**           | ddd                | 0~499           | Special data register                                                                                            |
| **FD**            | dddd               | 0~4095          | FlashROM register                                                                                                |
| **SFD**           | dddd               | 0~1999          | FlashROM register                                                                                                |
| **FS**            | dd                 | 0~47            | Special security register                                                                                        |
| **ID**            | ddddd              | 0~20099         | Ontology (ID10000~ID10999 is an extension module) (ID20000~20099 belongs to the extended BD module)              |
| **QD**            | ddddd              | 0~20099         | Ontology (QD10000~QD10999 is an extension module) (QD20000~QD20099 belongs to the extended BD module)            |
| **SEM**           | dd                 | 0~31            | Sequential function block WAIT Command coil                                                                      |

Thinget XD5/XDM Series

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Register name** | **Address format** | **Input scope** | **Remarks**                                                                                                      |
| **X**             | ooooo              | 0~20077         | Input coil (X10000~X11177 belongs to extended module) (X20000~X20277 belongs to extended BD module)              |
| **Y**             | ooooo              | 0~20077         | The output coil (Y10000~Y11177 belongs to the extended module) (Y20000~Y20277 belongs to the extended BD module) |
| **M**             | ddddd              | 0~20479         | Internal relay                                                                                                   |
| **HM**            | ddddd              | 0~11999         | Internal relay                                                                                                   |
| **SM**            | dddd               | 0~4095          | Special internal relay                                                                                           |
| **S**             | dddd               | 0~7999          | Technological process                                                                                            |
| **HS**            | ddd                | 0~999           | Technological process                                                                                            |
| **T**             | dddd               | 0~4095          | timer                                                                                                            |
| **TD**            | ddd                | 0~575           | Timer current value                                                                                              |
| **HT**            | dddd               | 0~1023          | timer                                                                                                            |
| **ET**            | dd                 | 0~39            | Precision timer                                                                                                  |
| **ETD**           | ddd                | 0~39            | Extended internal register                                                                                       |
| **C**             | dddd               | 0~4095          | Counter                                                                                                          |
| **CD**            | ddd                | 0~4095          | Counter current value                                                                                            |
| **HC**            | dddd               | 0~1023          | Counter                                                                                                          |
| **HSC**          | dd                 | 0~36            | High-speed counter                                                                                               |
| **D**             | ddddd              | 0~20479         | Data register                                                                                                    |
| **HD**            | ddddd              | 0~6143          | Data register                                                                                                    |
| **SD**            | dddd               | 0~4095          | Special data register                                                                                            |
| **HSD**           | dddd               | 0~1023          | Special data register                                                                                            |
| **FD**            | dddd               | 0~4095          | FlashROM register                                                                                                |
| **SFD**           | dddd               | 0~5999          | FlashROM register                                                                                                |
| **FS**            | dd                 | 0~47            | Special security register                                                                                        |
| **ID**            | ddddd              | 0~20099         | Ontology (ID10000~ID10999 is an extension module) (ID20000~20099 belongs to the extended BD module)              |
| **QD**            | ddddd              | 0~20099         | Ontology (QD10000~QD10999 is an extension module) (QD20000~QD20099 belongs to the extended BD module)            |
| **SEM**           | ddd                | 0~127           | Sequential function block WAIT Command coil                                                                      |

<img src="xinje.files/image009.gif" width="595" />

Note:

d represents decimal system, input scope is 0-9;

o represents octal input range 0-7;

Word in the remarks: represents the register can only be used as word;

Bit in the remarks: represents the register can only be used as bit;

Read only in the remarks represents that the register can only be read but not be written;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="xinje.files/image011.gif" width="595" />
