# Functieknop

De functieknop is een essentieel object van de HMI: hiermee voert u eenvoudig en snel veel functies uit. Klik op <img src="../../../configuration-guide/basic-control/function-button.files/function-button143.png" width="28" /> om het eigenschappenvenster te openen, zoals in afbeelding 4-82:

<img src="../../../configuration-guide/basic-control/function-button.files/function-button223.png" width="660" />

Afbeelding 4-82 Dialoogvenster Functieknop

<img src="../../../configuration-guide/basic-control/function-button.files/function-button264.png" width="130" />

Opmerking: zie voor vorm, randkleur, voorgrondkleur, achtergrondkleur en patroon het object Bit-knop.

**1. Achtergrondverlichting uitschakelen**

Kies de functie “Achtergrondverlichting uitschakelen”. Een druk op de knop schakelt de verlichting uit, terwijl de HMI normaal blijft werken. Raak het scherm ergens aan om de verlichting weer in te schakelen.

**2. Alarm bevestigen**

Kies de functie “Alarm bevestigen”. Een druk op de knop bevestigt het geselecteerde alarm

**3. Opnieuw starten**

Met de functie “Systeem opnieuw starten” start het touchscreen opnieuw bij aanraken van deze knop.

**4. Tijd schermbeveiliging**

Met de functie “Tijd schermbeveiliging instellen” verschijnt bij aanraken van deze knop een venster om de tijd van de schermbeveiliging in te stellen.

**5. Recept naar de PLC schrijven**

Deze functie stuurt het recept naar de PLC. Een druk op de knop stuurt het in de HMI opgeslagen recept naar de aaneengesloten dataregisters van de PLC of een ander apparaat. (Het adres is het schrijfadres dat bij het aanmaken van het recept in de software is ingesteld.)

**6. Recept uit de PLC lezen**

Deze functie leest het recept uit de PLC. Een druk op de knop leest de receptgegevens uit de aaneengesloten dataregisters van de PLC of een ander apparaat. (Het adres is het schrijfadres dat bij het aanmaken van het recept in de software is ingesteld.)

**7. Datum en tijd instellen**

Deze functie stelt datum en tijd in: een druk op de knop stelt de interne datum en tijd in.

**8. Alarm wissen**

Deze functie wist het alarm: een druk op de knop wist het geselecteerde en bevestigde alarm.

**9. Vorig recept**

Met de functie “Vorig recept” opent een druk op de knop het recept vóór het huidige. Is het huidige recept het eerste of is er maar één recept, dan veranderen de parameters niet.

**10. Volgend recept**

Met de functie “Volgend recept” opent een druk op de knop het recept na het huidige. Is het huidige recept het laatste of is er maar één recept, dan veranderen de parameters niet.

**11. Huidig recept opslaan**

Deze functie slaat het huidige recept op: een druk op de knop slaat de receptgegevens op uit de aaneengesloten dataregisters van de PLC of een ander apparaat, die bij het aanmaken van het recept zijn ingesteld.

**12. Schermafdruk**

Met de functie “Schermafdruk” wordt het huidige scherm als afbeelding opgeslagen op de door de gebruiker opgegeven locatie. De naam kan met een ASCII-invoer worden ingevoerd; hij mag geen ：#￥%&\*-+&lt;&gt; enz. bevatten en mag maximaal 20 tekens lang zijn.

**13. Systeemparameters**

Met de functie “Systeemparameters” opent een druk op de knop op de HMI het scherm met systeemparameters, waar u systeemtijd, tijd van de schermbeveiliging, contrast van de achtergrondverlichting enz. kunt wijzigen.

**14. Aanmelden**

Met de functie “Aanmelden” verschijnt bij een druk op de knop een aanmeldvenster. Na het kiezen van de gebruikersnaam verschijnt een toetsenbord om het wachtwoord in te voeren en toegang te krijgen.

**15. Afmelden**

Met de functie “Afmelden” wordt de huidige gebruiker afgemeld en verliest hij zijn rechten; zijn niveau wordt het laagste.

**16. Alarmgeluid (ON / OFF)**

De functie “Alarmgeluid ON / OFF” laat een geluid horen bij een alarm; de functieknop schakelt dit aan of uit. Is het aan, dan dempt een druk op de knop het alarmgeluid, en omgekeerd

**17. Aanraakgeluid (ON / OFF)**

Met de functie “Aanraakgeluid” schakelt een aanraking van de knop het aanraakgeluid aan of uit. Is het aan, dan wordt het uitgeschakeld, en omgekeerd.

**18. Alle historische gegevens wissen**

De in de HMI opgeslagen historische gegevens worden gewist.

**19. Historische alarmen wissen**

De in de HMI opgeslagen historische alarmen worden gewist.

**20. HMI-beveiliging ontgrendelen**

Voer het wachtwoord in om de HMI-beveiliging op te heffen.

**21. Recept lezen en opslaan**

Leest en slaat het recept op.

**22. Reservefunctie**

Alleen als reservefunctie; voert geen bewerking uit.

**23. Recept opnieuw laden**

Laadt de receptgegevens uit flash opnieuw in het bijbehorende RWI-adres.

**24. Taal wisselen**

Zet de tekst van alle objecten om naar de opgegeven taal

**25. Scherm afdrukken op een seriële printer**

Drukt het ingestelde scherm af op een seriële printer. De verbinding van het printerstuurprogramma wordt ingesteld onder “HMI-parameters” -&gt; “Printer- en downloadinstellingen”, in het linkerdeel van de software.

**26. IP-configuratie slave-apparaten**

Deze functie vereist de “Uitgebreide modus”, in te stellen in de “Eigenschappen communicatiepoort”. Voor Ethernet-communicatie met meerdere apparaten moeten vóór het object een stationsnummer en het adres van het register dat dit stationsnummer bestuurt worden toegevoegd. Klik tijdens de werking van het project in de HMI op het functieobject: het door de gebruiker ingestelde stationsnummer verschijnt in het venster “IP config”; stel daar de IP-parameters van dat station in voor Ethernet-communicatie met meerdere apparaten.

**27. Functies van DIP-schakelaars 1 en 3**

Functies wanneer DIP-schakelaars 1 en 3 van de hardware op ON staan: vooral IP-instelling, systeemtijd en achtergrondverlichting. Klik na de instelling op “OK” om opnieuw te starten.

Script gebruiken: vink “Script gebruiken” aan om de lijst met scripts te tonen; de gebruiker kiest een script dat bij het uitvoeren van de functie wordt uitgevoerd. Alleen gecompileerde scripts staan in de lijst.

<img src="../../../configuration-guide/basic-control/function-button.files/function-button6119.png" width="130" />

Opmerking: bij het wisselen naar het systeemscherm wordt het huidige project gesloten; bij terugkeer wordt het project opnieuw gestart en verschijnt het startscherm van het project.

Opmerking: de pagina “Label” van de functieknop is vergelijkbaar met die van de Bit-knop, maar heeft geen Tekst status 1 en Afbeelding status 1, omdat er maar één status is.

Opmerking: de pagina's “Geavanceerd” en “Zichtbaarheid” van de functieknop zijn gelijk aan die van de Bit-knop; zie voor sneltoetsen de Bit-knop.

Opmerking: Vorig recept, Volgend recept, Recept opslaan en Recept lezen en opslaan werken alleen op de huidige receptgroep. Stel voor een andere groep eerst LW61141 in.

Opmerking: het wissen van historische gegevens wist alle groepen historische gegevens.

Klik na het instellen van alle eigenschappen op “OK” om de knop aan het werkgebied (het scherm) toe te voegen
