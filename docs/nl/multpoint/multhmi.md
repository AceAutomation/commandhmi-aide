# Verbinding “één machine, meerdere schermen”

De touchscreens van de HMI-serie van CommandHMI ondersteunen via het MODBUS-protocol de verbinding “één machine, meerdere schermen” met een PLC. Alle touchscreens worden achter elkaar verbonden en het eerste scherm met de PLC. Alle touchscreens kunnen als slave worden ingesteld en de PLC als master: dubbelklik in de projectbeheerder op “Verbinding COM1”; in het venster met de eigenschappen van de communicatiepoort kiest u op de pagina “Algemeen” bij de apparaatdienst Modbus RTU en rechts Modbus RTU Slave. Of het eerste met de PLC verbonden touchscreen wordt master en de PLC en de andere schermen slave: kies dan bij het eerste scherm op de pagina “Algemeen” Modbus RTU en rechts Modbus RTU Master, zet op de pagina “Parameters” de modus op “Uitgebreide modus” en wijs de adressen van de touchscreens toe. De als slave ingestelde touchscreens communiceren dan via het eerste touchscreen met de PLC. In beide opstellingen communiceert alleen de master met de slaves; onderling communiceren de slaves niet.

Met de PLC als master en alle touchscreens als slave:

1. De communicatiepoort van de PLC is RS232; aansluiting en systeeminstellingen staan in afbeelding 8-1, 8-2 en 8-3:

<img src="../../multpoint/multhmi.files/multhmi1428.png" width="577" />

Afbeelding 8-1  Schema “één machine, meerdere schermen” met de PLC (RS232) als master

<img src="../../multpoint/multhmi.files/multhmi1528.png" width="589" />

Afbeelding 8-2 MODBUS-protocol kiezen en als slave instellen

<img src="../../multpoint/multhmi.files/multhmi1593.png" width="588" />

Afbeelding 8-3 Stationsadres van de HMI toewijzen

2. De communicatiepoort van de PLC is RS485; de aansluiting staat in afbeelding 8-4:

<img src="../../multpoint/multhmi.files/multhmi1744.png" width="598" />

Afbeelding 8-4  Schema “één machine, meerdere schermen” met de PLC (RS485) als master

Is de communicatiepoort van de PLC RS485 en zijn alle touchscreens slave, dan zijn de systeeminstellingen gelijk aan die bij RS232. Zie afbeelding 8-2 en 8-3.

Zijn alle schermen van de HMI-serie slave, dan kunnen tot 255 schermen worden aangesloten. Met veel touchscreens wordt de reactie echter traag.

 Met het eerste touchscreen als master en de PLC en alle andere schermen als slave:

1. De communicatiepoort van de PLC is RS232; aansluiting en systeeminstellingen staan in afbeelding 8-5, 8-6 en 8-7:

<img src="../../multpoint/multhmi.files/multhmi2462.png" width="579" />

Afbeelding 8-5   Schema “één machine, meerdere schermen” met de PLC (RS232) als slave

<img src="../../multpoint/multhmi.files/multhmi2563.png" width="588" />

Afbeelding 8-6 MODBUS-protocol kiezen voor het eerste scherm en dit als master instellen

<img src="../../multpoint/multhmi.files/multhmi2650.png" width="590" />

Afbeelding 8-7 Uitgebreide modus vereist als het eerste touchscreen master is

De systeeminstellingen van de touchscreens die slave zijn, zijn gelijk aan die van afbeelding 8-2 en 8-3.

<img src="../../multpoint/multhmi.files/multhmi2852.png" width="130" />

Opmerking: RS232 ondersteunt geen multidrop. Heeft de PLC bij de verbinding “één machine, meerdere schermen” geen RS485-poort, dan is een communicatieadapter nodig die RS485 naar RS232 omzet.

Opmerking: is bij de verbinding “één machine, meerdere schermen” een touchscreen van de HMI-serie master, dan moet de adresmodus van dat touchscreen op meerdere protocollen zijn ingesteld.

Met Modbus als master kunnen in principe tot 255 slaves worden toegevoegd; hoe meer slaves, hoe trager de communicatie.
