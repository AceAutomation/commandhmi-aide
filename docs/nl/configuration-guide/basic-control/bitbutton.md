# Bit-knop

De bit-knop bedient en toont de ON/OFF-status (1/0) van een bitadres van het met het touchscreen verbonden apparaat. Het is het meest elementaire en meest gebruikte object.

Een bit-knop instellen:

1\. Klik op het pictogram bit-knop<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton263.png" width="30" /> in de werkbalk om het eigenschappenvenster te openen, zoals in afbeelding 4-68:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton381.png" width="664" />

Afbeelding 4-68 Dialoogvenster Bit-knop

2\. Het dialoogvenster heeft vier pagina's: Algemeen, Label, Geavanceerd en Zichtbaarheid.

Vorm: klik op “Vorm” om de vorm van het object te kiezen, zoals in afbeelding 4-69

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton600.png" width="472" />

Afbeelding 4-69 Venster vormkeuze

• Randkleur: bij een vorm met rand kiest u hier een andere randkleur.

• Voorgrondkleur: om de voorgrondkleur te wijzigen, kiest u een kleur in de kleurenlijst (werkt alleen bij een verloopstijl).

• Achtergrondkleur: om de achtergrondkleur te wijzigen, kiest u een kleur in de kleurenlijst.

• Patroon: de lijst biedt 21 patronen, zoals in afbeelding 4-70:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton1213.png" width="662" />

Afbeelding 4-70 Vorm en patroon wijzigen

• Setten: met deze functie zet een druk op de bit-knop na het downloaden naar de HMI het schrijfadres op 1. Het schrijfadres van het aangesloten apparaat wordt ON en de status 1/ON wordt getoond.

• Resetten: met deze functie zet een druk op de bit-knop na het downloaden naar de HMI het schrijfadres op 0. Het schrijfadres van het aangesloten apparaat wordt OFF en de status 0/OFF wordt getoond.

• Tipfunctie (Inching): u kunt kiezen tussen “ingedrukt = 1” en “ingedrukt = 0”. Bij “ingedrukt = 1” wordt na het downloaden het schrijfadres van het apparaat 1/ON zolang de knop is ingedrukt en wordt 1/ON getoond; bij loslaten wordt het 0/OFF en wordt 0/OFF getoond. Bij “ingedrukt = 0” wordt het adres 0/OFF zolang de knop is ingedrukt en wordt 0/OFF getoond; bij loslaten wordt het 1/ON en wordt 1/ON getoond.

• Omschakelen: na het downloaden wordt het schrijfadres bij aanraken 1/ON als de huidige status 0/OFF is en wordt 1/ON getoond; is de status 1/ON, dan wordt het 0/OFF en wordt 0/OFF getoond. De status wisselt bij elke aanraking.

• Schrijfadres: klik op het toetsenbordpictogram naast “Schrijfadres” om het adres in te voeren. CommandHMI geeft de adressymbolen van het aangesloten apparaat. Bij de MITSUBISHI FX-2N-serie is X bijvoorbeeld het adres van een ingangsspoel, Y van een uitgangsspoel, M van een hulprelais (merker), C van een teller (status), T van een timer (status), D van een dataregister, C \* van een teller (tellerwaarde) en T \* van een timer (tellerwaarde). Bij de SIEMENS S7-200-serie is I het ingangsadres, Q het uitgangsadres, M het merkeradres en V het dataregisteradres. Zoals in afbeelding 4-71:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton3963.png" width="251" />

Afbeelding 4-71 Adresinvoer

Zo wordt de huidige status van de bit-knop met het juiste adressymbool naar de PLC of een ander apparaat geschreven. Het schrijf- of weergaveadres is 0/OFF als de knop 0/OFF is, en 1/ON als het object 1/ON is.

• Bewaken: vink “Bewaken” aan om het “Bewakingsadres” te tonen; de bit-knop toont dan de wijzigingen van dat adres. Het bewakingsadres is 0/OFF als de knop 0/OFF is, en 1/ON als hij 1/ON is. Bewakings- en schrijfadres mogen verschillen. Bij de functie “Setten” zet aanraken het schrijfadres bijvoorbeeld op 1/ON, maar staat het bewakingsadres op 0/OFF, dan toont de knop nog 0/OFF. Meestal kiest u “Bewakingsadres gelijk aan schrijfadres” om de geschreven waarde direct te zien.

