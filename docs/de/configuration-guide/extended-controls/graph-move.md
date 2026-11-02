# Grafikbewegung

Mit dem Objekt „Grafikbewegung“ bewegt sich eine Bibliotheksgrafik oder Grafikdatei in einer bestimmten Richtung über das Bild; die Bewegung wird durch die Werte der zugehörigen Variablen ausgelöst. So entsteht eine Animation im Bild.

Objekt „Grafikbewegung“ hinzufügen und Eigenschaften ändern:

Wählen Sie die Schaltfläche Grafikbewegung <img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move351.png" width="35" /> in der Werkzeugleiste, legen Sie die Eigenschaften im Dialogfeld fest und klicken Sie auf OK, wie in Abbildung 4-61:

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move459.png" width="662" />

Abbildung 4-61 Dialogfeld Grafikbewegung

• Grafikauswahl:

Wählen Sie auf der Seite „Grafiken“ eine Grafik als bewegte Grafik; sie kann auch benutzerdefiniert sein.

• Überwachungsadresse:

Die Überwachungsadresse der Grafikbewegung belegt drei Adressen: für den Zustand, den Wert der X-Achse und den Wert der Y-Achse. Beispiel: Überwachungsadresse LW1 im internen Speicher, Datentyp 16 Bit. (Die Werte von LW1, LW2 und LW3 steuern dann direkt Zustand, Bewegung in X und Bewegung in Y.) Bei Datentyp 32 Bit ist die Adresse des Zustands LW1, die der X-Koordinate LW3 und die der Y-Koordinate LW5.

• Bewegungsart: Die folgenden Beispiele verwenden alle die interne Adresse LW1 als Überwachungsadresse mit Datentyp 16 Bit:

• Waagerecht entlang der X-Achse: Die Grafik bewegt sich nur waagerecht, nicht senkrecht, und nicht unter die Untergrenze bzw. über die Obergrenze der X-Achse. Der Zustand ist der Wert von LW1, LW2 ist die X-Koordinate.

• Senkrecht entlang der Y-Achse: Die Grafik bewegt sich nur senkrecht, nicht waagerecht, und nicht unter die Untergrenze bzw. über die Obergrenze der Y-Achse. Der Zustand ist der Wert von LW1, LW2 ist die Y-Koordinate.

• Waagerecht und senkrecht gleichzeitig: Die Grafik bewegt sich gleichzeitig waagerecht und senkrecht, jeweils innerhalb der Grenzen der X- und der Y-Achse. Der Zustand ist der Wert von LW1, LW2 ist die X-Koordinate und LW3 die Y-Koordinate.

• Proportional waagerecht entlang der X-Achse: Die Grafik bewegt sich nur waagerecht, nicht senkrecht, und nicht unter die Untergrenze bzw. über die Obergrenze der X-Achse. Der Zustand ist der Wert von LW1, LW2 ist die X-Koordinate.

• Proportional senkrecht entlang der Y-Achse: Die Grafik bewegt sich nur senkrecht, nicht waagerecht, und nicht unter die Untergrenze bzw. über die Obergrenze der Y-Achse. Der Zustand ist der Wert von LW1, LW2 ist die X-Koordinate.

• Proportional waagerecht entgegen der X-Achse: Die Grafik bewegt sich nur waagerecht, nicht senkrecht, und nicht unter die Untergrenze bzw. über die Obergrenze der X-Achse. Der Zustand ist der Wert von LW1, LW2 ist die X-Koordinate.

• Proportional senkrecht entgegen der Y-Achse: Die Grafik bewegt sich nur senkrecht, nicht waagerecht, und nicht unter die Untergrenze bzw. über die Obergrenze der Y-Achse. Der Zustand ist der Wert von LW1, LW2 ist die X-Koordinate.

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move3614.png" width="130" />

• Zu den Seiten „Text“ und „Grafik“ siehe Objekt „Mehrzustandslampe“.

• Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.

• Über die Werte der beiden letzten Überwachungsadressen wird die Position der Grafik gesteuert.

• Die maximale Koordinate der X- bzw. Y-Achse entspricht der Bildgröße.
