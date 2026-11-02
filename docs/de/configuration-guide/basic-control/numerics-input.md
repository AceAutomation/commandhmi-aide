# Numerische Eingabe

Die numerische Eingabe ist das am häufigsten verwendete Objekt und in fast jeder Prozesssteuerung unverzichtbar. Sie gibt Werte in Datenregister der SPS oder anderer Geräte ein, zeigt sie an und speichert sie, z. B. Drehzahl, Strom oder Druck.

Numerische Eingabe und numerische Anzeige funktionieren im Wesentlichen gleich; der einzige Unterschied ist, dass die numerische Eingabe Werte in Datenregister der SPS oder anderer Geräte schreiben kann, statt sie nur anzuzeigen.

Numerische Eingabe anlegen:

Wählen Sie das Symbol numerische Eingabe <img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input596.png" width="31" /> in der Werkzeugleiste; es erscheint ein Dialogfeld, wie in Abbildung 4-95.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input665.png" width="662" />

Abbildung 4-95 Dialogfeld Numerische Eingabe

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input705.png" width="130" />

Hinweis: Form, Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster siehe Objekt „Bit-Taste“.

Hinweis: Zu „Ausrichtung“, „Füllung“, „Nachkommastellen“ und „Gesamtstellen“ siehe Objekt „Numerische Anzeige“.

Hinweis: Ein Doppelklick auf das Anzeigefeld öffnet Inhalt und Eigenschaften zur Bearbeitung. Im Betrieb auf dem HMI erscheint eine Bildschirmtastatur zur Dateneingabe, wie in Abbildung 4-96.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1192.png" width="693" />

Abbildung 4-96 Zifferntastatur

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1228.png" width="130" />

Hinweis: Bei Datentyp 32 Bit belegt die Adresse 2 Worte. Wird z. B. in ein Datenregister einer SIEMENS-SPS an V10 geschrieben, sind die Register V10 und V11 belegt; überwacht der Benutzer V11 zusätzlich mit einem anderen Objekt, entsteht ein Fehler. Achten Sie bei 32-Bit-Datentypen auf Daten- und Adressfehler.

Hinweis: Die Zahl der Nachkommastellen beeinflusst die Anzeige. Bei den Datentypen 16/32-Bit positive Ganzzahl und 16/32-Bit Ganzzahl wird der Dezimalpunkt des gelesenen Werts um die eingestellte Stellenzahl verschoben: Bei Wert 212 und 2 Nachkommastellen wird 2.12 angezeigt. Beim Datentyp 32-Bit-Gleitkommazahl wird nichts verschoben, sondern nur die Nachkommastellen begrenzt: Bei Wert 2.123 und 2 Nachkommastellen wird 2.12 angezeigt.

Hinweis: Die Gesamtstellenzahl ist die Summe aus Vor- und Nachkommastellen. Hat der Ganzzahlanteil des Werts mehr Stellen als vorgesehen, wird er in voller Länge angezeigt. Beispiel: Wert 2123, Länge 2, 1 Nachkommastelle: Angezeigt wird 212.3.

• Passworteingabe: Die eingegebenen Zeichen werden bei Eingabe und Anzeige als „\*“ dargestellt.

• Skript verwenden: Mit „Skript verwenden“ wird eine Skriptliste angezeigt. Der Benutzer kann ein Skript wählen, das beim Drücken der numerischen Eingabe ausgeführt wird. Nur kompilierte Skripte erscheinen in der Liste.

• Gesamtstellen: Gesamtzahl der Stellen, d. h. Vor- plus Nachkommastellen. Sie begrenzt die angezeigten und eingegebenen Werte. Bei 4 Gesamtstellen und 1 Nachkommastelle ist der Höchstwert 999.9, der größte Wert, den das Objekt annimmt und anzeigt. Eine größere Eingabe wird als Fehler gemeldet; bei der Anzeige werden überzählige Stellen ignoriert und nur die eingestellten angezeigt. Beispiel: 4 Gesamtstellen, 1 Nachkommastelle, tatsächlicher Wert 12345: Angezeigt wird 234.5.

Seite „Erweitert“: Hier werden Verstärkung, Offset und Bereichsprüfung der Eingabe festgelegt (Prüfung, ob der eingegebene Wert außerhalb des Bereichs liegt). Außerdem bietet die Seite die Optionen „Bedienbarkeit“ und „Benachrichtigung“, die wie beim Objekt „Bit-Taste“ funktionieren.

Klicken Sie auf die Registerkarte „Erweitert“, wie in Abbildung 4-97:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input3958.png" width="675" />

Abbildung 4-97 Seite „Erweitert“ der numerischen Eingabe