• Script: vink “Script gebruiken” aan om de lijst met scripts te tonen. De gebruiker kiest een script dat bij het indrukken van de bit-knop wordt uitgevoerd. Alleen gecompileerde scripts staan in de lijst.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5308.png" width="130" />

Is “Bewaken” niet aangevinkt, dan verandert de status van de knop niet, ook niet als het object wordt aangeraakt.

**Label**

Op het tabblad “Label” staan de eigenschappen van de tekst van status 0, zoals in afbeelding 4-72:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5512.png" width="664" />

Afbeelding 4-72 Pagina “Label” van de bit-knop

De pagina heeft vier onderdelen: “Tekst status 0”, “Tekst status 1”, “Afbeelding status 0” en “Afbeelding status 1”.

• Tekst status 0, Tekst status 1: wijzigen lettertype, lettergrootte, marge, kleur en positie van de tekst van status 0 of 1. CommandHMI kan de eigenschappen van de ene status naar de andere kopiëren, wat praktisch is en tijd bespaart.

• Alle teksten in de eerste taal: optie voor meertalige projecten (“Taal” in de projectbeheerder). Bij meer dan één taal zorgt deze optie dat de inhoud van het object niet met de taal meewisselt.

• Taal: optie voor meertalige projecten: voer de inhoud per taal in. (Kies in de functieknop “Taal wisselen” en de doeltaal; in de simulatie of op de HMI worden alle objecten met tekst dan in die taal getoond). Tekst, lettertype en lettergrootte kunnen per taal verschillen; kleur, tekenafstand en positie zijn gemeenschappelijk

• Lettertype: lettertype van de tekst; elke taal kan een eigen lettertype hebben.

• Lettergrootte: grootte van de tekst; elke taal kan een eigen grootte hebben.

• Kleur, marge, positie: kleur, marge en uitlijning van de geselecteerde tekst. Bij meerdere talen gelden de waarden van taal 1 en hebben deze opties bij de andere talen geen effect.

• Afbeelding status 0, Afbeelding status 1: hiermee voegt u per status afbeeldingen van verschillende formaten toe volgens de “Afbeeldingsbron”. De gekozen afbeelding wordt automatisch aan de pagina “Algemeen” toegevoegd. Met “Aanpassen aan objectgrootte” krijgt de afbeelding de grootte van het object.

• Aanpassen aan objectgrootte: indien aangevinkt krijgt de afbeelding de grootte van het object en worden de opties marge en positie verborgen.

• Importeert u een afbeelding uit een extern bestand, dan verschijnt de optie “Transparantie” om een bepaalde kleur transparant te maken

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton7699.png" width="130" />

Met “Knipperen” knippert de weergave in de ON/OFF-status. De standaardfrequentie is 1 s. Om die te wijzigen, dubbelklikt u in de projectbeheerder op “HMI-parameters” en past u de “Knipperfrequentie” aan.

Kies de pagina “Geavanceerd” om de eigenschappen te tonen, zoals in afbeelding 4-73

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8062.png" width="660" />

Afbeelding 4-73  Pagina “Geavanceerd” van de bit-knop

• Bitgestuurd: is de “Geldige status” 1, dan reageert de bit-knop alleen als het “Stuurbit” 1 is. Is de “Geldige status” 0, dan reageert hij alleen als het “Stuurbit” 0 is. In alle andere gevallen werkt de knop niet.

• Gestuurd door gebruikersniveau: de gebruiker kan meerdere opties aanvinken. In de simulatie of op de HMI wordt gecontroleerd of de huidige gebruiker die bevoegdheid heeft.

Bijvoorbeeld: zijn op de pagina “Geavanceerd” van het object de opties 2 en 3 van de niveaubesturing aangevinkt, en zijn de gebruikerswachtwoorden in de touchscreenparameters zoals in afbeelding 4-74:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8900.png" width="692" />

