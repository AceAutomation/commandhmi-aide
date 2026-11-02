# Numerische Anzeige

Die numerische Anzeige ist ein häufig verwendetes Objekt, das Werte aus Datenregistern der SPS oder anderer verbundener Geräte anzeigt, z. B. Drehzahl, Strom oder Druck.

Wählen Sie das Symbol <img src="../../../configuration-guide/basic-control/numerics-display.files/image002.jpg" width="30" /> in der Werkzeugleiste; es öffnet sich ein Dialogfeld, wie in Abbildung 4-91:

Abbildung 4-91 Dialogfeld Numerische Anzeige

In diesem Dialogfeld legen Sie die Darstellung des Werts aus dem Datenregister der SPS oder des Geräts fest, z. B. Stellenzahl, Nachkommastellen, Schriftgröße, Farbe und Ausrichtung des Textes.

• Datentyp: Je nach Wert der überwachten Registeradresse kann der Benutzer verschiedene Datentypen wählen.

• Anzeigetyp: Je nach Projektanforderung kann der Benutzer verschiedene Anzeigetypen wählen.

• Überwachungsadresse: Leseadresse. Das Objekt zeigt Daten an; die Überwachungsadresse ist die Adresse des Datenregisters in der SPS oder im Gerät, das die anzuzeigenden Daten enthält.

• Nachkommastellen: Anzahl der angezeigten Nachkommastellen.

• Schriftart: Normale Schrift oder Digitalschrift.

• Schriftgröße: Größe der angezeigten Schrift nach Bedarf.

• Ausrichtung: Standard ist „Mitte“.

• Links: Der Wert wird im linken Teil des Anzeigebereichs dargestellt.

• Mitte: Der Wert wird in der Mitte des Anzeigebereichs dargestellt.

• Rechts: Der Wert wird im rechten Teil des Anzeigebereichs dargestellt.

• Füllung: Standard ist „Nullunterdrückung“.

• Nullunterdrückung: Führende Nullen werden nicht angezeigt. <span id="OLE_LINK668"></span><span id="OLE_LINK669"></span>Ist der Wert der Überwachungsadresse 00123 (16-Bit positive Ganzzahl), wird 123 angezeigt.

• Führende Nullen: Führende Nullen werden angezeigt. Ist der Wert der Überwachungsadresse 00123 (16-Bit positive Ganzzahl), wird 00123 angezeigt.

• Führende Leerzeichen: Statt führender Nullen werden Leerzeichen angezeigt. Ist der Wert der Überwachungsadresse 00123 (16-Bit positive Ganzzahl), wird   123 angezeigt.

• Textfarbe: Schriftfarbe der angezeigten Daten;

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Hinweis: Form, Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster siehe Objekt „Bit-Taste“.

Hinweis: <span id="OLE_LINK678"></span><span id="OLE_LINK679"></span>Ein Doppelklick auf das Anzeigefeld öffnet Inhalt und Eigenschaften zur Bearbeitung. Im Betrieb auf dem HMI erscheint eine Bildschirmtastatur zur Dateneingabe.

Hinweis: <span id="OLE_LINK684"></span><span id="OLE_LINK685"></span>Die Zahl der Nachkommastellen beeinflusst die Anzeige. Bei den Datentypen 16/32-Bit positive Ganzzahl und 16/32-Bit Ganzzahl wird der Dezimalpunkt des gelesenen Werts um die eingestellte Stellenzahl verschoben: Bei Wert 212 und 2 Nachkommastellen wird 2.12 angezeigt. Beim Datentyp 32-Bit-Gleitkommazahl wird nichts verschoben, sondern nur die Nachkommastellen begrenzt: Bei Wert 2.123 und 2 Nachkommastellen wird 2.12 angezeigt.

Hinweis: Die Gesamtstellenzahl ist die Summe aus Vor- und Nachkommastellen. Hat der Ganzzahlanteil des Werts mehr Stellen als vorgesehen, wird er in voller Länge angezeigt. Beispiel: Wert 2123, Länge 2, 1 Nachkommastelle: Angezeigt wird 212.3.

Die Seite „Erweitert“ der numerischen Anzeige bietet leistungsfähige Funktionen wie Skalierung und Bereichsanzeige, wie in Abbildung 4-92:

<img src="../../../configuration-guide/basic-control/numerics-display.files/image005.jpg" width="675" />

Abbildung 4-92    Seite „Erweitert“ der numerischen Anzeige

• Skalierung: Ist diese Option aktiviert, zeigt das Objekt an: Wert der Überwachungs-(Lese-)adresse × Verstärkung + Offset

<span id="OLE_LINK696"></span><span id="OLE_LINK697"></span>• Bereich anzeigen: Ist diese Option aktiviert, kann der Benutzer untere und obere Grenzwerte sowie die Hintergrundfarben für unter- und oberhalb festlegen. Der vom Objekt überwachte (gelesene) Wert wird je nach Grenzwerten in unterschiedlichen Farben dargestellt.

• Variabler Bereich: Die Werte „Untere Grenze“ und „Obere Grenze“ ändern sich dynamisch je nach der vom Benutzer angegebenen Adresse

• Untere Grenze: Untergrenze der Anzeige. Liegt der angezeigte Wert darunter, wird die Hintergrundfarbe „Unterer Bereich“ verwendet.

• Obere Grenze: Obergrenze der Anzeige. Liegt der angezeigte Wert darüber, wird die Hintergrundfarbe „Oberer Bereich“ verwendet.

Beispiel: Hintergrund- und Textfarbe sind auf der Seite „Allgemein“ eingestellt, die Farben der Bereichsanzeige wie in Abbildung 4-93:

<img src="../../../configuration-guide/basic-control/numerics-display.files/image006.jpg" width="673" />

<img src="../../../configuration-guide/basic-control/numerics-display.files/image007.jpg" width="349" />

Abbildung 4-93 Einstellungen der Bereichsanzeige

Ändert sich der Wert der überwachten Adresse, ändern sich Text und Hintergrund der numerischen Anzeige entsprechend, wie in Abbildung 4-94:

<img src="../../../configuration-guide/basic-control/samdra93.gif" width="508" />

Abbildung 4-94    Beispiel einer numerischen Anzeige

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Hinweis: Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.

Hinweis: <span id="OLE_LINK682"></span><span id="OLE_LINK683"></span>Bei Datentyp 32 Bit belegt die Adresse 2 Worte. Wird z. B. in ein Datenregister einer SIEMENS-SPS an V10 geschrieben, sind die Register V10 und V11 belegt; überwacht der Benutzer V11 zusätzlich mit einem anderen Objekt, entsteht ein Fehler. Achten Sie bei 32-Bit-Datentypen auf Daten- und Adressfehler.

Klicken Sie nach den Einstellungen auf „OK“, um das Objekt in den Ansichtsbereich (das Bild) einzufügen
