# Eindimensionale Arrays

In der Programmierung fasst ein Array mehrere Variablen gleichen Typs geordnet zusammen. Eine geordnete Menge von Datenelementen gleichen Typs heißt Array. In C gehört das Array zu den zusammengesetzten Datentypen. Ein Array besteht aus mehreren Array-Elementen, die Grunddatentypen oder zusammengesetzte Typen sein können. Je nach Typ der Elemente unterscheidet man numerische Arrays, Zeichen-Arrays, Zeiger-Arrays, Struktur-Arrays usw.

Dieser Abschnitt behandelt numerische Arrays und Zeichen-Arrays; die anderen folgen in späteren Abschnitten. Ein Array muss in C vor der Verwendung deklariert werden. Die allgemeine Form der Deklaration ist: Typbezeichner Arrayname    \[konstanter Ausdruck\]. Dabei ist der Typbezeichner ein beliebiger Grund- oder zusammengesetzter Typ, der Arrayname ein vom Benutzer festgelegter Bezeichner. Der konstante Ausdruck in eckigen Klammern gibt die Anzahl der Elemente an, die Array-Länge.

Beispiel:

int a\[10\]; das int-Array a enthält 10 Elemente.

float b\[10\],c\[20\]; das float-Array b enthält 10 Elemente, das float-Array c 20 Elemente. char ch\[20\]; das Zeichen-Array ch enthält 20 Elemente.

Bei der Deklaration von Arrays ist Folgendes zu beachten:

1\.  Der Array-Typ ist der Typ der Elementwerte. Alle Elemente eines Arrays haben denselben Datentyp.

2\.  Der Arrayname muss den Regeln für Bezeichner entsprechen.

3\.  Der Arrayname darf nicht mit einem anderen Variablennamen übereinstimmen. Beispiel:   void main ()

```c
{
int a;
float a[10];
```

……

} ist falsch

4\.  Der konstante Ausdruck in eckigen Klammern gibt die Anzahl der Elemente an. a \[5\] bedeutet z. B., dass a 5 Elemente hat. Der Index beginnt bei 0; die fünf Elemente sind also a\[0\],a\[1\],a\[2\],a\[3\],a\[4\].

5\.  In den eckigen Klammern darf keine Variable als Elementanzahl stehen, wohl aber eine symbolische Konstante oder ein konstanter Ausdruck. Beispiel:

\#define FD    5

```c
void main ()
{
int a[3+2],b[7+FD];
```

……

```c
} is legal. However, the following expression form is incorrect. void main()
{
int n=5;
int a[n];
```

……

}

6\.  In einer Deklaration können mehrere Arrays und Variablen deklariert werden.

Beispiel: int a,b,c,d,k1\[10\],k2\[20\];

**1.  Array-Elemente**

Array-Elemente sind die Grundbausteine eines Arrays. Ein Element ist eine Variable, die durch Arrayname und Index bezeichnet wird. Der Index gibt die Position des Elements im Array an. Die allgemeine Form ist: Arrayname \[Index\]. Der Index ist eine ganzzahlige Konstante oder ein ganzzahliger Ausdruck; ein Dezimalwert wird von C automatisch in eine Ganzzahl umgewandelt. a\[5\],a\[i+j\],a\[i++\] sind z. B. gültige Array-Elemente. Array-Elemente heißen auch indizierte Variablen; sie können erst nach der Definition des Arrays verwendet werden. In C werden indizierte Variablen einzeln verwendet, nicht das ganze Array auf einmal.

Die allgemeine Form der Initialisierung ist: static Typbezeichner Arrayname \[konstanter Ausdruck\]=\[Wert……\]. static bezeichnet die statische Speicherklasse. In C können nur statische und externe Arrays initialisiert werden (die Begriffe statische und externe Speicherung werden in Kapitel 5 erläutert). Die Daten in {    } sind die Anfangswerte der Elemente, durch Kommas getrennt, z. B. static int a\[10\]={    0,1,2,3,4,5,6,7,8,9   }, gleichbedeutend mit a\[0\]=0;a\[1\]=1...a\[9\]=9;

**2.  Regeln für die Initialisierung von Arrays in C:**

1\.  Es dürfen nur einzelne Elemente initialisiert werden. Enthält {    } weniger Werte als Elemente, werden nur die ersten Elemente initialisiert. Beispiel: static int a\[10\]={0,1,2,3,4} initialisiert

die ersten 5 Elemente a\[0\]～a\[4\]; die letzten 5 Elemente werden automatisch auf 0 gesetzt.

2\.  Die Elemente müssen einzeln initialisiert werden; eine Gesamtzuweisung an das Array ist nicht möglich. Um z. B. 10 Elementen den Wert 1 zuzuweisen, schreibt man static int a\[10\]={1,1,1,1,1,1,1,1,1,1} und nicht static int a\[10\]=1.

3\.  Wird ein Array ohne Anfangswerte initialisiert, sind alle Elemente 0.

4\.  Werden alle Elemente initialisiert, kann die Elementanzahl in der Deklaration entfallen. Beispiel: static int a\[5\]={1,2,3,4,5} kann als     static int a\[\]={1,2,3,4,5} geschrieben werden. Werte können auch während der Programmausführung dynamisch zugewiesen werden, z. B. mit einer Schleife und der Funktion scanf Element für Element.

**3.  Zeichen-Arrays**

Ein Array zur Speicherung von Zeichen heißt Zeichen-Array. Seine Deklaration entspricht der eines numerischen Arrays, z. B. char c\[10\]. Da Zeichen und Ganzzahlen ähnlich sind, kann es auch als int c\[10\] definiert werden, dann belegt aber jedes Element 2 Byte. Zeichen-Arrays können auch zweidimensional sein, z. B. ist char c\[5\]\[10\] ein zweidimensionales Zeichen-Array. Zeichen-Arrays können bei der Deklaration initialisiert werden, z. B. static char c\[10\]={\`c\`,\`    \`,\`p\`,\`r\`,o\`,g\`,r\`,\`a\`,\`m\`}. Danach enthalten c\[0\] bis c\[9\] die Zeichen; c\[9\] wurde nicht zugewiesen und vom System automatisch auf 0 gesetzt. Werden alle Elemente initialisiert, kann die Längenangabe entfallen, z. B. static char c\[\]={\`c\`,\`    \`,\`p\`,\`r\`,\`o\`,\`g\`,\`r\`,\`a\`,\`m\`}; die Länge von c ist dann 9.

C erlaubt die Initialisierung von Arrays mit Zeichenketten. Beispiel: static char c\[\]={'c', ' ','p','r','o','g','r','a','m'} kann als static char c\[\]={"C program"} oder ohne {} als static char c\[\]="C program" geschrieben werden. Die Zuweisung als Zeichenkette belegt ein Byte mehr als die Einzelzuweisung: für das Endezeichen '\0'. Im Speicher steht das Array c also als C program\0; '\0' wird vom C-System automatisch angehängt. Dank '\0' wird die Array-Länge bei der Initialisierung mit Zeichenketten meist nicht angegeben, sondern vom System ermittelt. Mit Zeichenketten werden Ein- und Ausgabe von Zeichen-Arrays einfach: Außer der Initialisierung kann eine ganze Zeichenkette mit printf und scanf auf einmal aus- und eingegeben werden, ohne jedes Zeichen einzeln in einer Schleife zu behandeln.
