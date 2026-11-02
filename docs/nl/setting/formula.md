# Recept

In de productie beschrijft een recept de verhoudingen van de materialen voor een product: een reeks parameterinstellingen van variabelen die tijdens de productie worden gebruikt. Voor brood is bijvoorbeeld een basisrecept nodig, met de gewichten of verhoudingen van alle ingrediënten: water, bloem, suiker, eieren, olie enz. Het kan ook optionele ingrediënten vermelden, zoals fruit, noten, chocolade enz., die aan het basisrecept worden toegevoegd voor brood met verschillende smaken. Een ander voorbeeld is een staalfabriek: daar kan een recept een reeks machineparameters zijn. Bij batchprocessen kan een recept de verschillende stappen van de batch beschrijven.

Een machine kan zowel brood als cake maken, in verschillende smaken en vormen. Hier noemen we de ingrediëntenverhouding van brood een recept, en de verschillende verhoudingen voor verschillende smaken een bestand. Receptrecords staan dus in receptbestanden.

CommandHMI biedt een receptconfiguratie, bereikbaar via het menu “Recept” of via de projectbeheerder. Daar opent u het dialoogvenster van de receptconfiguratie en voegt u een nieuwe receptgroep toe. Zoals in afbeelding 7-32:

<img src="../../setting/formula.files/formula1334.png" width="515" />

Afbeelding 7-32 Eigenschappen continu recept

• Naam: naam van het huidige receptbestand.

• Beschrijving: beschrijving van het huidige receptbestand;

• Receptlengte: lengte en aantal van de door het huidige recept te lezen adressen. De adressen van de receptrecords worden automatisch door het systeem op volgorde gezet en kunnen niet worden gewijzigd. De maximale receptlengte is 4096.

• Totaal aantal: aantal recepten, maximaal 512;

• Huidige receptgroep bewerkbaar in de HMI: maakt het bewerken van het recept in de HMI mogelijk.

<img src="../../setting/formula.files/formula1872.png" width="794" />

Afbeelding 7-33 Eigenschappen discreet recept

• Groepsnaam: naam van het huidige receptbestand.

• Receptbeschrijving: beschrijving van het huidige receptbestand;

• Vlag recept geschreven: zodra het huidige recept naar de PLC is geschreven, wordt de waarde van het bitadres 1;

• Huidige receptgroep bewerkbaar in de HMI: maakt het bewerken van het recept in de HMI mogelijk.

<img src="../../setting/formula.files/formula2225.png" width="130" />

Opmerking: receptlengte \* bytes van het gegevenstype \* totaal aantal &lt;= 512KB

• Gegevenstype: gegevenstype van het gegevensregister;

• Recept naar PLC schrijven: bijbehorend gegevensregisteradres van recept en PLC;

• Recept uit PLC lezen: bijbehorend gegevensregisteradres van recept en PLC;

• Receptgeheugen: adresbereik van het recept in het geheugen van de HMI; automatisch gegenereerd en niet te wijzigen;

• Huidig recept: het receptadres in de HMI en het gegevensregister van de PLC worden automatisch op volgorde gegenereerd en kunnen niet worden gewijzigd;

• Receptnummerregister: de recepten worden automatisch op volgnummer gezet en kunnen niet worden gewijzigd; dit komt overeen met de volgorde van de receptnamen bij de gegevensitems.

De gegevensitems van het continue recept, zoals in afbeelding 7-33:

<img src="../../setting/formula.files/formula2990.png" width="514" />

Afbeelding 7-34 Pagina “Gegevensitems” continu recept

• Naam: naam van het huidige recept;

• Gegevens: schrijft en toont de waarde van elk adres van het huidige recept;

• Receptgegevens kopiëren: kopieert de gegevens van het bronrecept naar het doelrecept. Klik op “OK” om het huidige recept op te slaan en op “Annuleren” om het venster te sluiten. Na de receptconfiguratie kunnen de schermen voor het bedienen van het recept in de HMI worden ontworpen.

Toepassingsvoorbeeld recept:

1\. Maak een receptconfiguratie aan zoals hierboven beschreven. Het resultaat staat in afbeelding 7-34:

<img src="../../setting/formula.files/formula3531.png" width="515" />

Afbeelding 7-35  Functie receptgegevens kopiëren continu recept

