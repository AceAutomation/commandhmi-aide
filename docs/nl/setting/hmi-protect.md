# HMI-beveiliging

Met de HMI-beveiliging stelt u een periode in waarin de HMI normaal werkt. Na afloop van die periode springt de HMI naar een bepaald scherm, waar een wachtwoord nodig is om de HMI weer te gebruiken.

Dubbelklik op de optie “HMI-beveiliging” in de “projectbeheerder” om het dialoogvenster van afbeelding 7-14 te openen:

<img src="../../setting/hmi-protect.files/hmi-protect343.png" width="622" />

Afbeelding 7-14    Dialoogvenster HMI-beveiliging

Voorbeeld van het gebruik van deze functie:

➢ “Wachtwoord voor ontgrendelen” aanvinken: de volgende keer is een wachtwoord nodig om de HMI-beveiliging te openen.

➢ “Alle niveaus vrijgeven” aanvinken: wordt dit wachtwoord bij het ontgrendelen van de HMI-beveiliging ingevoerd, dan worden alle beveiligingsniveaus opgeheven.

➢ “HMI-beveiliging” aanvinken: u gaat automatisch naar de pagina “Beveiligingsinstellingen”, zoals hieronder:

<img src="../../setting/hmi-protect.files/hmi-protect743.png" width="623" />

Afbeelding 7-15    Instellingen HMI-beveiliging

Stel het “totaal aantal wachtwoordniveaus” in op 3; kies niveau 1, kies in de kolom “Geldigheidsduur” onder “Parameterinstellingen” 2009-04-01 en 12-00-00; kies scherm 1 als “Meldingsscherm”; stel het “Ontgrendelwachtwoord” in op 1111. Daarmee is niveau 1 ingesteld.

Stel op dezelfde manier de geldigheidsduur en wachtwoorden van niveau 2 en 3 in.

• Alle niveaus opheffen

Met deze functie ingeschakeld en een wachtwoord ingesteld, heft het hier ingestelde wachtwoord alle niveaus van de HMI-beveiliging op

•  Wachtwoord bij het openen

Met deze functie ingeschakeld en een wachtwoord ingesteld, moet de volgende keer dit wachtwoord worden ingevoerd om de gegevens van de HMI-beveiliging te bekijken

•  Wachtwoordbeveiliging inschakelen

Schakelt de HMI-beveiliging in. De details worden in de beveiligingsinstellingen ingesteld.

• Beveiligingsinstellingen

Totaal aantal wachtwoordniveaus: tot 15 niveaus HMI-beveiliging voor verschillende perioden naar behoefte

Huidig wachtwoordniveau: de volgende parameters gelden voor het huidige niveau

Parameterinstellingen:

Geldigheidsduur: vervaldatum van de HMI-beveiliging

Meldingsscherm bij verlopen: scherm dat verschijnt als de HMI-beveiliging verloopt

Ontgrendelwachtwoord: wachtwoord dat de beveiliging na het verlopen opheft

Geavanceerde instellingen:

Resterende dagen tonen: toont hoeveel dagen er nog resten tot het einde van de ingestelde geldigheidsduur

Vooraf:

Stelt in hoeveel dagen vóór het einde van de geldigheidsduur van de HMI-beveiliging een melding verschijnt

Vertraging:

Na het einde van de geldigheidsduur verschijnt na het ingestelde aantal dagen, met het opgegeven interval, het opgegeven scherm

Prioriteit vooraf en vertraging

Vooraf aangevinkt, vertraging aangevinkt: vooraf geldt

Vooraf niet aangevinkt, vertraging aangevinkt: vertraging geldt

Vooraf aangevinkt, vertraging aangevinkt, functieknop “HMI-beveiliging uitstellen” niet gebruikt: vooraf geldt

Vooraf aangevinkt, vertraging aangevinkt, functieknop “HMI-beveiliging uitstellen” gebruikt: vertraging geldt

•  Voorbeeld van het gebruik:

Stel dat het totale aantal wachtwoordniveaus in dit venster 3 is. Kies daarna 0 bij “Huidig wachtwoordniveau”. Kies onder “Parameterinstellingen” in de kolom “Geldigheidsduur” de datum, bijvoorbeeld 2009/04/01, en in de volgende kolom de tijd, bijvoorbeeld 12:00:00. Kies bij “Meldingsscherm bij verlopen” het scherm dat verschijnt, bijvoorbeeld scherm 1, en voer bij “Ontgrendelwachtwoord” het wachtwoord in, bijvoorbeeld 1111. Daarmee is niveau 1 van de HMI-beveiliging ingesteld.

Kies vervolgens 1 bij “Huidig wachtwoordniveau”, kies onder “Parameterinstellingen” in de kolom “Geldigheidsduur” de datum, bijvoorbeeld 2009-04-05, en in de volgende kolom de tijd, bijvoorbeeld 12-00-00. Kies bij “Meldingsscherm bij verlopen” scherm 2 en voer bij “Ontgrendelwachtwoord” 2222 in. Daarmee is niveau 2 ingesteld.

Kies daarna 2 bij “Huidig wachtwoordniveau”, kies onder “Parameterinstellingen” in de kolom “Geldigheidsduur” de datum, bijvoorbeeld 2009-04-10, en in de volgende kolom de tijd, bijvoorbeeld 12-00-00. Kies bij “Meldingsscherm bij verlopen” scherm 3 en voer bij “Ontgrendelwachtwoord” 3333 in. Daarmee is niveau 3 ingesteld.

Klik na het instellen van de 3 niveaus op “OK”.

Stel dat het vandaag 2009-04-01 is, 08-00-00. De geldigheidsduur van niveau 1 is 2009-04-01 12-00-00; die is nog niet bereikt, dus de HMI werkt normaal. Vier uur later, om 12-00-00 op 2009-04-01, springt de HMI automatisch naar het voor deze periode ingestelde scherm. Om de HMI te blijven gebruiken en andere schermen te bedienen, plaatst de gebruiker in dat scherm (scherm 1) een functieknop met de functie “HMI-vergrendeling opheffen”. Na het verlopen van niveau 1 klikt hij op die knop en voert hij in het venster het ontgrendelwachtwoord van niveau 1 in, hier 1111, om de beveiliging op te heffen.

Na het ontgrendelen van niveau 1 werkt de HMI weer normaal. Stel dat het na enige tijd 2009-04-05 12-00-00 is: dan is de tijd van niveau 2 bereikt en springt de HMI automatisch naar het ingestelde beveiligingsscherm (scherm 2). Op dezelfde manier gebruikt de gebruiker de functieknop “HMI-vergrendeling opheffen” en voert hij het wachtwoord van niveau 2 (2222) in, waarna de HMI weer normaal werkt.

Omdat hier ook niveau 3 is ingesteld, moet de gebruiker om 12-00-00 op 2009-04-10 eveneens de functieknop “HMI-vergrendeling opheffen” gebruiken en het ontgrendelwachtwoord van niveau 3 (3333) invoeren, waarna de HMI weer normaal werkt.

Zijn alle 3 niveaus ontgrendeld, dan vervalt de HMI-beveiliging en werkt de HMI normaal.

Deze voorbeelden tonen het gebruik van de HMI-beveiliging. Voor andere aantallen niveaus is de werkwijze gelijk; de gebruiker kan zich op het bovenstaande baseren.
