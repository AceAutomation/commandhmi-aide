# Fonctions de traitement des chaînes

|                                                 |                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nom de fonction**                             | **Fonction**                                                                                                                                                              |
| **[StringCat](#StringCat)**                     | Concatène deux chaînes                                                                                                                                                    |
| **[StringCompare](#StringCompare)**             | Compare deux chaînes en tenant compte de la casse                                                                                                                         |
| **[StringCompareNoCase](#StringCompareNoCase)** | Compare deux chaînes sans tenir compte de la casse                                                                                                                        |
| **[StringCopy](#StringCopy)**                   | Copie une chaîne                                                                                                                                                          |
| **[StringFind](#StringFind)**                   | Retourne la position de la première occurrence de la chaîne cherchée dans la chaîne source ; -1 si elle n'est pas trouvée.                                               |
| **[StringFindOneOf](#StringFindOneOf)**         | Retourne la position du premier caractère de la chaîne source présent dans la chaîne cherchée ; -1 s'il n'est pas trouvé.                                               |
| **[StringIncluding](#StringIncluding)**         | Extrait de la chaîne source une sous-chaîne formée des caractères de l'ensemble indiqué.                                                                                 |
| **[StringInsert](#StringInsert)**               | Insère une chaîne à une position donnée de la chaîne de destination.                                                                                                     |
| **[StringLength](#StringLength)**               | Retourne la longueur d'une chaîne.                                                                                                                                        |
| **[StringMid](#StringMid)**                     | Extrait une suite de caractères à partir de la position indiquée dans la chaîne source.                                                                                  |
| **[StringSplit](#StringSplit)**                 | Découpe la chaîne.                                                                                                                                                        |
| **[StringToLower](#StringToLower)**             | Convertit les caractères d'une chaîne en minuscules.                                                                                                                      |
| **[StringToUpper](#StringToUpper)**             | Convertit les caractères d'une chaîne en majuscules.                                                                                                                      |
| **[StringTrim](#StringTrim)**                   | Retire source2 de source1 et forme une nouvelle chaîne avec le reste.                                                                                                     |
| **[StringTrimLeft](#StringTrimLeft)**           | Retire de source1 tous les caractères présents dans source2 ; le résultat est placé dans dest.                                                                            |

**1、<span id="StringCat"></span>StringCat**

**\[Description\]**

Ajoute la chaîne source à la fin de la chaîne de destination.

**\[Syntaxe\]**

result=StringCat(dest\[start\],source);

**\[Exemple\]**

```c
char a[8]="abcd";
char *b="efg";
char *c;
c=StringCat(a,b); // c="abcdefg" ; il est préférable que a soit un tableau de caractères.
```

**2、<span id="StringCompare"></span>StringCompare**

**\[Description\]**

Compare deux chaînes en tenant compte de la casse.

**\[Syntaxe\]**

result = StringCompare(source1,source2);

**\[Exemple\]**

```c
int result;
char *a="abcd";
char *b="efg";
result = StringCompare(a,b); //result=-1 (si a>b, result=1 ; si a=b, result=0 ; si a<b, result=-1).
```

**3、<span id="StringCompareNoCase"></span>StringCompareNoCase** //

**\[Description\]**

Compare deux chaînes sans tenir compte de la casse.

**\[Syntaxe\]**

result = StringCompareNoCase(source1,source2)

**\[Exemple\]**

```c
int result;
char *a="abcd";
char *b="EFG";
result=StringCompare(a,b);//result=1;
result=StringCompareNoCase(a,b);//result=-1;
```

**4、<span id="StringCopy"></span>StringCopy**

**\[Description\]**

Copie une chaîne dans une autre.

**\[Syntaxe\]**

result = StringCopy(dest,source);

**\[Exemple\]**

```c
char a[4]="abcd";
char* b="efg";
char* c;
c=StringCopy(a,b);//c="abcdefg" ; il est préférable que a soit un tableau de caractères.
```

**5、<span id="StringFind"></span>StringFind**

**\[Description\]**

Retourne la position de la première occurrence de la chaîne cherchée dans la chaîne source.

**\[Syntaxe\]**

index=StringFind(source1,source2);

**\[Exemple\]**

```c
char a[8]="ab1c123d";
char* b="123";
char* c="ef";
int index;
index=StringFind(a,b); //index=4;
index=StringFind(a,c); //index=-1;
```

**6、<span id="StringFindOneOf"></span>StringFindOneOf**

**\[Description\]**

Retourne la position du premier caractère de la chaîne source présent dans la chaîne cherchée.

**\[Syntaxe\]**

index=StringFindOneOf(source1,source2);

**\[Exemple\]**

char a\[8\]="ab1c123d";

cahr\* b="1b";

in index;

index=StringFindOneOf(a,b); //index=2;

**7、<span id="StringIncluding"></span>StringIncluding**

**\[Description\]**

Extrait de la chaîne source une sous-chaîne formée des caractères de l'ensemble indiqué.

**\[Syntaxe\]**

```c
StringIncluding(source1,source2,dest);
```

**\[Exemple\]**

```c
char a[8]="aB1Eree";
char* b="aBe";
char dest[8];
StringIncluding(a,b,dest);//dest="aBee" ; il est préférable que dest soit un tableau de caractères.
```

**8、<span id="StringInsert"></span>StringInsert**

**\[Description\]**

Insère une chaîne à une position donnée de la chaîne de destination. Vérifiez que la chaîne de destination dispose d'un tampon suffisant.

**\[Syntaxe\]**

```c
StringInsert(pos,source,dest);
```

**\[Exemple\]**

```c
char a[8] = "aB1e";
char *b ="kdr";
int pos=2;
StringInsert(pos,b,a); //a="aBkdr1e".
```

**9、<span id="StringLength"></span>StringLength**

**\[Description\]**

Retourne la longueur d'une chaîne.

**\[Syntaxe\]**

result = StringLength(source);

**\[Exemple\]**

```c
char a[8]="ABerer";
int length;
length = StringLength(a); //length=6;
```

**10、<span id="StringMid"></span>StringMid**

**\[Description\]**

Extrait une suite de caractères à partir de la position indiquée dans la chaîne source et la place dans le tampon de destination.

**\[Syntaxe\]**

```c
StringMid(source,count,dest);
```

**\[Exemple\]**

```c
char a[8]="aB1e";
char b[3];
StringMid(a,2,b); //b="B1" ; il est préférable que b soit un tableau de caractères assez grand pour contenir les caractères extraits.
```

**11、<span id="StringSplit"></span>StringSplit**

**\[Description\]**

Découpe la chaîne.

**\[Syntaxe\]**

```c
StringSplit(dest1,dest2,source,pos);
```

**\[Exemple\]**

```c
char a[8]="aB1edge";
char b[5];
char c[5];
StringSplit(b,c,a,3); // il est préférable que b et c soient des tableaux de caractères.
```

**12、<span id="StringToLower"></span>StringToLower**

**\[Description\]**

Convertit les caractères d'une chaîne en minuscules.

**\[Syntaxe\]**

```c
StringToLower(source,dest); // il est préférable que dest soit un tableau de caractères.
```

**\[Exemple\]**

```c
char a[8]="ABeRe";
char b[8];
StringToLower(a,b);//b="abere".
```

**13、<span id="StringToUpper"></span>StringToUpper**

**\[Description\]**

Convertit les caractères d'une chaîne en majuscules. Vérifiez que le tampon est suffisant.

**\[Syntaxe\]**

```c
StringToUpper(source,dest);
```

**\[Exemple\]**

```c
char a[8]="ab1ere";
char b[8]; // il est préférable que b soit un tableau de caractères.
StringToUpper(a,b); //b="AB1ERE"；
```

**14、<span id="StringTrim"></span>StringTrim**

**\[Description\]**

retire source2 de source1 et place le résultat dans dest.

**\[Syntaxe\]**

```c
StringTrim(source1.source2,dest);
```

**\[Exemple\]**

```c
char a[12]="a1erd1esw";
char *b="1e";
char c[10];
StringTrim(a,b,c) //c="ardsw". Il est préférable que c soit un tableau de caractères.
```

**15、<span id="StringTrimLeft"></span>StringTrimLeft**

**\[Description\]**

retire de source1 tous les caractères présents dans source2 et place le résultat dans dest.

**\[Syntaxe\]**

```c
StringTrimLeft(source1,source2,dest);
```

**\[Exemple\]**

```c
char a[8]="aB1edge";
char* b="be";
char c[8];
StringTrimLeft(a,b,c);//c="aB1dg". Il est préférable que c soit un tableau de caractères.
```
