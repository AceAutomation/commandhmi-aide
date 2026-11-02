# Klok

De klokinstellingen omvatten drie functies: de systeemtijd naar de HMI downloaden, de tijd naar de PLC schrijven en met de PLC synchroniseren.

Dubbelklik op “Klok” in de projectbeheerder om de klokinstellingen te openen.

<img src="../../setting/clock.files/image004.jpg" width="388" />

<img src="../../setting/clock.files/image005.jpg" width="388" />

Afbeelding 7-11 Dialoogvenster klokinstellingen

Systeemklok naar HMI downloaden: of de systeemklok naar de HMI wordt gedownload.

• Tijd/datum naar PLC schrijven:

• Gegevenstype en lengte zijn standaardwaarden.

• Tijd: jaar-maand-dag-uur-minuut-seconde-weekdag. Zie LW 60000~LW 60006 bij de registeradressen. De weekdag van de systeemtijd kan niet worden gewijzigd.

Schrijfadres: de systeemtijd wordt naar dit PLC-adres geschreven.

• Startwijze:

Periodiek: schrijft de systeemtijd met het ingestelde interval naar het opgegeven PLC-adres.

Trigger: de systeemtijd wordt naar het opgegeven PLC-adres geschreven als het triggeradres 1 is.

Automatisch resetten: zet het triggeradres automatisch op 0 als het 1 is.

**Synchronisatie met de PLC-tijd:**

Gegevenstype en lengte zijn standaardwaarden.

 Tijd: jaar-maand-dag-uur-minuut-seconde-weekdag. Zie LW 60000~LW 60006 bij de registeradressen. De weekdag van de systeemtijd kan niet worden gewijzigd.

• Leesadres: de inhoud van dit PLC-adres wordt gelezen.

• Startwijze:

Periodiek: schrijft de systeemtijd met het ingestelde interval naar het opgegeven PLC-adres.

Trigger: de systeemtijd wordt met de PLC gesynchroniseerd als het triggeradres 1 is.

Automatisch resetten: zet het triggeradres automatisch op 0 als het 1 is.
