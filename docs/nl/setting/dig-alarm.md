# Digitale alarmregistratie

De alarminstellingen dienen om alarminformatie te tonen; alleen daarmee werken alarmweergave en alarmbalk normaal (zij tonen namelijk de berichten van de “digitale alarmregistratie” en de “analoge alarmregistratie”).

Klik in de projectbeheerder met de rechtermuisknop op “Alarmregistratie” en kies “Nieuw digitaal alarm”, zoals in afbeelding 7-22:

<img src="../../setting/dig-alarm.files/image001.jpg" width="274" alt="ScreenShot00094.jpg" />

Afbeelding 7-22    Alarmregistratie kiezen

Dubbelklik op de optie “Digitale alarmregistratie” om het dialoogvenster met de digitale alarminstellingen te openen, zoals in afbeelding 7-23:

<img src="../../setting/dig-alarm.files/dig-alarm508.png" width="558" />

Afbeelding 7-23    Opeenvolgende bits kiezen

Een digitale alarmregistratie maakt u als volgt:

• Voer eerst het leesadres in; hier wordt het interne adres LB1 gebruikt.

• Kies in de kolom “Aantal” het totale aantal alarmen, dus het totale aantal opeenvolgende bitadressen. Hier wordt 6 aangenomen.

• Stel de “Scantijd” van het bitalarm in, dus de scanfrequentie.

• Klik op een item in de lijst en ga met de muis naar de module “Bericht” rechts; voer in het tekstvak “Tekst” de alarminhoud in. Hier wordt aangenomen dat de berichten zijn zoals in afbeelding 7-23.

• Is “Gebruiken” aangevinkt, dan verschijnt de alarminformatie in de “alarmweergave” of de “alarmbalk”. Anders verschijnt het bericht niet, ook niet als het adres 1 is. Is de adreswaarde 0, dan verschijnt de alarminformatie niet.

• OFF-alarm: met deze optie aangevinkt ontstaat het alarm als de adreswaarde 0 (OFF) is; anders als de adreswaarde 1 (ON) is. Standaard ontstaat het alarm bij de waarde 1 (ON).

• U-export: exporteert de alarminstellingen

• U-import: importeert de alarminstellingen

Een voorbeeld: stel dat het type “Opeenvolgende bits” is.

• Is de waarde van LB1 0, dan verschijnt de alarminformatie niet in de “alarmweergave” en de “alarmbalk”, ongeacht of “Gebruiken” is aangevinkt.

• Is de waarde van LB1 1 en is “Gebruiken” niet aangevinkt, dan verschijnt de alarminformatie niet in de “alarmweergave” en de “alarmbalk”.

• Is de waarde van LB1 1 en is “Gebruiken” aangevinkt, dan verschijnt de alarminformatie in de “alarmweergave” en de “alarmbalk”.

Klik op “OK” om de digitale alarminstellingen af te ronden. Voeg 6 bit-knoppen met de functie “Omschakelen” toe met de adressen LB1-LB6, plaats een “alarmweergave” en een “alarmbalk” in het scherm en start de offline simulatie om te controleren of de alarminformatie verschijnt.

Hieronder een voorbeeld van de offline simulatie, zoals in afbeelding 7-24:

<img src="../../setting/dig-alarm.files/dig-alarm2644.png" width="1182" />

Afbeelding 7-24    Offline simulatie van een digitaal alarm

Is het type “Opeenvolgende bits van een woord”, zoals in afbeelding 7-25 hieronder:

<img src="../../setting/dig-alarm.files/dig-alarm2789.png" width="559" />

Afbeelding 7-25    Opeenvolgende bits van een woord kiezen

Is “Gebruiken” van een bepaald bitnummer aangevinkt, dan ontstaat een alarm als die bit 1 is.

<img src="../../setting/dig-alarm.files/dig-alarm2952.png" width="130" />

Opmerking: kopieert u alarmteksten uit andere documenten naar de alarmtekst van de digitale of analoge alarmregistratie, controleer dan of het bericht geen (onzichtbare) regeleinden bevat. Voer de berichten liever handmatig in dan te kopiëren en te plakken, om weergavefouten te vermijden.

Is het type “Woordwaarde”, zoals in afbeelding 7-26 hieronder:

<img src="../../setting/dig-alarm.files/dig-alarm3352.png" width="556" />

Afbeelding 7-26    Digitaal alarm van het type “Woordwaarde”

Is een waarde van het adres gekozen, dan ontstaat het alarm als de waarde van het adres gelijk is aan de in de lijst gekozen waarde.

Plaats een alarmweergave met 7 regels zoals in het voorbeeld van afbeelding 7-24 en een dynamische alarmbalk met de eigenschappen van afbeelding 7-27:

<img src="../../setting/dig-alarm.files/dig-alarm3691.png" width="675" />

Afbeelding 7-27    Eigenschappen dynamische alarmbalk

Voeg tot slot zes bit-knoppen toe met schrijfadres LB1-LB6 en de functies “Omschakelen”, “Bewaken” en “Bewakingsadres gelijk aan schrijfadres”. Klik daarna op de knop “Opslaan” in de werkbalk, kies “Offline” in het menu “Downloaden” en klik op de bit-knoppen LB1, LB2, LB4 en LB6. De alarmweergave en de dynamische alarmbalk tonen dan de alarminformatie van LB1, LB2, LB4 en LB6 uit het “digitale alarm”. Klikt u er opnieuw op, dan tonen “alarmweergave” en “dynamische alarmbalk” niets meer, omdat de waarden door de omschakelfunctie 0 zijn.

<img src="../../setting/dig-alarm.files/dig-alarm4400.png" width="130" />

Opmerking: met de functie taal wisselen is per taal andere alarminformatie mogelijk.

Opmerking: de HMI's van de HM-serie ondersteunen maximaal 10 digitale alarmen.
