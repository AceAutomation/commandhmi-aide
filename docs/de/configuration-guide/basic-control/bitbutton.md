# Bit-Taste

Mit der Bit-Taste wird der Zustand ON/OFF bzw. 1/0 einer Bitadresse des mit dem Touchscreen verbundenen Geräts gesteuert und angezeigt. Die Bit-Taste ist das grundlegendste und am häufigsten verwendete Objekt.

Bit-Taste anlegen:

1\. Klicken Sie auf das Symbol Bit-Taste <img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton263.png" width="30" /> in der Werkzeugleiste, um das Eigenschaftsdialogfeld der Bit-Taste zu öffnen, wie in Abbildung 4-68:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton381.png" width="664" />

Abbildung 4-68 Dialogfeld Bit-Taste

2\. Das Dialogfeld hat vier Seiten: Allgemein, Beschriftung, Erweitert und Sichtbarkeit.

Form (Shape): Mit der Schaltfläche „Shape“ wählen Sie eine Form für das Objekt, wie in Abbildung 4-69

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton600.png" width="472" />

Abbildung 4-69 Dialog zur Formauswahl

• Rahmenfarbe: Bei einer Form mit Rahmen wählen Sie mit dieser Schaltfläche eine andere Rahmenfarbe.

• Vordergrundfarbe: Um die Vordergrundfarbe zu ändern, klicken Sie auf diese Schaltfläche und wählen eine Farbe aus der Farbauswahl. (Die Vordergrundfarbe wirkt nur bei gewähltem Verlaufsmuster.)

• Hintergrundfarbe: Um die Hintergrundfarbe zu ändern, klicken Sie auf die Schaltfläche und wählen eine Farbe aus der Farbauswahl.

• Muster: Die Auswahlliste enthält insgesamt 21 Muster, wie in Abbildung 4-70:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton1213.png" width="662" />

Abbildung 4-70 Form und Muster ändern

• Setzen (Set): Mit der Funktion „Setzen“ wird nach dem Download auf das HMI der Wert der Schreibadresse durch Antippen der Bit-Taste auf 1 gesetzt, d. h. die Schreibadresse des verbundenen Geräts wird auf ON gesetzt und der Zustand 1/ON angezeigt.

• Rücksetzen (Reset): Mit der Funktion „Rücksetzen“ wird nach dem Download auf das HMI der Wert der Schreibadresse durch Antippen der Bit-Taste auf 0 gesetzt, d. h. die Schreibadresse des verbundenen Geräts wird auf OFF gesetzt und der Zustand 0/OFF angezeigt.

• Tippbetrieb (Inching): Hier kann „Drücken = 1“ oder „Drücken = 0“ gewählt werden. Bei „Drücken = 1“ wird nach dem Download auf das HMI die Schreibadresse des verbundenen Geräts beim Drücken der Bit-Taste auf 1/ON gesetzt und der Zustand 1/ON angezeigt; beim Loslassen wird sie auf 0/OFF gesetzt und der Zustand 0/OFF angezeigt. Bei „Drücken = 0“ wird die Schreibadresse beim Drücken auf 0/OFF gesetzt und der Zustand 0/OFF angezeigt; beim Loslassen wird sie auf 1/ON gesetzt und der Zustand 1/ON angezeigt.

• Umschalten (Alternate): Mit der Funktion „Umschalten“ wird nach dem Download auf das HMI bei aktuellem Zustand 0/OFF die Schreibadresse beim Antippen auf 1/ON gesetzt und 1/ON angezeigt; bei aktuellem Zustand 1/ON wird sie beim Antippen auf 0/OFF gesetzt und 0/OFF angezeigt. Der Zustand wechselt mit jeder Berührung.

• Schreibadresse: Klicken Sie auf das Tastatursymbol hinter „Write Address“, um die Adresse einzugeben. CommandHMI stellt je nach verbundenem Gerät die passenden Adresskennungen bereit. Bei der SPS-Serie FX-2N von MITSUBISHI z. B. steht X für Eingänge, Y für Ausgänge, M für Merker, C für Zähler (Schaltzustand), T für Timer (Schaltzustand), D für Datenregister, C \* für Zähler (Zählwert) und T \* für Timer (Zeitwert). Bei der Serie S7-200 von SIEMENS steht I für Eingänge, Q für Ausgänge, M für Merker und V für Datenregister. Siehe Abbildung 4-71:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton3963.png" width="251" />

Abbildung 4-71 Adresseingabe

So kann der aktuelle Zustand der Bit-Taste mit der passenden Adresskennung der SPS oder des verbundenen Geräts in die Adresse geschrieben werden. Im Zustand 0/OFF der Bit-Taste ist der Wert der Schreib- bzw. Anzeigeadresse 0/OFF, im Zustand 1/ON ist er 1/ON.

