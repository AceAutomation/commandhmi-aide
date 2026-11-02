# Datenumwandlungsfunktionen

|                                 |                                          |
|---------------------------------|------------------------------------------|
| **Funktionsname**               | **Funktion**                             |
| **[ASCII2DEC](#ASCII2DEC)**     | Wandelt eine Zeichenkette in einen Dezimalwert um.     |
| **[ASCII2FLOAT](#ASCII2FLOAT)** | Wandelt eine Zeichenkette in eine Gleitkommazahl um.    |
| **[ASCII2HEX](#ASCII2HEX)**     | Wandelt eine Zeichenkette in einen Hexadezimalwert um. |
| **[BCD2BIN](#BCD2BIN)**         | Wandelt einen BCD-Wert in einen Binärwert um.      |
| **[BIN2BCD](#BIN2BCD)**         | Wandelt einen Binärwert in einen BCD-Wert um.   |
| **[DEC2ASCII](#DEC2ASCII)**     | Wandelt einen Dezimalwert in eine Zeichenkette um.     |
| **[FLOAT2ASCII](#FLOAT2ASCII)** | Wandelt eine Gleitkommazahl in eine Zeichenkette um.    |
| **[HEX2ASCII](#HEX2ASCII)**     | Wandelt einen Hexadezimalwert in eine Zeichenkette um. |

**1、<span id="ASCII2DEC"></span>ASCII2DEC**

**\[Beschreibung\]**

Wandelt eine Zeichenkette in einen Dezimalwert um.

**\[Verwendung\]**

result=ASCII2DEC(source , sizeof(source))；

**\[Beispiel\]**

char source\[4\] = {'2', '3', '4', '5'}；

short result；

result=ASCII2DEC(source , 4)；//  result=2345

**2、<span id="ASCII2FLOAT"></span>ASCII2FLOAT**

**\[Beschreibung\]**

Wandelt eine Zeichenkette in eine Gleitkommazahl um.

**\[Syntax\]**

result=ASCII2FLOAT(source,sizeof(source))；

**\[Beispiel\]**

char source\[4\] = {'5', '.', '7', '8'}；

float result；

result=ASCII2FLOAT(source,4)；//  result = 5.78

**3、<span id="ASCII2HEX"></span>ASCII2HEX**

**\[Beschreibung\]**

Wandelt eine Zeichenkette in einen Hexadezimalwert um.

**\[Verwendung\]**

result=ASCII2HEX(source,sizeof(source))；

**\[Beispiel\]**

char source\[5\] = {'1','6','3','4'}；

short result；

result=ASCII2HEX(source,4)；//  result = 0x1634

**4、<span id="BCD2BIN"></span>BCD2BIN**

**\[Beschreibung\]**

Wandelt einen BCD-Wert in einen Binärwert um.

**\[Verwendung\]**

result=BCD2BIN(source)；

**\[Beispiel\]**

short source = 0x2648；

short result；

result=BCD2BIN(source)；  //  result = 2648

**5、<span id="BIN2BCD"></span>BIN2BCD**

**\[Beschreibung\]**

Wandelt einen Binärwert in einen BCD-Wert um.

**\[Syntax\]**

result=BIN2BCD(source)；

**\[Beispiel\]**

short source = 1234；

short result；

result=BIN2BCD(source)；//  result = 0x1234

**6、<span id="DEC2ASCII"></span>DEC2ASCII**

**\[Beschreibung\]**

Wandelt einen Dezimalwert in eine Zeichenkette um.

**\[Verwendung\]**

result= DEC2ASCII(source,sizeof(source))；

**\[Beispiel\]**

short source = 5678；

char \*result；

```c
result= DEC2ASCII(source,4)；
// result[0] == '5', result[1] == '6', result[2] == '7', result[3] == '8’
```

**7、<span id="FLOAT2ASCII"></span>FLOAT2ASCII**

**\[Beschreibung\]**

Wandelt eine Gleitkommazahl in eine Zeichenkette um.

**\[Verwendung\]**

result=FLOAT2ASCII(source);

**\[Beispiel\]**

```c
float source = 56.8;
char result[4];
result=FLOAT2ASCII(source);
//result[0] = '5',result[1] = '6',result[2] = '.',result[3] = '8'
```

**8、<span id="HEX2ASCII"></span>HEX2ASCII**

**\[Beschreibung\]**

Wandelt einen Hexadezimalwert in eine Zeichenkette um.

**\[Verwendung\]**

HEX2ASCII(source, result\[start\])；

**\[Beispiel\]**

short source = 0x5678；

char \*result；

```c
result = HEX2ASCII(source)；
//result[0] = '5', result[1] = '6', result[2] = '7', result[3] = '8'
```
