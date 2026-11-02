# Data operation function

|                       |                                                                |
|-----------------------|----------------------------------------------------------------|
| **Function name**     | **function**                                                   |
| **[GETBIT](#GETBIT)** | Get bit value.                                                 |
| **[HIByte](#HIByte)** | Retrieve the high byte from the low word of a specified value. |
| **[HIWord](#HIWord)** | Retrieve the high word from the specified value.               |
| **[INVBIT](#INVBIT)** | Set specific bit to be inversed (ON-&gt;OFF, OFF-&gt;ON).          |
| **[LOByte](#LOByte)** | Retrieve the low byte from the specified value.                |
| **[LOWord](#LOWord)** | Retrieve the low word from the specified value.                |
| **[SWAPB](#SWAPB)**   | Swap the low byte and high byte of the specified value.        |
| **[SWAPW](#SWAPW)**   | Swap the low word and high word of the specified value.        |
| **[SETBIT](#SETBIT)** | Set specific bit to be ON or OFF.                              |

**1、<span id="GETBIT"></span>GETBIT**

**\[Description\]**

  Get bit value.

   **\[Usage\]**

  result = GETBIT(source, bit_pos )；

**\[Example\]**

```c
short source = 0x5, bit_pos = 0 ,result；
result = GETBIT(source,bit_pos)；// result == 1
```

**2、<span id="HIByte"></span>HIByte**

**\[Description\]**

Retrieve the high byte from the low word of a specified value.

**\[Usage\]**

result=HIByte(source)；

**\[Example\]**

```c
short source = 0x1234,result；
result=HIByte(source)；// result = 0x12
```

**3、 <span id="HIWord"></span>HIWord**

**\[Description\]**

Retrieve the high word from the specified value.

**\[Usage\]**

result=HIWord(source)；

**\[Example\]**

```c
int source = 0x45232568,result；
result=HIWord(source)；// result = 0x4523
```

**4、<span id="INVBIT"></span>INVBIT**

**\[Description\]**

Set specific bit to be inversed (ON-&gt;OFF, OFF-&gt;ON).

**\[Usage\]**

result = INVBIT(source, bit_pos )；

**\[Example\]**

```c
short source = 0x6, bit_pos =1 ,result；
result=INVBIT(source, bit_pos)；// result = 4
```

**5、<span id="LOByte"></span>LOByte**

\[**Description\]**

Retrieve the low byte from the specified value.

**\[Usage\]**

result=LOByte(source)；

**\[Example\]**

```c
short source = 0x1234,result；
result= LOByte(source)；// result = 0x34
```

**6、 <span id="LOWord"></span>LOWord**

**\[Description\]**

Retrieve the low word from the specified value.

**\[Usage\]**

result=LOWord(source)；

**\[Example\]**

```c
int source = 0x12345678,result；
result=LOWord(source)；// result == 0x5678
```

**7、<span id="SWAPB"></span>SWAPB**

**\[Description\]**

Swap the low byte and high byte of the specified value.

**\[Usage\]**

result=SWAPB(source)；

**\[Example\]**

```c
short source = 0x1234,result；
result=SWAPB(source)；// result = 0x3412
```

**8、<span id="SWAPW"></span>SWAPW**

**\[Description\]**

Swap the low word and high word of the specified value.

**\[Usage\]**

result=SWAPW(source)；

**\[Example\]**

int  source = 0x12345678, ；

int  result；

result=SWAPW(source)；//  result = 0x56781234

**9、<span id="SETBIT"></span>SETBIT**

**\[Description\]**

Set specific bit to be ON or OFF.

**\[Usage\]**

result = SETBIT(source,bit_pos,1)；

**\[Example\]**

```c
short source = 0x4；
short bit_pos = 1, result；
result = SETBIT(source,bit_pos,1)；// result = 0x6
```
