# Historisches Trenddiagramm

• Übersicht: Dieses Trenddiagramm arbeitet mit dem „[Historischen Datensammler](../../setting/history-data.md)“ im Projektmanager zusammen und zeigt die Werte der dort erfassten Daten an.

• Übersicht XY-Trenddiagramm:

Dynamische, fortlaufende Anzeige veränderlicher Werte.

Darstellung mehrerer Referenzkurven: Zeit auf der X-Achse, Adresswert auf der Y-Achse, um den Verlauf eines Werts über einen Zeitraum genau und anschaulich zu beurteilen.

Bis zu 8 Kurven (Liniendiagramm) können angezeigt werden.

• Trenddiagramm hinzufügen und Eigenschaften ändern:

1.Wählen Sie das Symbol Trend <img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image002.jpg" width="34" /> in der Werkzeugleiste; es erscheint das Eigenschaftsdialogfeld des historischen Trends, wie in Abbildung 4-53:

Abbildung 4-53    Seite „Allgemein“ des historischen Trends

• Hintergrundfarbe: Hintergrundfarbe des Trenddiagramms. Die Änderung ist erst nach einem Klick auf „OK“ sichtbar.

• Transparenz: Transparenz der Hintergrundfarbe.

• Datenerfassung: Standardmäßig aus dem „Historischen Datensammler“ des Projektmanagers. Da CommandHMI mehrere Gruppen historischer Daten unterstützt, kann der Projektierer hier die zu verwendende Gruppe wählen. Siehe unten:

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image004.jpg" width="774" />

• Anzahl der Kurven: Anzahl der angezeigten Kurven, höchstens 8.

• Hintergrundfarbe: Farbe der Kurve (des Stifts).

• Steueradresse verwenden: Legt fest, ob eine Steueradresse verwendet wird. Sie belegt 28 Offsets und steuert die Anzeige jeder Kurve, Maximal- und Minimalwert, Endzeit, Zeitraum (Minuten), Maximal- und Minimalwert der Y-Achse, die Anzeige der Y-Achse und die Rückkehr in den Ausgangszustand.

|                |                                                                                                         |
|----------------|---------------------------------------------------------------------------------------------------------|
| Adress-Offset | Gesteuerte Größe                                                                                        |
| 0              | Gesamtzahl der angezeigten Kurven                                                                       |
| 1              | <span id="OLE_LINK534"></span><span id="OLE_LINK533"></span>Kurve 1 anzeigen                            |
| 2              | Kurve 2 anzeigen                                                                                        |
| 3              | Kurve 3 anzeigen                                                                                        |
| 4              | Kurve 4 anzeigen                                                                                        |
| 5              | Kurve 5 anzeigen                                                                                        |
| 6              | Kurve 6 anzeigen                                                                                        |
| 7              | Kurve 7 anzeigen                                                                                        |
| 8              | Kurve 8 anzeigen                                                                                        |
| 9              | Maximalwert der Y-Achse                                                                                 |
| 10             |                                                                                                         |
| 11             | Minimalwert der Y-Achse                                                                                 |
| 12             |                                                                                                         |
| 13             | 0: Standard-Maximal- und Minimalwert verwenden; 1: Ober- und Untergrenze verwenden                       |
| 14             | Startzeit der Abfrage                                                                                   |
| 15             |                                                                                                         |
| 16             |                                                                                                         |
| 17             |                                                                                                         |
| 18             |                                                                                                         |
| 19             |                                                                                                         |
| 20             | Endzeit der Abfrage                                                                                     |
| 21             |                                                                                                         |
| 22             |                                                                                                         |
| 23             |                                                                                                         |
| 24             |                                                                                                         |
| 25             |                                                                                                         |
| 26             | 1: Abfrage starten, danach automatisch zurück auf 0                                                     |
| 27             | 1: Ausgangszustand wiederherstellen, danach automatisch zurück auf 0                                    |

Steueradresse anzeigen:

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/2020-03-23_091355.jpg" width="774" />

**Messlinie**

• Aktiviert: Legt fest, ob die Messlinie (Referenzlinie) aktiviert ist.

• Farbe: Farbe der Messlinie (Referenzlinie).

• Messadresse: Der Wert an der aktuellen Messlinie (Referenzlinie) wird in dieses Register geschrieben.

• Messzeit anzeigen: Der Zeitpunkt an der aktuellen Messlinie (Referenzlinie) wird in dieses Register geschrieben; der Adresstyp ist für eine ASCII-Anzeige gedacht, Gesamtlänge 19 Worte.

• Zeitdifferenz des Messpunkts: Die Differenz zwischen dem Zeitpunkt an der Messlinie (Referenzlinie) und der Startzeit wird in dieses Register geschrieben; der Adresstyp ist für eine numerische Anzeige gedacht, 16-Bit Ganzzahl, in Sekunden.

2\. Die Seite „Kurven“ des historischen Trenddiagramms zeigt Abbildung 4-54.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image005.jpg" width="774" />

Abbildung 4-54    Registerkarte „Stift“ des historischen Trends

Hier werden Maximum, Minimum, Linienart und Farbe jeder Kurve festgelegt. Datenquelle ist der „[Historische Datensammler](../../setting/history-data.md)“ im Projektmanager; jede Kurve kann eine andere Datenquelle haben.

3\. Die Seite „XY-Achse“ des historischen Trenddiagramms zeigt Abbildung 4-55.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image006.jpg" width="774" />

Abbildung 4-55    Registerkarte „XY-Achse“ des historischen Trends

**X-Achse**

• Skala anzeigen: Legt fest, ob die Skala der X-Achse angezeigt wird.

• Y-Raster anzeigen: Legt fest, ob das Raster der Y-Achse angezeigt wird.

• Achsen-/Skalenfarbe: Farbe der X-Achse / Skala.

• Rasterfarbe: Farbe des X-Rasters.

• Hauptteilung: Hauptteilung der X-Achse.

• Unterteilung: Unterteilung der X-Achse.

• Zeit anzeigen: Zeitformat und Schriftgröße der Zeit.

• Zeitbereich: Im Trenddiagramm angezeigter Zeitbereich.

**Y-Achse**

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

• Mehrere Achsen anzeigen: Legt fest, ob mehrere Achsen angezeigt werden.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image007.jpg" width="130" />

Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.
