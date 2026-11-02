# Bit-Lampe

Die Bit-Lampe überwacht den ON/OFF-Zustand eines Bitkontakts des verbundenen Geräts und zeigt ihn auf dem HMI an.

Wie in Abbildung 4-78:

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image007.jpg" width="554" alt="2018_11_20_14_25_09.jpg" />

Abbildung 4-78

Bit-Lampe anlegen:

1\. Wählen Sie das Symbol Bit-Lampe <img src="../../../configuration-guide/basic-control/bit-lamp.files/image002.jpg" width="31" /> in der Werkzeugleiste: Es öffnet sich das Dialogfeld in Abbildung 4-79:

Abbildung 4-79    Dialogfeld Bit-Lampe

• Datentyp: Die Auswahlliste bietet drei Optionen: Bit, Wort-Bit und Doppelwort-Bit. Bei „Bit“ ist die Überwachungs-(Lese-)adresse eine Bitadresse, bei Doppelwort-Bit eine Doppelwortadresse.

• Bitnummer: Bei Datentyp „Wort-Bit“ oder „Doppelwort-Bit“ bestimmt die Bitnummer, welches Bit der Überwachungsadresse den Zustand ON/OFF liefert: 0 bis 15 bei Wort-Bit, 0 bis 31 bei Doppelwort-Bit.

Beispiel: Bei „Wort-Bit“ und Überwachungsadresse LW1 mit dem Wert 23 ist bei Bitnummer 3 der Zustand 0, denn 23 ist binär 10111, und die 3. Stelle von rechts nach links ist 0.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Hinweis: <span id="OLE_LINK707"></span><span id="OLE_LINK706"></span>Form, Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster siehe Objekt „Bit-Taste“.

2\. Wählen Sie im Dialogfeld der Bit-Lampe auf der Seite „Allgemein“ die Adresse, die diese Lampe überwacht. Auf der Seite „Beschriftung“ legen Sie die angezeigten Texte und Grafiken fest und ob die Lampe blinkt.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Hinweis: Die Seite „Beschriftung“ der Bit-Lampe entspricht der der Bit-Taste.

3\. Um die Eigenschaften der Lampe zu ändern, doppelklicken Sie darauf und ändern sie im Eigenschaftsdialog.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Hinweis: Die Seite „Sichtbarkeit“ der Bit-Lampe entspricht der des Objekts „Bit-Taste“.

Klicken Sie nach den Einstellungen auf „OK“, um das Objekt in den Ansichtsbereich (das Bild) einzufügen
