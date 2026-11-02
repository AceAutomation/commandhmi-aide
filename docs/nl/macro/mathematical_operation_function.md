# Wiskundige functies

|                       |                                                      |
|-----------------------|------------------------------------------------------|
| **Functienaam**     | **Functie**                                         |
| **[ACOS](#ACOS)**     | Het resultaat is de arccosinus van de bron.   |
| **[ADDSUM](#ADDSUM)** | Berekent een controlesom door optelling.                  |
| **[ASIN](#ASIN)**     | Het resultaat is de arcsinus van de bron.    |
| **[ATAN](#ATAN)**     | Het resultaat is de arctangens van de bron. |
| **[COT](#COT)**       | Het resultaat is de cotangens van de bron.  |
| **[COS](#COS)**       | Het resultaat is de cosinus van de bron.     |
| **[CRC](#CRC)**       | Get 16-bit CRC.                                      |
| **[CSC](#CSC)**       | Het resultaat is de cosecans van de bron.   |
| **[LOG](#LOG)**       | Berekent de natuurlijke logaritme van een getal.         |
| **[LOG10](#LOG10)**   | Berekent de logaritme met grondtal 10 van een getal.         |
| **[POW](#POW)**       | Berekent x tot de macht y.               |
| **[RAND](#RAND)**     | Genereert een pseudowillekeurig getal (bereik: 0~65535)       |
| **[SEC](#SEC)**       | Het resultaat is de secans van de bron.     |
| **[SIN](#SIN)**       | Het resultaat is de sinus van de bron.       |
| **[SQRT](#SQRT)**     | Het resultaat is de vierkantswortel van de bron.     |
| **[TAN](#TAN)**       | Het resultaat is de tangens van de bron.    |
| **[XORSUM](#XORSUM)** | Berekent een controlesom met XOR.                       |

**1、<span id="ACOS"></span>ACOS**

**\[Beschrijving\]**

Het resultaat is de arccosinus van de bron.

**\[Gebruik\]**

result = ACOS(source);

**\[Voorbeeld\]**

```c
float source=0.5;
float result;
result=ACOS(source);
```

**2、<span id="ADDSUM"></span>ADDSUM**

**\[Beschrijving\]**

Berekent een controlesom door optelling.

**\[Gebruik\]**

checksum=ADDSUM(data, sizeof(data));

**\[Voorbeeld\]**

```c
char data[5] = {0x1, 0x2, 0x3, 0x4, 0x20};
int checksum;
checksum=ADDSUM(data, 5); // checksum=0x2a;
```

<span id="ASIN"></span>**3、ASIN**

**\[Beschrijving\]**

Het resultaat is de arcsinus van de bron.

**\[Gebruik\]**

result = ASIN(source);

**\[Voorbeeld\]**

```c
float source=0.5;
float result;
result=ASIN(source);
```

**4、<span id="ATAN"></span>ATAN**

**\[Beschrijving\]**

Het resultaat is de arctangens van de bron.

**\[Gebruik\]**

result = ATAN(source);

**\[Voorbeeld\]**

```c
float source=1;
float result;
result=ATAN(source);
```

**5、<span id="COT"></span>COT**

**\[Beschrijving\]**

Het resultaat is de cotangens van de bron.

**\[Gebruik\]**

result = COT(source);

**\[Voorbeeld\]**

```c
float source=45(度);
float result;
result=COT(source); //result = 1
```

**6、<span id="COS"></span>COS**

**\[Beschrijving\]**

Het resultaat is de cosinus van de bron.

**\[Gebruik\]**

result = COS(source);

**\[Voorbeeld\]**

```c
float source=60(度);
float result;
result=COS(source); //result = 0.5
```

**7、<span id="CRC"></span>CRC**

**\[Beschrijving\]**

Berekent een 16-bits CRC.

**\[Gebruik\]**

bit_CRC=CRC(source,sizeof(source))；

**\[Voorbeeld\]**

char source\[5\] = {0x1, 0x2, 0x3, 0x4, 0x5}；

short bit_CRC；

bit_CRC=CRC(source,5)；

**8、<span id="CSC"></span>CSC**

**\[Beschrijving\]**

Het resultaat is de cosecans van de bron.

**\[Gebruik\]**

result = CSC(source);

**\[Voorbeeld\]**

```c
float source=30(度);
float result;
result=CSC(source); //result = 2
```

**9、<span id="LOG"></span>LOG**

**\[Beschrijving\]**

Berekent de natuurlijke logaritme van een getal.

**\[Gebruik\]**

result = LOG(source);

**\[Voorbeeld\]**

```c
float source =100,result;
result = LOG(source); //result =4.61
```

**10、<span id="LOG10"></span>LOG10**

**\[Beschrijving\]**

Berekent de logaritme met grondtal 10 van een getal.

**\[Gebruik\]**

result = lOG10(source)

**\[Voorbeeld\]**

```c
float source=100,result;
result = LOG10(source); //result = 2.00
```

**11、<span id="POW"></span>POW**

**\[Beschrijving\]**

Berekent x tot de macht y.

**\[Gebruik\]**

result = POW(x,y);  let op: x moet een constante zijn

**\[Voorbeeld\]**

```c
float result,y;
y=0.5;
result=POW(25,y); //result = 5
```

**12、<span id="RAND"></span>RAND**

**\[Beschrijving\]**

Genereert een pseudowillekeurig getal (bereik: 0~65535)

**\[Gebruik\]**

Random= RAND()

**\[Voorbeeld\]**

```c
unsigned short random;
random =RAND(); //random = 363
```

**13、<span id="SEC"></span>SEC**

**\[Beschrijving\]**

Het resultaat is de secans van de bron.

**\[Gebruik\]**

result = SEC(source);

**\[Voorbeeld\]**

```c
float source=60(度);
float result;
result=SEC(source); //result = 2
```

**14、<span id="SIN"></span>SIN**

**\[Beschrijving\]**

Het resultaat is de sinus van de bron.

**\[Gebruik\]**

result = SIN(source);

**\[Voorbeeld\]**

```c
float source=30(度);
float result;
result=SIN(source); //result = 0.5
```

**15、<span id="SQRT"></span>SQRT**

**\[Beschrijving\]**

Het resultaat is het kwadraat van de bron.

**\[Gebruik\]**

result = SQRT(source);

**\[Voorbeeld\]**

```c
float source=16;
float result;
result=SQRT(source); //result = 4
```

**16、<span id="TAN"></span>TAN**

**\[Beschrijving\]**

Het resultaat is de tangens van de bron.

**\[Gebruik\]**

result = TAN(source);

**\[Voorbeeld\]**

```c
float source=45(度);
float result;
result=TAN(source); //result = 1
```

**17、<span id="XORSUM"></span>XORSUM**

**\[Beschrijving\]**

Berekent een controlesom met XOR.

**\[Gebruik\]**

checksum = XORSUM(source, sizeof(source));

**\[Voorbeeld\]**

```c
char source[5] = {0x1, 0x20, 0x3, 0x48, 0x5};
short checksum;
checksum = XORSUM(source, 5); // checksum =0x6f;
```
