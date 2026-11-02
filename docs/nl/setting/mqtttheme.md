# Onderwerp

Ø  Publicatieonderwerp toevoegen

• Pagina “Algemeen”

![](../../setting/mqtttheme.files/addpublish.png)

- Naam

Projectnaam van het MQTT-onderwerp

- Onderwerp

Het onderwerp dat de MQTT-server ontvangt bij het verzenden van een bericht

- Formaat

\[JSON (algemeen)\]: gegevens in JSON-formaat met lijststructuur.

\[JSON (geavanceerd)\]: JSON-formaat met een vrij aanpasbare boomstructuur.

- Verzendmodus

**■  Automatisch**

Bij wijziging: de inhoud van het bewakingsadres wordt automatisch verzonden als die verandert.

Periodiek: de inhoud van het bewakingsadres wordt periodiek verzonden.

**■  Bittrigger**

De inhoud wordt verzonden als een opgegeven bitadres wordt geactiveerd.

• Adres (JSON algemeen)

Instelbaar als op de pagina \[Algemeen\] het formaat \[JSON algemeen\] is gekozen.
<img src="../../setting/mqtttheme.files/addgeneraladdr.png" width="606" />

Voegt een waarde toe. Het type kan bit of woord zijn; de waarde kan vast zijn of van een opgegeven adres worden gelezen.

• Adres (JSON geavanceerd)

Instelbaar als op de pagina \[Algemeen\] het formaat \[JSON geavanceerd\] is gekozen.
<img src="../../setting/mqtttheme.files/addextendaddr.png" width="606" />

De adresinstelling ondersteunt een boomstructuur met componenten, arrays enz.; tijdstempel en gegevensnaam kunnen ook worden aangepast.

- Element

Voegt een gegevenselement toe. Een component kan meerdere gegevens bevatten, elk met een eigen naam en waarde.

De gegevens van het element staan tussen accolades { }.

- Array

Voegt een gegevensarray toe. Een array kan meerdere gegevens bevatten, maar heeft slechts één naam.

De gegevens staan tussen vierkante haken \[ \].

- Waarde

Voegt een waarde, tekenreeks of tijdstempel toe. Een waarde of tekenreeks kan vast zijn of van een opgegeven adres worden gelezen.

- Sjabloon

Zet door de gebruiker bewerkte JSON-tekst om in een boomstructuur

- Voorbeeld

Zet de huidige boomstructuur om in JSON-tekst

• Pagina “Beveiliging”

Na inschakeling geldt dit als het ingestelde bitadres aan de triggervoorwaarde voldoet.
<img src="../../setting/mqtttheme.files/publishsecurity.png" width="606" />

Ø  Abonnementsonderwerp toevoegen

• Pagina “Algemeen”

<img src="../../setting/mqtttheme.files/addsubscribe.png" width="606" />

- Naam

Projectnaam van het MQTT-onderwerp

- Onderwerp

Onderwerp waarop bij de MQTT-server wordt geabonneerd

- Het formaat is

[zoals bij 【Publiceren】](#anchor-name)

- Bedrijfsmodus

■  Automatisch

automatisch.

■  Handmatig

Uitvoering via een opgegeven adres.

• Pagina “Adres”

[Zoals bij 【Publiceren】](#anchor-name)

• Pagina “Beveiliging”

[Zoals bij 【Publiceren】](#anchor-name)
