# Programme mit Verzweigung

**Vergleichsoperatoren und -ausdrücke**

In Programmen werden häufig zwei Werte verglichen, um den weiteren Ablauf festzulegen. Die Operatoren dafür heißen Vergleichsoperatoren. C kennt folgende Vergleichsoperatoren:

&lt;   kleiner als

&lt;= kleiner oder gleich

&gt; größer als

&gt;= größer oder gleich

== gleich

!= ungleich

Vergleichsoperatoren sind zweistellig und linksassoziativ. Ihre Rangfolge liegt unter der der arithmetischen und über der der Zuweisungsoperatoren. Von den sechs Vergleichsoperatoren haben &lt;,&lt;=,&gt;,&gt;= gleichen Rang, der höher ist als der von ==   und !=; ==    und != haben untereinander gleichen Rang.

**Vergleichsausdrücke**

Die allgemeine Form eines Vergleichsausdrucks ist: Ausdruck Vergleichsoperator Ausdruck. Beispiele gültiger Vergleichsausdrücke: a+b&gt;c-d,x&gt;3/2,'a'+1&lt;c,-i-5\*j==k+1. Da die Ausdrücke selbst Vergleichsausdrücke sein können, sind Verschachtelungen möglich, z. B. a&gt;(b&gt;c),a!=(c==d). Der Wert eines Vergleichsausdrucks ist „wahr“ oder „falsch“, dargestellt durch „1“ und „0“.

**1.  Logische Operatoren und Ausdrücke**

C kennt die logischen Operatoren UND &&, ODER \|\| und NICHT !. UND && und ODER \|\| sind zweistellig und linksassoziativ, NICHT ! ist einstellig und rechtsassoziativ. Die Rangfolge der logischen gegenüber den anderen Operatoren:

Aus der Rangfolge der Operatoren ergibt sich:

a&gt;b && c&gt;d entspricht (a&gt;b) &&   (c&gt;d)

!b==c\|\|d&lt;a entspricht ((!b)==c)\|\|(d&lt;a)

a+b&gt;c && x+y&lt;b entspricht ((a+b)&gt;c) && ((x+y)&lt;b) Auswertung logischer Operationen

Das Ergebnis einer logischen Operation ist wahr oder falsch, dargestellt durch 1 und 0. Es gelten folgende Regeln:

1\.  UND &&: Sind beide Werte wahr, ist das Ergebnis wahr, sonst falsch. Beispiel: 5&gt;0

&& 4&gt;2. Da 5&gt;0 wahr und 4&gt;2 wahr ist, ist das Ergebnis wahr.

2\.  ODER \|\|: Ist einer der beiden Werte wahr, ist das Ergebnis wahr; sind beide falsch, ist es falsch. Beispiel: 5&gt;0\|\|5&gt;8. Da 5&gt;0 wahr ist, ist das Ergebnis wahr.

3\.  NICHT !: Ist der Operand wahr, ist das Ergebnis falsch; ist er falsch, ist das Ergebnis wahr.

Beispiel: !(5&gt;0) ist falsch.

In C wird „wahr“ als „1“ und „falsch“ als „0“ dargestellt. Umgekehrt gilt bei der Prüfung eines Werts: 0 ist falsch, jeder Wert ungleich 0 ist wahr. Da z. B. 5 und 3 ungleich null sind, ist 5&&3 „wahr“ (also 1).

Ein weiteres Beispiel: 5\|\|0 ist „wahr“ (also 1).

Die allgemeine Form eines logischen Ausdrucks ist: Ausdruck – logischer Operator – Ausdruck. Die Ausdrücke können selbst logische Ausdrücke sein, sodass Verschachtelungen entstehen, z. B. (a&&b) &&c. Wegen der Linksassoziativität kann man dafür auch a&&b&&c schreiben. Der Wert eines logischen Ausdrucks ist das Endergebnis der logischen Operationen, dargestellt als „1“ für „wahr“ und „0“ für „falsch“.

**2.  if-Anweisung**

Mit der if-Anweisung lassen sich Verzweigungen bilden: Je nach Bedingung wird entschieden, welcher Programmzweig ausgeführt wird. Die if-Anweisung in C hat drei Grundformen.

1\.  Erste Form: Grundform. if (Ausdruck) Anweisung

