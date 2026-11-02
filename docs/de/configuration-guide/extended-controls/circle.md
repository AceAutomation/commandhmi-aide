# Dynamischer Kreis

Ein dynamischer Kreis ist eine Grafik im Bild, die sich entlang einer Bahn bewegt und ihre Größe ändert. Bewegung und Größe werden durch den Wert der Überwachungsadresse bestimmt. Objekt hinzufügen und Eigenschaften ändern:

Wählen Sie das Symbol Dynamischer Kreis <img src="../../../configuration-guide/extended-controls/circle.files/image002.jpg" width="32" /> in der Werkzeugleiste, wie in Abbildung 4-56:

Abbildung 4-56    Dialogfeld Dynamischer Kreis

Der dynamische Kreis liest drei Adresswerte: die X- und Y-Koordinate des Mittelpunkts und den Radius. Wie diese drei Adressen gelesen werden, hängt vom gewählten Datentyp ab.

• Steuerung:

• Mittelpunkt: Der Kreis bewegt sich mit der Position des Mittelpunkts, der Radius bleibt gleich.

• Radius: Nur der Radius ändert sich, die Position bleibt gleich.

• Mittelpunkt & Radius: Der Radius folgt dem Wert der Überwachungsadresse für den Radius, der Mittelpunkt den Werten für die X- und Y-Koordinate.

• Transparenz: Transparenz der Hintergrundfarbe des dynamischen Kreises.

<span id="OLE_LINK564"></span><span id="OLE_LINK565"></span>• Gefüllt:

Ohne „Gefüllt“ ist der Kreis leer, ohne Hintergrundfarbe. Andernfalls ist er gefüllt; die Hintergrundfarbe ist über die entsprechende Option änderbar.

• Rahmen

Ohne diese Option hat der Kreis keine Randlinie, deren Farbe dann nicht änderbar ist. Andernfalls hat der Kreis eine Randlinie, deren Farbe über die Option „Rahmenfarbe“ geändert wird.

Beispiel:

Wählen Sie den Datentyp „16-Bit Ganzzahl“; gemäß dem Adressformat der jeweiligen SPS werden drei aufeinanderfolgende Werte gelesen: X-Koordinate, Y-Koordinate des Mittelpunkts und Radius. Bei Überwachungsadresse LW1 <span id="OLE_LINK548"></span><span id="OLE_LINK549"></span>werden LW1, LW2 und LW3 gelesen, mit folgender Bedeutung:

LW1 ist die X-Koordinate des Mittelpunkts.

<span id="OLE_LINK552"></span><span id="OLE_LINK553"></span>         LW2 ist die Y-Koordinate des Mittelpunkts.

LW3 ist der Radius des Kreises.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Unabhängig davon, ob „Mittelpunkt“ oder „Radius“ gewählt ist, liest das HMI immer die drei Adressen mit derselben Bedeutung. Ist z. B. „Radius“ gewählt und die Überwachungsadresse LW1, steuert weiterhin nur LW3 den Radius.

Bei Datentyp „32-Bit Ganzzahl“ und Überwachungsadresse LW1 werden folgende Adressen gelesen, mit folgender Bedeutung:

<span id="OLE_LINK550"></span><span id="OLE_LINK551"></span>LW1 ist die X-Koordinate des Mittelpunkts.

LW3 ist die Y-Koordinate des Mittelpunkts.

LW5 ist der Radius des Kreises.

Bei Datentyp „32-Bit Ganzzahl“ werden gemäß dem Adressformat der jeweiligen SPS ab der Überwachungsadresse im Abstand von 2 die drei Werte für X-Koordinate, Y-Koordinate des Mittelpunkts und Radius gelesen.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.
