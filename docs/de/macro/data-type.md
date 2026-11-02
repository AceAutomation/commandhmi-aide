# Datentypen der Sprache C

**1.  Ganzzahlen**

Zu den Ganzzahlen gehören ganzzahlige Konstanten und Variablen. Ganzzahlige Konstanten sind ganze Zahlen. C kennt drei Schreibweisen: oktal, hexadezimal und dezimal.

**2.  Ganzzahlige Konstanten**

1\.  Oktale Konstanten

Oktale Konstanten beginnen mit 0, dem Präfix für Oktalzahlen. Ihre Ziffern sind 0-7. Oktalkonstanten sind meist vorzeichenlos. Gültige Oktalzahlen sind z. B.:

015 (dezimal: 13) 0101 (dezimal: 65) 0177777 (dezimal: 65535)

Ungültige Oktalzahlen: 256 (ohne Präfix 0)    03A2 (enthält Nicht-Oktalziffern)             -0127 (mit Minuszeichen)

2\.  Hexadezimale Konstanten

Hexadezimale Konstanten haben das Präfix 0X oder 0x. Ihre Ziffern sind 0-9, A-F bzw. a-f.

Gültige Hexadezimalzahlen sind z. B.:

0X2A (dezimal: 42) 0XA0 (dezimal: 160)    0XFFFF (dezimal: 65535) Ungültige Hexadezimalzahlen:

5A (ohne Präfix 0X)                0X3H (enthält Nicht-Hexadezimalziffern)

3\.  Dezimale Konstanten

Dezimale Konstanten haben kein Präfix. Ihre Ziffern sind 0-9. Gültige Dezimalzahlen sind z. B.:

237   -568   65535    1627

Ungültige Dezimalzahlen:

023 (Präfix 0 nicht erlaubt)          23D (enthält Nicht-Dezimalziffern)

Im Programm werden die Schreibweisen am Präfix unterschieden; ein falsches Präfix führt zu falschen Ergebnissen.

4\.  Auf einem 16-Bit-Rechner ist die Grundganzzahl 16 Bit breit, der Wertebereich also begrenzt. Vorzeichenlose Dezimalkonstanten reichen von 0 bis 65535, vorzeichenbehaftete von -32768 bis +32767. Vorzeichenlose Oktalzahlen reichen von 0 bis 0177777, vorzeichenlose Hexadezimalzahlen von 0X0 bis 0XFFFF bzw. 0x0 bis 0xFFFF. Größere Zahlen müssen als lange Ganzzahl angegeben werden, gekennzeichnet durch das Suffix „L“ oder „l“. Beispiele:

Dezimale long-Konstante 158L (dezimal: 158)   358000L (dezimal: -358000)

Oktale long-Konstante    012L (dezimal: 10)   077L (dezimal: 63)    0200000L (dezimal: 65536)

Hexadezimale long-Konstante   0X15L (dezimal: 21)    0XA5L (dezimal: 165)   0X10000L (dezimal: 65536). Der Wert von 158L und 158 ist gleich; da 158L aber eine lange Ganzzahl ist, reserviert der C-Compiler

dafür 4 Byte, für die Grundganzzahl 158 dagegen nur 2 Byte. Achten Sie daher auf Berechnungen und Ausgabeformate. Vorzeichenlose Zahlen werden ebenfalls durch ein Suffix gekennzeichnet: „U“ oder „u“. Beispiele:     358u,

0x38Au, 235Lu sind vorzeichenlose Zahlen. Präfixe und Suffixe lassen sich kombinieren. Beispiel:

0XA5Lu ist die vorzeichenlose lange Hexadezimalzahl A5, dezimal 165.

**3.  Ganzzahlige Variablen**

Ganzzahlige Variablen werden wie folgt eingeteilt:

1\.  Int

Typbezeichner int, belegt 2 Byte im Speicher. Ihr Wert ist immer eine Grundganzzahl.

2\.  Kurze Ganzzahl

Typbezeichner short int oder short. Größe und Wertebereich wie bei int.

3\.  Lange Ganzzahl

Typbezeichner long int oder long, belegt 4 Byte im Speicher. Ihr Wert ist immer eine lange Ganzzahl.

4\.  Vorzeichenlose Ganzzahl

Typbezeichner unsigned.

unsigned lässt sich mit den drei obigen Typen kombinieren:

(1)   Vorzeichenlose Ganzzahl: unsigned int oder unsigned. (2)   Vorzeichenlose kurze Ganzzahl: unsigned short.

(3)   Vorzeichenlose lange Ganzzahl: unsigned long.

