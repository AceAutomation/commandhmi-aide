# String handling functions

|                                                 |                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Function name**                               | **function**                                                                                                                                                              |
| **[StringCat](#StringCat)**                     | Joint two character strings                                                                                                                                               |
| **[StringCompare](#StringCompare)**             | Compare the values of two character strings; case sensitive                                                                                                               |
| **[StringCompareNoCase](#StringCompareNoCase)** | Compare the values of two character strings; case insensitive                                                                                                             |
| **[StringCopy](#StringCopy)**                   | String copy                                                                                                                                                               |
| **[StringFind](#StringFind)**                   | Return to the position of the first occurrence of target string in the source string; if there is no found in the source string, return to -1.                            |
| **[StringFindOneOf](#StringFindOneOf)**         | Return to the position of the first character in the source string that matches any character in target string; if there is no found in the source string, return to -1.  |
| **[StringIncluding](#StringIncluding)**         | Retrieve a substring of the source string that contains characters in the set string.                                                                                     |
| **[StringInsert](#StringInsert)**               | Insert a string into a specific position within the destination string content.                                                                                           |
| **[StringLength](#StringLength)**               | Obtain the length of a string.                                                                                                                                            |
| **[StringMid](#StringMid)**                     | Retrieve some characters sequence from the specified offset of the source string.                                                                                         |
| **[StringSplit](#StringSplit)**                 | Split out the string.                                                                                                                                                     |
| **[StringToLower](#StringToLower)**             | Convert the characters of a string to lowercase.                                                                                                                          |
| **[StringToUpper](#StringToUpper)**             | Convert the characters of a string to uppercase.                                                                                                                          |
| **[StringTrim](#StringTrim)**                   | Split the source2 out from source1 to form a new one with the rest.                                                                                                       |
| **[StringTrimLeft](#StringTrimLeft)**           | Split out any character of source2 in source1; Return the result to the dest.                                                                                             |

**1、<span id="StringCat"></span>StringCat**

**\[Description\]**

Append source string to destination string.

**\[Usage\]**

result=StringCat(dest\[start\],source);

**\[Example\]**

```c
char a[8]="abcd";
char *b="efg";
char *c;
c=StringCat(a,b); // c="abcdefg"，it is better if a is a character array.
```

**2、<span id="StringCompare"></span>StringCompare**

**\[Description\]**

Do a case-sensitive comparison of two strings.

**\[Usage\]**

result = StringCompare(source1,source2);

**\[Example\]**

```c
int result;
char *a="abcd";
char *b="efg";
result = StringCompare(a,b); //result=-1(if a>b, result=1;if a=b, result=0; if a<b then result=-1)。
```

**3、<span id="StringCompareNoCase"></span>StringCompareNoCase** //

**\[Description\]**

Do a case-insensitive comparison of two strings.

**\[Usage\]**

result = StringCompareNoCase(source1,source2)

**\[Example\]**

```c
int result;
char *a="abcd";
char *b="EFG";
result=StringCompare(a,b);//result=1;
result=StringCompareNoCase(a,b);//result=-1;
```

**4、<span id="StringCopy"></span>StringCopy**

**\[Description\]**

Copy ons string to another.

**\[Usage\]**

result = StringCopy(dest,source);

**\[Example\]**

```c
char a[4]="abcd";
char* b="efg";
char* c;
c=StringCopy(a,b);//c="abcdefg"; it is better if a is a character array.
```

**5、<span id="StringFind"></span>StringFind**

**\[Description\]**

Return the position of the first occurrence of target string in the source string.

**\[Usage\]**

index=StringFind(source1,source2);

**\[Example\]**

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

Return the position of the first character in the source string that matches any character in target string.

**\[Usage\]**

index=StringFindOneOf(source1,source2);

**\[Example\]**

char a\[8\]="ab1c123d";

cahr\* b="1b";

in index;

index=StringFindOneOf(a,b); //index=2;

**7、<span id="StringIncluding"></span>StringIncluding**

**\[Description\]**

Retrieve a substring of the source string that contains characters in the set string.

**\[Usage\]**

```c
StringIncluding(source1,source2,dest);
```

**\[Example\]**

```c
char a[8]="aB1Eree";
char* b="aBe";
char dest[8];
StringIncluding(a,b,dest);//dest="aBee"; it is better if dest is a character array.
```

**8、<span id="StringInsert"></span>StringInsert**

**\[Description\]**

Insert a string in a specific within the destination string content. Notice it that the destination string has sufficient buffer.

**\[Usage\]**

```c
StringInsert(pos,source,dest);
```

**\[Example\]**

```c
char a[8] = "aB1e";
char *b ="kdr";
int pos=2;
StringInsert(pos,b,a); //a="aBkdr1e".
```

**9、<span id="StringLength"></span>StringLength**

**\[Description\]**

Obtain the length of a string.

**\[Usage\]**

result = StringLength(source);

**\[Example\]**

```c
char a[8]="ABerer";
int length;
length = StringLength(a); //length=6;
```

**10、<span id="StringMid"></span>StringMid**

**\[Description\]**

Retrieve some characters sequence from the specified offset of the source string and store it in the destination buffer.

**\[Usage\]**

```c
StringMid(source,count,dest);
```

**\[Example\]**

```c
char a[8]="aB1e";
char b[3];
StringMid(a,2,b); //b="B1" it is better if b is a character array and it has enough memory to save the fetched character.
```

**11、<span id="StringSplit"></span>StringSplit**

**\[Description\]**

Split out the string.

**\[Usage\]**

```c
StringSplit(dest1,dest2,source,pos);
```

**\[Example\]**

```c
char a[8]="aB1edge";
char b[5];
char c[5];
StringSplit(b,c,a,3); // it is better if b and c are character arrays.
```

**12、<span id="StringToLower"></span>StringToLower**

**\[Description\]**

Convert the characters of a string to lowercase.

**\[Usage\]**

```c
StringToLower(source,dest); // it is better if dest is a character array.
```

**\[Example\]**

```c
char a[8]="ABeRe";
char b[8];
StringToLower(a,b);//b="abere".
```

**13、<span id="StringToUpper"></span>StringToUpper**

**\[Description\]**

Convert the characters of a string to uppercase.Notice if there is sufficient buffer.

**\[Usage\]**

```c
StringToUpper(source,dest);
```

**\[Example\]**

```c
char a[8]="ab1ere";
char b[8]; // it is better if b is a character array.
StringToUpper(a,b); //b="AB1ERE"；
```

**14、<span id="StringTrim"></span>StringTrim**

**\[Description\]**

split the source2 out from source1,return the result to dest.

**\[Usage\]**

```c
StringTrim(source1.source2,dest);
```

**\[Example\]**

```c
char a[12]="a1erd1esw";
char *b="1e";
char c[10];
StringTrim(a,b,c) //c="ardsw" . It is better if c is a character array.
```

**15、<span id="StringTrimLeft"></span>StringTrimLeft**

**\[Description\]**

split out any character of source2 in source1,Return the result to the dest.

**\[Usage\]**

```c
StringTrimLeft(source1,source2,dest);
```

**\[Example\]**

```c
char a[8]="aB1edge";
char* b="be";
char c[8];
StringTrimLeft(a,b,c);//c="aB1dg", It is better if c is a character array.
```
