# Datenbearbeitungsfunktionen

|                       |                                                                |
|-----------------------|----------------------------------------------------------------|
| **Funktionsname**     | **Funktion**                                                   |
| **[GETBIT](#GETBIT)** | Liest den Wert eines Bits.                                                 |
| **[HIByte](#HIByte)** | Liefert das High-Byte des Low-Worts eines Werts. |
| **[HIWord](#HIWord)** | Liefert das High-Wort eines Werts.               |
| **[INVBIT](#INVBIT)** | Invertiert ein bestimmtes Bit (ON-&gt;OFF, OFF-&gt;ON).          |
| **[LOByte](#LOByte)** | Liefert das Low-Byte eines Werts.                |
| **[LOWord](#LOWord)** | Liefert das Low-Wort eines Werts.                |
| **[SWAPB](#SWAPB)**   | Vertauscht Low- und High-Byte eines Werts.        |
| **[SWAPW](#SWAPW)**   | Vertauscht Low- und High-Wort eines Werts.        |
| **[SETBIT](#SETBIT)** | Setzt ein bestimmtes Bit auf ON oder OFF.                              |

**1、<span id="GETBIT"></span>GETBIT**

**\[Beschreibung\]**

  Liest den Wert eines Bits.

   **\[Syntax\]**

  result = GETBIT(source, bit_pos )；

**\[Beispiel\]**

```c
short source = 0x5, bit_pos = 0 ,result；
result = GETBIT(source,bit_pos)；// result == 1
```

**2、<span id="HIByte"></span>HIByte**

**\[Beschreibung\]**

Liefert das High-Byte des Low-Worts eines Werts.

**\[Verwendung\]**

result=HIByte(source)；

**\[Beispiel\]**

```c
short source = 0x1234,result；
result=HIByte(source)；// result = 0x12
```

**3、 <span id="HIWord"></span>HIWord**

**\[Beschreibung\]**

Liefert das High-Wort eines Werts.

**\[Verwendung\]**

result=HIWord(source)；

**\[Beispiel\]**

```c
int source = 0x45232568,result；
result=HIWord(source)；// result = 0x4523
```

**4、<span id="INVBIT"></span>INVBIT**

**\[Beschreibung\]**

Invertiert ein bestimmtes Bit (ON-&gt;OFF, OFF-&gt;ON).

**\[Verwendung\]**

result = INVBIT(source, bit_pos )；

**\[Beispiel\]**

```c
short source = 0x6, bit_pos =1 ,result；
result=INVBIT(source, bit_pos)；// result = 4
```

**5、<span id="LOByte"></span>LOByte**

\[**Beschreibung\]**

Liefert das Low-Byte eines Werts.

**\[Verwendung\]**

result=LOByte(source)；

**\[Beispiel\]**

```c
short source = 0x1234,result；
result= LOByte(source)；// result = 0x34
```

**6、 <span id="LOWord"></span>LOWord**

**\[Beschreibung\]**

Liefert das Low-Wort eines Werts.

**\[Verwendung\]**

result=LOWord(source)；

**\[Beispiel\]**

```c
int source = 0x12345678,result；
result=LOWord(source)；// result == 0x5678
```

**7、<span id="SWAPB"></span>SWAPB**

**\[Beschreibung\]**

Vertauscht Low- und High-Byte eines Werts.

**\[Verwendung\]**

result=SWAPB(source)；

**\[Beispiel\]**

```c
short source = 0x1234,result；
result=SWAPB(source)；// result = 0x3412
```

**8、<span id="SWAPW"></span>SWAPW**

**\[Beschreibung\]**

Vertauscht Low- und High-Wort eines Werts.

**\[Verwendung\]**

result=SWAPW(source)；

**\[Beispiel\]**

int  source = 0x12345678, ；

int  result；

result=SWAPW(source)；//  result = 0x56781234

**9、<span id="SETBIT"></span>SETBIT**

**\[Beschreibung\]**

Setzt ein bestimmtes Bit auf ON oder OFF.

**\[Verwendung\]**

result = SETBIT(source,bit_pos,1)；

**\[Beispiel\]**

```c
short source = 0x4；
short bit_pos = 1, result；
result = SETBIT(source,bit_pos,1)；// result = 0x6
```
