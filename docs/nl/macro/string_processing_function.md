# Tekenreeksfuncties

|                                                 |                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Functienaam**                               | **Functie**                                                                                                                                                              |
| **[StringCat](#StringCat)**                     | Voegt twee tekenreeksen samen                                                                                                                                               |
| **[StringCompare](#StringCompare)**             | Vergelijkt twee tekenreeksen met onderscheid tussen hoofd- en kleine letters                                                                                                               |
| **[StringCompareNoCase](#StringCompareNoCase)** | Vergelijkt twee tekenreeksen zonder onderscheid tussen hoofd- en kleine letters                                                                                                             |
| **[StringCopy](#StringCopy)**                   | Kopieert een tekenreeks                                                                                                                                                               |
| **[StringFind](#StringFind)**                   | Geeft de positie van het eerste voorkomen van de zoektekenreeks in de brontekenreeks; -1 als die niet wordt gevonden.                            |
| **[StringFindOneOf](#StringFindOneOf)**         | Geeft de positie van het eerste teken van de brontekenreeks dat in de zoektekenreeks voorkomt; -1 als er geen wordt gevonden.  |
| **[StringIncluding](#StringIncluding)**         | Geeft een deeltekenreeks van de bron met tekens uit de opgegeven set.                                                                                     |
| **[StringInsert](#StringInsert)**               | Voegt een tekenreeks in op een bepaalde positie van de doeltekenreeks.                                                                                           |
| **[StringLength](#StringLength)**               | Geeft de lengte van een tekenreeks.                                                                                                                                            |
| **[StringMid](#StringMid)**                     | Geeft een reeks tekens vanaf de opgegeven positie van de brontekenreeks.                                                                                         |
| **[StringSplit](#StringSplit)**                 | Splitst de tekenreeks.                                                                                                                                                     |
| **[StringToLower](#StringToLower)**             | Zet de tekens van een tekenreeks om in kleine letters.                                                                                                                          |
| **[StringToUpper](#StringToUpper)**             | Zet de tekens van een tekenreeks om in hoofdletters.                                                                                                                          |
| **[StringTrim](#StringTrim)**                   | Verwijdert source2 uit source1 en vormt met de rest een nieuwe tekenreeks.                                                                                                       |
| **[StringTrimLeft](#StringTrimLeft)**           | Verwijdert uit source1 alle tekens van source2; het resultaat staat in dest.                                                                                             |

**1、<span id="StringCat"></span>StringCat**

**\[Beschrijving\]**

Voegt de brontekenreeks toe aan het einde van de doeltekenreeks.

**\[Gebruik\]**

result=StringCat(dest\[start\],source);

**\[Voorbeeld\]**

```c
char a[8]="abcd";
char *b="efg";
char *c;
c=StringCat(a,b); // c="abcdefg"; a is bij voorkeur een tekenarray.
```

**2、<span id="StringCompare"></span>StringCompare**

**\[Beschrijving\]**

Vergelijkt twee tekenreeksen, hoofdlettergevoelig.

**\[Gebruik\]**

result = StringCompare(source1,source2);

**\[Voorbeeld\]**

```c
int result;
char *a="abcd";
char *b="efg";
result = StringCompare(a,b); //result=-1 (bij a>b is result=1; bij a=b is result=0; bij a<b is result=-1).
```

**3、<span id="StringCompareNoCase"></span>StringCompareNoCase** //

**\[Beschrijving\]**

Vergelijkt twee tekenreeksen, niet hoofdlettergevoelig.

**\[Gebruik\]**

result = StringCompareNoCase(source1,source2)

**\[Voorbeeld\]**

```c
int result;
char *a="abcd";
char *b="EFG";
result=StringCompare(a,b);//result=1;
result=StringCompareNoCase(a,b);//result=-1;
```

**4、<span id="StringCopy"></span>StringCopy**

**\[Beschrijving\]**

Kopieert een tekenreeks naar een andere.

**\[Gebruik\]**

result = StringCopy(dest,source);

**\[Voorbeeld\]**

```c
char a[4]="abcd";
char* b="efg";
char* c;
c=StringCopy(a,b);//c="abcdefg"; a is bij voorkeur een tekenarray.
```

**5、<span id="StringFind"></span>StringFind**

**\[Beschrijving\]**

Geeft de positie van het eerste voorkomen van de doeltekenreeks in de brontekenreeks.

**\[Gebruik\]**

index=StringFind(source1,source2);

**\[Voorbeeld\]**

```c
char a[8]="ab1c123d";
char* b="123";
char* c="ef";
int index;
index=StringFind(a,b); //index=4;
index=StringFind(a,c); //index=-1;
```

**6、<span id="StringFindOneOf"></span>StringFindOneOf**

**\[Beschrijving\]**

Geeft de positie van het eerste teken in de brontekenreeks dat overeenkomt met een teken uit de doeltekenreeks.

**\[Gebruik\]**

index=StringFindOneOf(source1,source2);

**\[Voorbeeld\]**

char a\[8\]="ab1c123d";

cahr\* b="1b";

in index;

index=StringFindOneOf(a,b); //index=2;

**7、<span id="StringIncluding"></span>StringIncluding**

**\[Beschrijving\]**

Haalt uit de brontekenreeks een deelreeks met de tekens uit de opgegeven verzameling.

**\[Gebruik\]**

```c
StringIncluding(source1,source2,dest);
```

**\[Voorbeeld\]**

```c
char a[8]="aB1Eree";
char* b="aBe";
char dest[8];
StringIncluding(a,b,dest);//dest="aBee"; dest is bij voorkeur een tekenarray.
```

**8、<span id="StringInsert"></span>StringInsert**

**\[Beschrijving\]**

Voegt een tekenreeks op een bepaalde positie in de doeltekenreeks in. Let op dat de doeltekenreeks voldoende buffer heeft.

**\[Gebruik\]**

```c
StringInsert(pos,source,dest);
```

**\[Voorbeeld\]**

```c
char a[8] = "aB1e";
char *b ="kdr";
int pos=2;
StringInsert(pos,b,a); //a="aBkdr1e".
```

**9、<span id="StringLength"></span>StringLength**

**\[Beschrijving\]**

Geeft de lengte van een tekenreeks.

**\[Gebruik\]**

result = StringLength(source);

**\[Voorbeeld\]**

```c
char a[8]="ABerer";
int length;
length = StringLength(a); //length=6;
```

**10、<span id="StringMid"></span>StringMid**

**\[Beschrijving\]**

Haalt een reeks tekens vanaf de opgegeven positie uit de brontekenreeks en slaat die op in de doelbuffer.

**\[Gebruik\]**

```c
StringMid(source,count,dest);
```

**\[Voorbeeld\]**

```c
char a[8]="aB1e";
char b[3];
StringMid(a,2,b); //b="B1"; b is bij voorkeur een tekenarray met genoeg geheugen voor de opgehaalde tekens.
```

**11、<span id="StringSplit"></span>StringSplit**

**\[Beschrijving\]**

Splitst de tekenreeks.

**\[Gebruik\]**

```c
StringSplit(dest1,dest2,source,pos);
```

**\[Voorbeeld\]**

```c
char a[8]="aB1edge";
char b[5];
char c[5];
StringSplit(b,c,a,3); // b en c zijn bij voorkeur tekenarrays.
```

**12、<span id="StringToLower"></span>StringToLower**

**\[Beschrijving\]**

Zet de tekens van een tekenreeks om in kleine letters.

**\[Gebruik\]**

```c
StringToLower(source,dest); // dest is bij voorkeur een tekenarray.
```

**\[Voorbeeld\]**

```c
char a[8]="ABeRe";
char b[8];
StringToLower(a,b);//b="abere".
```

**13、<span id="StringToUpper"></span>StringToUpper**

**\[Beschrijving\]**

Zet de tekens van een tekenreeks om in hoofdletters. Let op dat de buffer groot genoeg is.

**\[Gebruik\]**

```c
StringToUpper(source,dest);
```

**\[Voorbeeld\]**

```c
char a[8]="ab1ere";
char b[8]; // b is bij voorkeur een tekenarray.
StringToUpper(a,b); //b="AB1ERE"；
```

**14、<span id="StringTrim"></span>StringTrim**

**\[Beschrijving\]**

Verwijdert source2 uit source1 en geeft het resultaat in dest.

**\[Gebruik\]**

```c
StringTrim(source1.source2,dest);
```

**\[Voorbeeld\]**

```c
char a[12]="a1erd1esw";
char *b="1e";
char c[10];
StringTrim(a,b,c) //c="ardsw". c is bij voorkeur een tekenarray.
```

**15、<span id="StringTrimLeft"></span>StringTrimLeft**

**\[Beschrijving\]**

Verwijdert elk teken van source2 uit source1 en geeft het resultaat in dest.

**\[Gebruik\]**

```c
StringTrimLeft(source1,source2,dest);
```

**\[Voorbeeld\]**

```c
char a[8]="aB1edge";
char* b="be";
char c[8];
StringTrimLeft(a,b,c);//c="aB1dg". c is bij voorkeur een tekenarray.
```