• Überwachen (Monitor): Bei Aktivierung von „Überwachen“ wird die „Überwachungsadresse“ angezeigt: Die Bit-Taste zeigt dann die Wertänderungen der Überwachungsadresse an. Im Zustand 0/OFF der Bit-Taste ist der Wert der Überwachungsadresse 0/OFF, im Zustand 1/ON ist er 1/ON. Überwachungs- und Schreibadresse können verschieden sein. Bei der Funktion „Setzen“ z. B. setzt das Antippen die Schreibadresse auf 1/ON; ist die Überwachungsadresse jedoch zu diesem Zeitpunkt 0/OFF, zeigt die Bit-Taste weiterhin 0/OFF an. Meist wählt man „Überwachungsadresse gleich Schreibadresse“, um den geschriebenen Zustand direkt anzuzeigen.

• Skript (Macro): Mit „Skript verwenden“ wird eine Skriptliste angezeigt. Der Benutzer kann ein Skript wählen, das beim Drücken der Bit-Taste ausgeführt wird. Nur kompilierte Skripte erscheinen in der Liste.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5308.png" width="130" />

Ist „Überwachen“ nicht aktiviert, ändert sich der Schaltzustand der Taste auch beim Antippen nicht.

**Beschriftung (Mark)**

Auf der Seite „Beschriftung“ wird die Eigenschaft „Text Zustand 0“ angezeigt, wie in Abbildung 4-72:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5512.png" width="664" />

Abbildung 4-72 Seite „Beschriftung“ der Bit-Taste

Die Seite hat ebenfalls vier Bereiche: „Text Zustand 0“, „Text Zustand 1“, „Grafik Zustand 0“ und „Grafik Zustand 1“.

• Text Zustand 0, Text Zustand 1: Ändern Schriftart, Schriftgröße, Rand, Schriftfarbe und Position des Textes für Zustand 0 bzw. 1. CommandHMI bietet auch eine Kopierfunktion, mit der Eigenschaften von einem Zustand auf den anderen übertragen werden – praktisch und zeitsparend.

• Alle Texte in der ersten Sprache: Diese Option betrifft die Mehrsprachigkeit („Sprache“ im Projektmanager). Bei mehr als einer Sprache sorgt sie dafür, dass der Inhalt dieses Objekts beim Sprachwechsel nicht umgeschaltet wird.

• Sprache: Diese Option betrifft die Mehrsprachigkeit. Geben Sie die Inhalte für jede Sprache ein. (Wählen Sie bei einer Funktionstaste die Option „Sprache wechseln“ und die Zielsprache; in der Simulation oder auf dem HMI werden dann alle Objekte mit Text in der gewählten Sprache angezeigt.) Textinhalt, Schriftart und Schriftgröße können je Sprache verschieden sein, Farbe, Zeichenabstand und Position sind gleich

• Schriftart: Schriftart des Textes; je Sprache kann eine andere Schriftart gewählt werden.

• Schriftgröße: Schriftgröße des Textes; je Sprache kann eine andere Schriftgröße gewählt werden.

• Farbe, Rand, Position: Farbe, Rand und Ausrichtung des aktuellen Textes. Bei mehreren Sprachen gelten die Werte der Sprache 1; in den Einstellungen der anderen Sprachen sind sie wirkungslos.

• Grafik Zustand 0, Grafik Zustand 1: Je nach „Grafikquelle“ können für jeden Zustand Grafiken in verschiedenen Formaten hinzugefügt werden. Eine gewählte Grafik wird automatisch auf der Seite „Allgemein“ übernommen. Mit „An Objektgröße anpassen“ erhält die Grafik die Größe des Objekts.

• An Objektgröße anpassen: Ist diese Option aktiviert, erhält die gewählte Grafik die Größe des Objekts; die Optionen Rand und Position werden ausgeblendet.

• Beim Import einer Grafik aus einer externen Datei erscheint die Option „Transparenz“, mit der eine bestimmte Farbe transparent geschaltet wird

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton7699.png" width="130" />

Mit „Blinken“ blinkt die Anzeige im Zustand ON/OFF. Die Standard-Blinkfrequenz ist 1 s. Um sie zu ändern, doppelklicken Sie im Projektmanager auf „HMI-Parametereinstellungen“ und ändern die „Blinkfrequenz“.

Auf der Seite „Erweitert“ werden die erweiterten Eigenschaften angezeigt, wie in Abbildung 4-73

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8062.png" width="660" />

Abbildung 4-73  Seite „Erweitert“ der Bit-Taste

• Bitgesteuert: Ist „Bitgesteuert“ aktiviert und der „Gültige Zustand“ 1, reagiert die Bit-Taste nur dann auf Berührung, wenn das „Steuerbit“ den Wert 1 hat. Ist der „Gültige Zustand“ 0, reagiert sie nur, wenn das „Steuerbit“ 0 ist. Andernfalls ist die Bit-Taste wirkungslos.

• Benutzerebenen-gesteuert: Der Benutzer kann nach Bedarf mehrere Optionen wählen. In der Simulation oder auf dem HMI wird dann geprüft, ob der aktuelle Benutzer die nötige Berechtigung hat.

