# Fonctions de manipulation de données

|                       |                                                                |
|-----------------------|----------------------------------------------------------------|
| **Nom de fonction**   | **Fonction**                                                   |
| **[GETBIT](#GETBIT)** | Lit la valeur d'un bit.                                        |
| **[HIByte](#HIByte)** | Retourne l'octet de poids fort du mot de poids faible de la valeur. |
| **[HIWord](#HIWord)** | Retourne le mot de poids fort de la valeur.                    |
| **[INVBIT](#INVBIT)** | Inverse un bit donné (ON-&gt;OFF, OFF-&gt;ON).                     |
| **[LOByte](#LOByte)** | Retourne l'octet de poids faible de la valeur.                 |
| **[LOWord](#LOWord)** | Retourne le mot de poids faible de la valeur.                  |
| **[SWAPB](#SWAPB)**   | Échange l'octet de poids faible et l'octet de poids fort de la valeur. |
| **[SWAPW](#SWAPW)**   | Échange le mot de poids faible et le mot de poids fort de la valeur. |
| **[SETBIT](#SETBIT)** | Met un bit donné à ON ou OFF.                                  |

**1、<span id="GETBIT"></span>GETBIT**

**\[Description\]**

  Lit la valeur d'un bit.

   **\[Syntaxe\]**

  result = GETBIT(source, bit_pos )；

**\[Exemple\]**

```c
short source = 0x5, bit_pos = 0 ,result；
result = GETBIT(source,bit_pos)；// result == 1
```

**2、<span id="HIByte"></span>HIByte**

**\[Description\]**

Retourne l'octet de poids fort du mot de poids faible de la valeur.

**\[Syntaxe\]**

result=HIByte(source)；

**\[Exemple\]**

```c
short source = 0x1234,result；
result=HIByte(source)；// result = 0x12
```

**3、 <span id="HIWord"></span>HIWord**

**\[Description\]**

Retourne le mot de poids fort de la valeur.

**\[Syntaxe\]**

result=HIWord(source)；

**\[Exemple\]**

```c
int source = 0x45232568,result；
result=HIWord(source)；// result = 0x4523
```

**4、<span id="INVBIT"></span>INVBIT**

**\[Description\]**

Inverse un bit donné (ON-&gt;OFF, OFF-&gt;ON).

**\[Syntaxe\]**

result = INVBIT(source, bit_pos )；

**\[Exemple\]**

```c
short source = 0x6, bit_pos =1 ,result；
result=INVBIT(source, bit_pos)；// result = 4
```

**5、<span id="LOByte"></span>LOByte**

\[**Description\]**

Retourne l'octet de poids faible de la valeur.

**\[Syntaxe\]**

result=LOByte(source)；

**\[Exemple\]**

```c
short source = 0x1234,result；
result= LOByte(source)；// result = 0x34
```

**6、 <span id="LOWord"></span>LOWord**

**\[Description\]**

Retourne le mot de poids faible de la valeur.

**\[Syntaxe\]**

result=LOWord(source)；

**\[Exemple\]**

```c
int source = 0x12345678,result；
result=LOWord(source)；// result == 0x5678
```

**7、<span id="SWAPB"></span>SWAPB**

**\[Description\]**

Échange l'octet de poids faible et l'octet de poids fort de la valeur.

**\[Syntaxe\]**

result=SWAPB(source)；

**\[Exemple\]**

```c
short source = 0x1234,result；
result=SWAPB(source)；// result = 0x3412
```

**8、<span id="SWAPW"></span>SWAPW**

**\[Description\]**

Échange le mot de poids faible et le mot de poids fort de la valeur.

**\[Syntaxe\]**

result=SWAPW(source)；

**\[Exemple\]**

int  source = 0x12345678, ；

int  result；

result=SWAPW(source)；//  result = 0x56781234

**9、<span id="SETBIT"></span>SETBIT**

**\[Description\]**

Met un bit donné à ON ou OFF.

**\[Syntaxe\]**

result = SETBIT(source,bit_pos,1)；

**\[Exemple\]**

```c
short source = 0x4；
short bit_pos = 1, result；
result = SETBIT(source,bit_pos,1)；// result = 0x6
```
