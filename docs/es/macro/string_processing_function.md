# Funciones de cadenas

|                                                 |                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre de la función**                               | **Función**                                                                                                                                                              |
| **[StringCat](#StringCat)**                     | Concatena dos cadenas                                                                                                                                               |
| **[StringCompare](#StringCompare)**             | Compara dos cadenas distinguiendo mayúsculas y minúsculas                                                                                                               |
| **[StringCompareNoCase](#StringCompareNoCase)** | Compara dos cadenas sin distinguir mayúsculas y minúsculas                                                                                                             |
| **[StringCopy](#StringCopy)**                   | Copia una cadena                                                                                                                                                               |
| **[StringFind](#StringFind)**                   | Devuelve la posición de la primera aparición de la cadena buscada en la cadena de origen; -1 si no se encuentra.                            |
| **[StringFindOneOf](#StringFindOneOf)**         | Devuelve la posición del primer carácter de la cadena de origen que aparece en la cadena buscada; -1 si no se encuentra ninguno.  |
| **[StringIncluding](#StringIncluding)**         | Devuelve una subcadena de la cadena de origen formada por caracteres del conjunto indicado.                                                                                     |
| **[StringInsert](#StringInsert)**               | Inserta una cadena en una posición dada de la cadena de destino.                                                                                           |
| **[StringLength](#StringLength)**               | Devuelve la longitud de una cadena.                                                                                                                                            |
| **[StringMid](#StringMid)**                     | Devuelve una secuencia de caracteres a partir de la posición indicada de la cadena de origen.                                                                                         |
| **[StringSplit](#StringSplit)**                 | Divide la cadena.                                                                                                                                                     |
| **[StringToLower](#StringToLower)**             | Convierte los caracteres de una cadena a minúsculas.                                                                                                                          |
| **[StringToUpper](#StringToUpper)**             | Convierte los caracteres de una cadena a mayúsculas.                                                                                                                          |
| **[StringTrim](#StringTrim)**                   | Elimina source2 de source1 y forma una nueva cadena con el resto.                                                                                                       |
| **[StringTrimLeft](#StringTrimLeft)**           | Elimina de source1 todos los caracteres de source2; el resultado queda en dest.                                                                                             |

**1、<span id="StringCat"></span>StringCat**

**\[Descripción\]**

Añade la cadena de origen a la cadena de destino.

**\[Uso\]**

result=StringCat(dest\[start\],source);

**\[Ejemplo\]**

```c
char a[8]="abcd";
char *b="efg";
char *c;
c=StringCat(a,b); // c="abcdefg"; es preferible que a sea un array de caracteres.
```

**2、<span id="StringCompare"></span>StringCompare**

**\[Descripción\]**

Compara dos cadenas distinguiendo mayúsculas y minúsculas.

**\[Uso\]**

result = StringCompare(source1,source2);

**\[Ejemplo\]**

```c
int result;
char *a="abcd";
char *b="efg";
result = StringCompare(a,b); //result=-1 (si a>b, result=1; si a=b, result=0; si a<b, result=-1).
```

**3、<span id="StringCompareNoCase"></span>StringCompareNoCase** //

**\[Descripción\]**

Compara dos cadenas sin distinguir mayúsculas y minúsculas.

**\[Uso\]**

result = StringCompareNoCase(source1,source2)

**\[Ejemplo\]**

```c
int result;
char *a="abcd";
char *b="EFG";
result=StringCompare(a,b);//result=1;
result=StringCompareNoCase(a,b);//result=-1;
```

**4、<span id="StringCopy"></span>StringCopy**

**\[Descripción\]**

Copia una cadena en otra.

**\[Uso\]**

result = StringCopy(dest,source);

**\[Ejemplo\]**

```c
char a[4]="abcd";
char* b="efg";
char* c;
c=StringCopy(a,b);//c="abcdefg"; es preferible que a sea un array de caracteres.
```

**5、<span id="StringFind"></span>StringFind**

**\[Descripción\]**

Devuelve la posición de la primera aparición de la cadena buscada en la cadena de origen.

**\[Uso\]**

index=StringFind(source1,source2);

**\[Ejemplo\]**

```c
char a[8]="ab1c123d";
char* b="123";
char* c="ef";
int index;
index=StringFind(a,b); //index=4;
index=StringFind(a,c); //index=-1;
```

**6、<span id="StringFindOneOf"></span>StringFindOneOf**

**\[Descripción\]**

Devuelve la posición del primer carácter de la cadena de origen que aparece en la cadena buscada.

**\[Uso\]**

index=StringFindOneOf(source1,source2);

**\[Ejemplo\]**

char a\[8\]="ab1c123d";

cahr\* b="1b";

in index;

index=StringFindOneOf(a,b); //index=2;

**7、<span id="StringIncluding"></span>StringIncluding**

**\[Descripción\]**

Devuelve una subcadena de la cadena de origen formada por caracteres del conjunto indicado.

**\[Uso\]**

```c
StringIncluding(source1,source2,dest);
```

**\[Ejemplo\]**

```c
char a[8]="aB1Eree";
char* b="aBe";
char dest[8];
StringIncluding(a,b,dest);//dest="aBee"; es preferible que dest sea un array de caracteres.
```

**8、<span id="StringInsert"></span>StringInsert**

**\[Descripción\]**

Inserta una cadena en una posición dada de la cadena de destino. Compruebe que la cadena de destino tiene un búfer suficiente.

**\[Uso\]**

```c
StringInsert(pos,source,dest);
```

**\[Ejemplo\]**

```c
char a[8] = "aB1e";
char *b ="kdr";
int pos=2;
StringInsert(pos,b,a); //a="aBkdr1e".
```

**9、<span id="StringLength"></span>StringLength**

**\[Descripción\]**

Devuelve la longitud de una cadena.

**\[Uso\]**

result = StringLength(source);

**\[Ejemplo\]**

```c
char a[8]="ABerer";
int length;
length = StringLength(a); //length=6;
```

**10、<span id="StringMid"></span>StringMid**

**\[Descripción\]**

Extrae una secuencia de caracteres a partir de la posición indicada de la cadena de origen y la guarda en el búfer de destino.

**\[Uso\]**

```c
StringMid(source,count,dest);
```

**\[Ejemplo\]**

```c
char a[8]="aB1e";
char b[3];
StringMid(a,2,b); //b="B1"; es preferible que b sea un array de caracteres con memoria suficiente para guardar los caracteres extraídos.
```

**11、<span id="StringSplit"></span>StringSplit**

**\[Descripción\]**

Divide la cadena.

**\[Uso\]**

```c
StringSplit(dest1,dest2,source,pos);
```

**\[Ejemplo\]**

```c
char a[8]="aB1edge";
char b[5];
char c[5];
StringSplit(b,c,a,3); // es preferible que b y c sean arrays de caracteres.
```

**12、<span id="StringToLower"></span>StringToLower**

**\[Descripción\]**

Convierte los caracteres de una cadena a minúsculas.

**\[Uso\]**

```c
StringToLower(source,dest); // es preferible que dest sea un array de caracteres.
```

**\[Ejemplo\]**

```c
char a[8]="ABeRe";
char b[8];
StringToLower(a,b);//b="abere".
```

**13、<span id="StringToUpper"></span>StringToUpper**

**\[Descripción\]**

Convierte los caracteres de una cadena a mayúsculas. Compruebe que el búfer es suficiente.

**\[Uso\]**

```c
StringToUpper(source,dest);
```

**\[Ejemplo\]**

```c
char a[8]="ab1ere";
char b[8]; // es preferible que b sea un array de caracteres.
StringToUpper(a,b); //b="AB1ERE"；
```

**14、<span id="StringTrim"></span>StringTrim**

**\[Descripción\]**

Elimina source2 de source1 y devuelve el resultado en dest.

**\[Uso\]**

```c
StringTrim(source1.source2,dest);
```

**\[Ejemplo\]**

```c
char a[12]="a1erd1esw";
char *b="1e";
char c[10];
StringTrim(a,b,c) //c="ardsw". Es preferible que c sea un array de caracteres.
```

**15、<span id="StringTrimLeft"></span>StringTrimLeft**

**\[Descripción\]**

Elimina de source1 todos los caracteres de source2 y devuelve el resultado en dest.

**\[Uso\]**

```c
StringTrimLeft(source1,source2,dest);
```

**\[Ejemplo\]**

```c
char a[8]="aB1edge";
char* b="be";
char c[8];
StringTrimLeft(a,b,c);//c="aB1dg". Es preferible que c sea un array de caracteres.
```