Dit recept heeft in totaal 4 subrecepten met elk 16 items. De opslagadressen zijn RWI: 1 tot RWI: 16 in het geheugen van de HMI.

2. Na de receptconfiguratie kunt u het recept in het scherm tonen, wijzigen of direct naar de PLC downloaden. Daarvoor gebruikt u de volgende functieobjecten.

• Receptweergave: klik op numerieke weergave/invoer<img src="../../setting/formula.files/formula3946.png" width="23" /> (zie “Numerieke weergave/invoer”)

Kies het interne geheugenadres RWI: 0 om een numeriek weergave- en invoerobject in het scherm te maken. De ingevoerde en getoonde waarde is het volgnummer van het recept. De waarde 0 van RWI0 betekent receptnummer 1, de waarde 1 receptnummer 2, enz.

• Klik op de functieknop<img src="../../setting/formula.files/formula4264.png" width="21" />: zie de “Functieknop” voor de bediening.

Met functieknoppen met de bijbehorende functie kunnen knoppen worden gemaakt om het recept naar de PLC te schrijven, uit de PLC te lezen, op te slaan, en het vorige of volgende recept te kiezen.

Meerdere recepten: CommandHMI ondersteunt meerdere receptgroepen, maar slechts tien; anders verschijnt een melding zoals in 7-34-2

<img src="../../setting/formula.files/formula4682.png" width="248" />

Afbeelding 7-35-1

<img src="../../setting/formula.files/formula4698.png" width="321" />

Afbeelding 7-35-2

Met LW61141 wordt de receptgroep ingevoerd; RWI0 blijft dienen voor het receptnummer. Bij het kiezen van een recept moeten LW61141 en RWI0 dus samen worden ingesteld. Bijvoorbeeld: receptgroep 0 in LW61141 en volgnummer 2 in RWI0 kiest de gegevens van recept 2 in receptgroep 0.

3. Met de bovenstaande werkwijze kan een scherm worden gemaakt zoals in afbeelding 7-35:

Stel dat het te schrijven bewakingsadres D0 is, de receptlengte 16 en het totale aantal 4.

<img src="../../setting/formula.files/formula5250.png" width="746" />

Afbeelding 7-36 Resultaat van het recept

Met de functieknoppen en de numerieke weergave/invoer kunt u recepten eenvoudig wijzigen, opslaan, lezen en schrijven. Let wel op de volgende punten:

• De receptlijst moet worden aangemaakt voordat de receptfuncties worden gebruikt.

• Let bij het schrijven van receptparameters in de receptlijst op het gegevenstype. Een 16-bits gegeven neemt één woord in, een 32-bits gegeven twee woorden. Kies een consistent gegevenstype. Let vooral op bij 32-bits adressen: omdat een 32-bits gegeven twee woorden inneemt, moet u bij het invoeren van schrijf- en bewakingsadressen overlapping vermijden.

• Het adres RWI0 heeft een vaste functie en dient alleen om het receptnummer te wijzigen. De waarde 0 van RWI0 staat voor het eerste receptnummer, enz.

• De adressen van de receptparameters zijn opeenvolgend.

De gegevensitems van het discrete recept, zoals in afbeelding 7-33:

<img src="../../setting/formula.files/formula6181.png" width="795" />

Afbeelding 7-41  Pagina “Gegevensitems” discreet recept

• Totaal aantal recepten: aantal recepten, maximaal 128;

• Taal: de gebruiker kan per taal elementnamen en receptnamen instellen.

• Receptnaam: wijzigt de naam van het huidige recept, zoals “recept1”, “recept2”.

• Nieuw: opent het venster “Receptelement” om een element aan te maken, zoals in de afbeelding hieronder.

  <img src="../../setting/formula.files/formula6495.png" width="517" />

Afbeelding 7-42  Nieuw element discreet recept

• Verwijderen: verwijdert het huidige receptelement.

• Alles verwijderen: verwijdert alle elementen van dit recept.

• Wijzigen: opent het venster “Receptelement” van het huidige element om de gegevens te wijzigen.

• Exporteren: opent het venster “Opslaan als” om het recept als \*.csv-bestand op te slaan, met gekozen pad en naam.

• Importeren: opent het venster “Openen” om een \*.csv-bestand als huidig recept te kiezen.
