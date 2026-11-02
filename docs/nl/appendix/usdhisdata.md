# Gegevens exporteren via USB-stick

HMI's uit de HM-serie kunnen historische gegevens, recepten, historische alarmen en schermafdrukken naar een USB-stick exporteren.

Omdat CommandHMI meerdere groepen historische gegevens ondersteunt, moet bij het exporteren het groepsnummer worden opgegeven. LW60408 bevat het nummer van de gekozen groep. Bijvoorbeeld: is LW60408 gelijk aan 1, dan betreft de import en export via USB-stick alleen groep 0.

Opmerking: is de ingevoerde waarde groter dan het maximale aantal groepen min 1, dan werkt de functie niet.

**Historische gegevens exporteren naar een USB-stick**

1\. Steek de USB-stick in

2\. Geef in register LW60408 het groepsnummer van de te importeren/exporteren historische gegevens op.

3\. Zet LB60127 op ON: de HMI kopieert het groepsbestand naar de USB-stick met de naam hisdatai.csv; hisdata1.csv als het groepsnummer 1 is.

Zet LB60128 op ON en de HMI kopieert het groepsbestand naar de USB-stick; om groep 1 te importeren moet het bestand hisdata1.csv heten.

Deze triggers worden na de export automatisch op OFF teruggezet

Voor het exporteren van lokale gegevens worden de LW-registers LW60359-LW60429 gebruikt

**Recepten exporteren**

Omdat CommandHMI meerdere receptgroepen ondersteunt, moet voor het exporteren LW61143 worden ingesteld.

1\. Steek de USB-stick in.

2\. Geef het groepsnummer op in LW61143.

3\. Zet LB60163 op ON: de HMI kopieert het receptbestand van de groep naar de USB-stick

4\. Deze triggers worden na de export automatisch op OFF teruggezet

Opmerking: geëxporteerde historische gegevens kunnen op de computer niet direct worden geopend; hiervoor is het conversieprogramma SK_SQL_CSV.exe nodig, <img src="../../appendix/usdhisdata.files/image002.jpg" width="86" />dat in de hoofdmap van de HM-configuratiesoftware staat.

Dit programma zet het geëxporteerde bestand om in een CSV-bestand dat direct kan worden geopend. Dubbelklik om het te openen.

Voortgang: voortgang van de conversie.

Bestandsnaam: kies het om te zetten bestand.

Kies historische gegevens of alarmen. De codering is standaard ANSI en kan niet worden gewijzigd. Klik op “CSV aanmaken”; de conversie is voltooid als de voortgangsbalk 100 % bereikt.

**Schermafdrukken op een USB-stick opslaan**

1\. Steek de USB-stick in

2\. Maak in de configuratie een functieknop -&gt; Schermafdruk aan en kies “Exporteren naar USB-stick”

3\. Bij aanraken van deze functieknop slaat de HMI het huidige scherm op in het bijbehorende geheugen

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />

Opmerking:

 • Verwijder de USB-stick niet tijdens het exporteren;

• Houd de voeding ingeschakeld tijdens het exporteren;

• Zorg dat de USB-stick voldoende vrije ruimte heeft.

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />
