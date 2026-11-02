# Fonctions mathématiques

|                       |                                                      |
|-----------------------|------------------------------------------------------|
| **Nom de fonction**   | **Fonction**                                         |
| **[ACOS](#ACOS)**     | Le résultat est l'arc cosinus de la source.          |
| **[ADDSUM](#ADDSUM)** | Calcule une somme de contrôle par addition.          |
| **[ASIN](#ASIN)**     | Le résultat est l'arc sinus de la source.            |
| **[ATAN](#ATAN)**     | Le résultat est l'arc tangente de la source.         |
| **[COT](#COT)**       | Le résultat est la cotangente de la source.          |
| **[COS](#COS)**       | Le résultat est le cosinus de la source.             |
| **[CRC](#CRC)**       | Calcule un CRC 16 bits.                              |
| **[CSC](#CSC)**       | Le résultat est la cosécante de la source.           |
| **[LOG](#LOG)**       | Calcule le logarithme naturel d'un nombre.           |
| **[LOG10](#LOG10)**   | Calcule le logarithme décimal d'un nombre.           |
| **[POW](#POW)**       | Calcule x à la puissance y.                          |
| **[RAND](#RAND)**     | Génère un nombre pseudo-aléatoire (plage : 0~65535)  |
| **[SEC](#SEC)**       | Le résultat est la sécante de la source.             |
| **[SIN](#SIN)**       | Le résultat est le sinus de la source.               |
| **[SQRT](#SQRT)**     | Le résultat est la racine carrée de la source.       |
| **[TAN](#TAN)**       | Le résultat est la tangente de la source.            |
| **[XORSUM](#XORSUM)** | Calcule une somme de contrôle par XOR.               |

**1、<span id="ACOS"></span>ACOS**

**\[Description\]**

Le résultat est l'arc cosinus de la source.

**\[Syntaxe\]**

result = ACOS(source);

**\[Exemple\]**

```c
float source=0.5;
float result;
result=ACOS(source);
```

**2、<span id="ADDSUM"></span>ADDSUM**

**\[Description\]**

Calcule une somme de contrôle par addition.

**\[Syntaxe\]**

checksum=ADDSUM(data, sizeof(data));

**\[Exemple\]**

```c
char data[5] = {0x1, 0x2, 0x3, 0x4, 0x20};
int checksum;
checksum=ADDSUM(data, 5); // checksum=0x2a;
```

<span id="ASIN"></span>**3、ASIN**

**\[Description\]**

Le résultat est l'arc sinus de la source.

**\[Syntaxe\]**

result = ASIN(source);

**\[Exemple\]**

```c
float source=0.5;
float result;
result=ASIN(source);
```

**4、<span id="ATAN"></span>ATAN**

**\[Description\]**

Le résultat est l'arc tangente de la source.

**\[Syntaxe\]**

result = ATAN(source);

**\[Exemple\]**

```c
float source=1;
float result;
result=ATAN(source);
```

**5、<span id="COT"></span>COT**

**\[Description\]**

Le résultat est la cotangente de la source.

**\[Syntaxe\]**

result = COT(source);

**\[Exemple\]**

```c
float source=45(度);
float result;
result=COT(source); //result = 1
```

**6、<span id="COS"></span>COS**

**\[Description\]**

Le résultat est le cosinus de la source.

**\[Syntaxe\]**

result = COS(source);

**\[Exemple\]**

```c
float source=60(度);
float result;
result=COS(source); //result = 0.5
```

**7、<span id="CRC"></span>CRC**

**\[Description\]**

Calcule un CRC 16 bits.

**\[Syntaxe\]**

bit_CRC=CRC(source,sizeof(source))；

**\[Exemple\]**

char source\[5\] = {0x1, 0x2, 0x3, 0x4, 0x5}；

short bit_CRC；

bit_CRC=CRC(source,5)；

**8、<span id="CSC"></span>CSC**

**\[Description\]**

Le résultat est la cosécante de la source.

**\[Syntaxe\]**

result = CSC(source);

**\[Exemple\]**

```c
float source=30(度);
float result;
result=CSC(source); //result = 2
```

**9、<span id="LOG"></span>LOG**

**\[Description\]**

Calcule le logarithme naturel d'un nombre.

**\[Syntaxe\]**

result = LOG(source);

**\[Exemple\]**

```c
float source =100,result;
result = LOG(source); //result =4.61
```

**10、<span id="LOG10"></span>LOG10**

**\[Description\]**

Calcule le logarithme décimal d'un nombre.

**\[Syntaxe\]**

result = lOG10(source)

**\[Exemple\]**

```c
float source=100,result;
result = LOG10(source); //result = 2.00
```

**11、<span id="POW"></span>POW**

**\[Description\]**

Calcule x à la puissance y.

**\[Syntaxe\]**

result = POW(x,y);  remarque : x doit être une constante

**\[Exemple\]**

```c
float result,y;
y=0.5;
result=POW(25,y); //result = 5
```

**12、<span id="RAND"></span>RAND**

**\[Description\]**

Génère un nombre pseudo-aléatoire (plage : 0~65535)

**\[Syntaxe\]**

Random= RAND()

**\[Exemple\]**

```c
unsigned short random;
random =RAND(); //random = 363
```

**13、<span id="SEC"></span>SEC**

**\[Description\]**

Le résultat est la sécante de la source.

**\[Syntaxe\]**

result = SEC(source);

**\[Exemple\]**

```c
float source=60(度);
float result;
result=SEC(source); //result = 2
```

**14、<span id="SIN"></span>SIN**

**\[Description\]**

Le résultat est le sinus de la source.

**\[Syntaxe\]**

result = SIN(source);

**\[Exemple\]**

```c
float source=30(度);
float result;
result=SIN(source); //result = 0.5
```

**15、<span id="SQRT"></span>SQRT**

**\[Description\]**

Le résultat est la racine carrée de la source.

**\[Syntaxe\]**

result = SQRT(source);

**\[Exemple\]**

```c
float source=16;
float result;
result=SQRT(source); //result = 4
```

**16、<span id="TAN"></span>TAN**

**\[Description\]**

Le résultat est la tangente de la source.

**\[Syntaxe\]**

result = TAN(source);

**\[Exemple\]**

```c
float source=45(度);
float result;
result=TAN(source); //result = 1
```

**17、<span id="XORSUM"></span>XORSUM**

**\[Description\]**

Calcule une somme de contrôle par XOR.

**\[Syntaxe\]**

checksum = XORSUM(source, sizeof(source));

**\[Exemple\]**

```c
char source[5] = {0x1, 0x20, 0x3, 0x48, 0x5};
short checksum;
checksum = XORSUM(source, 5); // checksum =0x6f;
```