Vorzeichenlose Ganzzahlen belegen gleich viel Speicher wie die vorzeichenbehafteten, können aber ohne Vorzeichenbit keine negativen Zahlen darstellen. Die folgende Tabelle zeigt Speichergröße und Wertebereich der Ganzzahltypen auf ARM.

|                |                                        |                |
|----------------|----------------------------------------|----------------|
| Typbezeichner | Wertebereich                           | Belegte Bytes |
| Int            | -2147483648~2147483647                 | ■■■■           |
| Short int      | -2147483648~2147483647                 | ■■■■           |
| Signed int     | -2147483648~2147483647                 | ■■■■           |
| Unsigned int   | 0~4294967295                           | ■■■■           |
| Long int       | -922337203685477808~922337203685477807 | ■■■■■■■■       |
| Unsigned long  | 0~18446744073709551615                 | ■■■■■■■■       |

**4.  Deklaration ganzzahliger Variablen**

Allgemeine Form einer Variablendeklaration: Typbezeichner Variablenname, …. Beispiele:

```c
int a,b,c; (a,b,c is integer variable)
long x,y; (x,y is long integer variable)
```

unsigned p,q;    (p, q sind vorzeichenlose Ganzzahlvariablen)

Bei der Deklaration von Variablen ist Folgendes zu beachten:

1\.  Nach einem Typbezeichner können mehrere Variablen gleichen Typs stehen, durch Kommas getrennt. Zwischen Typbezeichner und Variablenname muss mindestens ein Leerzeichen stehen.

2\.  Nach dem letzten Variablennamen steht „;“.

3\.  Die Deklaration muss vor der Verwendung stehen, meist am Anfang des Funktionsrumpfs.

\[Übung\]    //1int a,b;

short int c; short d=100; a=d-20; b=a+d;

```c
c=a+b+d;
d=d-a+c-b.
```

**5.  Gleitkommakonstanten**

Reelle Konstanten heißen auch Gleitkommakonstanten. In C werden Gleitkommazahlen nur dezimal geschrieben, in zwei Formen: Dezimalform und Exponentialform

1\.  Dezimalform

Besteht aus den Ziffern 0-9 und einem Dezimalpunkt. Gültige Gleitkommazahlen sind z. B. 0.0,.25,5.789,0.13,5.0,300.,-267.8230.

2\.  Exponentialform

Besteht aus einer Dezimalzahl, dem Exponentzeichen „e“ oder „E“ und dem Exponenten (ganzzahlig, ggf. mit Vorzeichen). Die Grundform ist a E n (a dezimal, n ganzzahlig) mit dem Wert a\*10,n. Beispiele: 2.1E5 (= 2.1\*10,5), 3.7E-2    (= 3.7\*10,)-2\*) 0.5E7 (= 0.5\*10,7), -2.8E-2 (= -2.8\*10,)-2\*). Ungültige Gleitkommazahlen: 345 (ohne Dezimalpunkt)      E7 (keine Ziffer vor dem Exponentzeichen) -5 (ohne Exponentzeichen) 53.-E3   (Minuszeichen falsch platziert) 2.7E (ohne Exponent)

In Standard-C können Gleitkommazahlen ein Suffix haben: „f“ oder „F“ kennzeichnet eine Gleitkommazahl. 356f und 356 sind z. B. gleichwertig.

**6.  Gleitkommavariablen**

Gleitkommavariablen gibt es mit einfacher und doppelter Genauigkeit, Typbezeichner float und double. In Turbo C belegt float 4 Byte (32 Bit) mit einem Bereich von 3.4E-38～3.4E+38 und nur 7 gültigen Stellen. double belegt 8 Byte (64 Bit) mit einem Bereich von 1.7E-308 ～ 1.7E+308 und

16 gültigen Stellen.

Deklariert werden Gleitkommavariablen nach denselben Regeln wie Ganzzahlen. Beispiel:  float x,y;    (x, y einfach genau)

double a,b,c;   (a, b, c doppelt genau)

Gleitkommakonstanten werden nicht nach einfacher und doppelter Genauigkeit unterschieden; alle werden als double behandelt. a   ■■■■

b   ■■■■■■■■

a&lt;---33333.33333

b&lt;---33333.33333333333;

\[Übung\]    //float int a=32; float b;

double d; b=12345678; d=b\*100;

```c
d=d+a;
d=d+58.123456;
```

**7.  Zeichen**

Dazu gehören Zeichenkonstanten und Zeichenvariablen. Zeichenkonstante

Eine Zeichenkonstante ist ein Zeichen in einfachen Anführungszeichen, z. B. 'a'. 'b', '=', '+', , '?' sind gültige Zeichenkonstanten. Zeichenkonstanten in C haben folgende Merkmale:

