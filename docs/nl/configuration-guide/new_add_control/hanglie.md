# Tabel

Dit object toont door de gebruiker ingestelde gegevens in een raster, wat selectie en bediening vereenvoudigt. Functies: automatisch bladeren, invoegen, verwijderen, kopiëren en plakken.

Pagina “Algemeen”

![](../../../configuration-guide/new_add_control/hanglie.files/001.png)

Gegevensinstellingen

Totaal aantal velden: aantal kolommen van de tabel

Oorspronkelijk totaal aantal items: oorspronkelijk aantal rijen van de tabel

Aantal items per pagina: aantal getoonde rijen per pagina

Beginadres: adres van het eerste element van de tabel

Adresoffset: adresoffset van elke rij van de kolom

Adresvoorbeeld

Toont de adresverdeling van de tabel

Veldinstellingen

Huidig veld: huidige kolom

Veldtype: status, tekenreeks of numeriek

Veldbreedte: kolombreedte

Uitlijning: uitlijning van de elementen van de kolom

Totaal aantal statussen: totaal aantal statussen van het kolomelement

Geavanceerd

![](../../../configuration-guide/new_add_control/hanglie.files/002.png)

Status

Geselecteerde items: geselecteerde elementen

Werkelijk totaal aantal items: werkelijk aantal elementen

Totaal zichtbare items: totaal aantal zichtbare elementen

Huidige pagina: nummer van de huidige pagina

Totaal aantal pagina's: totaal aantal pagina's

Gegevens van de huidige pagina automatisch bijwerken: Ja: automatisch bijwerken; anders bestuurd door het ingestelde adres

Gegevens bijwerken: adres voor het bijwerken

Bediening

Onzichtbaarheidsbit: maakt de gegevens onzichtbaar

Onzichtbaarheidsniveau: voorwaarde waaronder de onzichtbaarheidsbit werkt

Triggeradres vorige pagina: naar de vorige pagina

Triggeradres volgende pagina: naar de volgende pagina

Triggeradres vorig item: selecteert het vorige item in deze kolom

Triggeradres volgend item: selecteert het volgende item in deze kolom

Triggeradres kopiëren: kopieert het huidige item

Triggeradres plakken: plakt gegevens

Triggeradres vervangen: overschrijft het huidige item met de geplakte gegevens

Triggeradres invoegen: voegt een item in bij het huidige item

Triggeradres knippen: knipt gegevens

Aanraakbeveiligingsbit: aanraakbeveiliging

Adres voor het geselecteerde item: stelt het te selecteren item in

Trigger selectie-item instellen: past de instelling van het selectie-item toe

Adres voor het totale aantal items: stelt het totale aantal items in

Trigger totaal aantal items: past de instelling van het totale aantal items toe

Geavanceerd 2

De tijdelijke opslag is een buffer waarin het element gegevens tijdelijk kan bewaren. Gegevens in de buffer kunnen bij geselecteerde items worden ingevoegd, toegevoegd of erin geschreven, en de gegevens van het geselecteerde item kunnen ook in de buffer worden ingelezen.

![](../../../configuration-guide/new_add_control/hanglie.files/003.png)

Tijdelijke opslag

Beginadres: beginadres van de tijdelijke opslag

Bit geselecteerd item invoegen: bij ON worden de gegevens in de buffer (adres: beginadres buffer + adresoffset item) bij het geselecteerde item ingevoegd en neemt het werkelijke aantal items met 1 toe. Heeft het werkelijke aantal items het maximum al bereikt, dan kan niets worden ingevoegd.

Bit geselecteerd item toevoegen: bij ON worden de gegevens in de buffer (adres: beginadres buffer + adresoffset item) aan het geselecteerde item toegevoegd en neemt het werkelijke aantal items met 1 toe. Heeft het werkelijke aantal items het maximum al bereikt, dan kan niets worden ingevoegd.

Aan het einde toevoegen: bij ON worden de gegevens in de buffer (adres: beginadres buffer + adresoffset item) aan het einde toegevoegd en neemt het werkelijke aantal items met 1 toe. Heeft het werkelijke aantal items het maximum al bereikt, dan kan niets worden ingevoegd.

Geselecteerd item lezen: bij ON wordt de inhoud van het geselecteerde item in de buffer ingelezen (adres: beginadres buffer + adresoffset item)

Geselecteerd item schrijven: bij ON worden de buffergegevens (adres: beginadres buffer + adresoffset item) in het geselecteerde item geschreven

Uiterlijk

![](../../../configuration-guide/new_add_control/hanglie.files/004.png)

Veldinstellingen

Stelt het tabelnummer enz. in

Stijl

Stelt rasterlijnen, achtergrondkleur, achtergrondkleur bij selectie enz. in
