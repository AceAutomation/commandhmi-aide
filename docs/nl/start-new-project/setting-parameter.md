# Parameters instellen en grafische objecten toevoegen

**Parameterinstellingen:**

1\. U wijzigt de parameters via “Voorkeuren” in het menu “Instellingen”, of door in de projectbeheerder onder “Instellingen” te dubbelklikken op [HMI-parameters](../setting/paramater.md). Het dialoogvenster van afbeelding 3-6 hieronder verschijnt:

<img src="../../start-new-project/setting-parameter.files/image001.jpg" width="643" alt="ScreenShot00218.jpg" />

Afbeelding 3-6     Dialoogvenster algemene parameters

• HMI-model: wijzigt het HMI-model.

• Weergavemodus: horizontale of verticale weergave van het scherm.

• Opstartinstellingen HMI

• Opstartscherm: het scherm dat de HMI na het inschakelen toont

• Tijd schermbeveiliging: stelt de tijd van de schermbeveiliging in

• Knipperfrequentie: knipperfrequentie van objecten die kunnen knipperen; u wijzigt de snelheid door direct een waarde in te voeren of met de pijltjes.

• Alarmgeluid: bij een alarm kan het touchscreen de gebruiker met een geluid waarschuwen; het vervolgmenu rechts biedt twee opties: met of zonder geluid.

• Aanraakgeluid: met de opties in het vervolgmenu rechts kiest u met of zonder geluid.

• Scherm schermbeveiliging: kies een bestaand scherm als schermbeveiliging; aanraken van het scherm brengt u terug naar het vorige scherm.

• Laadscherm: met deze optie toont de HMI na het inschakelen eerst enige tijd het gekozen laadscherm en daarna het opstartscherm; zo kunt u tips of opmerkingen tonen.

• Overige instellingen

• Muisaanwijzer verbergen: of de muisaanwijzer wordt getoond

• Floatinstellingen:

\[Standaard\]: hoge byte van de float eerst, lage byte daarna;

\[Aangepast\]: de gebruiker bepaalt de volgorde.

• Ongeldige aanraking: met “Aangepaste markering gebruiken” zijn aanraakbare objecten niet aanraakbaar en wordt het object gemarkeerd met de door de gebruiker gekozen afbeelding.

• Drukeffect van objecten tonen: CommandHMI kan nu een drukeffect tonen. Met dit effect verschijnt bij aanraking van een object een rechthoekig spoor in een door de gebruiker gekozen kleur. Momenteel ondersteunen bit-knop, woordknop, schermknop, functieknop, numerieke invoer en ASCII-invoer dit effect. Standaard is er geen effect.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2109.png" width="130" />

Ook bij elliptische objecten is het drukeffect een rechthoek.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2172.png" width="230" />

Afbeelding 3-7

2. Gebruikerswachtwoorden instellen

<img src="../../start-new-project/setting-parameter.files/setting-parameter2206.png" width="692" />

Afbeelding 3-8     Gebruikerswachtwoorden in het dialoogvenster HMI-parameters

Deze functie heeft 8 groepen gebruikerswachtwoorden, elk met acht niveaus.

• Standaardgebruikersniveau: het huidige standaardniveau is NULL.

• Uploaden van de configuratie toestaan: met deze optie kan het project van de HMI naar de pc worden geüpload; anders niet.

• Wachtwoord bij uploaden: of voor het uploaden van projecten een wachtwoord nodig is.

• Wachtwoord bij bijwerken via USB-stick: het ingestelde wachtwoord is nodig om het project in de HMI via een USB-stick bij te werken.

• Wachtwoord hoogste niveau: met dit wachtwoord kunnen alle objecten met niveaubeperking worden bediend.

• Uploaden: of dit wachtwoord het uploaden van projecten van de HMI naar de pc toestaat.

• Rechten: of dit wachtwoord alle beperkte bewerkingen mag uitvoeren.

**3. Instellingen voor printeraansluiting <span id="OLE_LINK247"></span><span id="OLE_LINK246"></span>en downloaden**

Klik op de knop “Instellingen printeraansluiting”, zoals in afbeelding 3-9:

<img src="../../start-new-project/setting-parameter.files/setting-parameter3209.png" width="693" />

Afbeelding 3-9      Instellingen verbinding HMI en printer

<span id="OLE_LINK245"></span><span id="OLE_LINK244"></span>Op deze pagina staan de parameters van de verbinding tussen printer en HMI; de gebruiker kiest ze volgens het printermodel.

**Downloadinstellingen:**

• Downloadwijze: kies USB of Ethernet. Bij Ethernet moeten het IP-adres en het poortnummer van de HMI worden ingesteld.

• Historische alarmen wissen: of de alarmgeschiedenis vóór het downloaden wordt gewist.

• Historische gegevens wissen: of de historische gegevens vóór het downloaden worden gewist.

• Recepten downloaden: of de recepten van het huidige project naar de HMI worden gedownload.

**Opties voor afbeeldingen:**

• Oorspronkelijk formaat behouden: het formaat van de afbeeldingen blijft bij het downloaden ongewijzigd.

• Naar JPG omzetten: alle afbeeldingen worden vóór het downloaden naar de HMI omgezet naar JPG.

(Opmerking: omdat BMP-afbeeldingen veel ruimte innemen, wordt deze optie aanbevolen.)

4. Opslaglocatie en alarmsysteem, zoals hieronder

<img src="../../start-new-project/setting-parameter.files/setting-parameter4305.png" width="692" />

Afbeelding 3-10   Dialoogvenster opslaglocatie en systeemalarm

• Opslaglocatie: locatie voor historische gegevens, historische alarmen en schermafdrukken. Er zijn opties “Lokaal (FLASH)” en “USB-stick”, naar behoefte. Standaard is dat Lokaal (FLASH).

• HMI-IP: netwerkparameters van het touchscreen

• Alarmsysteem

Alarmsysteem gebruiken: of het systeemalarm wordt gebruikt. Bij een alarm toont het alarmsysteem de huidige alarminformatie boven- of onderaan elk scherm, volgens de instellingen van de gebruiker.

Achtergrondkleur, tekstkleur, lettertype en lettergrootte van het alarm zijn eigenschappen van de alarmweergave van het systeem, naar behoefte in te stellen.

Weergavewijze: “Altijd tonen” toont het alarm voortdurend; “Cyclisch tonen” laat het alarm periodiek verschijnen en verdwijnen, wat een knippereffect geeft.

Positie van de alarmbalk: kies waar de alarmbalk verschijnt.

5. Overige instellingen, zoals hieronder

<img src="../../start-new-project/setting-parameter.files/setting-parameter5287.png" width="690" />

Afbeelding 3-11   Wachtwoord voor ontgrendelen schermbeveiliging

• Met deze optie aangevinkt moet de gebruiker dit wachtwoord invoeren om de schermbeveiliging te ontgrendelen.

<img src="../../start-new-project/setting-parameter.files/setting-parameter5429.png" width="130" />

Een gewijzigde tijd van de schermbeveiliging geldt pas als een “scherm voor de schermbeveiliging” is gekozen; aanraken van dat scherm brengt u terug naar het vorige scherm.
