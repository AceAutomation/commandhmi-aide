# Funzioni di gestione delle stringhe

|                                                 |                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome funzione**                               | **Funzione**                                                                                                                                                              |
| **[StringCat](#StringCat)**                     | Concatena due stringhe                                                                                                                                                    |
| **[StringCompare](#StringCompare)**             | Confronta due stringhe, distinguendo maiuscole e minuscole                                                                                                                |
| **[StringCompareNoCase](#StringCompareNoCase)** | Confronta due stringhe, senza distinguere maiuscole e minuscole                                                                                                          |
| **[StringCopy](#StringCopy)**                   | Copia una stringa                                                                                                                                                         |
| **[StringFind](#StringFind)**                   | Restituisce la posizione della prima occorrenza della stringa cercata nella stringa sorgente; se non viene trovata, restituisce -1.                                       |
| **[StringFindOneOf](#StringFindOneOf)**         | Restituisce la posizione del primo carattere della stringa sorgente che corrisponde a uno qualsiasi dei caratteri della stringa cercata; se non trovato, restituisce -1.  |
| **[StringIncluding](#StringIncluding)**         | Estrae dalla stringa sorgente una sottostringa composta dai caratteri dell'insieme specificato.                                                                          |
| **[StringInsert](#StringInsert)**               | Inserisce una stringa in una posizione specifica della stringa di destinazione.                                                                                          |
| **[StringLength](#StringLength)**               | Restituisce la lunghezza di una stringa.                                                                                                                                  |
| **[StringMid](#StringMid)**                     | Estrae una sequenza di caratteri a partire dall'offset specificato della stringa sorgente.                                                                               |
| **[StringSplit](#StringSplit)**                 | Divide la stringa.                                                                                                                                                        |
| **[StringToLower](#StringToLower)**             | Converte i caratteri di una stringa in minuscolo.                                                                                                                         |
| **[StringToUpper](#StringToUpper)**             | Converte i caratteri di una stringa in maiuscolo.                                                                                                                         |
| **[StringTrim](#StringTrim)**                   | Rimuove source2 da source1 e forma una nuova stringa con il resto.                                                                                                        |
| **[StringTrimLeft](#StringTrimLeft)**           | Rimuove da source1 tutti i caratteri presenti in source2; il risultato viene restituito in dest.                                                                          |

**1、<span id="StringCat"></span>StringCat**

**\[Descrizione\]**

Accoda la stringa sorgente alla stringa di destinazione.

**\[Sintassi\]**

result=StringCat(dest\[start\],source);

**\[Esempio\]**

```c
char a[8]="abcd";
char *b="efg";
char *c;
c=StringCat(a,b); // c="abcdefg"; è preferibile che a sia un array di caratteri.
```

**2、<span id="StringCompare"></span>StringCompare**

**\[Descrizione\]**

Esegue un confronto tra due stringhe distinguendo maiuscole e minuscole.

**\[Sintassi\]**

result = StringCompare(source1,source2);

**\[Esempio\]**

```c
int result;
char *a="abcd";
char *b="efg";
result = StringCompare(a,b); //result=-1 (se a>b, result=1; se a=b, result=0; se a<b, result=-1).
```

**3、<span id="StringCompareNoCase"></span>StringCompareNoCase** //

**\[Descrizione\]**

Esegue un confronto tra due stringhe senza distinguere maiuscole e minuscole.

**\[Sintassi\]**

result = StringCompareNoCase(source1,source2)

**\[Esempio\]**

```c
int result;
char *a="abcd";
char *b="EFG";
result=StringCompare(a,b);//result=1;
result=StringCompareNoCase(a,b);//result=-1;
```

**4、<span id="StringCopy"></span>StringCopy**

**\[Descrizione\]**

Copia una stringa in un'altra.

**\[Sintassi\]**

result = StringCopy(dest,source);

**\[Esempio\]**

```c
char a[4]="abcd";
char* b="efg";
char* c;
c=StringCopy(a,b);//c="abcdefg"; è preferibile che a sia un array di caratteri.
```

**5、<span id="StringFind"></span>StringFind**

**\[Descrizione\]**

Restituisce la posizione della prima occorrenza della stringa cercata nella stringa sorgente.

**\[Sintassi\]**

index=StringFind(source1,source2);

**\[Esempio\]**

```c
char a[8]="ab1c123d";
char* b="123";
char* c="ef";
int index;
index=StringFind(a,b); //index=4;
index=StringFind(a,c); //index=-1;
```

**6、<span id="StringFindOneOf"></span>StringFindOneOf**

**\[Descrizione\]**

Restituisce la posizione del primo carattere della stringa sorgente che corrisponde a uno qualsiasi dei caratteri della stringa cercata.

**\[Sintassi\]**

index=StringFindOneOf(source1,source2);

**\[Esempio\]**

char a\[8\]="ab1c123d";

cahr\* b="1b";

in index;

index=StringFindOneOf(a,b); //index=2;

**7、<span id="StringIncluding"></span>StringIncluding**

**\[Descrizione\]**

Estrae dalla stringa sorgente una sottostringa contenente i caratteri presenti nella stringa di riferimento.

**\[Sintassi\]**

```c
StringIncluding(source1,source2,dest);
```

**\[Esempio\]**

```c
char a[8]="aB1Eree";
char* b="aBe";
char dest[8];
StringIncluding(a,b,dest);//dest="aBee"; è preferibile che dest sia un array di caratteri.
```

**8、<span id="StringInsert"></span>StringInsert**

**\[Descrizione\]**

Inserisce una stringa in una posizione specifica all'interno della stringa di destinazione. Assicurarsi che la stringa di destinazione disponga di un buffer sufficiente.

**\[Sintassi\]**

```c
StringInsert(pos,source,dest);
```

**\[Esempio\]**

```c
char a[8] = "aB1e";
char *b ="kdr";
int pos=2;
StringInsert(pos,b,a); //a="aBkdr1e".
```

**9、<span id="StringLength"></span>StringLength**

**\[Descrizione\]**

Restituisce la lunghezza di una stringa.

**\[Sintassi\]**

result = StringLength(source);

**\[Esempio\]**

```c
char a[8]="ABerer";
int length;
length = StringLength(a); //length=6;
```

**10、<span id="StringMid"></span>StringMid**

**\[Descrizione\]**

Estrae una sequenza di caratteri dalla stringa sorgente a partire dall'offset specificato e la memorizza nel buffer di destinazione.

**\[Sintassi\]**

```c
StringMid(source,count,dest);
```

**\[Esempio\]**

```c
char a[8]="aB1e";
char b[3];
StringMid(a,2,b); //b="B1"; è preferibile che b sia un array di caratteri con memoria sufficiente a contenere i caratteri estratti.
```

**11、<span id="StringSplit"></span>StringSplit**

**\[Descrizione\]**

Divide la stringa.

**\[Sintassi\]**

```c
StringSplit(dest1,dest2,source,pos);
```

**\[Esempio\]**

```c
char a[8]="aB1edge";
char b[5];
char c[5];
StringSplit(b,c,a,3); // è preferibile che b e c siano array di caratteri.
```

**12、<span id="StringToLower"></span>StringToLower**

**\[Descrizione\]**

Converte in minuscolo i caratteri di una stringa.

**\[Sintassi\]**

```c
StringToLower(source,dest); // è preferibile che dest sia un array di caratteri.
```

**\[Esempio\]**

```c
char a[8]="ABeRe";
char b[8];
StringToLower(a,b);//b="abere".
```

**13、<span id="StringToUpper"></span>StringToUpper**

**\[Descrizione\]**

Converte in maiuscolo i caratteri di una stringa. Verificare che il buffer sia sufficiente.

**\[Sintassi\]**

```c
StringToUpper(source,dest);
```

**\[Esempio\]**

```c
char a[8]="ab1ere";
char b[8]; // è preferibile che b sia un array di caratteri.
StringToUpper(a,b); //b="AB1ERE"；
```

**14、<span id="StringTrim"></span>StringTrim**

**\[Descrizione\]**

Rimuove source2 da source1 e restituisce il risultato in dest.

**\[Sintassi\]**

```c
StringTrim(source1.source2,dest);
```

**\[Esempio\]**

```c
char a[12]="a1erd1esw";
char *b="1e";
char c[10];
StringTrim(a,b,c) //c="ardsw". È preferibile che c sia un array di caratteri.
```

**15、<span id="StringTrimLeft"></span>StringTrimLeft**

**\[Descrizione\]**

Rimuove da source1 tutti i caratteri presenti in source2 e restituisce il risultato in dest.

**\[Sintassi\]**

```c
StringTrimLeft(source1,source2,dest);
```

**\[Esempio\]**

```c
char a[8]="aB1edge";
char* b="be";
char c[8];
StringTrimLeft(a,b,c);//c="aB1dg". È preferibile che c sia un array di caratteri.
```
