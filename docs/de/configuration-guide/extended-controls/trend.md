# Trenddiagramm

**Übersicht Trenddiagramm:**

<span id="OLE_LINK525"></span><span id="OLE_LINK526"></span>Dynamische, fortlaufende Anzeige veränderlicher Werte.

Darstellung mehrerer Referenzkurven: Zeit auf der waagerechten Achse, Wert auf der senkrechten Achse, um den Verlauf eines Werts über einen Zeitraum genau und anschaulich zu beurteilen.

Bis zu 8 Kurven (Liniendiagramm) können angezeigt werden.

Trenddiagramm hinzufügen:

1. Wählen Sie das Symbol Trenddiagramm <img src="../../../configuration-guide/extended-controls/trend.files/image002.jpg" width="35" /> in der Werkzeugleiste; es erscheint das Eigenschaftsdialogfeld, wie in Abbildung 4-50

Abbildung 4-50    Allgemeine Einstellungen des Trenddiagramms

• Hintergrundfarbe: Hintergrundfarbe des Trenddiagramms. Die Änderung ist erst nach einem Klick auf OK sichtbar.

• Datentyp: 7 Datentypen stehen zur Auswahl.

• Lese-Triggerbit: Die Kurve bewegt sich nur, wenn die Adresse des Lese-Triggerbits den Wert 1 hat.

• Anzahl der Kurven: höchstens 8.

• Lese-Triggerbit automatisch zurücksetzen: Wird an der Leseadresse 1 erkannt, wird sie auf 0 gesetzt.

• Datenpunkte pro Gruppe: <span id="OLE_LINK492"></span><span id="OLE_LINK493"></span>Anzahl der auf der <span id="OLE_LINK494"></span><span id="OLE_LINK495"></span>X-Achse angezeigten Werte.

• Abtastzeit: Abtastfrequenz.

• Leseadresse: Der Wert der Leseadresse ist der Y-Wert jeder Kurve. Je nach Gruppenzahl und Datentyp werden die Adressen fortlaufend (16-Bit-Daten) oder im Abstand (32-Bit-Daten) gelesen.

• Variable Datenpunktzahl: „Datenpunkte pro Gruppe“ wird dynamisch über einen Adresswert festgelegt. Ist die Option aktiviert, ist der Anfangswert der Adresse die eingestellte Zahl der Datenpunkte pro Gruppe.

**Messlinie**

• Aktiviert: Legt fest, ob die Messlinie (Referenzlinie) aktiviert ist.

• Farbe: Farbe der Messlinie (Referenzlinie).

<span id="OLE_LINK527"></span><span id="OLE_LINK528"></span><span id="OLE_LINK543"></span>• Messadresse: Der Wert an der aktuellen Messlinie (Referenzlinie) wird in diese Adresse geschrieben.

• Steueradresse verwenden: Minimal- und Maximalwert der Y-Achse werden dynamisch über die Steueradresse festgelegt. Die Adresse belegt fünf aufeinanderfolgende Offsets: Minimal- und Maximalwert der Y-Skala sowie die Rückkehr in den Ausgangszustand.

|                |                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adress-Offset | Gesteuerte Größe                                                                                                                                                   |
| 0              | Minimalwert, niederwertige 16 Bit                                                                                                                                  |
| 1              | Minimalwert, höherwertige 16 Bit                                                                                                                                   |
| 2              | Maximalwert, niederwertige 16 Bit                                                                                                                                  |
| 3              | Maximalwert, höherwertige 16 Bit                                                                                                                                   |
| 4              | Rückkehr zu den Anfangswerten von Maximum und Minimum. Wert 1: dynamische Änderung; sonst werden die Anfangswerte wiederhergestellt                                |

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

Als Steueradresse sind nur interne Adressen zulässig; Minimal- und Maximalwert belegen je zwei aufeinanderfolgende Wortadressen.

E.g.:

Bei Datentyp 16 Bit und 8 Datengruppen werden, angenommen die eingegebene Adresse ist LW3, 8 aufeinanderfolgende Adresswerte gelesen:

LW3: Wert der Kurve 1

LW4: <span id="OLE_LINK513"></span><span id="OLE_LINK514"></span>Wert der Kurve 2

