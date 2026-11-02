# Zusammenfassung

1\.  Nach dem Ablauf unterscheidet man drei Grundstrukturen von Programmen: Sequenz, Verzweigung und Schleife.

2\.  Die kleinste Einheit der Programmausführung ist die Anweisung. C kennt fünf Arten von Anweisungen:

(1)   Ausdrucksanweisung: ein beliebiger Ausdruck mit Semikolon. Die häufigste Ausdrucksanweisung ist die Zuweisung.

(2)   Funktionsaufruf: ein Funktionsaufruf mit Semikolon.

(3)   Steueranweisung: steuert den Programmablauf und besteht aus bestimmten Schlüsselwörtern und den nötigen Ausdrücken; dazu gehören bedingte Anweisungen, Schleifen, goto usw.

(4)   Zusammengesetzte Anweisung: mehrere Anweisungen in {}. Sie gilt als einzelne Anweisung und kann überall stehen, wo eine Anweisung erlaubt ist, z. B. als Schleifenrumpf.

(5)   Leere Anweisung: nur ein Semikolon, ohne Wirkung.

3\.  Vergleichs- und logische Ausdrücke sind zwei wichtige Ausdrucksarten, die vor allem für Bedingungen von Verzweigungen und Schleifen verwendet werden.

4\.  C bietet mehrere bedingte Anweisungen für Verzweigungen. (1)   if: hauptsächlich für einfache Auswahl.

(2)   if-else: hauptsächlich für zweifache Auswahl.

(3)   if-else-if und switch: für Mehrfachauswahl. Diese Formen sind meist gegeneinander austauschbar.

5\.  C bietet drei Schleifenanweisungen.

(1)   for: hauptsächlich für Schleifen mit Anfangswert, Schrittweite und fester Anzahl von Durchläufen. (2)   Stehen Anzahl und Abbruchbedingung erst während der Schleife fest, verwendet man while

oder do-while.

(3)   Die drei Schleifenarten können ineinander verschachtelt werden. Schleifen dürfen nebeneinander liegen, sich aber nicht überkreuzen. (4)   Sprunganweisungen können eine Schleife verlassen, aber nicht von außen in einen Schleifenrumpf springen.

(5)   Endlosschleifen vermeiden: Die Schleifenvariable muss während der Ausführung verändert werden, sodass die Schleifenbedingung irgendwann falsch wird und die Schleife endet.

6\.  Übersicht der Anweisungen in C

Name                                Allgemeine Form

Einfache Anweisung                Ausdrucksanweisung; Leere Anweisung                           ;

Bedingte Anweisung          if(Ausdruck)Anweisung;

if(Ausdruck)Anweisung 1; else Anweisung 2;

if(Ausdruck 1)Anweisung 1;   else if(Ausdruck 2) Anweisung 2…else Anweisung n; switch-Anweisung                 switch(Ausdruck){ case Konstante: Anweisung…default: Anweisung;   } Schleifenanweisung                           while-Anweisung

```c
while(expression)statement;
for statement for(expression 1; expression 2; expression 3) statement; break statement break;
continue statement continue;
return statement return(expression);
```
