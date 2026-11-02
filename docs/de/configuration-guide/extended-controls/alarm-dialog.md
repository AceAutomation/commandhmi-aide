# Anzeige historischer Alarme

Die Anzeige historischer Alarme zeigt frühere Alarme an; die Bedienung entspricht der Alarmanzeige. Klicken Sie auf die Schaltfläche <img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog791.png" width="32" /> in der Werkzeugleiste, um das folgende Dialogfeld zu öffnen:

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog1031.png" width="650" />

Steueradresse: Schreiben Sie 1 in das Register mit Offset 0 (16-Bit Ganzzahl, ebenso für 1 bis 12), die Startzeit in die Register mit Offset 1 bis 6 und die Endzeit in die Register mit Offset 7 bis 12. Die Anzeige zeigt dann die Daten dieses Zeitraums an. Um alle historischen Alarme anzuzeigen, schreiben Sie 0 in das Register mit Offset 0. Das Register mit Offset 13 wird derzeit nicht verwendet.

Diese Adresse belegt 12 aufeinanderfolgende Offsets mit folgender Bedeutung:

|                |                                                                                              |
|----------------|----------------------------------------------------------------------------------------------|
| Adress-Offset | Gesteuerte Größe                                                                              |
| 0              | 1: Daten zwischen Start- und Endzeit anzeigen; 0: alle Daten anzeigen.                       |
| 1              | Startzeit (Jahr)                                                                             |
| 2              | Startzeit (Monat)                                                                            |
| 3              | Startzeit (Tag)                                                                              |
| 4              | Startzeit (Stunde)                                                                           |
| 5              | Startzeit (Minute)                                                                           |
| 6              | Startzeit (Sekunde)                                                                          |
| 7              | Endzeit (Jahr)                                                                               |
| 8              | Endzeit (Monat)                                                                              |
| 9              | Endzeit (Tag)                                                                                |
| 10             | Endzeit (Stunde)                                                                             |
| 11             | Endzeit (Minute)                                                                             |
| 12             | Endzeit (Sekunde)                                                                            |

• Alarmdatum löschen: Alarmdatum ausblenden

• Alarmzeit löschen: Alarmzeit ausblenden

• Alarm gelöscht: Zeilen gelöschter Alarme werden in dieser Farbe markiert

• Alarmstatistik: Aktiviert die Alarmzählung, die nach der Alarmmeldung angezeigt wird.

• Kumulierte Zeit: Aktiviert die kumulierte Alarmdauer, die nach der Alarmmeldung angezeigt wird.

• OK: Neu auftretende Alarme werden in dieser Farbe angezeigt

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog2576.png" width="130" />

Zur grundlegenden Bedienung siehe Objekt „Alarmanzeige“.

Zur Seite „Sichtbarkeit“ siehe Objekt „Bit-Taste“.
