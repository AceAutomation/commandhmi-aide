# Grafikanzeige

Die Grafikanzeige ist eine Erweiterung des Objekts „Statische Grafik“: Die statische Grafik zeigt nur eine Grafik an, die Grafikanzeige bis zu 32. Je nach gewählter Zustandsart kann die Grafikanzeige unterschiedlich definiert werden.

Vorgehen:

Klicken Sie auf das Symbol Grafikanzeige <img src="../../../configuration-guide/basic-control/picture-display.files/image002.jpg" width="32" /> in der Werkzeugleiste. Es erscheint das Dialogfeld in Abbildung 4-110:

Abbildung 4-110   Dialogfeld Grafikanzeige

• Bit: Bei „Bit“ gibt es nur zwei Zustände, 0 und 1. Die Überwachungsadresse kann nur eine Bitadresse sein. Das Objekt zeigt je nach Zustand 0 oder 1 der Überwachungsadresse die entsprechende Grafik an.

• Wert: Bei „Wert“ sind bis zu 2048 Zustände möglich; je nach Wert der Überwachungsadresse werden verschiedene Grafiken angezeigt. Bei Wert 0 wird die Grafik des Zustands 0 angezeigt usw.

• Automatisch wechseln: Bei „Automatisch wechseln“ sind bis zu 2048 Zustände möglich; das Objekt wechselt die Grafiken unabhängig vom Wert der Überwachungsadresse. Es genügt, die Gesamtzahl der Zustände und die Wechselfrequenz einzustellen. Im HMI wechselt das Objekt die Grafiken dann automatisch innerhalb dieses Bereichs.

<img src="../../../configuration-guide/basic-control/picture-display.files/image004.jpg" width="130" />

Hinweis: Die Seite „Grafik“ der Grafikanzeige entspricht weitgehend der des Objekts „Mehrzustandslampe“.

Hinweis: Zur „Sichtbarkeit“ siehe Objekt „Bit-Taste“.

Klicken Sie nach den Einstellungen auf „OK“, um das Objekt in den Ansichtsbereich (das Bild) einzufügen.