Afbeelding 4-74 Gebruikerswachtwoorden in de touchscreenparameters

Is het standaard gebruikersniveau NULL, dan reageert het object niet; met de functie “Gebruikersniveau wijzigen” van een functieknop kunt u het niveau wijzigen. Voert de gebruiker bijvoorbeeld 6666 in (niveau 6), dat alleen optie 1 heeft en niet 2 of 3, dan meldt het systeem dat het wachtwoord onjuist is; voert hij 2222 of 3333 in, dan hebben beide gebruikers optie 2, die overeenkomt met 2 of 3: het wachtwoord is geldig en het object reageert. Is het standaardniveau gebruiker 2 of 3, dan hebben beide optie 2 en reageert het object vanaf het begin in de simulatie of op het scherm; is het gebruiker 6, dan is er geen overeenkomst en reageert het object niet. De standaardinstellingen staan in de afbeelding hieronder:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton9956.png" width="459" />

Is “Gebruikersniveau wijzigen indien onvoldoende” aangevinkt, dan verschijnt bij een niet-passend niveau een aanmeldvenster om een passend niveau te kiezen en opnieuw aan te melden, zoals hieronder:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton10150.png" width="466" />

In CommandHMI hebben alleen de objecten bit-knop, keuzelijst, ASCII-invoer, functieknop, ASCII-toetsenbordinvoer, multifunctionele knop, meerstandenknop, receptkeuze, schermknop, keuzerondje, stapknop, woordknop, schuifregelaar en numerieke invoer deze functie; het gebruik is gelijk aan dat van de bit-knop.

• Minimale druktijd: aantal seconden dat moet worden gedrukt voordat het object in de simulatie of op de HMI reageert.

• Melding: reageert het object in de simulatie of op de HMI, dan wordt na een klik erop en invoer van een waarde via het pop-uptoetsenbord de status (1 of 0) naar het adres van het “Meldingsbit” geschreven.

• Meldingsregister: reageert het object in de simulatie of op de HMI, dan wordt na een klik erop en invoer van een waarde via het pop-uptoetsenbord die waarde naar het adres van het “Meldingsregister” geschreven.

• Sneltoets: met deze functie heeft een cijfer of teken hetzelfde effect als het indrukken van het object. Met 1 heeft bijvoorbeeld het indrukken van 1 op het numerieke toetsenbord in de simulatie of op de HMI, of op een extern toetsenbord, hetzelfde effect.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11418.png" width="161" />

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11420.png" width="130" />

Het standaard gebruikersniveau is NULL, het laagste. De ontwerper kan het wijzigen met de functie “Gebruikersniveau wijzigen” van een functieknop en het bijbehorende wachtwoord.

Een effectieve aanraking is een aanraking die een echte actie veroorzaakt: setten, resetten, tippen, omschakelen, enz. Een ander voorbeeld is de numerieke invoer: bij aanraken verschijnt het toetsenbord, maar er volgt geen melding omdat er niets naar het adres wordt geschreven. Het toetsenbord met ESC verlaten geeft ook geen melding. Alleen als een waarde tussen minimum en maximum wordt ingevoerd en op ENTER wordt gedrukt, volgt een melding.

Kies de pagina “Zichtbaarheid” om de eigenschappen te tonen die bepalen of het object wordt getoond of verborgen. Zoals in afbeelding 4-75

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12372.png" width="675" />

Afbeelding 4-75 Pagina “Zichtbaarheid” van de bit-knop

• Bitgestuurd: indien aangevinkt en de geldige status 1, wordt de bit-knop alleen op het touchscreen getoond als het stuurbit 1 is; is de geldige status 0, dan alleen als het stuurbit 0 is.

• Gestuurd door gebruikersniveau: de voorwaarden zijn gelijk aan die van de overeenkomstige optie op de pagina “Geavanceerd”; de knop wordt alleen getoond als eraan is voldaan.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12995.png" width="130" />

Is geen van beide opties aangevinkt, dan wordt het object altijd getoond.