Bedeutung: Ist der Ausdruck wahr, wird die folgende Anweisung ausgeführt, sonst nicht.

2\.  Zweite Form: if-else. if(Ausdruck)

Anweisung 1; else Anweisung 2;

Bedeutung: Ist der Ausdruck wahr, wird Anweisung 1 ausgeführt, sonst Anweisung 2.

Zwei ganze Zahlen einlesen und die größere ausgeben. Die Größe von a und b wird mit if-else verglichen. Ist a größer, wird a ausgegeben;

sonst b.

**3.  Dritte Form: if-else-if.**

Die ersten beiden Formen dienen meist für zwei Zweige. Bei mehreren Zweigen wird if-else-if verwendet. Die Grundform ist:

if(Ausdruck 1)

Anweisung 1;

else if(Ausdruck 2)

Anweisung   2;

else if(Ausdruck 3)

Anweisung   3;

…

else if(Ausdruck m)

Anweisung m; else Anweisung n;

Bedeutung: Die Ausdrücke werden der Reihe nach geprüft. Ist einer wahr, wird die zugehörige Anweisung ausgeführt und danach das Programm nach der if-Anweisung fortgesetzt. Sind alle Ausdrücke falsch, wird Anweisung n ausgeführt und dann das Programm fortgesetzt.

**Hinweise zur if-Anweisung:**

(1)   In allen drei Formen folgt auf if ein Ausdruck, meist ein logischer oder ein Vergleichsausdruck. Es kann aber auch ein anderer Ausdruck sein, etwa eine Zuweisung oder sogar eine Variable: if(a=5) Anweisung und if(b) Anweisung sind zulässig. Ist der Wert des Ausdrucks ungleich 0, gilt er als wahr. Bei if(a=5)…; ist der Ausdruck immer ungleich 0, sodass die folgende Anweisung immer ausgeführt wird. Das ist im Programm meist nicht beabsichtigt, aber syntaktisch zulässig.

Ein weiteres Beispiel: if(a=b)

```c
printf("%d",a); else printf("a=0");
```

Bedeutung: b wird a zugewiesen; ist der Wert ungleich 0, wird er ausgegeben, sonst die Zeichenkette „a=0“. Diese Anwendung kommt in Programmen häufig vor.

(2)   In der if-Anweisung muss der Bedingungsausdruck in Klammern stehen; die Anweisung endet mit einem Semikolon.

(3)   In allen drei Formen muss jeweils eine einzelne Anweisung stehen. Sollen mehrere Anweisungen bedingt ausgeführt werden, sind sie mit {} zu einer zusammengesetzten Anweisung zu klammern. Achtung: Nach } steht kein Semikolon.

Beispiel:

```c
if(a>b){ a++; b++;
}
else{ a=0;
b=10;
}
```

**4.  Bedingungsoperator und Bedingungsausdruck**

Wird in einer bedingten Anweisung nur eine einzelne Zuweisung ausgeführt, lässt sie sich meist mit einem Bedingungsausdruck formulieren; das vereinfacht das Programm und macht es effizienter.

Der Bedingungsoperator ? : ist dreistellig, d. h. er verknüpft drei Werte. Die allgemeine Form des Bedingungsausdrucks ist:

Ausdruck 1 ? Ausdruck 2: Ausdruck 3

Auswertung: Ist Ausdruck 1 wahr, ist der Wert von Ausdruck 2 der Wert des Bedingungsausdrucks; andernfalls der Wert von Ausdruck 3. Bedingungsausdrücke werden meist in Zuweisungen verwendet, z. B.:

```c
if(a>b) max=a;
else max=b;
```

max=(a&gt;b)?a:b; als Bedingungsausdruck. Bedeutung: Ist a&gt;b wahr, wird a an max zugewiesen, sonst b.

Bei der Verwendung von Bedingungsausdrücken ist Folgendes zu beachten:

1\.  Der Bedingungsoperator hat niedrigeren Rang als Vergleichs- und arithmetische Operatoren, aber höheren als Zuweisungsoperatoren. max=(a&gt;b)?a:b kann daher ohne Klammern als max=a&gt;b?a:b geschrieben werden.

2\.  ? und : bilden ein Paar und dürfen nicht getrennt verwendet werden.

3\.  Der Bedingungsoperator ist rechtsassoziativ.
