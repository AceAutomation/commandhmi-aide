# Mathematische Funktionen

|                       |                                                      |
|-----------------------|------------------------------------------------------|
| **Funktionsname**     | **Funktion**                                         |
| **[ACOS](#ACOS)**     | Ergebnis ist der Arkuskosinus der Quelle.   |
| **[ADDSUM](#ADDSUM)** | Berechnet eine Prüfsumme per Addition.                  |
| **[ASIN](#ASIN)**     | Ergebnis ist der Arkussinus der Quelle.    |
| **[ATAN](#ATAN)**     | Ergebnis ist der Arkustangens der Quelle. |
| **[COT](#COT)**       | Ergebnis ist der Kotangens der Quelle.  |
| **[COS](#COS)**       | Ergebnis ist der Kosinus der Quelle.     |
| **[CRC](#CRC)**       | Get 16-bit CRC.                                      |
| **[CSC](#CSC)**       | Ergebnis ist der Kosekans der Quelle.   |
| **[LOG](#LOG)**       | Berechnet den natürlichen Logarithmus einer Zahl.         |
| **[LOG10](#LOG10)**   | Berechnet den Zehnerlogarithmus einer Zahl.         |
| **[POW](#POW)**       | Berechnet x hoch y.               |
| **[RAND](#RAND)**     | Erzeugt eine Pseudozufallszahl (Bereich: 0~65535)       |
| **[SEC](#SEC)**       | Ergebnis ist der Sekans der Quelle.     |
| **[SIN](#SIN)**       | Ergebnis ist der Sinus der Quelle.       |
| **[SQRT](#SQRT)**     | Ergebnis ist die Quadratwurzel der Quelle.     |
| **[TAN](#TAN)**       | Ergebnis ist der Tangens der Quelle.    |
| **[XORSUM](#XORSUM)** | Berechnet eine Prüfsumme per XOR.                       |

**1、<span id="ACOS"></span>ACOS**

**\[Beschreibung\]**

Ergebnis ist der Arkuskosinus der Quelle.

**\[Syntax\]**

result = ACOS(source);

**\[Beispiel\]**

```c
float source=0.5;
float result;
result=ACOS(source);
```

**2、<span id="ADDSUM"></span>ADDSUM**

**\[Beschreibung\]**

Berechnet eine Prüfsumme per Addition.

**\[Verwendung\]**

checksum=ADDSUM(data, sizeof(data));

**\[Beispiel\]**

```c
char data[5] = {0x1, 0x2, 0x3, 0x4, 0x20};
int checksum;
checksum=ADDSUM(data, 5); // checksum=0x2a;
```

<span id="ASIN"></span>**3、ASIN**

**\[Beschreibung\]**

Ergebnis ist der Arkussinus der Quelle.

**\[Syntax\]**

result = ASIN(source);

**\[Beispiel\]**

```c
float source=0.5;
float result;
result=ASIN(source);
```

**4、<span id="ATAN"></span>ATAN**

**\[Beschreibung\]**

Ergebnis ist der Arkustangens der Quelle.

**\[Verwendung\]**

result = ATAN(source);

**\[Beispiel\]**

```c
float source=1;
float result;
result=ATAN(source);
```

**5、<span id="COT"></span>COT**

**\[Beschreibung\]**

Ergebnis ist der Kotangens der Quelle.

**\[Syntax\]**

result = COT(source);

**\[Beispiel\]**

```c
float source=45(度);
float result;
result=COT(source); //result = 1
```

**6、<span id="COS"></span>COS**

**\[Beschreibung\]**

Ergebnis ist der Kosinus der Quelle.

**\[Syntax\]**

result = COS(source);

**\[Beispiel\]**

```c
float source=60(度);
float result;
result=COS(source); //result = 0.5
```

**7、<span id="CRC"></span>CRC**

**\[Beschreibung\]**

Berechnet einen 16-Bit-CRC.

**\[Syntax\]**

bit_CRC=CRC(source,sizeof(source))；

**\[Beispiel\]**

char source\[5\] = {0x1, 0x2, 0x3, 0x4, 0x5}；

short bit_CRC；

bit_CRC=CRC(source,5)；

**8、<span id="CSC"></span>CSC**

**\[Beschreibung\]**

Ergebnis ist der Kosekans der Quelle.

**\[Syntax\]**

result = CSC(source);

**\[Beispiel\]**

```c
float source=30(度);
float result;
result=CSC(source); //result = 2
```

**9、<span id="LOG"></span>LOG**

**\[Beschreibung\]**

Berechnet den natürlichen Logarithmus einer Zahl.

**\[Verwendung\]**

result = LOG(source);

**\[Beispiel\]**

```c
float source =100,result;
result = LOG(source); //result =4.61
```

**10、<span id="LOG10"></span>LOG10**

**\[Beschreibung\]**

Berechnet den Zehnerlogarithmus einer Zahl.

**\[Verwendung\]**

result = lOG10(source)

**\[Beispiel\]**

```c
float source=100,result;
result = LOG10(source); //result = 2.00
```

**11、<span id="POW"></span>POW**

**\[Beschreibung\]**

Berechnet x hoch y.

**\[Syntax\]**

result = POW(x,y);  Hinweis: x muss eine Konstante sein

**\[Beispiel\]**

```c
float result,y;
y=0.5;
result=POW(25,y); //result = 5
```

**12、<span id="RAND"></span>RAND**

**\[Beschreibung\]**

Erzeugt eine Pseudozufallszahl (Bereich: 0~65535)

**\[Syntax\]**

Random= RAND()

**\[Beispiel\]**

```c
unsigned short random;
random =RAND(); //random = 363
```

**13、<span id="SEC"></span>SEC**

**\[Beschreibung\]**

Ergebnis ist der Sekans der Quelle.

**\[Syntax\]**

result = SEC(source);

**\[Beispiel\]**

```c
float source=60(度);
float result;
result=SEC(source); //result = 2
```

**14、<span id="SIN"></span>SIN**

**\[Beschreibung\]**

Ergebnis ist der Sinus der Quelle.

**\[Syntax\]**

result = SIN(source);

**\[Beispiel\]**

```c
float source=30(度);
float result;
result=SIN(source); //result = 0.5
```

**15、<span id="SQRT"></span>SQRT**

**\[Beschreibung\]**

Ergebnis ist die Quadratwurzel der Quelle.

**\[Syntax\]**

result = SQRT(source);

**\[Beispiel\]**

```c
float source=16;
float result;
result=SQRT(source); //result = 4
```

**16、<span id="TAN"></span>TAN**

**\[Beschreibung\]**

Ergebnis ist der Tangens der Quelle.

**\[Syntax\]**

result = TAN(source);

**\[Beispiel\]**

```c
float source=45(度);
float result;
result=TAN(source); //result = 1
```

**17、<span id="XORSUM"></span>XORSUM**

**\[Beschreibung\]**

Berechnet eine Prüfsumme per XOR.

**\[Syntax\]**

checksum = XORSUM(source, sizeof(source));

**\[Beispiel\]**

```c
char source[5] = {0x1, 0x20, 0x3, 0x48, 0x5};
short checksum;
checksum = XORSUM(source, 5); // checksum =0x6f;
```
