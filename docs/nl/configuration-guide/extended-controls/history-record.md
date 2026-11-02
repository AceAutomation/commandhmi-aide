# Weergave historische gegevens

<span id="OLE_LINK279"></span><span id="OLE_LINK278"></span>         In de praktijk kunnen gegevens van de PLC of andere apparaten op elk moment veranderen, zoals alarmen. Historische gegevens bekijkt u met de historische gegevensverzamelaar van CommandHMI.

CommandHMI biedt de historische gegevensverzamelaar, bereikbaar via de projectbeheerder. Klik in een nieuw project met de rechtermuisknop op “Historische gegevensverzamelaar” om er een toe te voegen en dubbelklik daarna op “Historische gegevensverzamelaar 0” om hem in te stellen. Zie de eigenschappen van de “[Historische gegevensverzamelaar](../../setting/history-data.md)” in hoofdstuk 6.

Klik op de knop weergave historische gegevens<img src="../../../configuration-guide/extended-controls/history-record.files/history-record687.png" width="32" /> in de werkbalk; het volgende dialoogvenster verschijnt:

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record747.png" width="579" />

Afbeelding 4-65 Dialoogvenster Weergave historische gegevens

**Algemeen:**

• Voorgrondkleur: klik op de kleur in het vak om de voorgrondkleur te wijzigen.

• Randkleur: klik op de kleur in het vak om de randkleur te wijzigen.

• Titel: lettergrootte en -stijl, achtergrondkleur, tekstkleur en of datum en tijd worden getoond. Zie voor de taal de “Alarmweergave”.

• Gegevens: lettergrootte, kleur en maximaal aantal getoonde regels.

Besturingsadres:

Schrijf 1 naar het register met offset 0 (16-bits geheel getal, idem voor 1 tot 12), de begintijd naar de registers met offset 1~6, de eindtijd naar de registers 7~12 en tot slot 1 naar register 13. De weergave toont dan de gegevens van die periode. Register 13 wordt automatisch gereset. Om alle historische gegevens te tonen, schrijft u 0 naar register 0.

Dit adres neemt 40 opeenvolgende offsets in. Betekenis:

|                |                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adresoffset | Door het besturingsregister bestuurd element                                                                                                                            |
| 0              | 1: toont de gegevens tussen begin- en eindtijd; 0: toont alle gegevens.                                                                             |
| 1              | Begintijd (jaar); één woord                                                                                                                                              |
| 2              | Begintijd (maand); één woord                                                                                                                                             |
| 3              | Begintijd (dag); één woord                                                                                                                                               |
| 4              | Begintijd (uur); één woord                                                                                                                                              |
| 5              | Begintijd (minuut); één woord                                                                                                                                               |
| 6              | Begintijd (seconde); één woord                                                                                                                                            |
| 7              | Eindtijd (jaar); één woord                                                                                                                                                |
| 8              | Eindtijd (maand); één woord                                                                                                                                               |
| 9              | Eindtijd (dag); één woord                                                                                                                                                 |
| 10             | Eindtijd (uur); één woord                                                                                                                                                |
| 11             | Eindtijd (minuut); één woord                                                                                                                                              |
| 12             | Eindtijd (seconde); één woord                                                                                                                                              |
| 13             | Van 0 naar 1 met offset 0 op 1: de gegevens van de opgegeven periode worden getoond; automatische reset; <span id="OLE_LINK339"></span>één woord |
| 14             | Totaal aantal historische gegevens tussen begin- en eindtijd; dubbelwoord                                                                                     |

Gegevens:

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record2617.png" width="581" />

Groepsnummer: CommandHMI biedt meerdere groepen historische gegevens om uit te kiezen.

Gebruik van de weergave historische gegevens: om de gegevens via besturingsadressen te tonen, is de configuratie als in afbeelding 4-65-1:

<img src="../../../configuration-guide/extended-controls/history-record.files/001.png" width="797" />

Afbeelding 4-65-1

Voer 1 in bij “Alle gegevens tonen” en 1 bij “Opvragen”: de verzamelaar toont alle historische gegevens tussen begin- en eindtijd. Zoals in afbeelding 4-65-2

<img src="../../../configuration-guide/extended-controls/history-record.files/002.png" width="795" />

Afbeelding 4-65-2

Voer 1 in bij “Alle gegevens tonen”, begintijd 2016-7-11 3: 30: 4 en eindtijd 2016-7-11 14: 39: 4; bij invoer van 1 in “Opvragen” worden alleen de gegevens van die periode getoond.

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record3263.png" width="130" />

Zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.
