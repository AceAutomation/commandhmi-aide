# Anweisungen in C

Der ausführbare Teil eines C-Programms besteht aus Anweisungen, die seine Funktionen umsetzen. C-Anweisungen werden in fünf Arten eingeteilt:

1\.  Ausdrucksanweisung

2\.  Steueranweisung

3\.  Zusammengesetzte Anweisung

4\.  Leere Anweisung

**1.  Ausdrucksanweisung**

Eine Ausdrucksanweisung besteht aus einem Ausdruck und einem Semikolon. Allgemeine Form: Ausdruck;. Bei der Ausführung wird der Ausdruck ausgewertet. Beispiel: x=y+z; ist eine Zuweisung; y+z; berechnet eine Summe, ohne das Ergebnis zu speichern, und ist daher sinnlos; i++; erhöht i um 1.

**2.  Steueranweisung**

Steueranweisungen steuern den Programmablauf und bilden die verschiedenen Programmstrukturen.

Sie bestehen aus bestimmten Schlüsselwörtern. C kennt neun Steueranweisungen in drei Gruppen:

(1)   Bedingte Anweisungen: if, switch

(2)   Schleifenanweisungen

do while, while, for

(3)   Sprunganweisungen

break, goto, continue, return

**3.  Leere Anweisung**

Eine Anweisung, die nur aus einem Semikolon besteht, heißt leere Anweisung; sie führt nichts aus. Sie kann als leerer Schleifenrumpf dienen, z. B. while (getchar()!='\n'): Solange das eingegebene Zeichen nicht Enter ist, wird erneut eingelesen. Der Schleifenrumpf ist hier eine leere Anweisung.

**4.  Zuweisung**

Eine Zuweisung besteht aus einem Zuweisungsausdruck und einem Semikolon. Allgemeine Form: Variable = Ausdruck. Funktion und Eigenschaften entsprechen denen des Zuweisungsausdrucks. Sie ist eine der häufigsten Anweisungen. Dabei ist Folgendes zu beachten:

1\.  Da der Ausdruck rechts von „=“ selbst eine Zuweisung sein kann, ist die Form Variable=(Variable=Ausdruck); zulässig und bildet eine verschachtelte Zuweisung. Ausgeschrieben: Variable=Variable=…=Ausdruck;

Beispiel:

```c
a=b=c=d=e=5; according to the right associativity of assignment operator, it is equivalent to: e=5 actually;
d=e; c=d; b=c; a=b;
```

2\.  Unterscheiden Sie zwischen der Initialisierung einer Variablen in der Deklaration und der Zuweisung.

Die Initialisierung ist Teil der Deklaration: Eine initialisierte Variable wird von den anderen Variablen durch ein Komma getrennt, eine Zuweisung endet dagegen mit einem Semikolon.

3\.  In einer Deklaration dürfen mehrere Variablen nicht verkettet initialisiert werden. int a=b=c=5 ist z. B. falsch und muss int a=5,b=5,c=5 lauten. Zuweisungen dürfen dagegen verkettet werden.

4\.  Unterscheiden Sie zwischen Zuweisungsausdruck und Zuweisung. Ein Zuweisungsausdruck ist ein Ausdruck und kann überall stehen, wo ein Ausdruck erlaubt ist; eine Zuweisung nicht.

Diese Anweisung ist zulässig: if((x=y+5)&gt;0) z=x; Bedeutung: Ist x=y+5 größer als 0, dann z=x.

Diese Anweisung ist unzulässig: if((x=y+5;)&gt;0) z=x; da x=y+5; eine Anweisung ist und nicht in einem Ausdruck stehen darf.
