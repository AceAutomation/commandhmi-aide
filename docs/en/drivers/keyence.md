# Keyence device driver

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>The device driver is used for HM series HMI to read and write the data or state of Keyence KV/VisualKV series PLC register. The serial communication connection is established through the serial port on the touch screen and that of Keyence KV/VisualKV series PLC, so as to operate Keyence KV/VisualKV series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and Keyence KV/VisualKV series PLC.</p></td>
</tr>
<tr class="even">
<td><p>How to establish connection with Keyence KV/VisualKV series PLC</p>
<p><strong>1. Hardware connection</strong></p>
<p>Connecting cable:</p>
<p>RS232 (serial port RS232 protocol)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HM series HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Keyence KV/VisualKV series</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>2</p></td>
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
<td><p>3</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="keyence.files/image002.gif" width="130" /><img src="keyence.files/image003.gif" width="90" /><img src="keyence.files/image004.gif" width="278" />

Terminal of HMI is DB9F, and that of Keyence KV/VisualKV series PLC is 6-pin registered jack.

**2. Software settings**

Select Keyence Corporation in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For setting of the PLC connected, refer to the technical documents of the Keyence KV/VisualKV series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | KV-1000/700 KV-L20(R)       | KV-1000/700 KV-L20(R)/ KV-/40 KV-P16         |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity bit**              | EVEN                        | EVEN/ODD/NONE                                |
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

l  KV-1000/700 KV-L20(R)

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                    |
| **R**             | dddDD              | 0~99915         | Bit: input/output relay        |
| **MR**            | dddDD              | 0~3915          | Bit: internal auxiliary relay  |
| **LR**            | dddDD              | 0~3999          | Bit: latching relay            |
| **CR**            | ddDD               | 0~3999          | Bit: control relay             |
| **T**             | dddd               | 0~65534         | Bit: timer                     |
| **C**             | dddd               | 0~65534         | Bit: counter                   |
| **DM**            | ddddd              | 0~32766         | Word: data storage             |
| **EM**            | ddddd              | 0~511           | Word: extended data storage    |
| **FM**            | ddddd              | 0~11998         | Word: file register            |
| **TM**            | ddd                | 0~3999          | Word: temporary data storage   |
| **CM**            | ddddd              | 0~3999          | Word: control storage          |
| **TV**            | dddd               | 0~99915         | Word: current value of timer   |
| **CV**            | dddd               | 0~3915          | Word: current value of counter |

l  KV-10/16/24/40 KV-P16

|                   |                    |                 |                                           |
|-------------------|--------------------|-----------------|-------------------------------------------|
| **Register name** | **Address format** | **Input range** | **Remarks**                               |
| RLY               | dddDD              | 0~99915         | Bit: relay                                |
| T                 | dddd               | 0~999           | Bit: timer                                |
| C                 | dddd               | 0~999           | Bit: counter                              |
| DM                | ddddd              | 0~9999          | Word: data storage                        |
| TM                | ddd                | 0~99            | Word: temporary data storage              |
| TV_c              | dddd               | 0~999           | Word: current value of timer              |
| TV_p              | dddd               | 0~999           | Word: preset value of timer               |
| CV_c              | dddd               | 0~999           | Word: current value of counter            |
| CV_p              | dddd               | 0~999           | Word: preset value of counter             |
| CTH               | dddd               | 0~9             | Word: current value of high speed counter |

l  KV-Nano

|                   |                    |                 |                                      |
|-------------------|--------------------|-----------------|--------------------------------------|
| **Register name** | **Address format** | **Input scope** | **Remarks**                          |
| **R**             | ddddd              | 0~59915         | Position: relay                      |
| **B**             | DDDD               | 0~1FFF          | Link Relay                           |
| **MR**            | ddddd              | 0~59915         | Internal auxiliary relay             |
| **LR**            | ddddd              | 0~19915         | Latching relay                       |
| **CR**            | dddd               | 0~8915          | Control relay                        |
| **VB**            | DDDD               | 0~1FFF          | Working relay                        |
| **T**             | ddd                | 0~511           | Bit timer                            |
| **C**             | ddd                | 0~255           | Bit: counter                         |
| **DM**            | dddd               | 0~32767         | Data memory                          |
| **W**             | DDDD               | 0~3FFF          | Link register                        |
| **TM**            | dddd               | 0~511           | Temporary data storage               |
| **Z**             | dddd               | 1~12            | Index register                       |
| **TC**            | dddd               | 0~511           | Double word: timer (current value)   |
| **TS**            | dddd               | 0~511           | Double word: timer (set value)       |
| **CC**            | ddd                | 0~255           | Double word: counter (current value) |
| **CS**            | ddd                | 0~255           | Double word: counter (set value)     |
| **CTH**           | d                  | 0~3             | High speed counter                   |
| **CTC**           | d                  | 0~7             | Double word: high speed comparator   |
| **CM**            | dddd               | 0~8999          | Control memory                       |
| **VM**            | dddd               | 0~9999          | Working memory                       |

<img src="keyence.files/image005.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

DD represents 16 bits, input range is 0-15;

Bit in the remarks: represents the register can only be used as bit;

Word in the remarks: represents the register can only be used as word;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device.

<img src="keyence.files/image005.gif" width="595" />
