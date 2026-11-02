# Nieuw project aanmaken

Deze bewerking is nodig als u een nieuw project wilt aanmaken. Kies “Nieuw project” in het menu “Bestand” of klik op de knop “Nieuw project” <img src="../../start-new-project/new-project.files/new-project136.png" width="28" /> in de werkbalk. CommandHMI opent het dialoogvenster “Nieuw project”, waarin u naam en opslagpad van het project kiest. Kies het juiste HMI-model en klik op “OK” om het project aan te maken en naar het dialoogvenster met de instellingen van de communicatiepoort te gaan; met “Annuleren” sluit u het venster.

**1. Dialoogvenster Nieuw project**

Projectnaam:

Pad: opslagpad van het nieuwe projectbestand; standaard C: \\

Model: beschikbare modellen voor projecten:

HM-035AE(320\*240)        HM-035UE(320\*240)        HM-043AE()480\*272        HM-043D(480\*272)        HM-043AD(480-272)        HM-043BE(480\*272)        HM-043BS(480\*272)        HM-043QE(480\*272)        HM-043UE(480\*272)        HM-043TE(480\*272)        HM-050AS(480\*272)        HM-050AE(480\*272)        HM-050BS(800\*480)        HM-050BE(800\*480)        HM-057AE(640\*480)        HM-070AS(800\*480)        HM-070AE(800\*480)        HM-070BS(800\*480)        HM-070BE(800\*480)        HM-070GS(800\*480)        HM-070GE(800\*480)        HM-070QS(800\*480)        HM-070QE(800\*480)        HM-070GG(800\*480)        HM-070GW(800\*480)        HM-070MS(800\*480)        HM-070ME(800\*480)        HM-070MG(800\*480)        HM-070MW(800\*480)        HM-T070XS(1024\*600)        HM-102AS(800\*480)        HM-102AE(800\*480)        HM-102BS(1024\*600)        HM-102BE(1024\*600)        HM-102CW(1024\*600)        HM-102CG(1024\*600)        HM-102HE(1024\*600)        HM-102HS(1024\*600)        HM-121AS(800\*600)        HM-121AE(800\*600)        HM-H150AS(1024\*768)        HM-156QS(1920\*1080)

Het standaardmodel is HM-070AE(800\*480); de schermresolutie (800 \* 480) tussen haakjes wordt in het dialoogvenster niet getoond.

Weergavemodus: oriëntatie van het touchscreen van het project. Mogelijkheden:

Horizontaal: configuratie met het touchscreen horizontaal.

Verticaal: configuratie met het touchscreen verticaal.

Standaard is dat horizontaal.

<img src="../../start-new-project/new-project.files/image002.jpg" width="547" alt="ScreenShot00217.jpg" />

Afbeelding 3-1      Dialoogvenster Nieuw project

In de afbeelding hierboven staat het dialoogvenster “Nieuw project”, waarin u naam, pad, model en weergavemodus kiest; klik daarna op “Volgende” om de communicatiepoort in te stellen.

Het model hangt af van het HMI-model van de gebruiker.

<img src="../../start-new-project/new-project.files/new-project1533.png" width="130" />

De naam van het nieuwe project mag de volgende tekens niet bevatten: \\ /: \* "&lt;&gt; \|?.

De locatie van het nieuwe project mag de volgende tekens niet bevatten: \\ /: \* "&lt;&gt; \|?.

## 2. Dialoogvenster communicatie-instellingen

In het dialoogvenster communicatie-instellingen stelt u de parameters van de communicatiepoort van de HMI in. Alleen met correcte parameters communiceren PLC en touchscreen normaal. De parameters hangen af van het model van de aan te sluiten PLC.

Verbindingsnaam: naam van de communicatiepoort.

Apparaatdienst: keuze van PLC-merk en CPU-type.

Verbindingsinterface: kies een COM-poort of de ethernetpoort.

Interval aaneengesloten PLC-adressen: ruimte tussen aaneengesloten PLC-adressen; de standaardwaarde wordt aanbevolen.

##

<img src="../../start-new-project/new-project.files/new-project2298.png" width="624" />

Afbeelding 3-2      Dialoogvenster communicatie-instellingen

In de afbeelding hierboven staat het dialoogvenster voor de communicatiepoort, waarin de engineer de apparaatdienst kiest volgens het type aangesloten apparaat. Kies voor een ethernetverbinding de optie “Directe verbinding (Ethernet)” bij “Verbindingstype”.

Verbindings-ID: interne parameter, kan niet worden gewijzigd!

De communicatie-eigenschappen kunnen ook via de verbinding in de projectbeheerder worden ingesteld; de andere parameters staan in de communicatie-eigenschappen.

**3.       Schermeigenschappen**

Klik in het dialoogvenster communicatie-instellingen op “Volgende”; het dialoogvenster “Nieuw scherm” verschijnt, waarin u naam en achtergrondkleur van het scherm instelt. De standaardnaam is het schermnummer, de standaardachtergrondkleur blauw. Bij elk nieuw scherm kent de configuratiesoftware CommandHMI een schermnummer toe dat de volgorde van de schermen in het project aangeeft. De nummering begint bij 1: het eerste scherm heeft nummer 1, scherm 5 is het vijfde scherm. Om de achtergrondkleur te wijzigen, klikt u op de rechthoek achter “Achtergrondkleur” om de kleurkeuze te openen. Met meer dan tweehonderd kleuren om snel uit te kiezen biedt CommandHMI een zeer ruime kleurkeuze. Is dat nog niet genoeg, klik dan rechtsonder in het kleurvenster om een eigen kleur te maken. Kies in het venster “Aangepaste kleuren” eerst een basiskleur, daarna een kleur in het vierkante gebied in het midden; sleep met de muis om de gewenste kleur te kiezen; u kunt ook in de verticale balk rechts slepen en daarna op “OK” klikken. U kunt de kleurwaarden ook direct invoeren.

<img src="../../start-new-project/new-project.files/new-project4278.png" width="626" />

Afbeelding 3-3      Dialoogvenster Nieuw scherm

<img src="../../start-new-project/new-project.files/new-project4313.png" width="506" />

Afbeelding 3-4      Dialoogvenster kleurkeuze

De engineer kan ook een eigen afbeelding als achtergrond kiezen. Klik op het padpictogram om het pad van de afbeelding te kiezen.

<img src="../../start-new-project/new-project.files/new-project4463.png" width="331" />

Afbeelding 3-5      Pad van de afbeelding instellen

Klik op “OK” om deze stappen af te ronden; het systeem opent direct het nieuwe scherm. De voorbereidingen zijn klaar; nu kunt u het project bewerken.
