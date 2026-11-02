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
<th>Adresse</th>
<th>Beschreibung</th>
<th>Hinweise</th>
<th>Lesen/Schreiben</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>59010~59057</td>
<td>Im erweiterten Modus wird die Kommunikation mit der angegebenen Station gesperrt. Stationen 0~255,<br />
jede Adresse entspricht 16 Stationsnummern: 59010 entspricht den Stationen 0~15 usw. Ist Bit X gleich 1, ist die Kommunikation mit Station X erlaubt; bei 0<br />
ist die Kommunikation mit Station X abgeschaltet.</td>
<td>COM1: 59010~59025<br />
COM2: 59026~59041<br />
COM3: 59106~59121<br />
Ethernet: 59042~59057</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>59058~59105</td>
<td>Anzeige des Kommunikationsstatus je Station, Stationen 0~255.<br />
jede Adresse entspricht 16 Stationsnummern: 59058 entspricht den Stationen 0~15 usw. Ist Bit X gleich 1,<br />
ist die Kommunikation mit dieser Station gestört; bei 0 ist sie normal.</td>
<td>COM1: 59058~59073<br />
COM2: 59074~59089<br />
COM3: 59154~59169<br />
Ethernet: 59090~59105</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60000</td>
<td>Ortszeit: Sekunden</td>
<td>BCD-Code, gültiger Bereich 0-59</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60001</td>
<td>Ortszeit</td>
<td>BCD-Code, gültiger Bereich 0-59</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60002</td>
<td>Ortszeit</td>
<td>BCD-Code, gültiger Bereich 0-23</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60003</td>
<td>Ortszeit: Tag</td>
<td>BCD-Code, gültiger Bereich 1-31</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60004</td>
<td>Ortszeit: Monat</td>
<td>BCD-Code, gültiger Bereich 1-12</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60005</td>
<td>Ortszeit: Jahr</td>
<td>BCD-Code, gültiger Bereich 0-9999</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60006</td>
<td>Ortszeit: Wochentag</td>
<td>BCD-Code, gültiger Bereich 1-7</td>
<td>R</td>
</tr>
<tr class="even">
<td>60007</td>
<td>Systemlaufzeit</td>
<td>Laufzeit des Systems in Stunden</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60008</td>
<td>Systemlaufzeit</td>
<td>Seit dem Start vergangene Zeit in Minuten</td>
<td>R</td>
</tr>
<tr class="even">
<td>60009</td>
<td>Systemlaufzeit in Sekunden</td>
<td>Seit dem Start vergangene Zeit in Sekunden</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60010</td>
<td>Nummer des aktuellen Bildes/Fensters</td>
<td>Nummer des angezeigten Bildes</td>
<td>R</td>
</tr>
<tr class="even">
<td>60012</td>
<td>Aktuelle Sprache</td>
<td>Nummer der zugehörigen Sprache</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60013</td>
<td>Obergrenze der numerischen Eingabe</td>
<td>Beim Öffnen der benutzerdefinierten Tastatur wird die zulässige Obergrenze als ASCII angezeigt</td>
<td>R</td>
</tr>
<tr class="even">
<td>60023</td>
<td>Untergrenze der numerischen Eingabe</td>
<td>Beim Öffnen der benutzerdefinierten Tastatur wird die zulässige Untergrenze als ASCII angezeigt</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60033</td>
<td>Auf der Tastatur angezeigte Eingabedaten</td>
<td>Auf der Tastatur angezeigte Eingabedaten (eingetippte Zeichen), ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60065</td>
<td>Angemeldeter Benutzer</td>
<td>Nummer des aktuellen Benutzers</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60066</td>
<td>Passwort des angemeldeten Benutzers</td>
<td>Zeigt das Passwort des aktuellen Benutzers an, 16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60074</td>
<td>Name des angemeldeten Benutzers</td>
<td>Zeigt den Namen des aktuellen Benutzers an, 32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60090</td>
<td>Benutzer 1 aktiviert</td>
<td>0 - deaktiviert, 1 - aktiviert</td>
<td>R</td>
</tr>
<tr class="even">
<td>60091</td>
<td>Benutzer 2 aktiviert</td>
<td>0 - deaktiviert, 1 - aktiviert</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60092</td>
<td>Benutzer 3 aktiviert</td>
<td>0 - deaktiviert, 1 - aktiviert</td>
<td>R</td>
</tr>
<tr class="even">
<td>60093</td>
<td>Benutzer 4 aktiviert</td>
<td>0 - deaktiviert, 1 - aktiviert</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60094</td>
<td>Benutzer 5 aktiviert</td>
<td>0 - deaktiviert, 1 - aktiviert</td>
<td>R</td>
</tr>
<tr class="even">
<td>60095</td>
<td>Benutzer 6 aktiviert</td>
<td>0 - deaktiviert, 1 - aktiviert</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60096</td>
<td>Benutzer 7 aktiviert</td>
<td>0 - deaktiviert, 1 - aktiviert</td>
<td>R</td>
</tr>
<tr class="even">
<td>60097</td>
<td>Benutzer 8 aktiviert</td>
<td>0 - deaktiviert, 1 - aktiviert</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60098</td>
<td>Name von Benutzer 1</td>
<td>32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60114</td>
<td>Name von Benutzer 2</td>
<td>32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60130</td>
<td>Name von Benutzer 3</td>
<td>32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60146</td>
<td>Name von Benutzer 4</td>
<td>32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60162</td>
<td>Name von Benutzer 5</td>
<td>32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60178</td>
<td>Name von Benutzer 6</td>
<td>32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60194</td>
<td>Name von Benutzer 7</td>
<td>32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60210</td>
<td>Name von Benutzer 8</td>
<td>32 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60226</td>
<td>Passwort von Benutzer 1</td>
<td>16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60234</td>
<td>Passwort von Benutzer 2</td>
<td>16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60242</td>
<td>Passwort von Benutzer 3</td>
<td>16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60250</td>
<td>Passwort von Benutzer 4</td>
<td>16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60258</td>
<td>Passwort von Benutzer 5</td>
<td>16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60266</td>
<td>Passwort von Benutzer 6</td>
<td>16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60274</td>
<td>Passwort von Benutzer 7</td>
<td>16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="even">
<td>60282</td>
<td>Passwort von Benutzer 8</td>
<td>16 Zeichen, ASCII-Anzeige</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60290</td>
<td>Bildschirmschoner-Zeit</td>
<td>Zeigt die in der Projektierung festgelegte Bildschirmschoner-Zeit an, Bereich 0~60</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60291</td>
<td>Blinkperiode der Lampen</td>
<td>Blinkperiode der Lampenobjekte, mindestens 0,1, in s</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60292</td>
<td>X-Position bei Berührung</td>
<td>X-Koordinate des berührten Punkts</td>
<td>R</td>
</tr>
<tr class="even">
<td>60293</td>
<td>Y-Position bei Berührung</td>
<td>Y-Koordinate des berührten Punkts</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60294</td>
<td>X-Position beim Loslassen</td>
<td>X-Koordinate beim Loslassen</td>
<td>R</td>
</tr>
<tr class="even">
<td>60295</td>
<td>Y-Position beim Loslassen</td>
<td>Y-Koordinate beim Loslassen</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60296</td>
<td>Berührungszustand</td>
<td>1-berührt, 0-losgelassen</td>
<td>R</td>
</tr>
<tr class="even">
<td>60297</td>
<td>Parität von COM1</td>
<td>Kommunikationsparameter, Parität: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60298</td>
<td>Baudrate von COM1</td>
<td>Kommunikationsparameter, Baudrate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60299</td>
<td>Stoppbits von COM1</td>
<td>Kommunikationsparameter, Stoppbits: 0-1 Bit, 1-2 Bit</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60300</td>
<td>Datenlänge von COM1</td>
<td>Kommunikationsparameter, Datenlänge: 0-7 Bit, 1-8 Bit</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60301</td>
<td>HMI-Adresse von COM1</td>
<td>Kommunikationsparameter, HMI-Adresse</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60302</td>
<td>PLC-Adresse von COM1</td>
<td>Kommunikationsparameter, SPS-Adresse</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60303</td>
<td>COM1: Intervall zusammenhängender SPS-Adressen</td>
<td>Maximale Länge zusammenhängender Adressen, die in einer Kommunikation gelesen werden</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60304</td>
<td>COM1: Kommunikationszeit</td>
<td>Kommunikationsverzögerung</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60305</td>
<td>COM1: Wiederholungen</td>
<td>Anzahl der Wiederholungen bei gestörter Kommunikation</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60306</td>
<td>COM1: Adressmodus</td>
<td>Adressmodus: 0-Standard, 1-erweitert</td>
<td>R</td>
</tr>
<tr class="even">
<td>60307</td>
<td>COM1: Kommunikations-Timeout</td>
<td>Timeout der Kommunikation in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60308</td>
<td>COM1: aktuelle Wartezeit der Kommunikation</td>
<td>Aktuelle Wartezeit der Kommunikation in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60309</td>
<td>COM1: Standort des HMI</td>
<td>0-lokal 1-entfernt</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60312</td>
<td>Parität von COM2</td>
<td>Kommunikationsparameter, Parität: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60313</td>
<td>Baudrate von COM2</td>
<td>Kommunikationsparameter, Baudrate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60314</td>
<td>Stoppbits von COM2</td>
<td>Kommunikationsparameter, Stoppbits: 0-1 Bit, 1-2 Bit</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60315</td>
<td>Datenlänge von COM2</td>
<td>Kommunikationsparameter, Datenlänge: 0-7 Bit, 1-8 Bit</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60316</td>
<td>HMI-Adresse von COM2</td>
<td>Kommunikationsparameter, HMI-Adresse</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60317</td>
<td>PLC-Adresse von COM2</td>
<td>Kommunikationsparameter, SPS-Adresse</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60318</td>
<td>COM2: Intervall zusammenhängender SPS-Adressen</td>
<td>Maximale Länge zusammenhängender Adressen, die in einer Kommunikation gelesen werden</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60319</td>
<td>COM2: Kommunikationszeit</td>
<td>Kommunikationsverzögerung</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60320</td>
<td>COM2: Wiederholungen</td>
<td>Anzahl der Wiederholungen bei gestörter Kommunikation</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60321</td>
<td>COM2: Adressmodus</td>
<td>Adressmodus: 0-Standard, 1-erweitert</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60322</td>
<td>COM2: Kommunikations-Timeout</td>
<td>Timeout der Kommunikation in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60323</td>
<td>COM2: aktuelle Wartezeit der Kommunikation</td>
<td>Aktuelle Wartezeit der Kommunikation in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60324</td>
<td>COM2: Standort des HMI</td>
<td>0-lokal, 1-entfernt</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61270</td>
<td>Parität von COM3</td>
<td>Kommunikationsparameter, Parität: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61271</td>
<td>Baudrate von COM3</td>
<td>Kommunikationsparameter, Baudrate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61272</td>
<td>Stoppbits von COM3</td>
<td>Kommunikationsparameter, Stoppbits: 0-1 Bit, 1-2 Bit</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61273</td>
<td>Datenlänge von COM3</td>
<td>Kommunikationsparameter, Datenlänge: 0-7 Bit, 1-8 Bit</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61274</td>
<td>HMI-Adresse von COM3</td>
<td>Kommunikationsparameter, HMI-Adresse</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61275</td>
<td>PLC-Adresse von COM3</td>
<td>Kommunikationsparameter, SPS-Adresse</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61276</td>
<td>COM3: Intervall zusammenhängender SPS-Adressen</td>
<td>Maximale Länge zusammenhängender Adressen, die in einer Kommunikation gelesen werden</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61277</td>
<td>COM3: Kommunikationszeit</td>
<td>Kommunikationsverzögerung</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61278</td>
<td>COM3: Wiederholungen</td>
<td>Anzahl der Wiederholungen bei gestörter Kommunikation</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61279</td>
<td>COM3: Adressmodus</td>
<td>Adressmodus: 0-Standard, 1-erweitert</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61280</td>
<td>COM3: Kommunikations-Timeout</td>
<td>Timeout der Kommunikation in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61281</td>
<td>COM3: aktuelle Wartezeit der Kommunikation</td>
<td>Aktuelle Wartezeit der Kommunikation in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61282</td>
<td>COM3: Standort des HMI</td>
<td>0-lokal, 1-entfernt</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60327</td>
<td>Anzahl historischer Alarme</td>
<td>Gesamtzahl der erfassten historischen Alarme</td>
<td>L/Doppelwort</td>
</tr>
<tr class="even">
<td>60329</td>
<td>Anzahl historischer Datensätze</td>
<td>Gesamtzahl der erfassten historischen Datensätze</td>
<td>L/Doppelwort</td>
</tr>
<tr class="odd">
<td>60333</td>
<td>Tastatursprache</td>
<td>1-chinesische Tastatur, 0-englische Tastatur, für die Standardtastatur</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60334</td>
<td>CPU-Auslastung</td>
<td>CPU-Auslastung des Systems</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60335</td>
<td>Aktuelle Helligkeit der Hintergrundbeleuchtung</td>
<td>Aktuelle Helligkeit der Hintergrundbeleuchtung (140~450)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60337</td>
<td>Erstellungsdatum des Projekts: Jahr</td>
<td>Erstellungsjahr der aktuellen Projektdatei</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60338</td>
<td>Erstellungsdatum des Projekts: Monat</td>
<td>Erstellungsmonat der aktuellen Projektdatei</td>
<td>R</td>
</tr>
<tr class="even">
<td>60339</td>
<td>Erstellungsdatum des Projekts: Tag</td>
<td>Erstellungstag der aktuellen Projektdatei</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60340</td>
<td>Aktuelle Benutzersprache</td>
<td>Legt die aktuelle Sprache fest</td>
<td>W</td>
</tr>
<tr class="even">
<td>60359</td>
<td>Bei 1 werden die historischen Alarme des angegebenen Nummernbereichs auf den USB-Stick kopiert</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60361</td>
<td>Bei 1 werden die historischen Alarme des angegebenen Zeitbereichs auf den USB-Stick kopiert</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60363</td>
<td>Export historischer Alarme: Startnummer</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60365</td>
<td>Export historischer Alarme: Endnummer</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60367</td>
<td>Export historischer Alarme: Startzeit</td>
<td>Länge 6 Worte: Jahr, Monat, Tag, Stunde, Minute und Sekunde.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60373</td>
<td>Export historischer Alarme: Endzeit</td>
<td>Länge 6 Worte: Jahr, Monat, Tag, Stunde, Minute und Sekunde.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60379</td>
<td>Dateiname beim Export historischer Alarme auf USB-Stick</td>
<td>22 Zeichen lang</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60408</td>
<td>Steueradresse der aktuellen Gruppe historischer Daten</td>
<td>Legt die aktuelle Gruppe historischer Daten fest</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60409</td>
<td>Bei 1 werden die historischen Daten des angegebenen Nummernbereichs auf den USB-Stick kopiert</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60411</td>
<td>Bei 1 werden die historischen Daten des angegebenen Zeitbereichs auf den USB-Stick kopiert</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60413</td>
<td>Export historischer Daten: Startnummer</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60415</td>
<td>Export historischer Daten: Endnummer</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60417</td>
<td>Export historischer Daten: Startzeit</td>
<td>Länge 6 Worte: Jahr, Monat, Tag, Stunde, Minute und Sekunde.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60423</td>
<td>Export historischer Daten: Endzeit</td>
<td>Länge 6 Worte: Jahr, Monat, Tag, Stunde, Minute und Sekunde.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60429</td>
<td>Dateiname beim Export historischer Daten auf USB-Stick</td>
<td>24 Zeichen lang</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60441</td>
<td>Puffer zum Ändern des Passworts von Benutzer 1</td>
<td>16 Zeichen lang, ASCII-Anzeige</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60449</td>
<td>Ändern des Passworts von Benutzer 1 freigeben</td>
<td>Bei 1 wird das Passwort von Benutzer 1 durch das Passwort im Puffer ersetzt, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60451</td>
<td>Puffer zum Ändern des Passworts von Benutzer 2</td>
<td>16 Zeichen lang, ASCII-Anzeige</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60459</td>
<td>Ändern des Passworts von Benutzer 2 freigeben</td>
<td>Bei 1 wird das Passwort von Benutzer 2 durch das Passwort im Puffer ersetzt, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60461</td>
<td>Puffer zum Ändern des Passworts von Benutzer 3</td>
<td>16 Zeichen lang, ASCII-Anzeige</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60469</td>
<td>Ändern des Passworts von Benutzer 3 freigeben</td>
<td>Bei 1 wird das Passwort von Benutzer 3 durch das Passwort im Puffer ersetzt, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60471</td>
<td>Puffer zum Ändern des Passworts von Benutzer 4</td>
<td>16 Zeichen lang, ASCII-Anzeige</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60479</td>
<td>Ändern des Passworts von Benutzer 4 freigeben</td>
<td>Bei 1 wird das Passwort von Benutzer 4 durch das Passwort im Puffer ersetzt, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60481</td>
<td>Puffer zum Ändern des Passworts von Benutzer 5</td>
<td>16 Zeichen lang, ASCII-Anzeige</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60489</td>
<td>Ändern des Passworts von Benutzer 5 freigeben</td>
<td>Bei 1 wird das Passwort von Benutzer 5 durch das Passwort im Puffer ersetzt, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60491</td>
<td>Puffer zum Ändern des Passworts von Benutzer 6</td>
<td>16 Zeichen lang, ASCII-Anzeige</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60499</td>
<td>Ändern des Passworts von Benutzer 6 freigeben</td>
<td>Bei 1 wird das Passwort von Benutzer 6 durch das Passwort im Puffer ersetzt, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60501</td>
<td>Puffer zum Ändern des Passworts von Benutzer 7</td>
<td>16 Zeichen lang, ASCII-Anzeige</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60509</td>
<td>Ändern des Passworts von Benutzer 7 freigeben</td>
<td>Bei 1 wird das Passwort von Benutzer 7 durch das Passwort im Puffer ersetzt, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60511</td>
<td>Puffer zum Ändern des Passworts von Benutzer 8</td>
<td>16 Zeichen lang, ASCII-Anzeige</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60519</td>
<td>Ändern des Passworts von Benutzer 8 freigeben</td>
<td>Bei 1 wird das Passwort von Benutzer 8 durch das Passwort im Puffer ersetzt, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60520</td>
<td>HMI-Modell</td>
<td>40 Zeichen</td>
<td>R</td>
</tr>
<tr class="even">
<td>60540</td>
<td>Bootloader-Version</td>
<td>40 Zeichen</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60560</td>
<td>Betriebssystemversion</td>
<td>40 Zeichen</td>
<td>R</td>
</tr>
<tr class="even">
<td>60580</td>
<td>Softwareversion</td>
<td>40 Zeichen</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60600</td>
<td>Bedienprotokoll aktivieren</td>
<td>Bei 1 werden Bedienungen protokolliert</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60601</td>
<td>Anzahl der Protokolleinträge</td>
<td>Zeigt die aktuelle Anzahl der Protokolleinträge an</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60602</td>
<td>Screenshot aktivieren</td>
<td>Bei 1 wird ein Screenshot erstellt, danach automatische Rücksetzung</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60603</td>
<td>Speicherort der Screenshots</td>
<td>0-USB-Stick</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60604</td>
<td>HMI-Schutz aktivieren</td>
<td>Bei 1 wird der HMI-Schutz verwendet</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60605</td>
<td>Anzahl der Passwortebenen des HMI-Schutzes</td>
<td>Anzahl der Passwortebenen des HMI-Schutzes, höchstens 15</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60606-60835</td>
<td>Gültigkeitsdauer des HMI-Schutzes</td>
<td>60606-60628: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 1 sowie das Entsperrpasswort (16 Zeichen)<br />
60629-60651: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 2 sowie das Entsperrpasswort (16 Zeichen)<br />
60652-60674: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 3 sowie das Entsperrpasswort (16 Zeichen)<br />
60675-60697: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 4 sowie das Entsperrpasswort (16 Zeichen)<br />
60698-60720: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 5 sowie das Entsperrpasswort (16 Zeichen)<br />
60721-60743: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 6 sowie das Entsperrpasswort (16 Zeichen)<br />
60744-60766: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 7 sowie das Entsperrpasswort (16 Zeichen)<br />
60767-60789: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 8 sowie das Entsperrpasswort (16 Zeichen)<br />
60790-60812: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 9 sowie das Entsperrpasswort (16 Zeichen)<br />
60813-60835: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 10 sowie das Entsperrpasswort (16 Zeichen)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63000-63114</td>
<td>Gültigkeitsdauer des HMI-Schutzes</td>
<td>63000-63022: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 11 sowie das Entsperrpasswort (16 Zeichen)<br />
63023-63045: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 12 sowie das Entsperrpasswort (16 Zeichen)<br />
63046-63068: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 13 sowie das Entsperrpasswort (16 Zeichen)<br />
63069-63091: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 14 sowie das Entsperrpasswort (16 Zeichen)<br />
63092-63114: Jahr, Monat, Tag, Stunde, Minute, Sekunde und Warnbild beim Ablauf des Passworts der Ebene 15 sowie das Entsperrpasswort (16 Zeichen)</td>
<td></td>
</tr>
<tr class="odd">
<td>63115~63130</td>
<td>Eingabeadresse zum Ändern des Passworts der höchsten Ebene</td>
<td>63115~63131: Adresse zum Ändern des Passworts der höchsten Ebene (16 Zeichen); nach der Eingabe 1 in LW63131 schreiben, damit es wirksam wird</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63131</td>
<td>Freigabeadresse des Passworts der höchsten Ebene</td>
<td>63115~63130: Nach Eingabe des Passworts der höchsten Ebene 1 in diese Adresse schreiben, damit es wirksam wird</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60836</td>
<td>Im HMI speichern</td>
<td>Bei 1 werden die Einstellungen des HMI-Schutzes im HMI gespeichert, danach automatische Rücksetzung.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60837</td>
<td>HMI-Schutz zurücksetzen</td>
<td>Setzt den HMI-Schutz in den Ausgangszustand zurück. Bereits entsperrte Benutzer müssen erneut entsperren</td>
<td>W</td>
</tr>
<tr class="odd">
<td>60997</td>
<td>Belegung des USB-Eingangs.</td>
<td>Standard 0: USB-Tastatur oder -Maus. Bei 1: Barcodescanner</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60998</td>
<td>Endezeichen des USB-2D-Barcodescanners: 0-ENTER, 1-TAB+ENTER</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60999</td>
<td>Codelänge des USB-2D-Barcodescanners</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61000 - 61127</td>
<td>Speicherung und Verwendung des gelesenen 2D-Codes</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61128</td>
<td>Verwendung der Druckerparameter</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61138</td>
<td>Rezeptimport: ID des Quellrezepts</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61139</td>
<td>Rezeptimport: ID des Zielrezepts</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61140</td>
<td>ID des zu löschenden Rezepts</td>
<td>-1 bei Anzeige des Anfangswerts als 16-Bit Ganzzahl; sonst 65535</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61141</td>
<td>Wechselt die aktuelle Rezeptgruppe im laufenden HMI</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61143</td>
<td>Gruppennummer für Import/Export von Rezepten per USB-Stick</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61146</td>
<td>Nummer des zu druckenden Fensters bei registergesteuertem Druck</td>
<td>Nummer des zu druckenden Fensters eingeben, dann LB60175 setzen, um den Druck auszulösen (automatische Rücksetzung)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62020-62039</td>
<td>Name des aktuellen Rezepts</td>
<td>ASCII-Anzeige, Unicode-Kodierung, Länge 20; zeigt den Namen des aktuellen Rezepts an</td>
<td>R</td>
</tr>
<tr class="odd">
<td>62040</td>
<td>Auswahl der Anmeldeebene</td>
<td>Benutzerebene, mit der angemeldet werden soll; entspricht der unter „Touchscreen-Parameter“ → „Benutzerpasswörter“ aktivierten Ebene</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62041~62056</td>
<td>Eingabeadresse des Anmeldepassworts</td>
<td>Passwort der in 62040 festgelegten Ebene eingeben. Das Passwort der höchsten Ebene entsperrt alle Ebenen (16 Zeichen) und schließt die Anmeldung ab.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>62057</td>
<td>Register für die Anzahl der HMI-Verlängerungen</td>
<td>Ist im HMI-Schutz die Verlängerungsoption aktiviert, wird hier die Anzahl der Verlängerungen geändert; Standardwert 1</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63141~63146</td>
<td>Ablaufdatum des dynamischen Passworts</td>
<td>Jahr, Monat, Tag, Stunde, Minute, Sekunde: LW63141~63146, 16-Bit Ganzzahl; nach Eingabe des Datums LB60182 setzen, damit es wirksam wird (automatische Rücksetzung)</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63147~63152</td>
<td>Adresse des Schlüssels für das dynamische Passwort</td>
<td>Ändert den Schlüssel des dynamischen Passworts, Adresse LW63147, Typ ASCII, Länge 6; LB60179 setzen, damit er wirksam wird (automatische Rücksetzung)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63153~63184</td>
<td>Rezeptname ändern</td>
<td>ASCII-Eingabe, Länge 32; die Änderung wird mit LB60180 wirksam</td>
<td>W</td>
</tr>
<tr class="odd">
<td>63186~63189</td>
<td>IP-Adresse des Ethernet-Geräts</td>
<td>IP-Adresse des Ethernet-Geräts im Standardmodus, 16-Bit Ganzzahl. Nach Einstellung von IP, Port und Stationsnummer LB60178 setzen, damit sie wirksam werden</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63190</td>
<td>Stationsnummer des Ethernet-Geräts</td>
<td>Stationsnummer des Ethernet-Geräts im Standardmodus, 16-Bit Ganzzahl. IP, Port und Stationsnummer werden mit LB60178 wirksam</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63191</td>
<td>Port des Ethernet-Geräts</td>
<td>Port des Ethernet-Geräts im Standardmodus, 16-Bit Ganzzahl. Nach Einstellung von IP, Port und Stationsnummer LB60178 setzen, damit sie wirksam werden</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60838~60853</td>
<td>Name des angemeldeten Benutzers</td>
<td>Rechteverwaltung: zeigt den Namen des angemeldeten Benutzers an; Objekt: ASCII-Anzeige, Länge 32</td>
<td>R</td>
</tr>
<tr class="odd">
<td>63200~63215</td>
<td>Gruppe des angemeldeten Benutzers</td>
<td>Rechteverwaltung: zeigt die Gruppe des angemeldeten Benutzers an (seine erste Gruppe); Objekt: ASCII-Anzeige, Länge 32</td>
<td>R</td>
</tr>
</tbody>
</table>
