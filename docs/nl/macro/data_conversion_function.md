# Conversiefuncties

|                                 |                                          |
|---------------------------------|------------------------------------------|
| **Functienaam**               | **Functie**                             |
| **[ASCII2DEC](#ASCII2DEC)**     | Zet een tekenreeks om in een decimale waarde.     |
| **[ASCII2FLOAT](#ASCII2FLOAT)** | Zet een tekenreeks om in een drijvendekommawaarde.    |
| **[ASCII2HEX](#ASCII2HEX)**     | Zet een tekenreeks om in een hexadecimale waarde. |
| **[BCD2BIN](#BCD2BIN)**         | Zet een BCD-waarde om in een binaire waarde.      |
| **[BIN2BCD](#BIN2BCD)**         | Zet een binaire waarde om in een BCD-waarde.   |
| **[DEC2ASCII](#DEC2ASCII)**     | Zet een decimale waarde om in een tekenreeks.     |
| **[FLOAT2ASCII](#FLOAT2ASCII)** | Zet een drijvendekommawaarde om in een tekenreeks.    |
| **[HEX2ASCII](#HEX2ASCII)**     | Zet een hexadecimale waarde om in een tekenreeks. |

**1、<span id="ASCII2DEC"></span>ASCII2DEC**

**\[Beschrijving\]**

Zet een tekenreeks om in een decimale waarde.

**\[Gebruik\]**

result=ASCII2DEC(source , sizeof(source))；

**\[Voorbeeld\]**

char source\[4\] = {'2', '3', '4', '5'}；

short result；

result=ASCII2DEC(source , 4)；//  result=2345

**2、<span id="ASCII2FLOAT"></span>ASCII2FLOAT**

**\[Beschrijving\]**

Zet een tekenreeks om in een floatwaarde.

**\[Gebruik\]**

result=ASCII2FLOAT(source,sizeof(source))；

**\[Voorbeeld\]**

char source\[4\] = {'5', '.', '7', '8'}；

float result；

result=ASCII2FLOAT(source,4)；//  result = 5.78

**3、<span id="ASCII2HEX"></span>ASCII2HEX**

**\[Beschrijving\]**

Zet een tekenreeks om in een hexadecimale waarde.

**\[Gebruik\]**

result=ASCII2HEX(source,sizeof(source))；

**\[Voorbeeld\]**

char source\[5\] = {'1','6','3','4'}；

short result；

result=ASCII2HEX(source,4)；//  result = 0x1634

**4、<span id="BCD2BIN"></span>BCD2BIN**

**\[Beschrijving\]**

Zet een BCD-waarde om in een binaire waarde.

**\[Gebruik\]**

result=BCD2BIN(source)；

**\[Voorbeeld\]**

short source = 0x2648；

short result；

result=BCD2BIN(source)；  //  result = 2648

**5、<span id="BIN2BCD"></span>BIN2BCD**

**\[Beschrijving\]**

Zet een binaire waarde om in een BCD-waarde.

**\[Gebruik\]**

result=BIN2BCD(source)；

**\[Voorbeeld\]**

short source = 1234；

short result；

result=BIN2BCD(source)；//  result = 0x1234

**6、<span id="DEC2ASCII"></span>DEC2ASCII**

**\[Beschrijving\]**

Zet een decimale waarde om in een tekenreeks.

**\[Gebruik\]**

result= DEC2ASCII(source,sizeof(source))；

**\[Voorbeeld\]**

short source = 5678；

char \*result；

```c
result= DEC2ASCII(source,4)；
// result[0] == '5', result[1] == '6', result[2] == '7', result[3] == '8’
```

**7、<span id="FLOAT2ASCII"></span>FLOAT2ASCII**

**\[Beschrijving\]**

Zet een floatwaarde om in een tekenreeks.

**\[Gebruik\]**

result=FLOAT2ASCII(source);

**\[Voorbeeld\]**

```c
float source = 56.8;
char result[4];
result=FLOAT2ASCII(source);
//result[0] = '5',result[1] = '6',result[2] = '.',result[3] = '8'
```

**8、<span id="HEX2ASCII"></span>HEX2ASCII**

**\[Beschrijving\]**

Zet een hexadecimale waarde om in een tekenreeks.

**\[Gebruik\]**

HEX2ASCII(source, result\[start\])；

**\[Voorbeeld\]**

short source = 0x5678；

char \*result；

```c
result = HEX2ASCII(source)；
//result[0] = '5', result[1] = '6', result[2] = '7', result[3] = '8'
```