• Bitgesteuert: Ist diese Option aktiviert, ist das Objekt nur unter bestimmten Bedingungen bedienbar. Ist der „Gültige Zustand“ 1, reagiert das Objekt nur, wenn das „Steuerbit“ 1 ist; ist der „Gültige Zustand“ 0, nur wenn das „Steuerbit“ 0 ist. Andernfalls ist das Objekt wirkungslos.

• Benutzerebenen-gesteuert: Der Benutzer kann nach Bedarf mehrere Optionen wählen. In der Simulation oder auf dem HMI wird dann geprüft, ob der aktuelle Benutzer die nötige Berechtigung hat.

• Tastenkürzel verwenden: Siehe Bit-Taste.

• Wert anzeigen: Ist diese Option aktiviert, zeigt die Eingabetastatur den aktuellen Wert des Objekts an. Ist der angezeigte Wert z. B. 389, erscheint beim Antippen der numerischen Eingabe 389 im Eingabefeld; andernfalls ist das Eingabefeld leer, wie unten gezeigt:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4972.png" width="93" />

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4974.png" width="630" />

Beispiel: Auf der Seite „Erweitert“ des Objekts sind unter „Gültige Ebene“ die Optionen 2 und 3 gewählt, und die Benutzerpasswörter in den Touchscreen-Parametern sind wie in Abbildung 4-98 eingestellt:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input5185.png" width="605" />

Abbildung 4-98 Benutzerpasswörter in den Touchscreen-Parametern

Ist die Standard-Benutzerebene NULL, ist das Objekt nicht bedienbar; mit der Funktionstaste „Benutzerebene ändern“ lässt sich die Ebene wechseln. Gibt der Benutzer z. B. das Passwort 6666 ein (Benutzerebene 6), hat dieser Benutzer nur Option 1 gewählt, die nicht zu Option 2 oder 3 passt: Das System meldet ein falsches Passwort. Bei Passwort 2222 oder 3333 haben beide Benutzer Option 2, die passt: Das Passwort ist gültig und das Objekt wird bedienbar. Ist die Standard-Benutzerebene Benutzer 2 bis 3, haben beide Ebenen Option 2, und das Objekt ist in der Simulation bzw. im Startbild bedienbar; ist sie Benutzer 3, passt keine Option, und das Objekt ist nicht bedienbar. Die Standardeinstellung zeigt die folgende Abbildung:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6241.png" width="266" />

Ist „Benutzerebene bei unzureichender Berechtigung ändern“ gewählt, erscheint bei unpassender Ebene ein Anmeldefenster, in dem sich der Benutzer mit einer passenden Ebene erneut anmelden kann, wie unten gezeigt:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6435.png" width="268" />

• Benachrichtigung: Ist das Objekt bedienbar, wird nach dem Antippen in der Simulation oder auf dem Bild und der Eingabe eines Werts über die eingeblendete Tastatur der eingestellte Zustand (1 oder 0) in die Adresse „Benachrichtigungsbit“ geschrieben.

• Skalierung: Ist diese Option aktiviert, gilt: in die Adresse geschriebener Wert = (über die Tastatur eingegebener Wert - Offset) / Verstärkung; angezeigter Wert (d. h. Wert der Überwachungsadresse) = Wert der Überwachungsadresse × Verstärkung + Offset

• Bereich anzeigen: Ist diese Option aktiviert, kann der Benutzer untere und obere Grenzwerte sowie die Hintergrundfarben für unter- und oberhalb festlegen. Der vom Objekt überwachte (gelesene) Wert wird je nach Grenzwerten in unterschiedlichen Farben dargestellt.

• Variabler Bereich: Die Werte „Untere Grenze“ und „Obere Grenze“ ändern sich dynamisch je nach der vom Benutzer angegebenen Adresse

• Untere Grenze: Untergrenze der Anzeige. Liegt der angezeigte Wert darunter, wird die Hintergrundfarbe „Unterer Bereich“ verwendet.

• Obere Grenze: Obergrenze der Anzeige. Liegt der angezeigte Wert darüber, wird die Hintergrundfarbe „Oberer Bereich“ verwendet.

• Bereichsprüfung: Prüft, ob der eingegebene Wert über dem eingestellten Maximum oder unter dem Minimum liegt.

Klicken Sie nach den Einstellungen auf „OK“, um das Objekt in den Ansichtsbereich (das Bild) einzufügen

• Mit den Einstellungen der Seite „Allgemein“ wie unten wird die Zahl binär angezeigt, die Eingabe erfolgt dezimal. Bei anderen Anzeigetypen entspricht der Eingabetyp dem Anzeigetyp.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input8099.png" width="663" />

• Nach dem Einstellen der Eigenschaften klicken Sie auf OK; der Mauszeiger wird zum Kreuz. Ziehen Sie mit der Maus ein Rechteck im Bild auf, um das Objekt einzufügen.
