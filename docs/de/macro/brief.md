# Zusammenfassung

**1.  Datentypen in C**

Grundtypen, zusammengesetzte Typen, Zeigertypen und void

**2.  Einteilung und Merkmale der Grundtypen**

|                   |        |                                         |
|-------------------|--------|-----------------------------------------|
| Typbezeichner    | Byte   | Wertebereich                            |
| char              | 1      | C-Zeichensatz                         |
| int               | 4      | -214783648～214783647                   |
| short int         | 4      | -214783648～214783647                   |
| long int          | 8      | -922337203685477808～922337203685477807 |
| unsigned          | 4      | 0～4294967295                           |
| unsigned long     | 8      | 0～1844744073709551615                  |
| float             | 4      | 3/4E-38～3/4E+38                        |
| double            | 8      | 1/7E-308～1/7E+308                      |

**3.  Konstantensuffixe**

L oder l für long int

U oder u für unsigned

F oder f für float

**4.  Konstantentypen**

Int, long int, unsigned, float, char, Zeichenkette, symbolische Konstante und Escape-Sequenz

**5.  Typumwandlung**

Automatische Umwandlung

Bei gemischten Operationen mit Daten unterschiedlicher Typen wandelt das System automatisch vom kürzeren in den längeren Typ um. Auch bei Zuweisungen zwischen unterschiedlichen Typen wird automatisch umgewandelt, und zwar in den Typ der linken Seite.

Erzwungene Umwandlung

Sie erfolgt mit dem Typumwandlungsoperator (Cast).

**6.  Rangfolge und Assoziativität der Operatoren**

Im Allgemeinen haben einstellige Operatoren hohen und Zuweisungsoperatoren niedrigen Rang; arithmetische Operatoren haben höheren Rang als Vergleichs- und logische Operatoren. Die meisten Operatoren sind linksassoziativ; rechtsassoziativ sind die einstelligen Operatoren, der dreistellige Operator und die Zuweisung.

**7.  Ausdrücke**

Ein Ausdruck verknüpft Konstanten, Variablen und Funktionen mit Operatoren. Jeder Ausdruck hat einen Wert und einen Typ. Die Auswertung erfolgt in der durch Rangfolge und Assoziativität der Operatoren festgelegten Reihenfolge.

**8.  Arrays**

1\.  Das Array ist die häufigste Datenstruktur in der Programmierung. Es gibt numerische Arrays (int-, float-Arrays), Zeichen-Arrays sowie die später beschriebenen Zeiger- und Struktur-Arrays.

2\.  Arrays können ein-, zwei- oder mehrdimensional sein.

3\.  Die Deklaration eines Arrays besteht aus Typbezeichner, Arrayname und Array-Länge (Anzahl der Elemente). Array-Elemente heißen auch indizierte Variablen; der Array-Typ ist der Typ ihrer Werte.

4\.  Arrays können auf drei Arten belegt werden: durch Initialisierung, dynamisch über Eingabefunktionen und durch Zuweisungen. Numerische Arrays können nicht als Ganzes zugewiesen, ein- oder ausgegeben werden, sondern nur Element für Element in einer Schleife.
