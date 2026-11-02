# Flussblock

Ein Flussblock ist eine animierte Grafik, die den Flüssigkeitsfluss in einem Rohr nachbildet. Ob er fließt, bestimmt der Zustand der Triggeradresse: Bei 1 fließt der Block, bei 0 steht er still. Die Fließgeschwindigkeit legt der Benutzer fest. Klicken Sie auf die Schaltfläche <img src="../../../configuration-guide/extended-controls/pipe.files/image002.jpg" width="28" /> in der Werkzeugleiste; es erscheint folgendes Dialogfeld:

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

<img src="../../../configuration-guide/extended-controls/pipe.files/image004.jpg" width="130" />

Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.
