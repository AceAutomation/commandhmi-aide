# Math arithmetic function

|                       |                                                      |
|-----------------------|------------------------------------------------------|
| **Function name**     | **function**                                         |
| **[ACOS](#ACOS)**     | The result is equal to the arcosine of the source.   |
| **[ADDSUM](#ADDSUM)** | Use addition to calculate checksum.                  |
| **[ASIN](#ASIN)**     | The result is equal to the arcsine of the source.    |
| **[ATAN](#ATAN)**     | The result is equal to the arctangent of the source. |
| **[COT](#COT)**       | The result is equal to the cotangent of the source.  |
| **[COS](#COS)**       | The result is equal to the cosine of the source.     |
| **[CRC](#CRC)**       | Get 16-bit CRC.                                      |
| **[CSC](#CSC)**       | The result is equal to the cosecant of the source.   |
| **[LOG](#LOG)**       | Calculate the natural logarithm of a number.         |
| **[LOG10](#LOG10)**   | Calculate the base-10 logarithm of a number.         |
| **[POW](#POW)**       | Calculates x raised to the power of y.               |
| **[RAND](#RAND)**     | Produces a pseudorandom number (range:0~65535)       |
| **[SEC](#SEC)**       | The result is equal to the secant of the source.     |
| **[SIN](#SIN)**       | The result is equal to the sine of the source.       |
| **[SQRT](#SQRT)**     | The result is equal to the square of the source.     |
| **[TAN](#TAN)**       | The result is equal to the tangent of the source.    |
| **[XORSUM](#XORSUM)** | Use XOR to calculate checksum.                       |

**1、<span id="ACOS"></span>ACOS**

**\[Description\]**

The result is equal to the arcosine of the source.

**\[Usage\]**

result = ACOS(source);

**\[Example\]**

```c
float source=0.5;
float result;
result=ACOS(source);
```

**2、<span id="ADDSUM"></span>ADDSUM**

**\[Description\]**

Use addition to calculate checksum.

**\[Usage\]**

checksum=ADDSUM(data, sizeof(data));

**\[Example\]**

```c
char data[5] = {0x1, 0x2, 0x3, 0x4, 0x20};
int checksum;
checksum=ADDSUM(data, 5); // checksum=0x2a;
```

<span id="ASIN"></span>**3、ASIN**

**\[Description\]**

The result is equal to the arcsine of the source.

**\[Usage\]**

result = ASIN(source);

**\[Example\]**

```c
float source=0.5;
float result;
result=ASIN(source);
```

**4、<span id="ATAN"></span>ATAN**

**\[Description\]**

The result is equal to the arctangent of the source.

**\[Usage\]**

result = ATAN(source);

**\[Example\]**

```c
float source=1;
float result;
result=ATAN(source);
```

**5、<span id="COT"></span>COT**

**\[Description\]**

The result is equal to the cotangent of the source.

**\[Usage\]**

result = COT(source);

**\[Example\]**

```c
float source=45(度);
float result;
result=COT(source); //result = 1
```

**6、<span id="COS"></span>COS**

**\[Description\]**

The result is equal to the cosine of the source.

**\[Usage\]**

result = COS(source);

**\[Example\]**

```c
float source=60(度);
float result;
result=COS(source); //result = 0.5
```

**7、<span id="CRC"></span>CRC**

**\[Description\]**

Get 16-bit CRC.

**\[Usage\]**

bit_CRC=CRC(source,sizeof(source))；

**\[Example\]**

char source\[5\] = {0x1, 0x2, 0x3, 0x4, 0x5}；

short bit_CRC；

bit_CRC=CRC(source,5)；

**8、<span id="CSC"></span>CSC**

**\[Description\]**

The result is equal to the cosecant of the source.

**\[Usage\]**

result = CSC(source);

**\[Example\]**

```c
float source=30(度);
float result;
result=CSC(source); //result = 2
```

**9、<span id="LOG"></span>LOG**

**\[Description\]**

Calculate the natural logarithm of a number.

**\[Usage\]**

result = LOG(source);

**\[Example\]**

```c
float source =100,result;
result = LOG(source); //result =4.61
```

**10、<span id="LOG10"></span>LOG10**

**\[Description\]**

Calculate the base-10 logarithm of a number.

**\[Usage\]**

result = lOG10(source)

**\[Example\]**

```c
float source=100,result;
result = LOG10(source); //result = 2.00
```

**11、<span id="POW"></span>POW**

**\[Description\]**

Calculates x raised to the power of y.

**\[Usage\]**

result = POW(x,y);  note:x must be constant

**\[Example\]**

```c
float result,y;
y=0.5;
result=POW(25,y); //result = 5
```

**12、<span id="RAND"></span>RAND**

**\[Description\]**

Produces a pseudorandom number (range:0~65535)

**\[Usage\]**

Random= RAND()

**\[Example\]**

```c
unsigned short random;
random =RAND(); //random = 363
```

**13、<span id="SEC"></span>SEC**

**\[Description\]**

The result is equal to the secant of the source.

**\[Usage\]**

result = SEC(source);

**\[Example\]**

```c
float source=60(度);
float result;
result=SEC(source); //result = 2
```

**14、<span id="SIN"></span>SIN**

**\[Description\]**

The result is equal to the sine of the source.

**\[Usage\]**

result = SIN(source);

**\[Example\]**

```c
float source=30(度);
float result;
result=SIN(source); //result = 0.5
```

**15、<span id="SQRT"></span>SQRT**

**\[Description\]**

The result is equal to the square of the source.

**\[Usage\]**

result = SQRT(source);

**\[Example\]**

```c
float source=16;
float result;
result=SQRT(source); //result = 4
```

**16、<span id="TAN"></span>TAN**

**\[Description\]**

The result is equal to the tangent of the source.

**\[Usage\]**

result = TAN(source);

**\[Example\]**

```c
float source=45(度);
float result;
result=TAN(source); //result = 1
```

**17、<span id="XORSUM"></span>XORSUM**

**\[Description\]**

Use XOR to calculate checksum.

**\[Usage\]**

checksum = XORSUM(source, sizeof(source));

**\[Example\]**

```c
char source[5] = {0x1, 0x20, 0x3, 0x48, 0x5};
short checksum;
checksum = XORSUM(source, 5); // checksum =0x6f;
```
