# Historische Datenanzeige

<span id="OLE_LINK279"></span><span id="OLE_LINK278"></span>         Im Betrieb werden Daten der SPS oder anderer Geräte laufend aktualisiert, z. B. Alarme. Für historische Daten steht in CommandHMI der historische Datensammler zur Verfügung.

CommandHMI bietet die Funktion „Historischer Datensammler“. Das Dialogfeld öffnen Sie im Projektmanager. Bei einem neuen Projekt fügen Sie per Rechtsklick auf „Historischer Datensammler“ einen hinzu und öffnen dann per Doppelklick auf „Historischer Datensammler 0“ die Einstellungen. Einzelheiten siehe „[Historischer Datensammler](../../setting/history-data.md)“ in Kapitel 6.

Klicken Sie auf die Schaltfläche Historische Datenanzeige <img src="../../../configuration-guide/extended-controls/history-record.files/history-record687.png" width="32" /> in der Werkzeugleiste; es erscheint folgendes Dialogfeld:

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record747.png" width="579" />

Abbildung 4-65 Dialogfeld Historische Datenanzeige

**Allgemein:**

• Vordergrundfarbe: Klicken Sie auf das Farbfeld, um die Vordergrundfarbe der Anzeige zu ändern.

• Rahmenfarbe: Klicken Sie auf das Farbfeld, um die Rahmenfarbe der Anzeige zu ändern.

• Titel: Schriftgröße, Schriftstil, Hintergrundfarbe, Textfarbe und ob Datum und Uhrzeit angezeigt werden. Zu den Spracheinstellungen siehe „Alarmanzeige“.

• Daten: Schriftgröße, Farbe und maximale Zahl der angezeigten Zeilen.

Steueradresse:

Schreiben Sie 1 in das Register mit Offset 0 (16-Bit Ganzzahl, ebenso für 1 bis 12), die Startzeit in die Register mit Offset 1 bis 6, die Endzeit in die Register mit Offset 7 bis 12 und zuletzt 1 in das Register mit Offset 13. Die Anzeige zeigt dann die Daten dieses Zeitraums an; das Register mit Offset 13 wird automatisch zurückgesetzt. Um alle historischen Daten anzuzeigen, schreiben Sie 0 in das Register mit Offset 0.

Diese Adresse belegt 40 aufeinanderfolgende Offsets mit folgender Bedeutung:

|                |                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adress-Offset | Gesteuerte Größe                                                                                                                                                         |
| 0              | 1: Daten zwischen Start- und Endzeit anzeigen; 0: alle Daten anzeigen.                                                                                                   |
| 1              | Startzeit (Jahr); ein Wort                                                                                                                                               |
| 2              | Startzeit (Monat); ein Wort                                                                                                                                              |
| 3              | Startzeit (Tag); ein Wort                                                                                                                                                |
| 4              | Startzeit (Stunde); ein Wort                                                                                                                                             |
| 5              | Startzeit (Minute); ein Wort                                                                                                                                             |
| 6              | Startzeit (Sekunde); ein Wort                                                                                                                                            |
| 7              | Endzeit (Jahr); ein Wort                                                                                                                                                 |
| 8              | Endzeit (Monat); ein Wort                                                                                                                                                |
| 9              | Endzeit (Tag); ein Wort                                                                                                                                                  |
| 10             | Endzeit (Stunde); ein Wort                                                                                                                                               |
| 11             | Endzeit (Minute); ein Wort                                                                                                                                               |
| 12             | Endzeit (Sekunde); ein Wort                                                                                                                                              |
| 13             | Wechsel von 0 auf 1 bei Offset 0 = 1: Daten des Zeitraums anzeigen; automatische Rücksetzung; <span id="OLE_LINK339"></span>ein Wort                                     |
| 14             | Anzahl aller historischen Datensätze zwischen Start- und Endzeit; Doppelwort                                                                                             |

Daten:

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record2617.png" width="581" />

Gruppennummer: CommandHMI bietet mehrere Gruppen historischer Daten zur Auswahl.

Bedienung der historischen Datenanzeige: Für die Anzeige über Steueradressen wird wie in Abbildung 4-65-1 projektiert:

<img src="../../../configuration-guide/extended-controls/history-record.files/001.png" width="797" />

Abbildung 4-65-1

Geben Sie hier 1 bei „Alle Daten anzeigen“ und 1 bei „Abfragen“ ein: Der Datensammler zeigt alle historischen Daten zwischen Start- und Endzeit an. Siehe Abbildung 4-65-2

<img src="../../../configuration-guide/extended-controls/history-record.files/002.png" width="795" />

Abbildung 4-65-2

Geben Sie 1 bei „Alle Daten anzeigen“ ein, als Startzeit 2016-7-11 3: 30: 4 und als Endzeit 2016-7-11 14: 39: 4; bei „Abfragen“ = 1 werden nur die Daten dieses Zeitraums angezeigt.

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record3263.png" width="130" />

Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.
