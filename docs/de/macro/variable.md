# Anfangswerte von Variablen und Typumwandlung

**1.  Initialisierung von Variablen**

Variablen erhalten im Programm häufig einen Anfangswert; das heißt Initialisierung und ist auf mehrere Arten möglich. In der Deklaration hat sie die allgemeine Form:

Typbezeichner Variable 1 = 1, Variable 2 = 2, ……; Beispiel:

```c
int a=b=c=5;
float x=3.2,y=3f,z=0.75;
char ch1='K',ch2='P';
```

Hinweis: Verkettete Zuweisungen sind in der Deklaration nicht erlaubt; a=b=c=5 ist z. B. ungültig.

**2.  Typumwandlung von Variablen**

Der Typ einer Variablen kann auf zwei Arten umgewandelt werden: automatisch oder erzwungen.

Automatische Umwandlung

Werden Daten unterschiedlicher Typen gemeinsam verarbeitet, wandelt der Compiler sie automatisch nach folgenden Regeln um:

1\.  Haben die Daten verschiedene Typen, werden sie zuerst in einen gemeinsamen Typ umgewandelt und dann verarbeitet.

2\.  Umgewandelt wird in den längeren Typ, um die Genauigkeit zu erhalten. Bei int und long z. B. wird int in long umgewandelt.

3\.  Alle Gleitkommaberechnungen erfolgen in double; auch ein Ausdruck nur mit float wird in double umgewandelt.

4\.  char und short werden für Berechnungen in int umgewandelt.

5\.  Bei einer Zuweisung wird der Wert rechts von „=“ in den Typ der linken Seite umgewandelt, falls die Typen verschieden sind. Ist der rechte Typ länger, geht ein Teil der Daten verloren und die Genauigkeit sinkt; der verlorene Teil wird gerundet.

**3.  Erzwungene Typumwandlung**

Die erzwungene Umwandlung erfolgt mit dem Typumwandlungsoperator, allgemeine Form (Typbezeichner) (Ausdruck). Sie wandelt das Ergebnis in den angegebenen Typ um. Beispiele: (float) a wandelt a in float um, (int)(x+y) wandelt das Ergebnis von x+y in eine Ganzzahl um. Dabei ist Folgendes zu beachten:

1\.  Typbezeichner und Ausdruck müssen in Klammern stehen (eine einzelne Variable muss nicht geklammert werden). (int)(x+y)

als (int)x+y geschrieben bedeutet: x in int umwandeln und dann y addieren.

2\.  Ob erzwungen oder automatisch: Es handelt sich nur um eine vorübergehende Umwandlung für die Berechnung; der deklarierte Typ der Variablen ändert sich nicht.
