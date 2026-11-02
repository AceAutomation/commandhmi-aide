# ASCII-invoer

Klik op het pictogram ASCII-invoer<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input38.png" width="30" />; het dialoogvenster van afbeelding 4-100 verschijnt:

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input93.png" width="665" />

Afbeelding 4-100 Dialoogvenster ASCII-invoer

• Schrijfadres: de ASCII-tekst wordt naar dit adres geschreven.

• Bewaken: adreswaarde die het object leest en toont.

• Bewakingsadres gelijk aan schrijfadres: het bewakingsadres is hetzelfde als het schrijfadres.

• Bewakingsadres: gelezen adres

• Totaal: maximaal aantal tekens dat kan worden getoond.

• Lettergrootte: grootte van de getoonde tekens

• Hoge en lage byte van de invoer verwisselen: in de door de gebruiker ingevoerde waarde worden hoge en lage byte verwisseld en het resultaat wordt in het bewaakte woordadres opgeslagen.

• Wachtwoord: indien aangevinkt toont het object geen tekens maar sterretjes (\*)

• UNICODE gebruiken: de waarde van het bewakingsadres wordt in Unicode-codering getoond

Uitlijning:

• Links: de tekens worden links in het weergavegebied getoond.

• Midden: de tekens worden in het midden van het weergavegebied getoond.

• Rechts: de tekens worden rechts in het weergavegebied getoond.

• Script gebruiken: vink “Script gebruiken” aan om de lijst met scripts te tonen. De gebruiker kiest een script dat bij het indrukken wordt uitgevoerd. Alleen gecompileerde scripts staan in de lijst.

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input1310.png" width="130" />

Opmerking: bij een gegevenstype van 32 bits neemt het adres bijvoorbeeld 2 woorden in. Wordt naar het dataregister V10 van een SIEMENS-PLC geschreven, dan worden V10 en V11 bezet; bewaakt een ander object ook V11, dan ontstaat een fout. Let op bij 32-bits gegevenstypen om gegevens- en adresfouten te voorkomen.

Opmerking: de overige functies van de pagina “Algemeen” zijn gelijk aan die van de ASCII-weergave.

Opmerking: zie voor de pagina's “Geavanceerd” en “Zichtbaarheid” de Bit-knop.
