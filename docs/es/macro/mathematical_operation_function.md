# Funciones matemáticas

|                       |                                                      |
|-----------------------|------------------------------------------------------|
| **Nombre de la función**     | **Función**                                         |
| **[ACOS](#ACOS)**     | El resultado es el arcocoseno del origen.   |
| **[ADDSUM](#ADDSUM)** | Calcula una suma de control por adición.                  |
| **[ASIN](#ASIN)**     | El resultado es el arcoseno del origen.    |
| **[ATAN](#ATAN)**     | El resultado es el arcotangente del origen. |
| **[COT](#COT)**       | El resultado es la cotangente del origen.  |
| **[COS](#COS)**       | El resultado es el coseno del origen.     |
| **[CRC](#CRC)**       | Get 16-bit CRC.                                      |
| **[CSC](#CSC)**       | El resultado es la cosecante del origen.   |
| **[LOG](#LOG)**       | Calcula el logaritmo natural de un número.         |
| **[LOG10](#LOG10)**   | Calcula el logaritmo en base 10 de un número.         |
| **[POW](#POW)**       | Calcula x elevado a y.               |
| **[RAND](#RAND)**     | Genera un número pseudoaleatorio (rango: 0~65535)       |
| **[SEC](#SEC)**       | El resultado es la secante del origen.     |
| **[SIN](#SIN)**       | El resultado es el seno del origen.       |
| **[SQRT](#SQRT)**     | El resultado es la raíz cuadrada del origen.     |
| **[TAN](#TAN)**       | El resultado es la tangente del origen.    |
| **[XORSUM](#XORSUM)** | Calcula una suma de control por XOR.                       |

**1、<span id="ACOS"></span>ACOS**

**\[Descripción\]**

El resultado es el arcocoseno del origen.

**\[Uso\]**

result = ACOS(source);

**\[Ejemplo\]**

```c
float source=0.5;
float result;
result=ACOS(source);
```

**2、<span id="ADDSUM"></span>ADDSUM**

**\[Descripción\]**

Calcula una suma de control por adición.

**\[Uso\]**

checksum=ADDSUM(data, sizeof(data));

**\[Ejemplo\]**

```c
char data[5] = {0x1, 0x2, 0x3, 0x4, 0x20};
int checksum;
checksum=ADDSUM(data, 5); // checksum=0x2a;
```

<span id="ASIN"></span>**3、ASIN**

**\[Descripción\]**

El resultado es el arcoseno del origen.

**\[Uso\]**

result = ASIN(source);

**\[Ejemplo\]**

```c
float source=0.5;
float result;
result=ASIN(source);
```

**4、<span id="ATAN"></span>ATAN**

**\[Descripción\]**

El resultado es el arcotangente del origen.

**\[Uso\]**

result = ATAN(source);

**\[Ejemplo\]**

```c
float source=1;
float result;
result=ATAN(source);
```

**5、<span id="COT"></span>COT**

**\[Descripción\]**

El resultado es la cotangente del origen.

**\[Uso\]**

result = COT(source);

**\[Ejemplo\]**

```c
float source=45(度);
float result;
result=COT(source); //result = 1
```

**6、<span id="COS"></span>COS**

**\[Descripción\]**

El resultado es el coseno del origen.

**\[Uso\]**

result = COS(source);

**\[Ejemplo\]**

```c
float source=60(度);
float result;
result=COS(source); //result = 0.5
```

**7、<span id="CRC"></span>CRC**

**\[Descripción\]**

Calcula un CRC de 16 bits.

**\[Uso\]**

bit_CRC=CRC(source,sizeof(source))；

**\[Ejemplo\]**

char source\[5\] = {0x1, 0x2, 0x3, 0x4, 0x5}；

short bit_CRC；

bit_CRC=CRC(source,5)；

**8、<span id="CSC"></span>CSC**

**\[Descripción\]**

El resultado es la cosecante del origen.

**\[Uso\]**

result = CSC(source);

**\[Ejemplo\]**

```c
float source=30(度);
float result;
result=CSC(source); //result = 2
```

**9、<span id="LOG"></span>LOG**

**\[Descripción\]**

Calcula el logaritmo natural de un número.

**\[Uso\]**

result = LOG(source);

**\[Ejemplo\]**

```c
float source =100,result;
result = LOG(source); //result =4.61
```

**10、<span id="LOG10"></span>LOG10**

**\[Descripción\]**

Calcula el logaritmo en base 10 de un número.

**\[Uso\]**

result = lOG10(source)

**\[Ejemplo\]**

```c
float source=100,result;
result = LOG10(source); //result = 2.00
```

**11、<span id="POW"></span>POW**

**\[Descripción\]**

Calcula x elevado a y.

**\[Uso\]**

result = POW(x,y);  nota: x debe ser una constante

**\[Ejemplo\]**

```c
float result,y;
y=0.5;
result=POW(25,y); //result = 5
```

**12、<span id="RAND"></span>RAND**

**\[Descripción\]**

Genera un número pseudoaleatorio (rango: 0~65535)

**\[Uso\]**

Random= RAND()

**\[Ejemplo\]**

```c
unsigned short random;
random =RAND(); //random = 363
```

**13、<span id="SEC"></span>SEC**

**\[Descripción\]**

El resultado es la secante del origen.

**\[Uso\]**

result = SEC(source);

**\[Ejemplo\]**

```c
float source=60(度);
float result;
result=SEC(source); //result = 2
```

**14、<span id="SIN"></span>SIN**

**\[Descripción\]**

El resultado es el seno del origen.

**\[Uso\]**

result = SIN(source);

**\[Ejemplo\]**

```c
float source=30(度);
float result;
result=SIN(source); //result = 0.5
```

**15、<span id="SQRT"></span>SQRT**

**\[Descripción\]**

El resultado es la raíz cuadrada del origen.

**\[Uso\]**

result = SQRT(source);

**\[Ejemplo\]**

```c
float source=16;
float result;
result=SQRT(source); //result = 4
```

**16、<span id="TAN"></span>TAN**

**\[Descripción\]**

El resultado es la tangente del origen.

**\[Uso\]**

result = TAN(source);

**\[Ejemplo\]**

```c
float source=45(度);
float result;
result=TAN(source); //result = 1
```

**17、<span id="XORSUM"></span>XORSUM**

**\[Descripción\]**

Calcula una suma de control por XOR.

**\[Uso\]**

checksum = XORSUM(source, sizeof(source));

**\[Ejemplo\]**

```c
char source[5] = {0x1, 0x20, 0x3, 0x48, 0x5};
short checksum;
checksum = XORSUM(source, 5); // checksum =0x6f;
```