1.   Zeichenkonstanten stehen in einfachen Anführungszeichen, nicht in doppelten oder anderen Klammern.

2.   Eine Zeichenkonstante ist ein einzelnes Zeichen, keine Zeichenkette.

3.   Es kann jedes Zeichen des Zeichensatzes sein. Eine als Zeichen definierte Ziffer kann jedoch nicht für Berechnungen verwendet werden: '5' und 5 sind verschieden; '5' ist eine Zeichenkonstante und wird nicht berechnet.

**8.  Zeichenvariablen**

Der Wert einer Zeichenvariablen ist eine Zeichenkonstante, also ein einzelnes Zeichen. Ihr Typbezeichner ist char. Deklariert wird sie nach denselben Regeln wie Ganzzahlvariablen.

Beispiel:

char a,b;

Jede Zeichenvariable belegt ein Byte Speicher und enthält nur ein Zeichen, gespeichert als ASCII-Code. Der dezimale ASCII-Code von x ist z. B. 120, der von y

121\. Werden den Zeichenvariablen a und b die Zeichen 'x' und 'y' zugewiesen: a='x', b='y', werden tatsächlich 120 und 121 in a und b gespeichert:

a 0   1    1   1    1   0    0   0 b 0   1    1   1    1   0    0   1

Sie können daher wie Ganzzahlen behandelt werden. C erlaubt, Ganzzahlvariablen Zeichen und Zeichenvariablen Ganzzahlen zuzuweisen sowie Zeichenvariablen als Ganzzahlen und Ganzzahlen als Zeichen auszugeben. Die Ganzzahl belegt

2 Byte, das Zeichen 1 Byte; wird eine Ganzzahl als Zeichen behandelt, wird nur das niederwertige Byte verwendet. \[Übung\]    //charint a=49;

char b; char d; b=a+10; d=a+b;

\[Übung\]    //char c1,c2;

```c
c1='a';c2='b';
c1=c1-32;c2=c2-32;
```

**9.  Zeichenkettenkonstanten**

Eine Zeichenkettenkonstante ist eine Zeichenfolge in doppelten Anführungszeichen, z. B. "CHINA", "C program", "\$12.5". Zeichenkettenkonstanten unterscheiden sich von Zeichenkonstanten wie folgt:

1\.  Zeichenkonstanten stehen in einfachen, Zeichenkettenkonstanten in doppelten Anführungszeichen.

2\.  Eine Zeichenkonstante ist ein einzelnes Zeichen, eine Zeichenkettenkonstante enthält ein oder mehrere Zeichen.

3\.  Einer Zeichenvariablen kann ein Zeichen zugewiesen werden, aber keine Zeichenkettenkonstante; C kennt keinen Variablentyp für Zeichenketten.

4\.  Eine Zeichenkonstante belegt ein Byte Speicher, eine Zeichenkettenkonstante so viele Bytes wie Zeichen plus 1. Im zusätzlichen Byte steht das Zeichen "\0" (ASCII-Code 0), das Ende-Zeichen der Zeichenkette. "C program" steht im Speicher z. B. als C program\0. Obwohl die Zeichenkonstante 'a' und die Zeichenkettenkonstante ''a'' beide nur ein Zeichen enthalten, belegen sie unterschiedlich viel Speicher.

'a' belegt ein Byte, dargestellt als a

''a'' belegt zwei Bytes, dargestellt als a\0.

**10. Symbolische Konstanten**

In C kann eine Konstante durch einen Bezeichner dargestellt werden, eine symbolische Konstante. Sie muss vor der Verwendung definiert werden. Allgemeine Form:

\#define Bezeichner Konstante

\#define ist eine Präprozessoranweisung, die Makrodefinition. Sie ordnet dem Bezeichner den Konstantenwert zu; danach wird der Bezeichner im gesamten Programm durch diesen Wert ersetzt. Üblicherweise werden symbolische Konstanten in Großbuchstaben und Variablen in Kleinbuchstaben geschrieben, um sie zu unterscheiden.

```c
#define PI 3.14159 void main(){
float s,r; r=5; s=PI*r*r;
printf("s=%f\n",s);
}
```

Per Makrodefinition wird PI als 3.14159 festgelegt; s, r sind float.    5-&gt;r     PI\*r\*r-&gt;s

Das Programm gibt float s,r aus, mit r=5 und s=PI\*r\*r. PI wird vor der Funktion main per Makrodefinition auf 3.14159 festgelegt und ersetzt PI im Programm; s=PI\*r\*r entspricht also s=3.14159\*r\*r. Achtung: Eine symbolische Konstante ist keine Variable; ihr Wert kann in ihrem Gültigkeitsbereich nicht geändert und im Programm nicht neu zugewiesen werden.
