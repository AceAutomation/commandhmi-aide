# Historische gegevensverzamelaar

De historische gegevensverzamelaar werkt samen met de [weergave historische gegevens](../configuration-guide/extended-controls/history-record.md) in de werkbalk. De eerste dient vooral voor de parameterinstellingen, de tweede voor de weergave van de historische gegevens.

Maak een historische gegevensverzamelaar aan door met de rechtermuisknop op “Historische gegevensverzamelaar” te klikken en “Nieuwe historische gegevensverzamelaar” te kiezen.

Opmerking: CommandHMI ondersteunt meerdere groepen historische gegevens; er kunnen tot vier historische gegevensverzamelaars worden aangemaakt.

Er kunnen niet meer dan vier groepen worden aangemaakt; anders verschijnt de volgende foutmelding:

<img src="../../setting/history-data.files/image008.jpg" width="456" />

Dubbelklik op “Historische gegevensverzamelaar 0” in de “projectbeheerder” om het dialoogvenster van afbeelding 7-19 te openen:

<img src="../../setting/history-data.files/image009.jpg" width="627" />

Afbeelding 7-19     Dialoogvenster historische gegevensverzamelaar

• Naam: de naam in de projectbeheerder.

• Bemonsteringslengte: aantal gegevens dat telkens uit het geheugen wordt gelezen.

• Totaal aantal monsters: aantal keren dat gegevens worden opgehaald.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Opmerking: benodigd geheugen = (20 + totaal aantal bytes van de gegevenstypen van alle gegevensitems) \* totaal aantal monsters.

“20” zijn de bytes voor tijd en datum;

“Totaal aantal bytes van de gegevenstypen van alle gegevensitems” is de som van de gegevenstypen van elk item op de pagina “Gegevensitems”.

Bijvoorbeeld, zoals in afbeelding 7-20:

a. Is het gegevenstype van elk item “16-bits positief geheel getal”, dan is het “totaal aantal bytes van de gegevenstypen van alle gegevensitems” = 2 +2 +2 +2 +2; het benodigde geheugen is dus (20 + 10) \* 2 = 60; een “16-bits gegeven” neemt 2 bytes in, een “32-bits gegeven” 4 bytes.

b\. Is het gegevenstype van “LH1” en “LH3” “32-bits positief geheel getal” (dan toont de pagina “Gegevensitems” de adressen LH0, LH1, LH3, LH5, LH6), dan is “het totale aantal bytes van alle gegevensitems” = 2 + 4 + 4 + 2 + 2 = 14; het benodigde geheugen is dan (20 + 14) \* 2 = 68.

Leesadres: beginadres voor het lezen van de gegevens (zie “Gegevensitems” voor details)

Bemonsteringswijze:

• Periodiek: leest de gegevens met het ingestelde interval.

• Trigger: leest de gegevens als het triggeradres 1 is.

• Klok: begint met lezen op een door de gebruiker ingesteld tijdstip.

Bij volle bemonstering: wat er gebeurt als het maximale aantal monsters is bereikt.

Bemonstering stoppen: stopt de bemonstering als het maximum is bereikt; is deze optie niet aangevinkt, dan vervangen nieuwe gegevens de oudste.

Melden: zet een adres op 1 als het aantal monsters het maximum bereikt.

Klik op het tabblad “Gegevensitems” en stel de eigenschappen in, zoals in afbeelding 7-20:

<img src="../../setting/history-data.files/image002.jpg" width="627" />

Afbeelding 7-20 Gegevensitems van de historische gegevensverzamelaar

Is meertaligheid gekozen, dan moeten bij het toevoegen van gegevensitems namen voor elke taal worden ingesteld; anders kunnen geen items worden toegevoegd.

In CommandHMI kunnen de adressen van elke groep historische gegevens discreet worden ingesteld, afhankelijk van de LW-registers, bijvoorbeeld: S1 is LW1, S2 is LW89, S3 is LW8905.

Klik op een item in de lijst om de eigenschappen in te stellen.

Een uitgewerkt voorbeeld:

