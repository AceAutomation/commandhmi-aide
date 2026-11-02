# ASCII-Eingabe

Klicken Sie auf das Symbol ASCII-Eingabe <img src="../../../configuration-guide/basic-control/asc-input.files/asc-input38.png" width="30" />; es öffnet sich das Dialogfeld in Abbildung 4-100:

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input93.png" width="665" />

Abbildung 4-100 Dialogfeld ASCII-Eingabe

• Schreibadresse (Write Address): ASCII-Text wird in diese Adresse geschrieben.

• Überwachen (Monitor): Adresse, deren Wert dieses Objekt liest und anzeigt.

• Überwachungsadresse gleich Schreibadresse: Die Überwachungsadresse ist identisch mit der Schreibadresse.

• Überwachungsadresse: Die zu lesende Adresse

• Anzahl (Total): Maximale Anzahl angezeigter Zeichen.

• Schriftgröße: Schriftgröße der angezeigten Zeichen

• High- und Low-Byte der Eingabe tauschen: High- und Low-Byte des eingegebenen Werts werden vertauscht und das Ergebnis in der überwachten Wortadresse gespeichert.

• Passwort: Ist diese Option aktiviert, zeigt das Objekt statt der Zeichen Sternchen (\*) an

• UNICODE verwenden: Der Wert der Überwachungsadresse wird in Unicode-Kodierung angezeigt

Ausrichtung:

• Links: Die Zeichen werden im linken Teil des Anzeigebereichs dargestellt.

• Mitte: Die Zeichen werden in der Mitte des Anzeigebereichs dargestellt.

• Rechts: Die Zeichen werden im rechten Teil des Anzeigebereichs dargestellt.

• Skript verwenden (Use Macro): Mit der Option „Skript verwenden“ wird eine Skriptliste angezeigt. Der Benutzer kann ein Skript wählen, das beim Drücken ausgeführt wird. Nur kompilierte Skripte erscheinen in der Liste.

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input1310.png" width="130" />

Hinweis: Bei Datentyp 32 Bit belegt die Adresse 2 Worte. Wird z. B. in ein Datenregister einer SIEMENS-SPS an V10 geschrieben, sind die Register V10 und V11 belegt; überwacht der Benutzer V11 zusätzlich mit einem anderen Objekt, entsteht ein Fehler. Achten Sie bei 32-Bit-Datentypen auf Daten- und Adressfehler.

Hinweis: Die übrigen Funktionen der Seite „Allgemein“ entsprechen denen der ASCII-Anzeige.

Hinweis: Zu den Seiten „Erweitert“ und „Sichtbarkeit“ siehe „Bit-Taste“.
