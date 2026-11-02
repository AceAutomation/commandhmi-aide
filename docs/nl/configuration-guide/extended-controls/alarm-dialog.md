# Weergave historische alarmen

De weergave historische alarmen toont eerdere alarmen; ze werkt zoals de alarmweergave. Klik op de knop historische alarmen <img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog791.png" width="32" /> in de werkbalk om het volgende venster te openen:

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog1031.png" width="650" />

Besturingsadres: schrijf 1 naar het register met offset 0 (16-bits geheel getal, idem voor 1 tot 12), de begintijd naar de registers met offset 1~6 en de eindtijd naar de registers 7~12. De weergave toont dan de gegevens van die periode. Om alle historische alarmen te tonen, schrijft u 0 naar register 0. Register met offset 13 wordt voorlopig niet gebruikt.

Dit adres neemt 12 opeenvolgende offsets in; de betekenis is als volgt:

|                |                                                                                              |
|----------------|----------------------------------------------------------------------------------------------|
| Adresoffset | Door het besturingsregister bestuurd element                                                |
| 0              | 1: toont de gegevens tussen begin- en eindtijd; 0: toont alle gegevens. |
| 1              | Begintijd (jaar)                                                                            |
| 2              | Begintijd (maand)                                                                           |
| 3              | Begintijd (dag)                                                                             |
| 4              | Begintijd (uur)                                                                           |
| 5              | Begintijd (minuut)                                                                             |
| 6              | Begintijd (seconde)                                                                          |
| 7              | Eindtijd (jaar)                                                                              |
| 8              | Eindtijd (maand)                                                                             |
| 9              | Eindtijd (dag)                                                                               |
| 10             | Eindtijd (uur)                                                                              |
| 11             | Eindtijd (minuut)                                                                            |
| 12             | Eindtijd (seconde)                                                                            |

• Alarmdatum wissen: verbergt de alarmdatum

• Alarmtijd wissen: verbergt de alarmtijd

• Alarm wissen: de regel van een gewist alarm wordt in deze kleur gemarkeerd

• Alarmstatistiek: activeert de telling van alarmen, getoond na het bericht.

• Cumulatieve tijd: activeert de cumulatieve alarmtijd, getoond na het bericht.

• OK: het alarm wordt in deze kleur getoond wanneer het optreedt

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog2576.png" width="130" />

Zie voor het basisgebruik het object “Alarmweergave”.

Zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.
