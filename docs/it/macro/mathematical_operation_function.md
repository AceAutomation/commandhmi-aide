# Funzioni matematiche

|                       |                                                      |
|-----------------------|------------------------------------------------------|
| **Nome funzione**     | **Funzione**                                         |
| **[ACOS](#ACOS)**     | Il risultato è l'arcocoseno della sorgente.          |
| **[ADDSUM](#ADDSUM)** | Calcola il checksum per somma.                       |
| **[ASIN](#ASIN)**     | Il risultato è l'arcoseno della sorgente.            |
| **[ATAN](#ATAN)**     | Il risultato è l'arcotangente della sorgente.        |
| **[COT](#COT)**       | Il risultato è la cotangente della sorgente.         |
| **[COS](#COS)**       | Il risultato è il coseno della sorgente.             |
| **[CRC](#CRC)**       | Calcola il CRC a 16 bit.                             |
| **[CSC](#CSC)**       | Il risultato è la cosecante della sorgente.          |
| **[LOG](#LOG)**       | Calcola il logaritmo naturale di un numero.          |
| **[LOG10](#LOG10)**   | Calcola il logaritmo in base 10 di un numero.        |
| **[POW](#POW)**       | Calcola x elevato alla potenza y.                    |
| **[RAND](#RAND)**     | Genera un numero pseudocasuale (intervallo: 0~65535) |
| **[SEC](#SEC)**       | Il risultato è la secante della sorgente.            |
| **[SIN](#SIN)**       | Il risultato è il seno della sorgente.               |
| **[SQRT](#SQRT)**     | Il risultato è la radice quadrata della sorgente.    |
| **[TAN](#TAN)**       | Il risultato è la tangente della sorgente.           |
| **[XORSUM](#XORSUM)** | Calcola il checksum tramite XOR.                     |

**1、<span id="ACOS"></span>ACOS**

**\[Descrizione\]**

Il risultato è l'arcocoseno del valore sorgente.

**\[Sintassi\]**

result = ACOS(source);

**\[Esempio\]**

```c
float source=0.5;
float result;
result=ACOS(source);
```

**2、<span id="ADDSUM"></span>ADDSUM**

**\[Descrizione\]**

Calcola il checksum per addizione.

**\[Sintassi\]**

checksum=ADDSUM(data, sizeof(data));

**\[Esempio\]**

```c
char data[5] = {0x1, 0x2, 0x3, 0x4, 0x20};
int checksum;
checksum=ADDSUM(data, 5); // checksum=0x2a;
```

<span id="ASIN"></span>**3、ASIN**

**\[Descrizione\]**

Il risultato è l'arcoseno del valore sorgente.

**\[Sintassi\]**

result = ASIN(source);

**\[Esempio\]**

```c
float source=0.5;
float result;
result=ASIN(source);
```

**4、<span id="ATAN"></span>ATAN**

**\[Descrizione\]**

Il risultato è l'arcotangente del valore sorgente.

**\[Sintassi\]**

result = ATAN(source);

**\[Esempio\]**

```c
float source=1;
float result;
result=ATAN(source);
```

**5、<span id="COT"></span>COT**

**\[Descrizione\]**

Il risultato è la cotangente del valore sorgente.

**\[Sintassi\]**

result = COT(source);

**\[Esempio\]**

```c
float source=45(度);
float result;
result=COT(source); //result = 1
```

**6、<span id="COS"></span>COS**

**\[Descrizione\]**

Il risultato è il coseno del valore sorgente.

**\[Sintassi\]**

result = COS(source);

**\[Esempio\]**

```c
float source=60(度);
float result;
result=COS(source); //result = 0.5
```

**7、<span id="CRC"></span>CRC**

**\[Descrizione\]**

Calcola il CRC a 16 bit.

**\[Sintassi\]**

bit_CRC=CRC(source,sizeof(source))；

**\[Esempio\]**

char source\[5\] = {0x1, 0x2, 0x3, 0x4, 0x5}；

short bit_CRC；

bit_CRC=CRC(source,5)；

**8、<span id="CSC"></span>CSC**

**\[Descrizione\]**

Il risultato è la cosecante del valore sorgente.

**\[Sintassi\]**

result = CSC(source);

**\[Esempio\]**

```c
float source=30(度);
float result;
result=CSC(source); //result = 2
```

**9、<span id="LOG"></span>LOG**

**\[Descrizione\]**

Calcola il logaritmo naturale di un numero.

**\[Sintassi\]**

result = LOG(source);

**\[Esempio\]**

```c
float source =100,result;
result = LOG(source); //result =4.61
```

**10、<span id="LOG10"></span>LOG10**

**\[Descrizione\]**

Calcola il logaritmo in base 10 di un numero.

**\[Sintassi\]**

result = lOG10(source)

**\[Esempio\]**

```c
float source=100,result;
result = LOG10(source); //result = 2.00
```

**11、<span id="POW"></span>POW**

**\[Descrizione\]**

Calcola x elevato alla potenza y.

**\[Sintassi\]**

result = POW(x,y);  nota: x deve essere una costante

**\[Esempio\]**

```c
float result,y;
y=0.5;
result=POW(25,y); //result = 5
```

**12、<span id="RAND"></span>RAND**

**\[Descrizione\]**

Genera un numero pseudocasuale (intervallo: 0~65535)

**\[Sintassi\]**

Random= RAND()

**\[Esempio\]**

```c
unsigned short random;
random =RAND(); //random = 363
```

**13、<span id="SEC"></span>SEC**

**\[Descrizione\]**

Il risultato è la secante del valore sorgente.

**\[Sintassi\]**

result = SEC(source);

**\[Esempio\]**

```c
float source=60(度);
float result;
result=SEC(source); //result = 2
```

**14、<span id="SIN"></span>SIN**

**\[Descrizione\]**

Il risultato è il seno del valore sorgente.

**\[Sintassi\]**

result = SIN(source);

**\[Esempio\]**

```c
float source=30(度);
float result;
result=SIN(source); //result = 0.5
```

**15、<span id="SQRT"></span>SQRT**

**\[Descrizione\]**

Il risultato è la radice quadrata del valore sorgente.

**\[Sintassi\]**

result = SQRT(source);

**\[Esempio\]**

```c
float source=16;
float result;
result=SQRT(source); //result = 4
```

**16、<span id="TAN"></span>TAN**

**\[Descrizione\]**

Il risultato è la tangente del valore sorgente.

**\[Sintassi\]**

result = TAN(source);

**\[Esempio\]**

```c
float source=45(度);
float result;
result=TAN(source); //result = 1
```

**17、<span id="XORSUM"></span>XORSUM**

**\[Descrizione\]**

Calcola il checksum tramite XOR.

**\[Sintassi\]**

checksum = XORSUM(source, sizeof(source));

**\[Esempio\]**

```c
char source[5] = {0x1, 0x20, 0x3, 0x48, 0x5};
short checksum;
checksum = XORSUM(source, 5); // checksum =0x6f;
```
