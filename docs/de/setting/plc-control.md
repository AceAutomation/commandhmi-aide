# SPS-Steuerung

Mit der SPS-Steuerung werden Bildwechsel, Änderung der Benutzerebene, Rezeptwechsel und Schreiben von Rezepten von der SPS aus gesteuert. Doppelklicken Sie im Projektmanager auf „SPS-Steuerung“; es öffnet sich das Dialogfeld in Abbildung 7-8:

Abbildung 7-8      Dialogfeld SPS-Steuerung

• Rezept wechseln: Das HMI wechselt das Rezept entsprechend dem Adresswert.

• Rezept schreiben: Das HMI steuert das Schreiben des Rezepts entsprechend dem Adresswert.

• Aktuelle Benutzerebene: Das HMI stellt die aktuelle Benutzerebene entsprechend diesem Adresswert ein.

• Bildwechsel über Wortadresse: Das HMI wechselt das Bild entsprechend dem Wert dieser Wortadresse; ist der Wert n, wechselt es zum n-ten Bild.

• Bildwechsel über Bitadresse: Doppelklicken Sie auf die Zeile „Neu“; es öffnet sich das Dialogfeld in Abbildung 7-9:

Neue Bit-Steuerung:

<img src="../../setting/plc-control.files/image004.jpg" width="458" />

Neue Wort-Steuerung

<img src="../../setting/plc-control.files/image006.jpg" width="497" />

Bild: Die Wort-Steuerung der SPS wechselt nur zwischen Bildern

Fenster: Die Wort-Steuerung der SPS wechselt nur zwischen Fenstern

Bild/Fenster: Die Wort-Steuerung der SPS wechselt zwischen Bildern und Fenstern

<img src="../../setting/plc-control.files/image005.jpg" width="130" />

Hinweis: Beim Bildwechsel über die SPS bewirkt der zuerst gelesene Wert keinen Bildwechsel. Erst wenn sich der Wert des SPS-Registers vom zuerst gelesenen Wert unterscheidet, wird gewechselt.
