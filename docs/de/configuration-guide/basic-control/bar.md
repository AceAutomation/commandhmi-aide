# Balkendiagramm

Das Balkendiagramm stellt Änderungen von Zahlenwerten in Echtzeit als Balken dar, sodass der Benutzer sie anschaulicher verfolgen kann. Es kann die Werte von Datenregistern der SPS oder anderer verbundener Geräte sowie alle analogen Prozessgrößen in Echtzeit darstellen. Siehe folgende Abbildung.

<img src="../../../configuration-guide/basic-control/bar.files/image006.jpg" width="535" alt="2018_11_20_14_27_19.jpg" />

Abbildung 4-101   Balkendiagramm

Balkendiagramm hinzufügen und Eigenschaften ändern:

1\. Wählen Sie das Symbol Balkendiagramm <img src="../../../configuration-guide/basic-control/samdra8.gif" width="20" /> in der Werkzeugleiste oder im Menü „Tools“. Es erscheint das Dialogfeld in Abbildung 4-102.

2\. Legen Sie die Eigenschaften des Balkendiagramms im Dialogfeld fest und klicken Sie auf OK:

• Hintergrundfarbe: Hintergrundfarbe des Balkendiagramms

• Rahmenfarbe: Rahmenfarbe des Balkens. In Abbildung 4-102 ist die Rahmenfarbe wirkungslos; wählt man eine andere „Form“, wird die Änderung sichtbar.

• Transparent: Hintergrund des Balkens transparent

• Richtung: Füllrichtung des Balkens, vier Richtungen: aufwärts, abwärts, nach links und nach rechts.

• Aufwärts: Steigt der Wert der Überwachungsadresse, füllt sich der Balken von unten nach oben

• Abwärts: Steigt der Wert der Überwachungsadresse, füllt sich der Balken von oben nach unten

• Nach links: Steigt der Wert der Überwachungsadresse, füllt sich der Balken von rechts nach links

• Nach rechts: Steigt der Wert der Überwachungsadresse, füllt sich der Balken von links nach rechts

• Datentyp: Datentyp des gelesenen Werts, d. h. Wort- oder Doppelwortadresse.

• Überwachungsadresse: Im Balken dargestellte Datenregisteradresse, d. h. die Leseadresse

• Maximum: Höchstwert der Überwachungs-(Lese-)adresse. Ist der Wert größer, ist der Balken voll und ändert sich nicht weiter

• Minimum: Mindestwert der Überwachungs-(Lese-)adresse. Ist der Wert kleiner, ist der Balken leer und ändert sich nicht weiter

• Variabler Bereich: Maximum und Minimum ändern sich dynamisch je nach der vom Benutzer angegebenen Adresse; deren Datentyp entspricht dem eingestellten „Datentyp“

• Bipolarer Balken: Der Balken kann je nach Wert des Datenregisters nach beiden Seiten dargestellt werden.

• Mittelpunkt: Mittelpunkt des bipolaren Balkens.

<img src="../../../configuration-guide/basic-control/bar.files/image002.jpg" width="675" />

Abbildung 4-102   Dialogfeld Balkendiagramm

Beispiel: Maximum 100, Minimum 10, Richtung aufwärts, bipolarer Balken aktiviert und Mittelpunkt 70. Steigt der Wert der Überwachungsadresse von 0 an, ergibt sich die Darstellung in Abbildung 4-103.

<img src="../../../configuration-guide/basic-control/samdra10.gif" width="534" />

Abbildung 4-103 Bipolares Balkendiagramm

3\. Balkendiagramm ändern: Klicken Sie auf das Diagramm; es erscheinen acht kleine grüne Punkte, mit denen Sie die Größe per Maus ändern können.

Seite „Bereich“:

Auf dieser Seite wird festgelegt, dass Werte der Überwachungsadresse in bestimmten Bereichen mit anderer Vorder- und Hintergrundfarbe dargestellt werden. Die Eigenschaften zeigt Abbildung 4-104:

Abbildung 4-104   Seite „Bereich“ des Balkendiagramms

• Bereich anzeigen: Ist diese Option aktiviert, kann der Benutzer untere und obere Grenzwerte sowie die Hintergrundfarben für unter- und oberhalb festlegen. Der vom Objekt überwachte (gelesene) Wert wird je nach Grenzwerten in unterschiedlichen Farben dargestellt.

• Variabler Bereich: Die Werte „Untere Grenze“ und „Obere Grenze“ ändern sich dynamisch je nach der vom Benutzer angegebenen Adresse

• Untere Grenze: Untergrenze der Anzeige. Liegt der angezeigte Wert darunter, wird die Hintergrundfarbe „Unterer Bereich“ verwendet.

• Obere Grenze: Obergrenze der Anzeige. Liegt der angezeigte Wert darüber, wird die Hintergrundfarbe „Oberer Bereich“ verwendet.

<span id="OLE_LINK727"></span><span id="OLE_LINK726"></span>Klicken Sie nach den Einstellungen auf „OK“, um das Objekt in den Ansichtsbereich (das Bild) einzufügen

<img src="../../../configuration-guide/basic-control/bar.files/image004.jpg" width="130" />

Hinweis: Liegt der Wert der Überwachungsadresse zwischen Maximum und Minimum, entsprechen Vorder- und Hintergrundfarbe den Einstellungen der Seite „Allgemein“.

Hinweis: Zur „Sichtbarkeit“ siehe „Bit-Taste“.
