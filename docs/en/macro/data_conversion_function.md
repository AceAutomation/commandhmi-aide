# Data switch function

|                                 |                                          |
|---------------------------------|------------------------------------------|
| **Function name**               | **function**                             |
| **[ASCII2DEC](#ASCII2DEC)**     | Convert a string to a decimal value.     |
| **[ASCII2FLOAT](#ASCII2FLOAT)** | Convert a string to a floating value.    |
| **[ASCII2HEX](#ASCII2HEX)**     | Convert a string to a hexadecimal value. |
| **[BCD2BIN](#BCD2BIN)**         | Convert a BCD value to a BIN value.      |
| **[BIN2BCD](#BIN2BCD)**         | Convert a binary value to a BCD value.   |
| **[DEC2ASCII](#DEC2ASCII)**     | Convert a decimal value to a string.     |
| **[FLOAT2ASCII](#FLOAT2ASCII)** | Convert a floating value to a string.    |
| **[HEX2ASCII](#HEX2ASCII)**     | Convert a hexadecimal value to a string. |

**1、<span id="ASCII2DEC"></span>ASCII2DEC**

**\[Description\]**

Convert a string to a decimal value.

**\[Usage\]**

result=ASCII2DEC(source , sizeof(source))；

**\[Example\]**

char source\[4\] = {'2', '3', '4', '5'}；

short result；

result=ASCII2DEC(source , 4)；//  result=2345

**2、<span id="ASCII2FLOAT"></span>ASCII2FLOAT**

**\[Description\]**

Convert a string to a floating value.

**\[Usage\]**

result=ASCII2FLOAT(source,sizeof(source))；

**\[Example\]**

char source\[4\] = {'5', '.', '7', '8'}；

float result；

result=ASCII2FLOAT(source,4)；//  result = 5.78

**3、<span id="ASCII2HEX"></span>ASCII2HEX**

**\[Description\]**

Convert a string to a hexadecimal value.

**\[Usage\]**

result=ASCII2HEX(source,sizeof(source))；

**\[Example\]**

char source\[5\] = {'1','6','3','4'}；

short result；

result=ASCII2HEX(source,4)；//  result = 0x1634

**4、<span id="BCD2BIN"></span>BCD2BIN**

**\[Description\]**

Convert a BCD value to a BIN value.

**\[Usage\]**

result=BCD2BIN(source)；

**\[Example\]**

short source = 0x2648；

short result；

result=BCD2BIN(source)；  //  result = 2648

**5、<span id="BIN2BCD"></span>BIN2BCD**

**\[Description\]**

Convert a binary value to a BCD value.

**\[Usage\]**

result=BIN2BCD(source)；

**\[Example\]**

short source = 1234；

short result；

result=BIN2BCD(source)；//  result = 0x1234

**6、<span id="DEC2ASCII"></span>DEC2ASCII**

**\[Description\]**

Convert a decimal value to a string.

**\[Usage\]**

result= DEC2ASCII(source,sizeof(source))；

**\[Example\]**

short source = 5678；

char \*result；

```c
result= DEC2ASCII(source,4)；
// result[0] == '5', result[1] == '6', result[2] == '7', result[3] == '8’
```

**7、<span id="FLOAT2ASCII"></span>FLOAT2ASCII**

**\[Description\]**

Convert a floating value to a string.

**\[Usage\]**

result=FLOAT2ASCII(source);

**\[Example\]**

```c
float source = 56.8;
char result[4];
result=FLOAT2ASCII(source);
//result[0] = '5',result[1] = '6',result[2] = '.',result[3] = '8'
```

**8、<span id="HEX2ASCII"></span>HEX2ASCII**

**\[Description\]**

Convert a hexadecimal value to a string.

**\[Usage\]**

HEX2ASCII(source, result\[start\])；

**\[Example\]**

short source = 0x5678；

char \*result；

```c
result = HEX2ASCII(source)；
//result[0] = '5', result[1] = '6', result[2] = '7', result[3] = '8'
```
