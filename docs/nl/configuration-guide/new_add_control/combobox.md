# Keuzelijst

De keuzelijst toont een lijst met items die de gebruiker kan bekijken en kiezen. Na selectie van een item wordt de bijbehorende waarde naar het besturingsadres van het register geschreven.

Het pictogram in de werkbalk is<img src="../../../configuration-guide/new_add_control/combobox.files/combobox771.png" width="35" />; klik erop om het dialoogvenster van afbeelding 4-115 te openen:

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1012.png" width="677" />

Afbeelding 4-115   Pagina “Algemeen” van de keuzelijst

• Totaal aantal statussen: aantal statussen van dit object. Elk item staat voor een status en wordt in de lijst getoond. De waarde van het item kan naar \[Besturingsadres\] worden geschreven.

• Achtergrondkleur: kies de achtergrondkleur van het geselecteerde object

• Tekstkleur: kies de tekstkleur van het geselecteerde object

• Besturingsadres: schrijfadres

• Script gebruiken: voert het gekozen script uit bij aanraken.

Statusinstellingen: klik op de pagina “Statusinstellingen”; de volgende afbeelding verschijnt (afbeelding 4-116):

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1554.png" width="675" />

Afbeelding 4-116   Pagina “Statusinstellingen” van de keuzelijst

• Taal: gebruikt hetzelfde “lettertype” en dezelfde “lettergrootte” voor alle statussen, maar verschillende “lettertypen” en “lettergrootten” per taal.

• Waarde: stel een waarde in voor elk item, met inachtneming van de volgende twee regels:

a\. \[Lezen\]: detecteert het systeem een wijziging in de inhoud van \[Besturingsadres\], dan vergelijkt het object die inhoud met zijn waarden en kiest het eerste overeenkomende item. Komt geen item overeen, dan springt het naar de foutstatus en zet het de foutmeldingsbit (indien ingesteld).

b\. \[Schrijven\]: bij selectie van een item schrijft het systeem de waarde naar \[Besturingsadres\].

• Label: de gebruiker kan voor elk item een tekst instellen. Het menu toont de teksten van alle items in de lijst om te bekijken en te kiezen.

• Foutmelding

a\. Is \[Aantal statussen\] bijvoorbeeld 8, dan is status 8 de foutstatus. Evenzo is bij 11 status 11 de foutstatus.

b\. Bij een fout toont het keuzemenu de tekst van de foutstatus.

Bij een fout zet het systeem een bepaalde bit op ON / OFF (geschreven naar \[Adres foutmelding\]). Deze melding kan een bewerking starten om de fout te corrigeren.

Zie voor “Geavanceerd” en “Zichtbaarheid” de “Bit-knop”.
