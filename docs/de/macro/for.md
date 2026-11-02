# for-Anweisung

Die for-Anweisung ist eine sehr leistungsfähige und häufig verwendete Schleifenanweisung in C. Ihre allgemeine Form ist:

For (Ausdruck 1;Ausdruck 2;Ausdruck 3)

Anweisung;

Ausdruck 1: setzt meist den Anfangswert der Schleifenvariablen, ist also eine Zuweisung. Die Initialisierung kann auch außerhalb der for-Anweisung erfolgen; dann kann der Ausdruck entfallen.

Ausdruck 2: meist die Schleifenbedingung, ein Vergleichs- oder logischer Ausdruck. Ausdruck 3: ändert meist den Wert der Schleifenvariablen, ist also eine Zuweisung.

Jeder der drei Ausdrücke kann ein Kommaausdruck sein, also aus mehreren Ausdrücken bestehen. Alle drei sind optional und können entfallen.

Die „Anweisung“ in der allgemeinen Form ist der Schleifenrumpf. Ablauf der for-Anweisung:

1\.  Zuerst wird Ausdruck 1 ausgewertet.

2\.  Dann wird Ausdruck 2 ausgewertet. Ist er wahr (ungleich 0), wird der Schleifenrumpf einmal ausgeführt; sonst wird die Schleife verlassen.

3\.  Dann wird Ausdruck 3 ausgewertet und zu Schritt 2 zurückgekehrt. Ausdruck 1 wird nur einmal ausgewertet, Ausdruck 2 und 3 eventuell mehrfach. Der Schleifenrumpf kann mehrfach oder gar nicht ausgeführt werden.

Hinweise zur for-Anweisung:

1\.  Jeder Ausdruck der for-Anweisung kann entfallen, die Semikolons müssen aber bleiben. Beispiel:

&lt;1&gt;for(Ausdruck; Ausdruck) ein Ausdruck entfällt

&lt;2&gt;for(Ausdruck; Ausdruck;) ein Ausdruck entfällt

&lt;3&gt;for(;Ausdruck; Ausdruck) alle Ausdrücke entfallen

2\.  Ist die Schleifenvariable bereits initialisiert, kann Ausdruck 1 entfallen, wie in Beispiel 3.27. Entfällt Ausdruck

2 oder 3, kann eine Endlosschleife entstehen; die Schleife muss dann im Schleifenrumpf beendet werden.

3\.  Der Schleifenrumpf kann eine leere Anweisung sein.

```c
#include" stdio.h" void main(){
int n=0;
printf("input a string:\n"); for(;getchar()!='\n';n++); printf("%d",n);
}
```

In diesem Beispiel entfällt Ausdruck 1 der for-Anweisung, und Ausdruck 3 ändert nicht die Schleifenvariable, sondern zählt die eingegebenen Zeichen. Das Zählen, das sonst im Schleifenrumpf stünde, erfolgt im Ausdruck; der Schleifenrumpf ist daher eine leere Anweisung. Achtung: Das Semikolon der leeren Anweisung ist unverzichtbar; fehlt es, wird die folgende printf-Anweisung zum Schleifenrumpf. Umgekehrt darf nach der Klammer der for-Anweisung kein Semikolon stehen, wenn der Schleifenrumpf nicht leer ist, sonst gilt der Rumpf als leer und wird nicht wiederholt. Dies sind häufige Fehler, auf die besonders zu achten ist.
