# LW

LW

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Adres</th>
<th>Beschrijving</th>
<th>Opmerkingen</th>
<th>Lezen/schrijven</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>59010~59057</td>
<td>Blokkeert in uitgebreide modus de communicatie met het opgegeven station. Stations 0~255,<br />
elk adres komt overeen met 16 stationsnummers: 59010 met de stations 0~15, enz. Is bit X gelijk aan 1, dan is communicatie met station X toegestaan; bij 0<br />
is de communicatie met station X uitgeschakeld.</td>
<td>COM1: 59010~59025<br />
COM2: 59026~59041<br />
COM3: 59106~59121<br />
Ethernet: 59042~59057</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>59058~59105</td>
<td>Weergave van de communicatiestatus per station, stations 0~255.<br />
elk adres komt overeen met 16 stationsnummers: 59058 met de stations 0~15, enz. Is bit X gelijk aan 1,<br />
dan is de communicatie met dat station gestoord; bij 0 is ze normaal.</td>
<td>COM1: 59058~59073<br />
COM2: 59074~59089<br />
COM3: 59154~59169<br />
Ethernet: 59090~59105</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60000</td>
<td>Lokale tijd: seconden</td>
<td>BCD-code, geldig bereik 0-59</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60001</td>
<td>Lokale tijd</td>
<td>BCD-code, geldig bereik 0-59</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60002</td>
<td>Lokale tijd</td>
<td>BCD-code, geldig bereik 0-23</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60003</td>
<td>Lokale tijd: dag</td>
<td>BCD-code, geldig bereik 1-31</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60004</td>
<td>Lokale tijd: maand</td>
<td>BCD-code, geldig bereik 1-12</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60005</td>
<td>Lokale tijd: jaar</td>
<td>BCD-code, geldig bereik 0-9999</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60006</td>
<td>Lokale tijd: weekdag</td>
<td>BCD-code, geldig bereik 1-7</td>
<td>R</td>
</tr>
<tr class="even">
<td>60007</td>
<td>Bedrijfstijd</td>
<td>Bedrijfstijd van het systeem in uren</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60008</td>
<td>Bedrijfstijd</td>
<td>Verstreken tijd sinds het opstarten in minuten</td>
<td>R</td>
</tr>
<tr class="even">
<td>60009</td>
<td>Bedrijfstijd in seconden</td>
<td>Verstreken tijd sinds het opstarten in seconden</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60010</td>
<td>Nummer van het huidige scherm/venster</td>
<td>Nummer van het weergegeven scherm</td>
<td>R</td>
</tr>
<tr class="even">
<td>60012</td>
<td>Huidige taal</td>
<td>Nummer van de bijbehorende taal</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60013</td>
<td>Bovengrens van de numerieke invoer</td>
<td>Bij het openen van het aangepaste toetsenbord wordt de toegestane bovengrens als ASCII getoond</td>
<td>R</td>
</tr>
<tr class="even">
<td>60023</td>
<td>Ondergrens van de numerieke invoer</td>
<td>Bij het openen van het aangepaste toetsenbord wordt de toegestane ondergrens als ASCII getoond</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60033</td>
<td>Invoergegevens op het toetsenbord</td>
<td>Invoergegevens op het toetsenbord (getypte tekens), ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60065</td>
<td>Aangemelde gebruiker</td>
<td>Nummer van de huidige gebruiker</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60066</td>
<td>Wachtwoord van de aangemelde gebruiker</td>
<td>Toont het wachtwoord van de huidige gebruiker, 16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60074</td>
<td>Naam van de aangemelde gebruiker</td>
<td>Toont de naam van de huidige gebruiker, 32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60090</td>
<td>Gebruiker 1 geactiveerd</td>
<td>0 - uit, 1 - aan</td>
<td>R</td>
</tr>
<tr class="even">
<td>60091</td>
<td>Gebruiker 2 geactiveerd</td>
<td>0 - uit, 1 - aan</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60092</td>
<td>Gebruiker 3 geactiveerd</td>
<td>0 - uit, 1 - aan</td>
<td>R</td>
</tr>
<tr class="even">
<td>60093</td>
<td>Gebruiker 4 geactiveerd</td>
<td>0 - uit, 1 - aan</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60094</td>
<td>Gebruiker 5 geactiveerd</td>
<td>0 - uit, 1 - aan</td>
<td>R</td>
</tr>
<tr class="even">
<td>60095</td>
<td>Gebruiker 6 geactiveerd</td>
<td>0 - uit, 1 - aan</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60096</td>
<td>Gebruiker 7 geactiveerd</td>
<td>0 - uit, 1 - aan</td>
<td>R</td>
</tr>
<tr class="even">
<td>60097</td>
<td>Gebruiker 8 geactiveerd</td>
<td>0 - uit, 1 - aan</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60098</td>
<td>Naam van gebruiker 1</td>
<td>32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60114</td>
<td>Naam van gebruiker 2</td>
<td>32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60130</td>
<td>Naam van gebruiker 3</td>
<td>32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60146</td>
<td>Naam van gebruiker 4</td>
<td>32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60162</td>
<td>Naam van gebruiker 5</td>
<td>32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60178</td>
<td>Naam van gebruiker 6</td>
<td>32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60194</td>
<td>Naam van gebruiker 7</td>
<td>32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60210</td>
<td>Naam van gebruiker 8</td>
<td>32 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60226</td>
<td>Wachtwoord van gebruiker 1</td>
<td>16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60234</td>
<td>Wachtwoord van gebruiker 2</td>
<td>16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60242</td>
<td>Wachtwoord van gebruiker 3</td>
<td>16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60250</td>
<td>Wachtwoord van gebruiker 4</td>
<td>16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60258</td>
<td>Wachtwoord van gebruiker 5</td>
<td>16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60266</td>
<td>Wachtwoord van gebruiker 6</td>
<td>16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60274</td>
<td>Wachtwoord van gebruiker 7</td>
<td>16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="even">
<td>60282</td>
<td>Wachtwoord van gebruiker 8</td>
<td>16 tekens, ASCII-weergave</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60290</td>
<td>Tijd schermbeveiliging</td>
<td>Toont de in het project ingestelde tijd van de schermbeveiliging, bereik 0~60</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60291</td>
<td>Knipperperiode van de lampen</td>
<td>Knipperperiode van de lampobjecten, minimaal 0,1, in s</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60292</td>
<td>X-positie bij aanraken</td>
<td>X-coördinaat van het aangeraakte punt</td>
<td>R</td>
</tr>
<tr class="even">
<td>60293</td>
<td>Y-positie bij aanraken</td>
<td>Y-coördinaat van het aangeraakte punt</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60294</td>
<td>X-positie bij loslaten</td>
<td>X-coördinaat bij loslaten</td>
<td>R</td>
</tr>
<tr class="even">
<td>60295</td>
<td>Y-positie bij loslaten</td>
<td>Y-coördinaat bij loslaten</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60296</td>
<td>Aanraakstatus</td>
<td>1-aangeraakt, 0-losgelaten</td>
<td>R</td>
</tr>
<tr class="even">
<td>60297</td>
<td>Pariteit van COM1</td>
<td>Communicatieparameter, pariteit: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60298</td>
<td>Baudrate van COM1</td>
<td>Communicatieparameter, baudrate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60299</td>
<td>Stopbits van COM1</td>
<td>Communicatieparameter, stopbits: 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60300</td>
<td>Datalengte van COM1</td>
<td>Communicatieparameter, datalengte: 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60301</td>
<td>HMI-adres van COM1</td>
<td>Communicatieparameter, HMI-adres</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60302</td>
<td>PLC-adres van COM1</td>
<td>Communicatieparameter, PLC-adres</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60303</td>
<td>COM1: interval aaneengesloten PLC-adressen</td>
<td>Maximale lengte aaneengesloten adressen die in één communicatie worden gelezen</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60304</td>
<td>COM1: communicatietijd</td>
<td>Communicatievertraging</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60305</td>
<td>COM1: herhalingen</td>
<td>Aantal herhalingen bij gestoorde communicatie</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60306</td>
<td>COM1: adresmodus</td>
<td>Adresmodus: 0-standaard, 1-uitgebreid</td>
<td>R</td>
</tr>
<tr class="even">
<td>60307</td>
<td>COM1: time-out van de communicatie</td>
<td>Time-out van de communicatie in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60308</td>
<td>COM1: huidige wachttijd van de communicatie</td>
<td>Huidige wachttijd van de communicatie in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60309</td>
<td>COM1: locatie van de HMI</td>
<td>0-lokaal 1-op afstand</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60312</td>
<td>Pariteit van COM2</td>
<td>Communicatieparameter, pariteit: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60313</td>
<td>Baudrate van COM2</td>
<td>Communicatieparameter, baudrate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60314</td>
<td>Stopbits van COM2</td>
<td>Communicatieparameter, stopbits: 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60315</td>
<td>Datalengte van COM2</td>
<td>Communicatieparameter, datalengte: 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60316</td>
<td>HMI-adres van COM2</td>
<td>Communicatieparameter, HMI-adres</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60317</td>
<td>PLC-adres van COM2</td>
<td>Communicatieparameter, PLC-adres</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60318</td>
<td>COM2: interval aaneengesloten PLC-adressen</td>
<td>Maximale lengte aaneengesloten adressen die in één communicatie worden gelezen</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60319</td>
<td>COM2: communicatietijd</td>
<td>Communicatievertraging</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60320</td>
<td>COM2: herhalingen</td>
<td>Aantal herhalingen bij gestoorde communicatie</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60321</td>
<td>COM2: adresmodus</td>
<td>Adresmodus: 0-standaard, 1-uitgebreid</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60322</td>
<td>COM2: time-out van de communicatie</td>
<td>Time-out van de communicatie in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60323</td>
<td>COM2: huidige wachttijd van de communicatie</td>
<td>Huidige wachttijd van de communicatie in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60324</td>
<td>COM2: locatie van de HMI</td>
<td>0-lokaal, 1-op afstand</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61270</td>
<td>Pariteit van COM3</td>
<td>Communicatieparameter, pariteit: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61271</td>
<td>Baudrate van COM3</td>
<td>Communicatieparameter, baudrate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61272</td>
<td>Stopbits van COM3</td>
<td>Communicatieparameter, stopbits: 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61273</td>
<td>Datalengte van COM3</td>
<td>Communicatieparameter, datalengte: 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61274</td>
<td>HMI-adres van COM3</td>
<td>Communicatieparameter, HMI-adres</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61275</td>
<td>PLC-adres van COM3</td>
<td>Communicatieparameter, PLC-adres</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61276</td>
<td>COM3: interval aaneengesloten PLC-adressen</td>
<td>Maximale lengte aaneengesloten adressen die in één communicatie worden gelezen</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61277</td>
<td>COM3: communicatietijd</td>
<td>Communicatievertraging</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61278</td>
<td>COM3: herhalingen</td>
<td>Aantal herhalingen bij gestoorde communicatie</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61279</td>
<td>COM3: adresmodus</td>
<td>Adresmodus: 0-standaard, 1-uitgebreid</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61280</td>
<td>COM3: time-out van de communicatie</td>
<td>Time-out van de communicatie in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61281</td>
<td>COM3: huidige wachttijd van de communicatie</td>
<td>Huidige wachttijd van de communicatie in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61282</td>
<td>COM3: locatie van de HMI</td>
<td>0-lokaal, 1-op afstand</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60327</td>
<td>Aantal historische alarmen</td>
<td>Totaal aantal geregistreerde historische alarmen</td>
<td>L/dubbelwoord</td>
</tr>
<tr class="even">
<td>60329</td>
<td>Aantal historische gegevens</td>
<td>Totaal aantal geregistreerde historische gegevens</td>
<td>L/dubbelwoord</td>
</tr>
<tr class="odd">
<td>60333</td>
<td>Taal van het toetsenbord</td>
<td>1-Chinees toetsenbord, 0-Engels toetsenbord, voor het standaardtoetsenbord</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60334</td>
<td>CPU-belasting</td>
<td>CPU-belasting van het systeem</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60335</td>
<td>Huidige helderheid van de achtergrondverlichting</td>
<td>Huidige helderheid van de achtergrondverlichting (140~450)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60337</td>
<td>Aanmaakdatum project: jaar</td>
<td>Aanmaakjaar van het huidige projectbestand</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60338</td>
<td>Aanmaakdatum project: maand</td>
<td>Aanmaakmaand van het huidige projectbestand</td>
<td>R</td>
</tr>
<tr class="even">
<td>60339</td>
<td>Aanmaakdatum project: dag</td>
<td>Aanmaakdag van het huidige projectbestand</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60340</td>
<td>Huidige gebruikerstaal</td>
<td>Bepaalt de huidige taal</td>
<td>W</td>
</tr>
<tr class="even">
<td>60359</td>
<td>Bij 1 worden de historische alarmen van het opgegeven nummerbereik naar de USB-stick gekopieerd</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60361</td>
<td>Bij 1 worden de historische alarmen van het opgegeven tijdbereik naar de USB-stick gekopieerd</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60363</td>
<td>Export historische alarmen: beginnummer</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60365</td>
<td>Export historische alarmen: eindnummer</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60367</td>
<td>Export historische alarmen: begintijd</td>
<td>Lengte 6 woorden: jaar, maand, dag, uur, minuut en seconde.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60373</td>
<td>Export historische alarmen: eindtijd</td>
<td>Lengte 6 woorden: jaar, maand, dag, uur, minuut en seconde.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60379</td>
<td>Bestandsnaam bij export van historische alarmen naar USB-stick</td>
<td>Lengte 22 tekens</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60408</td>
<td>Besturingsadres van de huidige groep historische gegevens</td>
<td>Bepaalt de huidige groep historische gegevens</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60409</td>
<td>Bij 1 worden de historische gegevens van het opgegeven nummerbereik naar de USB-stick gekopieerd</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60411</td>
<td>Bij 1 worden de historische gegevens van het opgegeven tijdbereik naar de USB-stick gekopieerd</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60413</td>
<td>Export historische gegevens: beginnummer</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60415</td>
<td>Export historische gegevens: eindnummer</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60417</td>
<td>Export historische gegevens: begintijd</td>
<td>Lengte 6 woorden: jaar, maand, dag, uur, minuut en seconde.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60423</td>
<td>Export historische gegevens: eindtijd</td>
<td>Lengte 6 woorden: jaar, maand, dag, uur, minuut en seconde.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60429</td>
<td>Bestandsnaam bij export van historische gegevens naar USB-stick</td>
<td>Lengte 24 tekens</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60441</td>
<td>Buffer voor het wijzigen van het wachtwoord van gebruiker 1</td>
<td>Lengte 16 tekens, ASCII-weergave</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60449</td>
<td>Wijzigen van het wachtwoord van gebruiker 1 activeren</td>
<td>Bij 1 wordt het wachtwoord van gebruiker 1 vervangen door het wachtwoord in de buffer, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60451</td>
<td>Buffer voor het wijzigen van het wachtwoord van gebruiker 2</td>
<td>Lengte 16 tekens, ASCII-weergave</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60459</td>
<td>Wijzigen van het wachtwoord van gebruiker 2 activeren</td>
<td>Bij 1 wordt het wachtwoord van gebruiker 2 vervangen door het wachtwoord in de buffer, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60461</td>
<td>Buffer voor het wijzigen van het wachtwoord van gebruiker 3</td>
<td>Lengte 16 tekens, ASCII-weergave</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60469</td>
<td>Wijzigen van het wachtwoord van gebruiker 3 activeren</td>
<td>Bij 1 wordt het wachtwoord van gebruiker 3 vervangen door het wachtwoord in de buffer, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60471</td>
<td>Buffer voor het wijzigen van het wachtwoord van gebruiker 4</td>
<td>Lengte 16 tekens, ASCII-weergave</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60479</td>
<td>Wijzigen van het wachtwoord van gebruiker 4 activeren</td>
<td>Bij 1 wordt het wachtwoord van gebruiker 4 vervangen door het wachtwoord in de buffer, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60481</td>
<td>Buffer voor het wijzigen van het wachtwoord van gebruiker 5</td>
<td>Lengte 16 tekens, ASCII-weergave</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60489</td>
<td>Wijzigen van het wachtwoord van gebruiker 5 activeren</td>
<td>Bij 1 wordt het wachtwoord van gebruiker 5 vervangen door het wachtwoord in de buffer, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60491</td>
<td>Buffer voor het wijzigen van het wachtwoord van gebruiker 6</td>
<td>Lengte 16 tekens, ASCII-weergave</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60499</td>
<td>Wijzigen van het wachtwoord van gebruiker 6 activeren</td>
<td>Bij 1 wordt het wachtwoord van gebruiker 6 vervangen door het wachtwoord in de buffer, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60501</td>
<td>Buffer voor het wijzigen van het wachtwoord van gebruiker 7</td>
<td>Lengte 16 tekens, ASCII-weergave</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60509</td>
<td>Wijzigen van het wachtwoord van gebruiker 7 activeren</td>
<td>Bij 1 wordt het wachtwoord van gebruiker 7 vervangen door het wachtwoord in de buffer, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60511</td>
<td>Buffer voor het wijzigen van het wachtwoord van gebruiker 8</td>
<td>Lengte 16 tekens, ASCII-weergave</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60519</td>
<td>Wijzigen van het wachtwoord van gebruiker 8 activeren</td>
<td>Bij 1 wordt het wachtwoord van gebruiker 8 vervangen door het wachtwoord in de buffer, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60520</td>
<td>HMI-model</td>
<td>40 tekens</td>
<td>R</td>
</tr>
<tr class="even">
<td>60540</td>
<td>Bootloaderversie</td>
<td>40 tekens</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60560</td>
<td>Versie besturingssysteem</td>
<td>40 tekens</td>
<td>R</td>
</tr>
<tr class="even">
<td>60580</td>
<td>Softwareversie</td>
<td>40 tekens</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60600</td>
<td>Bedieningslogboek activeren</td>
<td>Bij 1 worden bedieningen gelogd</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60601</td>
<td>Aantal logboekregels</td>
<td>Toont het huidige aantal logboekregels</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60602</td>
<td>Schermafdruk activeren</td>
<td>Bij 1 wordt een schermafdruk gemaakt, daarna automatische reset</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60603</td>
<td>Opslaglocatie schermafdrukken</td>
<td>0-USB-stick</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60604</td>
<td>HMI-beveiliging activeren</td>
<td>Bij 1 wordt de HMI-beveiliging gebruikt</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60605</td>
<td>Aantal wachtwoordniveaus van de HMI-beveiliging</td>
<td>Aantal wachtwoordniveaus van de HMI-beveiliging, maximaal 15</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60606-60835</td>
<td>Geldigheidsduur van de HMI-beveiliging</td>
<td>60606-60628: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 1, en het ontgrendelwachtwoord (16 tekens)<br />
60629-60651: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 2, en het ontgrendelwachtwoord (16 tekens)<br />
60652-60674: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 3, en het ontgrendelwachtwoord (16 tekens)<br />
60675-60697: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 4, en het ontgrendelwachtwoord (16 tekens)<br />
60698-60720: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 5, en het ontgrendelwachtwoord (16 tekens)<br />
60721-60743: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 6, en het ontgrendelwachtwoord (16 tekens)<br />
60744-60766: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 7, en het ontgrendelwachtwoord (16 tekens)<br />
60767-60789: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 8, en het ontgrendelwachtwoord (16 tekens)<br />
60790-60812: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 9, en het ontgrendelwachtwoord (16 tekens)<br />
60813-60835: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 10, en het ontgrendelwachtwoord (16 tekens)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63000-63114</td>
<td>Geldigheidsduur van de HMI-beveiliging</td>
<td>63000-63022: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 11, en het ontgrendelwachtwoord (16 tekens)<br />
63023-63045: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 12, en het ontgrendelwachtwoord (16 tekens)<br />
63046-63068: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 13, en het ontgrendelwachtwoord (16 tekens)<br />
63069-63091: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 14, en het ontgrendelwachtwoord (16 tekens)<br />
63092-63114: jaar, maand, dag, uur, minuut, seconde en waarschuwingsscherm bij het verlopen van het wachtwoord van niveau 15, en het ontgrendelwachtwoord (16 tekens)</td>
<td></td>
</tr>
<tr class="odd">
<td>63115~63130</td>
<td>Invoeradres voor het wijzigen van het wachtwoord van het hoogste niveau</td>
<td>63115~63131: adres voor het wijzigen van het wachtwoord van het hoogste niveau (16 tekens); schrijf na invoer 1 naar LW63131 om het toe te passen</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63131</td>
<td>Activeringsadres van het wachtwoord van het hoogste niveau</td>
<td>63115~63130: schrijf na invoer van het wachtwoord van het hoogste niveau 1 naar dit adres om het toe te passen</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60836</td>
<td>Opslaan in de HMI</td>
<td>Bij 1 worden de instellingen van de HMI-beveiliging in de HMI opgeslagen, daarna automatische reset.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60837</td>
<td>HMI-beveiliging resetten</td>
<td>Zet de HMI-beveiliging terug naar de beginstatus. Reeds ontgrendelde gebruikers moeten opnieuw ontgrendelen</td>
<td>W</td>
</tr>
<tr class="odd">
<td>60997</td>
<td>Gebruik van de USB-ingang.</td>
<td>Standaard 0: USB-toetsenbord of -muis. Bij 1: barcodescanner</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60998</td>
<td>Eindteken van de USB-2D-barcodescanner: 0-ENTER, 1-TAB+ENTER</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60999</td>
<td>Codelengte van de USB-2D-barcodescanner</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61000 - 61127</td>
<td>Opslag en gebruik van de gelezen 2D-code</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61128</td>
<td>Gebruik van de printerparameters</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61138</td>
<td>Receptimport: ID van het bronrecept</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61139</td>
<td>Receptimport: ID van het doelrecept</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61140</td>
<td>ID van het te wissen recept</td>
<td>-1 bij weergave van de beginwaarde als 16-bits geheel getal; anders 65535</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61141</td>
<td>Wisselt de huidige receptgroep tijdens de werking van de HMI</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61143</td>
<td>Groepsnummer voor import/export van recepten via USB-stick</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61146</td>
<td>Nummer van het af te drukken venster bij registergestuurd afdrukken</td>
<td>Voer het nummer van het af te drukken venster in en zet LB60175 om het afdrukken te starten (automatische reset)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62020-62039</td>
<td>Naam van het huidige recept</td>
<td>ASCII-weergave, Unicode-codering, lengte 20; toont de naam van het huidige recept</td>
<td>R</td>
</tr>
<tr class="odd">
<td>62040</td>
<td>Keuze van het aanmeldniveau</td>
<td>Gebruikersniveau waarmee wordt aangemeld; komt overeen met het niveau dat is geactiveerd onder “Touchscreenparameters” → “Gebruikerswachtwoorden”</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62041~62056</td>
<td>Invoeradres van het aanmeldwachtwoord</td>
<td>Voer het wachtwoord in van het in 62040 ingestelde niveau. Het wachtwoord van het hoogste niveau ontgrendelt alle niveaus (16 tekens) en voltooit de aanmelding.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>62057</td>
<td>Register voor het aantal verlengingen van de HMI</td>
<td>Is in de HMI-beveiliging de verlengingsoptie geactiveerd, dan wordt hier het aantal verlengingen gewijzigd; standaardwaarde 1</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63141~63146</td>
<td>Vervaldatum van het dynamische wachtwoord</td>
<td>Jaar, maand, dag, uur, minuut, seconde: LW63141~63146, 16-bits geheel getal; zet na invoer van de datum LB60182 om die toe te passen (automatische reset)</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63147~63152</td>
<td>Adres van de sleutel van het dynamische wachtwoord</td>
<td>Wijzigt de sleutel van het dynamische wachtwoord, adres LW63147, type ASCII, lengte 6; zet LB60179 om die toe te passen (automatische reset)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63153~63184</td>
<td>Receptnaam wijzigen</td>
<td>ASCII-invoer, lengte 32; de wijziging wordt toegepast met LB60180</td>
<td>W</td>
</tr>
<tr class="odd">
<td>63186~63189</td>
<td>IP-adres van het Ethernet-apparaat</td>
<td>IP-adres van het Ethernet-apparaat in standaardmodus, 16-bits geheel getal. Zet na het instellen van IP, poort en stationsnummer LB60178 om ze toe te passen</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63190</td>
<td>Stationsnummer van het Ethernet-apparaat</td>
<td>Stationsnummer van het Ethernet-apparaat in standaardmodus, 16-bits geheel getal. IP, poort en stationsnummer worden toegepast met LB60178</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63191</td>
<td>Poort van het Ethernet-apparaat</td>
<td>Poort van het Ethernet-apparaat in standaardmodus, 16-bits geheel getal. Zet na het instellen van IP, poort en stationsnummer LB60178 om ze toe te passen</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60838~60853</td>
<td>Naam van de aangemelde gebruiker</td>
<td>Rechtenbeheer: toont de naam van de aangemelde gebruiker; object: ASCII-weergave, lengte 32</td>
<td>R</td>
</tr>
<tr class="odd">
<td>63200~63215</td>
<td>Groep van de aangemelde gebruiker</td>
<td>Rechtenbeheer: toont de groep van de aangemelde gebruiker (zijn eerste groep); object: ASCII-weergave, lengte 32</td>
<td>R</td>
</tr>
</tbody>
</table>
