# Programme mit Schleifen

Die Schleife ist eine wichtige Programmstruktur: Solange eine Bedingung erfüllt ist, wird ein Programmabschnitt wiederholt ausgeführt. Die Bedingung heißt Schleifenbedingung, der wiederholte Abschnitt Schleifenrumpf. C bietet mehrere Schleifenanweisungen für unterschiedliche Schleifenstrukturen.

**1.  while-Anweisung**

Allgemeine Form der while-Anweisung: While (Ausdruck) Anweisung;

Dabei ist der Ausdruck die Schleifenbedingung und die Anweisung der Schleifenrumpf.

Bedeutung: Der Ausdruck wird ausgewertet; ist er wahr (ungleich 0), wird der Schleifenrumpf ausgeführt.

Hinweise zur while-Anweisung:

1\.  Der Ausdruck der while-Anweisung ist meist ein Vergleichs- oder logischer Ausdruck. Solange er wahr (ungleich 0) ist, läuft die Schleife weiter.

2\.  Besteht der Schleifenrumpf aus mehreren Anweisungen, sind sie mit {} zu einer zusammengesetzten Anweisung zu klammern.

3\.  Auf die Schleifenbedingung achten, um Endlosschleifen zu vermeiden.

**2.  do-while-Anweisung**

Allgemeine Form der do-while-Anweisung:

```c
do statement;
while (expression);
```

Dabei ist die Anweisung der Schleifenrumpf und der Ausdruck die Schleifenbedingung. Bedeutung der do-while-Anweisung:

Zuerst wird der Schleifenrumpf einmal ausgeführt, dann der Ausdruck geprüft. Ist er wahr (ungleich 0), läuft die Schleife weiter, sonst endet sie.

Der Unterschied zwischen do-while und while: do-while führt zuerst aus und prüft danach, der Schleifenrumpf wird also mindestens einmal ausgeführt. while prüft zuerst und führt danach aus; ist die Bedingung nicht erfüllt, wird der Rumpf kein einziges Mal ausgeführt.

while- und do-while-Anweisungen lassen sich meist ineinander umschreiben.

In diesem Beispiel wird die Schleifenbedingung zu --n umgeschrieben, sonst wird ein Durchlauf zu viel ausgeführt. Hinweise zur do-while-Anweisung:

1\.  Bei if- und while-Anweisungen steht nach dem Ausdruck kein Semikolon, bei do-while muss der Ausdruck mit einem Semikolon enden.

2\.  do-while-Anweisungen können verschachtelt und mit while-Anweisungen kombiniert werden.

3\.  Besteht der Schleifenrumpf zwischen do und while aus mehreren Anweisungen, sind sie mit {} zu einer zusammengesetzten Anweisung zu klammern.

4\.  Beim Umschreiben zwischen do-while und while die Schleifenbedingung entsprechend anpassen.
