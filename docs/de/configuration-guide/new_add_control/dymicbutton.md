# Animation

Animation: Die Bewegungsbahn eines Elements wird vorab festgelegt; seine Position auf der Bahn wird über die Daten zweier Register gesteuert, eines für den Zustand und eines für die Position.

Das Symbol in der Werkzeugleiste ist <img src="../../../configuration-guide/new_add_control/dymicbutton.files/image002.jpg" width="28" />. Zeichnen Sie im Bildbereich die Bahnpunkte (Hinweis: höchstens 64 Punkte) und schließen Sie mit einem Rechtsklick ab.

Ein Doppelklick auf das Objekt öffnet das Dialogfeld in Abbildung 4-118:

Abbildung 4-118   Seite „Allgemein“ der Animation

Gesamtzahl der Zustände: Anzahl der Zustände des Elements

Position:

Register: Bei „Register“ werden Zustand und Position des Elements über Registerdaten gesteuert.

Leseadresse: Werden Zustand und Position über Registerdaten bestimmt, muss die Leseadresse richtig eingestellt sein. Ihr Format zeigt folgende Tabelle.

|           |                            |                              |
|-----------|----------------------------|------------------------------|
| Datentyp | Steueradresse Zustand | Steueradresse Position |
| 16-Bit    | Adresse                    | Adresse + 1                  |
| 32-Bit    | Adresse                    | Adresse + 2                  |

Beispiel: Register \[LW100\], Datenformat „16-Bit positive Ganzzahl“: \[LW100\] enthält den Zustand des Elements, \[LW101\] seine Position. Bei \[LW100\] = 2 und \[LW101\] = 1 zeigt das Element Zustand 2 an Position 1, wie in Abbildung 4-119.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image004.gif" width="520" />

Abbildung 4-119

• Takt: Bei „Takt“ wechselt das Element Zustand und Position automatisch. Unter „Automatische Positionssteuerung“ wird festgelegt, wie Zustand und Position wechseln.

• Geschwindigkeit: Geschwindigkeit des Positionswechsels in Einheiten von 0,1 s. Bei 10 rückt das Element jede Sekunde eine Position weiter.

• Zurück: Angenommen, das Element hat vier Positionen 0, 1, 2 und 3. Ohne diese Option springt es nach der letzten Position (3) zur Anfangsposition (0) und wiederholt den Ablauf.

Position 0-&gt; Position 1-&gt; Position 2-&gt; Position 3-&gt; Position 0-&gt; Position 1-&gt; Position 2...

Mit dieser Option läuft das Element nach der letzten Position denselben Weg zurück zur Anfangsposition (0). Die Reihenfolge ist dann:

Position 0-&gt; Position 1-&gt; Position 2-&gt; Position 3-&gt; Position 2-&gt; Position 1-&gt; Position 0...

Zustandswechsel: Art des Zustandswechsels

Zur Wahl stehen „Positionsabhängig“ und „Zeitabhängig“. Bei „Positionsabhängig“ wechselt der Zustand mit der Position.

Bei „Zeitabhängig“ wechseln Position und Zustand gemäß den Punkten im Bild.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image005.jpg" width="484" />

Abbildung 4-120   Automatische Positionssteuerung

**Seite „Profil“:**

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image006.jpg" width="484" />

Größe der Vektorgrafik:

• Breite: Breite des <span id="OLE_LINK520"></span><span id="OLE_LINK521"></span>Grafikobjekts auf der Seite „Allgemein“.

• Höhe: Höhe des Grafikobjekts auf der Seite „Allgemein“.

• Bahn: Durch Auswahl der Bahnpunkte lässt sich deren Position anpassen.

Zu den Seiten „Text“ und „Grafik“ siehe „Mehrzustandslampe“.

<span id="OLE_LINK676"></span><span id="OLE_LINK677"></span>Zur Seite „Sichtbarkeit“ siehe „Bit-Taste“.
