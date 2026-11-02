# Mehrzustandslampe

Die Mehrzustandslampe zeigt je nach Wert der Überwachungsadresse verschiedene Zustände an, höchstens 32.

Klicken Sie auf das Symbol Mehrzustandslampe <img src="../../../configuration-guide/basic-control/multiple-lamp.files/image002.jpg" width="28" /> in der Werkzeugleiste, um das Dialogfeld in Abbildung 4-83 zu öffnen.

Abbildung 4-83    Dialogfeld Mehrzustandslampe

1\. Allgemein:

• Zustand: Der Benutzer kann den Zustand wählen und für jeden Zustand Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster des Objekts ändern

• Zustandstyp: (angenommen, der vom Benutzer eingegebene Wert ist n)

• Wert: Der geschriebene Wert liegt zwischen null und der Gesamtzahl der Zustände minus 1.

• Registerbit: Der geschriebene Wert ist 2 hoch n.

E.g.:

<span id="OLE_LINK657"></span><span id="OLE_LINK511"></span><span id="OLE_LINK510"></span>Die Überwachungs-(Lese-)adresse ist LW3, die Gesamtzahl der Zustände 8. Klicken Sie auf OK, um das Objekt in das Bild einzufügen; fügen Sie dann eine numerische Eingabe mit Schreib- und Überwachungsadresse LW3 hinzu und speichern Sie das Projekt.

In der Simulation oder auf dem Bild tippt der Benutzer die numerische Eingabe an und gibt über die Tastatur einen Zustandswert ein. Bei Eingabe von 2 ist der Wert der Überwachungs-(Lese-)adresse 1, und das Objekt zeigt den Text des Zustands 1 (den Text des Zustands 1 auf der Seite „Text“); entsprechend zeigt es bei LW3 = 8 den Text des Zustands 3. Bei LW3 = 3 wechselt die Mehrzustandslampe in keinen Zustand.

• Benutzerdefinierte Zustandswerte: Bei Aktivierung dieser Option erscheint die Schaltfläche „Defined status value“. Ein Klick darauf öffnet das Dialogfeld „Benutzerdefinierte Zustandswerte“, wie in Abbildung 4-84:

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image004.jpg" width="333" />

Abbildung 4-84    Dialogfeld benutzerdefinierte Zustandswerte

In diesem Dialogfeld enthält die Spalte „S \#“ den Zustand; der ausgewählte Wert gibt den Wert des Zustands an. Per Doppelklick auf einen Wert geben Sie den gewünschten Wert für den aktuellen Zustand ein.

Beispiel: Die Überwachungs-(Lese-)adresse ist LW3, die Gesamtzahl der Zustände 8. Klicken Sie auf OK, um das Objekt in das Bild einzufügen; fügen Sie dann eine numerische Eingabe mit Schreib- und Überwachungsadresse LW3 hinzu und speichern Sie das Projekt.

In der Simulation oder auf dem Bild tippt der Benutzer die numerische Eingabe an und gibt über die Tastatur einen Zustandswert ein. Bei Eingabe von 1 ist der Wert der Überwachungsadresse 1, und das Objekt zeigt den Text des Zustands 1 (den Text des Zustands 1 auf der Seite „Text“); entsprechend zeigt es bei LW3 = 33 den Text des Zustands 2. Bei LW3 = 2 wechselt die Mehrzustandslampe in keinen Zustand.

• Datentyp: Datentyp der Schreib- und Überwachungs-(Lese-)adresse

• Überwachungsadresse: Leseadresse, deren Wert gelesen wird und den vom Benutzer festgelegten aktuellen Zustand des Objekts bestimmt.

• Gesamtzahl der Zustände: Der Benutzer kann die Anzahl der Zustände nach Bedarf festlegen, höchstens 32, also Zustand 0 bis 31.

Beispiel: Datentyp 16-Bit positive Ganzzahl, 32 Zustände. Ist der Wert der Überwachungsadresse 0, zeigt die Mehrzustandslampe Text und Grafik des Zustands 0; bei 5 Text und Grafik des Zustands 5. Bei 60 zeigt sie weiterhin Zustand 31 an, da es höchstens 32 Zustände gibt.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Hinweis: Form, Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster siehe Objekt „Bit-Taste“.

