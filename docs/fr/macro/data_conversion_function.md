# Fonctions de conversion de données

|                                 |                                          |
|---------------------------------|------------------------------------------|
| **Nom de fonction**             | **Fonction**                             |
| **[ASCII2DEC](#ASCII2DEC)**     | Convertit une chaîne en valeur décimale. |
| **[ASCII2FLOAT](#ASCII2FLOAT)** | Convertit une chaîne en valeur flottante. |
| **[ASCII2HEX](#ASCII2HEX)**     | Convertit une chaîne en valeur hexadécimale. |
| **[BCD2BIN](#BCD2BIN)**         | Convertit une valeur BCD en valeur binaire. |
| **[BIN2BCD](#BIN2BCD)**         | Convertit une valeur binaire en valeur BCD. |
| **[DEC2ASCII](#DEC2ASCII)**     | Convertit une valeur décimale en chaîne. |
| **[FLOAT2ASCII](#FLOAT2ASCII)** | Convertit une valeur flottante en chaîne. |
| **[HEX2ASCII](#HEX2ASCII)**     | Convertit une valeur hexadécimale en chaîne. |

**1、<span id="ASCII2DEC"></span>ASCII2DEC**

**\[Description\]**

Convertit une chaîne en valeur décimale.

**\[Syntaxe\]**

result=ASCII2DEC(source , sizeof(source))；

**\[Exemple\]**

char source\[4\] = {'2', '3', '4', '5'}；

short result；

result=ASCII2DEC(source , 4)；//  result=2345

**2、<span id="ASCII2FLOAT"></span>ASCII2FLOAT**

**\[Description\]**

Convertit une chaîne en valeur flottante.

**\[Syntaxe\]**

result=ASCII2FLOAT(source,sizeof(source))；

**\[Exemple\]**

char source\[4\] = {'5', '.', '7', '8'}；

float result；

result=ASCII2FLOAT(source,4)；//  result = 5.78

**3、<span id="ASCII2HEX"></span>ASCII2HEX**

**\[Description\]**

Convertit une chaîne en valeur hexadécimale.

**\[Syntaxe\]**

result=ASCII2HEX(source,sizeof(source))；

**\[Exemple\]**

char source\[5\] = {'1','6','3','4'}；

short result；

result=ASCII2HEX(source,4)；//  result = 0x1634

**4、<span id="BCD2BIN"></span>BCD2BIN**

**\[Description\]**

Convertit une valeur BCD en valeur binaire.

**\[Syntaxe\]**

result=BCD2BIN(source)；

**\[Exemple\]**

short source = 0x2648；

short result；

result=BCD2BIN(source)；  //  result = 2648

**5、<span id="BIN2BCD"></span>BIN2BCD**

**\[Description\]**

Convertit une valeur binaire en valeur BCD.

**\[Syntaxe\]**

result=BIN2BCD(source)；

**\[Exemple\]**

short source = 1234；

short result；

result=BIN2BCD(source)；//  result = 0x1234

**6、<span id="DEC2ASCII"></span>DEC2ASCII**

**\[Description\]**

Convertit une valeur décimale en chaîne.

**\[Syntaxe\]**

result= DEC2ASCII(source,sizeof(source))；

**\[Exemple\]**

short source = 5678；

char \*result；

```c
result= DEC2ASCII(source,4)；
// result[0] == '5', result[1] == '6', result[2] == '7', result[3] == '8’
```

**7、<span id="FLOAT2ASCII"></span>FLOAT2ASCII**

**\[Description\]**

Convertit une valeur flottante en chaîne.

**\[Syntaxe\]**

result=FLOAT2ASCII(source);

**\[Exemple\]**

```c
float source = 56.8;
char result[4];
result=FLOAT2ASCII(source);
//result[0] = '5',result[1] = '6',result[2] = '.',result[3] = '8'
```

**8、<span id="HEX2ASCII"></span>HEX2ASCII**

**\[Description\]**

Convertit une valeur hexadécimale en chaîne.

**\[Syntaxe\]**

HEX2ASCII(source, result\[start\])；

**\[Exemple\]**

short source = 0x5678；

char \*result；

```c
result = HEX2ASCII(source)；
//result[0] = '5', result[1] = '6', result[2] = '7', result[3] = '8'
```
