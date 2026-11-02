# Funciones de manipulación de datos

|                       |                                                                |
|-----------------------|----------------------------------------------------------------|
| **Nombre de la función**     | **Función**                                                   |
| **[GETBIT](#GETBIT)** | Lee el valor de un bit.                                                 |
| **[HIByte](#HIByte)** | Devuelve el byte alto de la palabra baja de un valor. |
| **[HIWord](#HIWord)** | Devuelve la palabra alta de un valor.               |
| **[INVBIT](#INVBIT)** | Invierte un bit concreto (ON-&gt;OFF, OFF-&gt;ON).          |
| **[LOByte](#LOByte)** | Devuelve el byte bajo de un valor.                |
| **[LOWord](#LOWord)** | Devuelve la palabra baja de un valor.                |
| **[SWAPB](#SWAPB)**   | Intercambia el byte bajo y el alto de un valor.        |
| **[SWAPW](#SWAPW)**   | Intercambia la palabra baja y la alta de un valor.        |
| **[SETBIT](#SETBIT)** | Pone un bit concreto a ON u OFF.                              |

**1、<span id="GETBIT"></span>GETBIT**

**\[Descripción\]**

  Lee el valor de un bit.

   **\[Uso\]**

  result = GETBIT(source, bit_pos )；

**\[Ejemplo\]**

```c
short source = 0x5, bit_pos = 0 ,result；
result = GETBIT(source,bit_pos)；// result == 1
```

**2、<span id="HIByte"></span>HIByte**

**\[Descripción\]**

Devuelve el byte alto de la palabra baja de un valor.

**\[Uso\]**

result=HIByte(source)；

**\[Ejemplo\]**

```c
short source = 0x1234,result；
result=HIByte(source)；// result = 0x12
```

**3、 <span id="HIWord"></span>HIWord**

**\[Descripción\]**

Devuelve la palabra alta de un valor.

**\[Uso\]**

result=HIWord(source)；

**\[Ejemplo\]**

```c
int source = 0x45232568,result；
result=HIWord(source)；// result = 0x4523
```

**4、<span id="INVBIT"></span>INVBIT**

**\[Descripción\]**

Invierte un bit concreto (ON-&gt;OFF, OFF-&gt;ON).

**\[Uso\]**

result = INVBIT(source, bit_pos )；

**\[Ejemplo\]**

```c
short source = 0x6, bit_pos =1 ,result；
result=INVBIT(source, bit_pos)；// result = 4
```

**5、<span id="LOByte"></span>LOByte**

\[**Descripción\]**

Devuelve el byte bajo de un valor.

**\[Uso\]**

result=LOByte(source)；

**\[Ejemplo\]**

```c
short source = 0x1234,result；
result= LOByte(source)；// result = 0x34
```

**6、 <span id="LOWord"></span>LOWord**

**\[Descripción\]**

Devuelve la palabra baja de un valor.

**\[Uso\]**

result=LOWord(source)；

**\[Ejemplo\]**

```c
int source = 0x12345678,result；
result=LOWord(source)；// result == 0x5678
```

**7、<span id="SWAPB"></span>SWAPB**

**\[Descripción\]**

Intercambia el byte bajo y el alto de un valor.

**\[Uso\]**

result=SWAPB(source)；

**\[Ejemplo\]**

```c
short source = 0x1234,result；
result=SWAPB(source)；// result = 0x3412
```

**8、<span id="SWAPW"></span>SWAPW**

**\[Descripción\]**

Intercambia la palabra baja y la alta de un valor.

**\[Uso\]**

result=SWAPW(source)；

**\[Ejemplo\]**

int  source = 0x12345678, ；

int  result；

result=SWAPW(source)；//  result = 0x56781234

**9、<span id="SETBIT"></span>SETBIT**

**\[Descripción\]**

Pone un bit concreto a ON u OFF.

**\[Uso\]**

result = SETBIT(source,bit_pos,1)；

**\[Ejemplo\]**

```c
short source = 0x4；
short bit_pos = 1, result；
result = SETBIT(source,bit_pos,1)；// result = 0x6
```
