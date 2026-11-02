# Eck-Flussblock

Der Eck-Flussblock funktioniert ähnlich wie der Flussblock, kann aber zusätzlich Ecken zeichnen und ist dadurch flexibler.

 Klicken Sie auf das Symbol <img src="../../../configuration-guide/new_add_control/corner-flow-block.files/image001.jpg" width="74" alt="ScreenShot00054.jpg" /> in der Werkzeugleiste und bewegen Sie den Mauszeiger in den Bildbereich; er wird zum Fadenkreuz. Klicken Sie auf die Anfangsposition des Eck-Flussblocks und bewegen Sie die Maus: Zwischen Anfangsposition und Fadenkreuz erscheint eine Linie. Ein Klick auf die Endposition erzeugt den ersten Block. Die Endposition ist zugleich der Anfang des nächsten Blocks, mit einem Winkel von 90°. So entstehen mehrere Abschnitte. Ein Rechtsklick beendet das Zeichnen. Das Ergebnis zeigt Abbildung 4-134.

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block1511.png" width="405" />

Abbildung4-134  Eck-Flussblock

Doppelklicken Sie nach dem Zeichnen auf den Block oder wählen Sie per Rechtsklick „Eigenschaften“; es erscheint das Dialogfeld des Eck-Flussblocks, wie in Abbildung 4-135.

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block1691.png" width="661" />

Abbildung4-135 Dialogfeld Eck-Flussblock

Farbe: Farbeigenschaften des Flussblocks.

• Vordergrundfarbe des Flussblocks: Klicken Sie auf die Farbschaltfläche, um die Vordergrundfarbe festzulegen;

• Hintergrundfarbe des Flussblocks: Klicken Sie auf die Farbschaltfläche, um die Hintergrundfarbe festzulegen;

• Vordergrundfarbe des Rohrs: Klicken Sie auf die Farbschaltfläche, um die Vordergrundfarbe des Rohrs festzulegen;

• Hintergrundfarbe des Rohrs: Klicken Sie auf die Farbschaltfläche, um die Hintergrundfarbe des Rohrs festzulegen;

• Rahmenfarbe: Klicken Sie auf die Schaltfläche, um die Rahmenfarbe des Objekts festzulegen;

• Muster: Muster des Flussblocks; Standard ist „Solid“.

• Triggeradresse: Adresse, die Stillstand oder Bewegung des Flussblocks steuert; bei Wert 1 fließt der Block.

• Eigenschaften: Eigenschaften des Flussblocks wie Richtung und Fließgeschwindigkeit.

• Anzeigemodus: „Horizontal“ lässt den Flussblock waagerecht fließen, „Vertikal“ senkrecht.

• Richtung: Im Modus „Horizontal“ „Links“ oder „Rechts“, sonst „Oben“ oder „Unten“.

• Richtung über Triggeradresse umkehren: Ist der Wert der „Triggeradresse“ gleich dem eingestellten „Gültigen Zustand“, wird die Fließrichtung umgekehrt.

Beispiel: Fließrichtung „Links“, Option aktiviert, Triggeradresse LB2, gültiger Zustand 1. Ist LB2 = 1, fließt der Block nach „Rechts“; ist LB2 = 0, wieder nach „Links“.

• Blöcke: Anzahl der Flusselemente, 1 bis 30;

• Ohne Rahmen: Bei Aktivierung werden die Ränder des Flussblocks ausgeblendet.

• Fließgeschwindigkeit: Fest oder dynamisch

• Feste Geschwindigkeit: Hoch, Mittel oder Niedrig.

• Dynamische Geschwindigkeit: Die Geschwindigkeit wird durch den Wert einer Wortadresse zwischen 1 und 10 bestimmt. Bei 0 fließt der Block nicht, bei 1 am langsamsten, bei 10 am schnellsten.

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block3818.png" width="130" />

Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.
