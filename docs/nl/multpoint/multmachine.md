# Verbinding “één scherm, meerdere machines”

De HMI-serie ondersteunt via het MODBUS-protocol niet alleen “één machine, meerdere schermen” maar ook “één scherm, meerdere machines”. Daarbij bedient één touchscreen direct de registeradressen van meerdere aangesloten PLC's, mits die het MODBUS-protocol ondersteunen. Kies bij de systeeminstelling op de pagina “Algemeen” bij de apparaatdienst Modbus RTU en rechts Modbus RTU Master: het touchscreen is dan master en alle PLC's zijn slave. Het touchscreen kan dan de registeradressen van de PLC's bedienen. De registernamen van de PLC's komen overeen met die van het MODBUS-protocol.

<img src="../../multpoint/multmachine.files/multmachine744.png" width="506" />

Afbeelding 8-8      Verbinding “één scherm, meerdere machines”

<img src="../../multpoint/multmachine.files/multmachine805.png" width="590" />

Afbeelding 8-9      Touchscreen als master instellen

<img src="../../multpoint/multmachine.files/multmachine857.png" width="588" />

Afbeelding 8-10    Uitgebreide modus vereist als het touchscreen master is

Na deze instelling gelden de PLC-adressen in de eigenschappen van de communicatiepoort niet meer. Klikt de gebruiker op een object om een adres in te voeren, dan verschijnt het adresinvoervenster van afbeelding 8-11. Rechts van de registernaam staat een vervolgkeuzelijst; het daar gekozen nummer is het slave-adres van de PLC.

<img src="../../multpoint/multmachine.files/multmachine1294.png" width="251" />

Afbeelding 8-11    Adresinvoervenster

<img src="../../multpoint/multmachine.files/multmachine1326.png" width="130" />

**Besturingsadressen voor het in-/uitschakelen van de communicatie per station in uitgebreide modus:**

Per seriële poort zijn 16 woorden gereserveerd voor de stationsnummers, dus maximaal 256 bestuurbare stations, met LW59000 als basisadres

COM1 komt overeen met 59010~59025: LW59010 met de stations 0~15, LW59011 met de stations 16~31, enz.

COM2 komt overeen met 59026~59041: LW59026 met de stations 0~15, LW59027 met de stations 16~31, enz.

Ethernet komt overeen met 59026~59041: LW59026 met de stations 0~15, LW59027 met de stations 16~31, enz.

Bij het starten van de HMI zijn standaard alle bits aan; met een script kunt u per bit de verbinding met een station starten of stoppen.

<img src="../../multpoint/multmachine.files/multmachine1993.png" width="130" />

Opmerking: RS232 ondersteunt geen multidrop. Heeft de PLC bij de verbinding “één scherm, meerdere machines” geen RS485-poort, dan is een communicatieadapter nodig die RS485 naar RS232 omzet.
