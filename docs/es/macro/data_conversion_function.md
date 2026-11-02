# Funciones de conversión de datos

|                                 |                                          |
|---------------------------------|------------------------------------------|
| **Nombre de la función**               | **Función**                             |
| **[ASCII2DEC](#ASCII2DEC)**     | Convierte una cadena en valor decimal.     |
| **[ASCII2FLOAT](#ASCII2FLOAT)** | Convierte una cadena en valor de coma flotante.    |
| **[ASCII2HEX](#ASCII2HEX)**     | Convierte una cadena en valor hexadecimal. |
| **[BCD2BIN](#BCD2BIN)**         | Convierte un valor BCD en binario.      |
| **[BIN2BCD](#BIN2BCD)**         | Convierte un valor binario en BCD.   |
| **[DEC2ASCII](#DEC2ASCII)**     | Convierte un valor decimal en cadena.     |
| **[FLOAT2ASCII](#FLOAT2ASCII)** | Convierte un valor de coma flotante en cadena.    |
| **[HEX2ASCII](#HEX2ASCII)**     | Convierte un valor hexadecimal en cadena. |

**1、<span id="ASCII2DEC"></span>ASCII2DEC**

**\[Descripción\]**

Convierte una cadena en valor decimal.

**\[Uso\]**

result=ASCII2DEC(source , sizeof(source))；

**\[Ejemplo\]**

char source\[4\] = {'2', '3', '4', '5'}；

short result；

result=ASCII2DEC(source , 4)；//  result=2345

**2、<span id="ASCII2FLOAT"></span>ASCII2FLOAT**

**\[Descripción\]**

Convierte una cadena en valor de coma flotante.

**\[Uso\]**

result=ASCII2FLOAT(source,sizeof(source))；

**\[Ejemplo\]**

char source\[4\] = {'5', '.', '7', '8'}；

float result；

result=ASCII2FLOAT(source,4)；//  result = 5.78

**3、<span id="ASCII2HEX"></span>ASCII2HEX**

**\[Descripción\]**

Convierte una cadena en valor hexadecimal.

**\[Uso\]**

result=ASCII2HEX(source,sizeof(source))；

**\[Ejemplo\]**

char source\[5\] = {'1','6','3','4'}；

short result；

result=ASCII2HEX(source,4)；//  result = 0x1634

**4、<span id="BCD2BIN"></span>BCD2BIN**

**\[Descripción\]**

Convierte un valor BCD en binario.

**\[Uso\]**

result=BCD2BIN(source)；

**\[Ejemplo\]**

short source = 0x2648；

short result；

result=BCD2BIN(source)；  //  result = 2648

**5、<span id="BIN2BCD"></span>BIN2BCD**

**\[Descripción\]**

Convierte un valor binario en BCD.

**\[Uso\]**

result=BIN2BCD(source)；

**\[Ejemplo\]**

short source = 1234；

short result；

result=BIN2BCD(source)；//  result = 0x1234

**6、<span id="DEC2ASCII"></span>DEC2ASCII**

**\[Descripción\]**

Convierte un valor decimal en cadena.

**\[Uso\]**

result= DEC2ASCII(source,sizeof(source))；

**\[Ejemplo\]**

short source = 5678；

char \*result；

```c
result= DEC2ASCII(source,4)；
// result[0] == '5', result[1] == '6', result[2] == '7', result[3] == '8’
```

**7、<span id="FLOAT2ASCII"></span>FLOAT2ASCII**

**\[Descripción\]**

Convierte un valor de coma flotante en cadena.

**\[Uso\]**

result=FLOAT2ASCII(source);

**\[Ejemplo\]**

```c
float source = 56.8;
char result[4];
result=FLOAT2ASCII(source);
//result[0] = '5',result[1] = '6',result[2] = '.',result[3] = '8'
```

**8、<span id="HEX2ASCII"></span>HEX2ASCII**

**\[Descripción\]**

Convierte un valor hexadecimal en cadena.

**\[Uso\]**

HEX2ASCII(source, result\[start\])；

**\[Ejemplo\]**

short source = 0x5678；

char \*result；

```c
result = HEX2ASCII(source)；
//result[0] = '5', result[1] = '6', result[2] = '7', result[3] = '8'
```
