# Funzioni di conversione dei dati

|                                 |                                          |
|---------------------------------|------------------------------------------|
| **Nome funzione**               | **Funzione**                             |
| **[ASCII2DEC](#ASCII2DEC)**     | Converte una stringa in un valore decimale. |
| **[ASCII2FLOAT](#ASCII2FLOAT)** | Converte una stringa in un valore in virgola mobile. |
| **[ASCII2HEX](#ASCII2HEX)**     | Converte una stringa in un valore esadecimale. |
| **[BCD2BIN](#BCD2BIN)**         | Converte un valore BCD in un valore binario. |
| **[BIN2BCD](#BIN2BCD)**         | Converte un valore binario in un valore BCD. |
| **[DEC2ASCII](#DEC2ASCII)**     | Converte un valore decimale in una stringa. |
| **[FLOAT2ASCII](#FLOAT2ASCII)** | Converte un valore in virgola mobile in una stringa. |
| **[HEX2ASCII](#HEX2ASCII)**     | Converte un valore esadecimale in una stringa. |

**1、<span id="ASCII2DEC"></span>ASCII2DEC**

**\[Descrizione\]**

Converte una stringa in un valore decimale.

**\[Sintassi\]**

result=ASCII2DEC(source , sizeof(source))；

**\[Esempio\]**

char source\[4\] = {'2', '3', '4', '5'}；

short result；

result=ASCII2DEC(source , 4)；//  result=2345

**2、<span id="ASCII2FLOAT"></span>ASCII2FLOAT**

**\[Descrizione\]**

Converte una stringa in un valore in virgola mobile.

**\[Sintassi\]**

result=ASCII2FLOAT(source,sizeof(source))；

**\[Esempio\]**

char source\[4\] = {'5', '.', '7', '8'}；

float result；

result=ASCII2FLOAT(source,4)；//  result = 5.78

**3、<span id="ASCII2HEX"></span>ASCII2HEX**

**\[Descrizione\]**

Converte una stringa in un valore esadecimale.

**\[Sintassi\]**

result=ASCII2HEX(source,sizeof(source))；

**\[Esempio\]**

char source\[5\] = {'1','6','3','4'}；

short result；

result=ASCII2HEX(source,4)；//  result = 0x1634

**4、<span id="BCD2BIN"></span>BCD2BIN**

**\[Descrizione\]**

Converte un valore BCD in un valore binario (BIN).

**\[Sintassi\]**

result=BCD2BIN(source)；

**\[Esempio\]**

short source = 0x2648；

short result；

result=BCD2BIN(source)；  //  result = 2648

**5、<span id="BIN2BCD"></span>BIN2BCD**

**\[Descrizione\]**

Converte un valore binario in un valore BCD.

**\[Sintassi\]**

result=BIN2BCD(source)；

**\[Esempio\]**

short source = 1234；

short result；

result=BIN2BCD(source)；//  result = 0x1234

**6、<span id="DEC2ASCII"></span>DEC2ASCII**

**\[Descrizione\]**

Converte un valore decimale in una stringa.

**\[Sintassi\]**

result= DEC2ASCII(source,sizeof(source))；

**\[Esempio\]**

short source = 5678；

char \*result；

```c
result= DEC2ASCII(source,4)；
// result[0] == '5', result[1] == '6', result[2] == '7', result[3] == '8’
```

**7、<span id="FLOAT2ASCII"></span>FLOAT2ASCII**

**\[Descrizione\]**

Converte un valore in virgola mobile in una stringa.

**\[Sintassi\]**

result=FLOAT2ASCII(source);

**\[Esempio\]**

```c
float source = 56.8;
char result[4];
result=FLOAT2ASCII(source);
//result[0] = '5',result[1] = '6',result[2] = '.',result[3] = '8'
```

**8、<span id="HEX2ASCII"></span>HEX2ASCII**

**\[Descrizione\]**

Converte un valore esadecimale in una stringa.

**\[Sintassi\]**

HEX2ASCII(source, result\[start\])；

**\[Esempio\]**

short source = 0x5678；

char \*result；

```c
result = HEX2ASCII(source)；
//result[0] = '5', result[1] = '6', result[2] = '7', result[3] = '8'
```