Beispiel: Auf der Seite „Erweitert“ des Objekts sind unter „Gültige Ebene“ die Optionen 2 und 3 gewählt, und die Benutzerpasswörter in den Touchscreen-Parametern sind wie in Abbildung 4-74 eingestellt:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8900.png" width="692" />

Abbildung 4-74 Benutzerpasswörter in den Touchscreen-Parametern

Ist die Standard-Benutzerebene NULL, ist das Objekt nicht bedienbar; mit der Funktionstaste „Benutzerebene ändern“ lässt sich die Ebene wechseln. Gibt der Benutzer z. B. das Passwort 6666 ein (Benutzerebene 6), hat dieser Benutzer nur Option 1 gewählt, die nicht zu Option 2 oder 3 passt: Das System meldet ein falsches Passwort. Bei Passwort 2222 oder 3333 haben beide Benutzer Option 2, die passt: Das Passwort ist gültig und das Objekt wird bedienbar. Ist die Standard-Benutzerebene Benutzer 2 bis 3, haben beide Ebenen Option 2, und das Objekt ist in der Simulation bzw. im Startbild bedienbar; ist sie Benutzer 6, passt keine Option, und das Objekt ist nicht bedienbar. Die Standardeinstellung zeigt die folgende Abbildung:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton9956.png" width="459" />

Ist „Benutzerebene bei unzureichender Berechtigung ändern“ gewählt, erscheint bei unpassender Ebene ein Anmeldefenster, in dem sich der Benutzer mit einer passenden Ebene erneut anmelden kann, wie unten gezeigt:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton10150.png" width="466" />

In CommandHMI haben nur die Objekte Bit-Taste, Auswahlliste, ASCII-Eingabe, Funktionstaste, ASCII-Tastatureingabe, Multifunktionstaste, Mehrzustandstaste, Rezeptauswahl, Bildwechsel-Taste, Optionsfeld, Schritttaste, Wort-Taste, Schieberegler und numerische Eingabe diese Funktion; ihre Anwendung entspricht der der Bit-Taste.

• Mindestdruckzeit: Wie viele Sekunden das Objekt nach dem Drücken in der Simulation oder auf dem HMI braucht, um zu reagieren.

• Benachrichtigung: Ist das Objekt in der Simulation oder auf dem HMI bedienbar, wird nach dem Antippen und der Eingabe eines Werts über die eingeblendete Tastatur der Zustand (1 oder 0) in die eingestellte Adresse „Benachrichtigungsbit“ geschrieben.

• Benachrichtigungsregister: Ist das Objekt in der Simulation oder auf dem HMI bedienbar, wird nach dem Antippen und der Eingabe eines Werts über die eingeblendete Tastatur dieser Wert in die eingestellte „Benachrichtigungsregister“-Adresse geschrieben.

• Tastenkürzel (Hotkey): Mit dieser Funktion kann eine Ziffer oder ein Zeichen dieselbe Wirkung wie das Drücken auslösen. Bei Eingabe von 1 z. B. wirkt die Taste 1 des Ziffernblocks in der Simulation, auf dem HMI oder über eine externe Tastatur gleich.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11418.png" width="161" />

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11420.png" width="130" />

Die Standard-Benutzerebene ist NULL, die niedrigste Ebene. Der Projektierer kann sie mit der Funktionstaste „Benutzerebene ändern“ und dem entsprechenden Passwort ändern.

Eine wirksame Berührung liegt vor, wenn die Berührung des Objekts tatsächlich etwas bewirkt, z. B. erfolgreiches Setzen, Rücksetzen, Tippen oder Umschalten. Anderes Beispiel: die numerische Eingabe. Beim Antippen erscheint die Tastatur, aber es entsteht noch keine Benachrichtigung, da nichts in die Adresse geschrieben wird. Auch das Verlassen der Tastatur mit ESC erzeugt keine Benachrichtigung. Erst wenn ein Wert zwischen Minimum und Maximum eingegeben und mit ENTER bestätigt wird, erfolgt eine Benachrichtigung.

Auf der Seite „Anzeige“ wird festgelegt, ob das Objekt angezeigt oder ausgeblendet wird, wie in Abbildung 4-75

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12372.png" width="675" />

Abbildung 4-75 Seite „Sichtbarkeit“ der Bit-Taste

• Bitgesteuert: Ist diese Option aktiviert und der „Gültige Zustand“ 1, wird die Bit-Taste nur angezeigt, wenn das Steuerbit 1 ist; ist der „Gültige Zustand“ 0, nur wenn das Steuerbit 0 ist.

• Benutzerebenen-gesteuert: Es gelten dieselben Bedingungen wie bei der Option auf der Seite „Erweitert“; nur wenn sie erfüllt sind, wird die Bit-Taste auf dem Touchscreen angezeigt.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12995.png" width="130" />

Ist keine der beiden Optionen aktiviert, wird das Objekt immer angezeigt.