Stel op de pagina “Algemeen” het leesadres in op LW1, met opeenvolgende registeradressen en een bemonsteringslengte van 5; klik op het tabblad “Gegevensitems” en voeg 5 kolommen (LH0-LH4) toe. Stel voor elke kolom de eigenschappen in: naam, adres, gegevenstype, totaal aantal cijfers, decimalen en of er wordt geschaald.

Stel dat naam, gegevenstype en schaling van LH0-LH4 zijn ingesteld zoals in afbeelding 7-20 en de andere eigenschappen standaard zijn:

LH0 - 16-bits positief geheel getal, geschaald, versterking 3 en offset 2

LH1 - 32-bits positief geheel getal, geschaald, versterking 2 en offset 1

LH2 - 16-bits geheel getal, niet geschaald

LH3 - 32-bits geheel getal, niet geschaald

LH4 - drijvende komma, geschaald, versterking 4 en offset 5

Omdat de bemonsteringslengte 5 is (pagina “Algemeen”), worden daarna vanaf het “leesadres” 5 opeenvolgende adreswaarden gelezen, volgens het gegevenstype van elk item.

Bij 16-bits gegevens zijn de gelezen adressen opeenvolgend, bij 32-bits gegevens liggen ze verder uit elkaar. Met schaling is de uiteindelijke waarde gelijk aan de waarde van het leesadres vermenigvuldigd met de versterking plus de offset.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Opmerking: de versterking bij schaling moet groter zijn dan 1!

Met de ingestelde gegevenstypen en schaling worden de volgende adressen gelezen:

LH0-LW1 (16-bits gegeven, leesadres + 1) Eindwaarde LH0 = waarde van LW1 × 3 + 2

LH1-LW2 (32-bits gegeven, leesadres + 2) Eindwaarde LH1 = waarde van LW2 × 2 + 1

LH2-LW4 (16-bits gegeven, leesadres + 1) Eindwaarde LH2 = waarde van LW4

LH3-LW5 (32-bits gegeven, leesadres + 2) Eindwaarde LH3 = waarde van LW5

LH4-LW7 (32-bits gegeven, leesadres + 2) Eindwaarde LH4 = waarde van LW7 × 4 + 5

Klik na de instellingen op “OK”. Klik op het pictogram “Weergave historische gegevens” in de werkbalk; stel in het dialoogvenster het aantal regels in op 5 en laat de andere eigenschappen standaard.

Klik op “OK” om automatisch een tabel in het scherm te maken, zoals in afbeelding 7-21:

Afbeelding 7-21 Gegevenstabel van de weergave historische gegevens

Uitleg bij de tabel hierboven:

• Datum: de datum waarop de adreswaarde is gelezen

• Tijd: het tijdstip waarop de adreswaarde is gelezen

• “LH0”: toont de waarde van LW1 op een bepaald moment.

• “LH1”: toont de waarde van LW2 op een bepaald moment.

• “LH2”: toont de waarde van LW4 op een bepaald moment.

• “LH3”: toont de waarde van adres LW5 op een bepaald moment.

• “LH4”: toont de waarde van adres LW7 op een bepaald moment.

Voorbeeld: leesadres LW1, bemonsteringslengte 3, totaal aantal monsters 10, bemonsteringswijze Trigger, interval 1 seconde, gegevenstype standaard;

1). “Bemonstering stoppen” niet aangevinkt:

De waarden van LW1, LW2 en LW3 worden elke seconde gelezen. Omdat het totale aantal monsters 10 is, zijn na tien seconden 10 reeksen gelezen. Omdat “Bemonstering stoppen” niet is aangevinkt, gaat het proces door. Voor de gelezen gegevens wordt een vast geheugengebied gereserveerd op basis van bemonsteringslengte, totaal aantal monsters en gegevenstype; zodra het aantal reeksen het “totaal aantal monsters” bereikt, vervangen de nieuwste gegevens de oudste.

2). “Bemonstering stoppen” aangevinkt:

Het enige verschil is dat de bemonstering stopt zodra het totale aantal monsters is bereikt.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Gebruik de “[Historische trend](../configuration-guide/extended-controls/histrendgraphics.md)” of de “[Weergave historische gegevens](../configuration-guide/extended-controls/history-record.md)” om de waarden overzichtelijker te bekijken.
