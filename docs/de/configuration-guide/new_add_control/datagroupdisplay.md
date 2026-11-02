# Datengruppenanzeige

Datengruppenanzeige: Eine Datengruppe (oder ein Datenblock) umfasst die Daten aufeinanderfolgender Adressen, z. B. LW12, LW13, LW14, LW15 usw. Das Objekt zeigt den Inhalt mehrerer Datengruppen gleichzeitig an, z. B. die Gruppen LW12 bis LW15 und RWI12 bis RWI15, sodass die Register beobachtet und verglichen werden können. Für mehrere Datengruppen lassen sich Referenzkurven zeichnen: Punktnummer auf der waagerechten Achse, Wert jeder Adresse auf der senkrechten Achse, um den Verlauf eines Werts über einen Zeitraum genau und anschaulich zu beurteilen. Bis zu 8 Kurven (Liniendiagramm) können angezeigt werden.

Das Symbol in der Werkzeugleiste ist <img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay756.png" width="31" />; ein Klick darauf öffnet das Dialogfeld in Abbildung 4-122:

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay838.png" width="741" />

Abbildung 4-122 Seite „Allgemein“ der Datengruppenanzeige

• Hintergrundfarbe: Hintergrundfarbe des Diagramms.

• Datentyp: 7 Datentypen stehen zur Auswahl.

• Lese-Triggerbit: Die Kurve bewegt sich nur, wenn die Adresse des Lese-Triggerbits den Wert 1 hat.

• Automatisch zurücksetzen: Ist die „Lese-Triggerbit-Adresse“ 1, wird sie nach dem Loslassen der Maustaste automatisch auf 0 gesetzt.

• Kanalanzahl: Anzahl der Datengruppen und damit der Kurven.

• Aktueller Kanal: Wählen Sie einen Kanal, um dessen \[Steueradresse\] festzulegen.

• Steueradresse: Leseadresse; jeder Kanal hat eine eigene Steueradresse.

Je Kanal kann eine eigene Anfangsadresse eingestellt werden; die Länge des Adressbereichs = Len \* Anzeigepunkte (Len = 1 bei 16-Bit-Daten, Len = 2 bei 32-Bit-Daten).

Beispiel: Anfangsadresse von Kanal 1 LW1, Datentyp 32-Bit Ganzzahl, 4 Anzeigepunkte: Kanal 1 belegt LW1, LW3, LW5, LW7;

• Anzeigepunkte: Anzahl der je Kanal gelesenen Werte.

• Messlinie

• Aktiviert: Legt fest, ob die Messlinie (Referenzlinie) aktiviert ist.

• Farbe: Farbe der Messlinie (Referenzlinie).

• Messadresse: Der Wert an der aktuellen Messlinie wird in dieses Register geschrieben.

• Beispiel

16 Bit, 4 Kanäle, 10 Anzeigepunkte, \[Steueradresse\] LW1 für Kanal 1, LW100 für Kanal 2, LW200 für Kanal 3 und RWI1 für Kanal 4. Dann gilt:

Kurve 1: LW1 bis LW10

Kurve 2: LW100 bis LW109

Kurve 3: LW200 bis LW209

Kurve 4: RWI1 bis RWI10

Bei 32-Bit-Daten und sonst gleichen Einstellungen:

Kurve 1: LW1 bis LW20

Kurve 2: LW100 bis LW119

Kurve 3: LW200 bis LW219

Kurve 4: RWI1 bis RWI20

Bei 32-Bit-Daten und N Datengruppen werden also gemäß den Adressregeln der jeweiligen SPS die Werte im Abstand von 2 gelesen.

• Hintergrundfarbe: Farbe des Kurvenbereichs.

• Lösch-Triggerbit: Beim Wechsel der Adresse von 0 auf 1 (steigende Flanke) werden alle Kurven gelöscht; beim Wechsel von 1 auf 0 (fallende Flanke) oder ohne Änderung bleiben sie erhalten.

• Datenpunkt-Markierung: Jede Kurve besteht aus Punkten

• Linienmarkierung: Jede Kurve besteht aus Linien.

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay3263.png" width="130" />

Zur Seite „Sichtbarkeit“ siehe „Bit-Taste“.