LW5: <span id="OLE_LINK515"></span><span id="OLE_LINK516"></span>Wert der Kurve 3

LW6: Wert der Kurve 4

LW7: Wert der Kurve 5

LW8: Wert der Kurve 6

LW9: Wert der Kurve 7

LW10: Wert der Kurve 8

Bei 16-Bit-Daten und N Datengruppen werden also gemäß den Adressregeln der jeweiligen SPS N aufeinanderfolgende Adresswerte gelesen.

Bei Datentyp 32 Bit und 5 Datengruppen werden, angenommen die eingegebene Adresse ist LW3, 5 Adresswerte gelesen:

LW3: <span id="OLE_LINK517"></span><span id="OLE_LINK518"></span>Wert der Kurve 1

LW5: Wert der Kurve 2

LW7: Wert der Kurve 3

LW9: Wert der Kurve 4

LW11: Wert der Kurve 5

Bei 32-Bit-Daten und N Datengruppen werden also gemäß den Adressregeln der jeweiligen SPS N Adresswerte im Abstand von 2 gelesen.

• Richtung:

• Von links nach rechts: Die Kurve läuft von links.

• Von rechts nach links: Die Kurve läuft von rechts.

• Hintergrundfarbe: Farbe der Kurve

• Lösch-Triggerbit: Beim Wechsel der Adresse von 0 auf 1 (steigende Flanke) werden alle Kurven gelöscht. Beim Wechsel von 1 auf 0 (fallende Flanke) oder ohne Änderung bleiben die Kurven erhalten.

Die Seite „Kurven“ des Trenddiagramms zeigt Abbildung 4-51: Hier werden Maximum, Minimum, Linienart und Farbe jedes Stifts festgelegt.

<img src="../../../configuration-guide/extended-controls/trend.files/image005.jpg" width="774" />

Abbildung 4-51    Dialogfeld „Stift“ des Trenddiagramms

Der Datentyp auf der Seite „Allgemein“ bestimmt den Typ von Maximum und Minimum hier.

Ist z. B. Maximum oder Minimum eine Gleitkommazahl, muss auf der Seite „Allgemein“ zuerst der Datentyp 32-Bit-Gleitkommazahl gewählt werden; sonst tritt beim Klick auf „OK“ ein Fehler auf.

3\. Die Seite „XY-Achse“ des Trenddiagramms zeigt Abbildung 4-52:

<img src="../../../configuration-guide/extended-controls/trend.files/image006.jpg" width="774" />

Abbildung 4-52    Dialogfeld „XY-Achse“ des Trenddiagramms

• X-Achse

• Skala anzeigen: Legt fest, ob die Skala der X-Achse angezeigt wird.

• Y-Raster anzeigen: Legt fest, ob das Raster der Y-Achse angezeigt wird.

• Achsen-/Skalenfarbe: Farbe der X-Achse / Skala.

• Rasterfarbe: Farbe des X-Rasters.

• Hauptteilung: Hauptteilung der X-Achse.

• Unterteilung: Unterteilung der X-Achse.

Skala anzeigen: Legt fest, ob die Skala der X-Achse angezeigt wird.

• Y-Achse

• Skala anzeigen: Legt fest, ob die Skala der Y-Achse angezeigt wird.

• X-Raster anzeigen: Legt fest, ob das Raster der X-Achse angezeigt wird.

• Achsen-/Skalenfarbe: Farbe der Y-Achse / Skala.

• Rasterfarbe: Farbe des Y-Rasters.

• Hauptteilung: Anzahl der Hauptteilungen der Y-Achse.

• Unterteilung: Anzahl der Unterteilungen der Y-Achse.

• Beschriftung anzeigen: Legt fest, ob die Skalenbeschriftung der Y-Achse angezeigt wird.

• Schriftgröße: Schriftgröße der Y-Skala.

• Minimum: Kleinster Wert der Y-Skala.

• Maximum: Größter Wert der Y-Skala.

• Gesamtstellen: Maximale Stellenzahl der angezeigten Daten.

• Nachkommastellen: Maximale Zahl der Stellen nach dem Dezimalpunkt.

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.
