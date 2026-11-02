# Grundlegende Operatoren und Ausdrücke

**Arten, Rangfolge und Assoziativität der Operatoren**

C bietet sehr viele Operatoren und Ausdrücke, mehr als die meisten Hochsprachen. Gerade diese reichhaltigen Operatoren und Ausdrücke machen C so vollständig; sie sind eines der Hauptmerkmale der Sprache.

Die Operatoren in C haben unterschiedliche Rangfolgen und zudem jeweils eine Assoziativität. In einem Ausdruck richtet sich die Auswertung nicht nur nach der Rangfolge, sondern auch nach der Assoziativität, die bestimmt, ob von links nach rechts oder von rechts nach links ausgewertet wird. Diese Assoziativität gibt es in anderen Hochsprachen nicht; sie macht C komplexer.

Operatorarten

Die Operatoren von C lassen sich wie folgt einteilen:

**1.  Arithmetische Operatoren**

Für Berechnungen: Addition (+), Subtraktion (-), Multiplikation (\*), Division (/) (bzw. Modulo, %), Inkrement (++) und Dekrement (--).

**2.  Vergleichsoperatoren**

Für Vergleiche: größer als (&gt;), kleiner als (&lt;), gleich (==), größer oder gleich (&gt;=), kleiner oder gleich (&lt;=) und ungleich (! =).

**3.  Logische Operatoren**

Für logische Verknüpfungen: UND (&&), ODER (\|\|) und NICHT (!).

**4.  Bitoperatoren**

Die Operanden werden bitweise verarbeitet: bitweises UND (&), bitweises ODER (\|), bitweises NICHT (~), bitweises exklusives ODER (^), Linksschieben (&lt;&lt;) und Rechtsschieben (&gt;&gt;).

**5.  Zuweisungsoperatoren**

Für Zuweisungen: einfache Zuweisung (=), zusammengesetzte arithmetische Zuweisung (+=,-=,\*=, /=, %=)

und zusammengesetzte Bit-Zuweisung (&=,\|=, ^=,&gt;&gt;=,&lt;&lt;=).

**6.  Bedingungsoperator**

Ein dreistelliger Operator für bedingte Auswertung (?:).

**7.  Kommaoperator**

Fasst mehrere Ausdrücke zu einem Ausdruck zusammen (, ).

**8.  Zeigeroperatoren**

Für zwei Operationen: Inhalt (\*) und Adresse (&).

**9.  Größenoperator**

Ermittelt die Größe von Daten (sizeof).

**10. Sonderoperatoren**

Dazu gehören Klammern (), Index \[\] usw.
