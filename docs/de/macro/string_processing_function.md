# Zeichenkettenfunktionen

|                                                 |                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Funktionsname**                               | **Funktion**                                                                                                                                                              |
| **[StringCat](#StringCat)**                     | Verkettet zwei Zeichenketten                                                                                                                                               |
| **[StringCompare](#StringCompare)**             | Vergleicht zwei Zeichenketten unter Beachtung der Groß-/Kleinschreibung                                                                                                               |
| **[StringCompareNoCase](#StringCompareNoCase)** | Vergleicht zwei Zeichenketten ohne Beachtung der Groß-/Kleinschreibung                                                                                                             |
| **[StringCopy](#StringCopy)**                   | Kopiert eine Zeichenkette                                                                                                                                                               |
| **[StringFind](#StringFind)**                   | Liefert die Position des ersten Vorkommens der Suchzeichenkette in der Quellzeichenkette; -1, wenn sie nicht gefunden wird.                            |
| **[StringFindOneOf](#StringFindOneOf)**         | Liefert die Position des ersten Zeichens der Quellzeichenkette, das in der Suchzeichenkette vorkommt; -1, wenn keines gefunden wird.  |
| **[StringIncluding](#StringIncluding)**         | Liefert eine Teilzeichenkette der Quelle aus Zeichen der angegebenen Menge.                                                                                     |
| **[StringInsert](#StringInsert)**               | Fügt eine Zeichenkette an einer bestimmten Stelle der Zielzeichenkette ein.                                                                                           |
| **[StringLength](#StringLength)**               | Liefert die Länge einer Zeichenkette.                                                                                                                                            |
| **[StringMid](#StringMid)**                     | Liefert eine Zeichenfolge ab der angegebenen Position der Quellzeichenkette.                                                                                         |
| **[StringSplit](#StringSplit)**                 | Teilt die Zeichenkette.                                                                                                                                                     |
| **[StringToLower](#StringToLower)**             | Wandelt die Zeichen einer Zeichenkette in Kleinbuchstaben um.                                                                                                                          |
| **[StringToUpper](#StringToUpper)**             | Wandelt die Zeichen einer Zeichenkette in Großbuchstaben um.                                                                                                                          |
| **[StringTrim](#StringTrim)**                   | Entfernt source2 aus source1 und bildet aus dem Rest eine neue Zeichenkette.                                                                                                       |
| **[StringTrimLeft](#StringTrimLeft)**           | Entfernt aus source1 alle Zeichen von source2; das Ergebnis steht in dest.                                                                                             |

**1、<span id="StringCat"></span>StringCat**

**\[Beschreibung\]**

Hängt die Quellzeichenkette an die Zielzeichenkette an.

**\[Verwendung\]**

result=StringCat(dest\[start\],source);

**\[Beispiel\]**

```c
char a[8]="abcd";
char *b="efg";
char *c;
c=StringCat(a,b); // c="abcdefg"; a sollte möglichst ein Zeichen-Array sein.
```

**2、<span id="StringCompare"></span>StringCompare**

**\[Beschreibung\]**

Vergleicht zwei Zeichenketten unter Beachtung der Groß-/Kleinschreibung.

**\[Verwendung\]**

result = StringCompare(source1,source2);

**\[Beispiel\]**

```c
int result;
char *a="abcd";
char *b="efg";
result = StringCompare(a,b); //result=-1 (bei a>b ist result=1, bei a=b result=0, bei a<b result=-1).
```

**3、<span id="StringCompareNoCase"></span>StringCompareNoCase** //

**\[Beschreibung\]**

Vergleicht zwei Zeichenketten ohne Beachtung der Groß-/Kleinschreibung.

**\[Verwendung\]**

result = StringCompareNoCase(source1,source2)

**\[Beispiel\]**

```c
int result;
char *a="abcd";
char *b="EFG";
result=StringCompare(a,b);//result=1;
result=StringCompareNoCase(a,b);//result=-1;
```

**4、<span id="StringCopy"></span>StringCopy**

**\[Beschreibung\]**

Kopiert eine Zeichenkette in eine andere.

**\[Verwendung\]**

result = StringCopy(dest,source);

**\[Beispiel\]**

```c
char a[4]="abcd";
char* b="efg";
char* c;
c=StringCopy(a,b);//c="abcdefg"; a sollte möglichst ein Zeichen-Array sein.
```

**5、<span id="StringFind"></span>StringFind**

**\[Beschreibung\]**

Liefert die Position des ersten Vorkommens der Suchzeichenkette in der Quellzeichenkette.

**\[Verwendung\]**

index=StringFind(source1,source2);

**\[Beispiel\]**

```c
char a[8]="ab1c123d";
char* b="123";
char* c="ef";
int index;
index=StringFind(a,b); //index=4;
index=StringFind(a,c); //index=-1;
```

**6、<span id="StringFindOneOf"></span>StringFindOneOf**

**\[Beschreibung\]**

Liefert die Position des ersten Zeichens der Quellzeichenkette, das in der Suchzeichenkette vorkommt.

**\[Verwendung\]**

index=StringFindOneOf(source1,source2);

**\[Beispiel\]**

char a\[8\]="ab1c123d";

cahr\* b="1b";

in index;

index=StringFindOneOf(a,b); //index=2;

**7、<span id="StringIncluding"></span>StringIncluding**

**\[Beschreibung\]**

Liefert eine Teilzeichenkette der Quelle aus Zeichen der angegebenen Menge.

**\[Verwendung\]**

```c
StringIncluding(source1,source2,dest);
```

**\[Beispiel\]**

```c
char a[8]="aB1Eree";
char* b="aBe";
char dest[8];
StringIncluding(a,b,dest);//dest="aBee"; dest sollte möglichst ein Zeichen-Array sein.
```

**8、<span id="StringInsert"></span>StringInsert**

**\[Beschreibung\]**

Fügt eine Zeichenkette an einer bestimmten Stelle der Zielzeichenkette ein. Achten Sie auf ausreichenden Puffer in der Zielzeichenkette.

**\[Verwendung\]**

```c
StringInsert(pos,source,dest);
```

**\[Beispiel\]**

```c
char a[8] = "aB1e";
char *b ="kdr";
int pos=2;
StringInsert(pos,b,a); //a="aBkdr1e".
```

**9、<span id="StringLength"></span>StringLength**

**\[Beschreibung\]**

Liefert die Länge einer Zeichenkette.

**\[Verwendung\]**

result = StringLength(source);

**\[Beispiel\]**

```c
char a[8]="ABerer";
int length;
length = StringLength(a); //length=6;
```

**10、<span id="StringMid"></span>StringMid**

**\[Beschreibung\]**

Liefert eine Zeichenfolge ab der angegebenen Position der Quellzeichenkette und speichert sie im Zielpuffer.

**\[Verwendung\]**

```c
StringMid(source,count,dest);
```

**\[Beispiel\]**

```c
char a[8]="aB1e";
char b[3];
StringMid(a,2,b); //b="B1"; b sollte möglichst ein Zeichen-Array sein, das groß genug für die gelesenen Zeichen ist.
```

**11、<span id="StringSplit"></span>StringSplit**

**\[Beschreibung\]**

Teilt die Zeichenkette.

**\[Verwendung\]**

```c
StringSplit(dest1,dest2,source,pos);
```

**\[Beispiel\]**

```c
char a[8]="aB1edge";
char b[5];
char c[5];
StringSplit(b,c,a,3); // b und c sollten möglichst Zeichen-Arrays sein.
```

**12、<span id="StringToLower"></span>StringToLower**

**\[Beschreibung\]**

Wandelt die Zeichen einer Zeichenkette in Kleinbuchstaben um.

**\[Verwendung\]**

```c
StringToLower(source,dest); // dest sollte möglichst ein Zeichen-Array sein.
```

**\[Beispiel\]**

```c
char a[8]="ABeRe";
char b[8];
StringToLower(a,b);//b="abere".
```

**13、<span id="StringToUpper"></span>StringToUpper**

**\[Beschreibung\]**

Wandelt die Zeichen einer Zeichenkette in Großbuchstaben um. Achten Sie auf ausreichenden Puffer.

**\[Verwendung\]**

```c
StringToUpper(source,dest);
```

**\[Beispiel\]**

```c
char a[8]="ab1ere";
char b[8]; // b sollte möglichst ein Zeichen-Array sein.
StringToUpper(a,b); //b="AB1ERE"；
```

**14、<span id="StringTrim"></span>StringTrim**

**\[Beschreibung\]**

entfernt source2 aus source1 und legt das Ergebnis in dest ab.

**\[Verwendung\]**

```c
StringTrim(source1.source2,dest);
```

**\[Beispiel\]**

```c
char a[12]="a1erd1esw";
char *b="1e";
char c[10];
StringTrim(a,b,c) //c="ardsw". c sollte möglichst ein Zeichen-Array sein.
```

**15、<span id="StringTrimLeft"></span>StringTrimLeft**

**\[Beschreibung\]**

entfernt aus source1 alle Zeichen von source2 und legt das Ergebnis in dest ab.

**\[Verwendung\]**

```c
StringTrimLeft(source1,source2,dest);
```

**\[Beispiel\]**

```c
char a[8]="aB1edge";
char* b="be";
char c[8];
StringTrimLeft(a,b,c);//c="aB1dg". c sollte möglichst ein Zeichen-Array sein.
```