Hinweis: Bei Datentyp 32 Bit belegt die Adresse der Mehrzustandslampe 2 Worte. <span id="OLE_LINK673"></span><span id="OLE_LINK672"></span>Wird z. B. in ein Datenregister einer SIEMENS-SPS an V10 geschrieben, sind die Register V10 und V11 belegt; überwacht der Benutzer V11 zusätzlich mit einem anderen Objekt, entsteht ein Fehler. Achten Sie bei 32-Bit-Datentypen auf Daten- und Adressfehler.

Hinweis: Der Datentyp muss zu den anzuzeigenden Daten passen.

2\. Text:

Klicken Sie im Eigenschaftsdialog der Mehrzustandslampe auf die Registerkarte „Text“, um die Texteinstellungen anzuzeigen, wie in Abbildung 4-85:

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image006.jpg" width="675" />

Abbildung 4-85 Seite „Text“ der Mehrzustandslampe

Alle Sprachen verwenden den Text der ersten Sprache: Diese Option betrifft die Mehrsprachigkeit, d. h. wenn unter „Sprache“ im Projektmanager mehr als eine Sprache eingestellt ist; der Text des Objekts ändert sich dann beim Sprachwechsel nicht.

<span id="OLE_LINK737"></span><span id="OLE_LINK736"></span>• Sprache: Diese Option betrifft die Mehrsprachigkeit. Für jede Sprache können Sie für die verschiedenen Zustände eigene Texte eingeben. (Wählen Sie bei einer Funktionstaste die Option „Sprache wechseln“ und die Zielsprache; beim Antippen in der Simulation oder auf dem Bild werden alle Objekte mit Text in die gewählte Sprache umgeschaltet.) Textinhalt, Schriftart und Schriftgröße können je Sprache verschieden sein, Farbe, Zeichenabstand und Position sind gleich.

• Schriftart: Schriftart des eingegebenen Textes; je Zustand und je Sprache kann eine andere Schriftart gewählt werden.

• Schriftgröße: Schriftgröße des eingegebenen Textes; je Zustand und je Sprache kann eine andere Schriftgröße gewählt werden.

• Farbe, Zeichenabstand, Position: Farbe, Zeichenabstand und Ausrichtung des gewählten Textes. Ist im Projektmanager mehr als eine Sprache eingestellt und wählen Sie auf der Seite „Text“ eine andere als Sprache 1, sind diese drei Einstellungen wirkungslos, da sie von Sprache 1 übernommen werden.

3\. Grafik:

Klicken Sie im Eigenschaftsdialog der Mehrzustandslampe auf die Registerkarte „Grafik“, um die Einstellungen in Abbildung 4-86 anzuzeigen.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image007.jpg" width="675" />

Abbildung 4-86 Seite „Grafik“ der Mehrzustandslampe

Auf dieser Seite werden den Zuständen Grafiken zugeordnet. Standardmäßig hat kein Zustand eine Grafik; dies kann nach Bedarf geändert werden.

• Vorgehen: Wählen Sie in der Liste den Eintrag, dessen Grafik geändert werden soll, und wählen Sie eine Grafik aus der Systembibliothek oder aus einem Windows-Verzeichnis. Beim Anklicken der verschiedenen Zustände wird darunter die jeweilige Grafik geladen. Zusätzlich kann der Benutzer festlegen, ob die Grafik an das Objekt angepasst wird; wenn nicht, lassen sich Rand und Position anpassen, um die Darstellung zu verbessern.

• An Objekt anpassen: Ist diese Option aktiviert, hat die Grafik die Größe des Objekts auf der Seite „Allgemein“, und die Optionen Rand und Position werden ausgeblendet; andernfalls werden sie angezeigt.

Beim Import einer Grafik aus einer externen Datei steht die Option „Transparent“ zur Verfügung, mit der eine bestimmte Farbe transparent geschaltet wird

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Hinweis: Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.

Klicken Sie nach allen Einstellungen auf „OK“ und fügen Sie das Objekt in das Bild ein
