# Bewerkingsfuncties voor gegevens

|                       |                                                                |
|-----------------------|----------------------------------------------------------------|
| **Functienaam**     | **Functie**                                                   |
| **[GETBIT](#GETBIT)** | Leest de waarde van een bit.                                                 |
| **[HIByte](#HIByte)** | Geeft de hoge byte van het lage woord van een waarde. |
| **[HIWord](#HIWord)** | Geeft het hoge woord van een waarde.               |
| **[INVBIT](#INVBIT)** | Inverteert een bepaalde bit (ON-&gt;OFF, OFF-&gt;ON).          |
| **[LOByte](#LOByte)** | Geeft de lage byte van een waarde.                |
| **[LOWord](#LOWord)** | Geeft het lage woord van een waarde.                |
| **[SWAPB](#SWAPB)**   | Verwisselt de lage en hoge byte van een waarde.        |
| **[SWAPW](#SWAPW)**   | Verwisselt het lage en hoge woord van een waarde.        |
| **[SETBIT](#SETBIT)** | Zet een bepaalde bit op ON of OFF.                              |

**1、<span id="GETBIT"></span>GETBIT**

**\[Beschrijving\]**

  Leest de waarde van een bit.

   **\[Gebruik\]**

  result = GETBIT(source, bit_pos )；

**\[Voorbeeld\]**

```c
short source = 0x5, bit_pos = 0 ,result；
result = GETBIT(source,bit_pos)；// result == 1
```

**2、<span id="HIByte"></span>HIByte**

**\[Beschrijving\]**

Haalt de hoge byte uit het lage woord van een waarde.

**\[Gebruik\]**

result=HIByte(source)；

**\[Voorbeeld\]**

```c
short source = 0x1234,result；
result=HIByte(source)；// result = 0x12
```

**3、 <span id="HIWord"></span>HIWord**

**\[Beschrijving\]**

Haalt het hoge woord uit een waarde.

**\[Gebruik\]**

result=HIWord(source)；

**\[Voorbeeld\]**

```c
int source = 0x45232568,result；
result=HIWord(source)；// result = 0x4523
```

**4、<span id="INVBIT"></span>INVBIT**

**\[Beschrijving\]**

Inverteert een bepaalde bit (ON-&gt;OFF, OFF-&gt;ON).

**\[Gebruik\]**

result = INVBIT(source, bit_pos )；

**\[Voorbeeld\]**

```c
short source = 0x6, bit_pos =1 ,result；
result=INVBIT(source, bit_pos)；// result = 4
```

**5、<span id="LOByte"></span>LOByte**

\[**Beschrijving\]**

Haalt de lage byte uit een waarde.

**\[Gebruik\]**

result=LOByte(source)；

**\[Voorbeeld\]**

```c
short source = 0x1234,result；
result= LOByte(source)；// result = 0x34
```

**6、 <span id="LOWord"></span>LOWord**

**\[Beschrijving\]**

Haalt het lage woord uit een waarde.

**\[Gebruik\]**

result=LOWord(source)；

**\[Voorbeeld\]**

```c
int source = 0x12345678,result；
result=LOWord(source)；// result == 0x5678
```

**7、<span id="SWAPB"></span>SWAPB**

**\[Beschrijving\]**

Verwisselt de lage en hoge byte van een waarde.

**\[Gebruik\]**

result=SWAPB(source)；

**\[Voorbeeld\]**

```c
short source = 0x1234,result；
result=SWAPB(source)；// result = 0x3412
```

**8、<span id="SWAPW"></span>SWAPW**

**\[Beschrijving\]**

Verwisselt het lage en hoge woord van een waarde.

**\[Gebruik\]**

result=SWAPW(source)；

**\[Voorbeeld\]**

int  source = 0x12345678, ；

int  result；

result=SWAPW(source)；//  result = 0x56781234

**9、<span id="SETBIT"></span>SETBIT**

**\[Beschrijving\]**

Zet een bepaalde bit op ON of OFF.

**\[Gebruik\]**

result = SETBIT(source,bit_pos,1)；

**\[Voorbeeld\]**

```c
short source = 0x4；
short bit_pos = 1, result；
result = SETBIT(source,bit_pos,1)；// result = 0x6
```
