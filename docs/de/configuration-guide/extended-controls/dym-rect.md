# Dynamisches Rechteck

Das dynamische Rechteck funktioniert ähnlich wie der dynamische Kreis: Beide zeigen den Zustand der Überwachungsadresse in Echtzeit, indem sie Position oder Größe der Grafik je nach Wert ändern.

Wählen Sie das Symbol Dynamisches Rechteck <img src="../../../configuration-guide/extended-controls/dym-rect.files/image002.jpg" width="34" /> in der Werkzeugleiste, um das Dialogfeld in Abbildung 4-57 zu öffnen.

Abbildung 4-57    Dialogfeld Dynamisches Rechteck

Das dynamische Rechteck liest vier Adresswerte: X-Koordinate, Y-Koordinate, Breite und Höhe des Rechtecks. Wie diese vier Adressen gelesen werden, hängt vom gewählten Datentyp ab.

• Linienbreite: Breite der Linie

• Typ: Rechtwinklige, abgeschrägte oder abgerundete Ecken.

• Hinweis: „Typ“ wirkt nur bei einer Linienbreite größer als 1.

Beispiel:

Bei Datentyp „16-Bit Ganzzahl“ und Überwachungsadresse LW1 werden die vier Adressen LW1, LW2, LW3 und LW4 gelesen, mit folgender Bedeutung:

LW1 ist die X-Koordinate <span id="OLE_LINK558"></span><span id="OLE_LINK559"></span>des Rechtecks;

LW2 ist die Y-Koordinate des Rechtecks;

LW3 ist die Breite des Rechtecks;

LW4 ist die Höhe des Rechtecks.

Bei Datentyp „16-Bit Ganzzahl“ werden gemäß dem Adressformat der jeweiligen SPS vier aufeinanderfolgende Werte gelesen: X-Koordinate, Y-Koordinate, Breite und Höhe des Rechtecks.

Bei Datentyp „32-Bit Ganzzahl“ und Überwachungsadresse LW1 werden die Adressen LW1, LW3, LW5 und LW7 gelesen.

LW1 ist die X-Koordinate des Rechtecks;

LW3 ist die Y-Koordinate des Rechtecks;

LW5 ist die Breite des Rechtecks;

LW7 ist die Höhe des Rechtecks;

Bei Datentyp „32-Bit Ganzzahl“ werden gemäß dem Adressformat der jeweiligen SPS ab der Überwachungsadresse im Abstand von 2 die vier Werte für X-Koordinate, Y-Koordinate, Breite und Höhe des Rechtecks gelesen.

**Steuerung:**

• Position: Höhe und Breite des Rechtecks bleiben gleich; die Position folgt den Werten der Überwachungsadressen für die X- und Y-Koordinate.

• Größe: Höhe und Breite des Rechtecks ändern sich bezogen auf einen der vier folgenden Fixpunkte; die Position bleibt gleich.

• Oben links: <span id="OLE_LINK562"></span><span id="OLE_LINK563"></span>Der Fixpunkt liegt in der oberen linken Ecke; das Rechteck wächst nach rechts unten.

• Oben rechts: Der Fixpunkt liegt in der oberen rechten Ecke; das Rechteck wächst nach links unten.

• Unten links: Der Fixpunkt liegt in der unteren linken Ecke; das Rechteck wächst nach rechts oben.

• Unten rechts: Der Fixpunkt liegt in der unteren rechten Ecke; das Rechteck wächst nach links oben.

**Gefüllt:**

Ohne „Gefüllt“ ist das Rechteck leer, ohne Hintergrundfarbe. Andernfalls ist es gefüllt; die Hintergrundfarbe ist über die entsprechende Option änderbar.

**Rahmen:**

Ohne diese Option hat das Rechteck keine Randlinie, deren Farbe dann nicht änderbar ist. Andernfalls hat es eine Randlinie, deren Farbe über die Option „Rahmenfarbe“ geändert wird.

Transparenz: Transparenz der Hintergrundfarbe des dynamischen Rechtecks.

<span id="OLE_LINK570"></span><span id="OLE_LINK571"></span><img src="../../../configuration-guide/extended-controls/dym-rect.files/image004.jpg" width="130" />

Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.
