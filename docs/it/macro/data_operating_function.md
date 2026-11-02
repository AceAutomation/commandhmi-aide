# Funzioni di elaborazione dei dati

|                       |                                                                |
|-----------------------|----------------------------------------------------------------|
| **Nome funzione**     | **Funzione**                                                   |
| **[GETBIT](#GETBIT)** | Legge il valore di un bit.                                     |
| **[HIByte](#HIByte)** | Restituisce il byte alto della word bassa del valore specificato. |
| **[HIWord](#HIWord)** | Restituisce la word alta del valore specificato.               |
| **[INVBIT](#INVBIT)** | Inverte un bit specifico (ON-&gt;OFF, OFF-&gt;ON).                 |
| **[LOByte](#LOByte)** | Restituisce il byte basso del valore specificato.              |
| **[LOWord](#LOWord)** | Restituisce la word bassa del valore specificato.              |
| **[SWAPB](#SWAPB)**   | Scambia il byte basso e il byte alto del valore specificato.   |
| **[SWAPW](#SWAPW)**   | Scambia la word bassa e la word alta del valore specificato.   |
| **[SETBIT](#SETBIT)** | Imposta un bit specifico a ON o OFF.                           |

**1、<span id="GETBIT"></span>GETBIT**

**\[Descrizione\]**

Legge il valore di un bit.

   **\[Sintassi\]**

  result = GETBIT(source, bit_pos )；

**\[Esempio\]**

```c
short source = 0x5, bit_pos = 0 ,result；
result = GETBIT(source,bit_pos)；// result == 1
```

**2、<span id="HIByte"></span>HIByte**

**\[Descrizione\]**

Estrae il byte alto dalla word bassa del valore specificato.

**\[Sintassi\]**

result=HIByte(source)；

**\[Esempio\]**

```c
short source = 0x1234,result；
result=HIByte(source)；// result = 0x12
```

**3、 <span id="HIWord"></span>HIWord**

**\[Descrizione\]**

Estrae la word alta dal valore specificato.

**\[Sintassi\]**

result=HIWord(source)；

**\[Esempio\]**

```c
int source = 0x45232568,result；
result=HIWord(source)；// result = 0x4523
```

**4、<span id="INVBIT"></span>INVBIT**

**\[Descrizione\]**

Inverte il bit specificato (ON->OFF, OFF->ON).

**\[Sintassi\]**

result = INVBIT(source, bit_pos )；

**\[Esempio\]**

```c
short source = 0x6, bit_pos =1 ,result；
result=INVBIT(source, bit_pos)；// result = 4
```

**5、<span id="LOByte"></span>LOByte**

\[**Descrizione\]**

Estrae il byte basso dal valore specificato.

**\[Sintassi\]**

result=LOByte(source)；

**\[Esempio\]**

```c
short source = 0x1234,result；
result= LOByte(source)；// result = 0x34
```

**6、 <span id="LOWord"></span>LOWord**

**\[Descrizione\]**

Estrae la word bassa dal valore specificato.

**\[Sintassi\]**

result=LOWord(source)；

**\[Esempio\]**

```c
int source = 0x12345678,result；
result=LOWord(source)；// result == 0x5678
```

**7、<span id="SWAPB"></span>SWAPB**

**\[Descrizione\]**

Scambia il byte basso e il byte alto del valore specificato.

**\[Sintassi\]**

result=SWAPB(source)；

**\[Esempio\]**

```c
short source = 0x1234,result；
result=SWAPB(source)；// result = 0x3412
```

**8、<span id="SWAPW"></span>SWAPW**

**\[Descrizione\]**

Scambia la word bassa e la word alta del valore specificato.

**\[Sintassi\]**

result=SWAPW(source)；

**\[Esempio\]**

int  source = 0x12345678, ；

int  result；

result=SWAPW(source)；//  result = 0x56781234

**9、<span id="SETBIT"></span>SETBIT**

**\[Descrizione\]**

Imposta il bit specificato a ON o a OFF.

**\[Sintassi\]**

result = SETBIT(source,bit_pos,1)；

**\[Esempio\]**

```c
short source = 0x4；
short bit_pos = 1, result；
result = SETBIT(source,bit_pos,1)；// result = 0x6
```
