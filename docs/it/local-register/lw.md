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
<th>indirizzo</th>
<th>descrizione</th>
<th>Note</th>
<th>proprietà di lettura/scrittura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>59010~59057</td>
<td>In modalità estesa, disabilita la comunicazione con il numero di stazione specificato. Numeri di stazione 0~255,<br />
ogni indirizzo corrisponde a 16 numeri di stazione: 59010 indica le stazioni 0~15, e così via. Se il bit X è 1, la comunicazione con la stazione X è consentita; se è 0,<br />
la comunicazione con la stazione X è chiusa.</td>
<td>COM1: 59010~59025<br />
COM2: 59026~59041<br />
COM3: 59106~59121<br />
Ethernet: 59042~59057</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>59058~59105</td>
<td>Indicazione dello stato di comunicazione per numero di stazione, stazioni 0~255.<br />
ogni indirizzo corrisponde a 16 numeri di stazione: 59058 indica le stazioni 0~15, e così via. Se il bit X è 1,<br />
la comunicazione con quella stazione è anomala; se il bit è 0, la comunicazione è normale.</td>
<td>COM1: 59058~59073<br />
COM2: 59074~59089<br />
COM3: 59154~59169<br />
Ethernet: 59090~59105</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60000</td>
<td>ora locale: secondi</td>
<td>Codice BCD, intervallo valido 0-59</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60001</td>
<td>ora locale</td>
<td>Codice BCD, intervallo valido 0-59</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60002</td>
<td>ora locale</td>
<td>Codice BCD, intervallo valido 0-23</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60003</td>
<td>ora locale: giorno</td>
<td>Codice BCD, intervallo valido 1-31</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60004</td>
<td>ora locale: mese</td>
<td>Codice BCD, intervallo valido 1-12</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60005</td>
<td>ora locale: anno</td>
<td>Codice BCD, intervallo valido 0-9999</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60006</td>
<td>ora locale: giorno della settimana</td>
<td>Codice BCD, intervallo valido 1-7</td>
<td>R</td>
</tr>
<tr class="even">
<td>60007</td>
<td>tempo di funzionamento del sistema</td>
<td>Tempo di funzionamento del sistema, ore</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60008</td>
<td>tempo di funzionamento del sistema</td>
<td>Tempo trascorso dall'avvio del sistema, minuti</td>
<td>R</td>
</tr>
<tr class="even">
<td>60009</td>
<td>Tempo di funzionamento del sistema in secondi</td>
<td>Tempo trascorso dall'avvio del sistema, secondi</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60010</td>
<td>Numero della finestra corrente</td>
<td>Numero della pagina corrente</td>
<td>R</td>
</tr>
<tr class="even">
<td>60012</td>
<td>lingua corrente</td>
<td>Numero della lingua corrispondente</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60013</td>
<td>Limite superiore consentito per l'immissione numerica</td>
<td>Quando viene visualizzata la tastiera personalizzata, mostra in ASCII il limite superiore consentito</td>
<td>R</td>
</tr>
<tr class="even">
<td>60023</td>
<td>Limite inferiore consentito per l'immissione numerica</td>
<td>Quando viene visualizzata la tastiera personalizzata, mostra in ASCII il limite inferiore consentito</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60033</td>
<td>Dati immessi visualizzati sulla tastiera</td>
<td>Dati immessi visualizzati sulla tastiera (caratteri digitati), visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60065</td>
<td>Utente attualmente connesso al sistema</td>
<td>numero dell'utente corrente</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60066</td>
<td>Password dell'utente attualmente connesso</td>
<td>Mostra la password dell'utente corrente, 16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60074</td>
<td>Nome dell'utente attualmente connesso</td>
<td>Mostra il nome dell'utente corrente, 32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60090</td>
<td>Utente 1 abilitato</td>
<td>0 - non abilitato, 1 - abilitato</td>
<td>R</td>
</tr>
<tr class="even">
<td>60091</td>
<td>Utente 2 abilitato</td>
<td>0 - non abilitato, 1 - abilitato</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60092</td>
<td>Utente 3 abilitato</td>
<td>0 - non abilitato, 1 - abilitato</td>
<td>R</td>
</tr>
<tr class="even">
<td>60093</td>
<td>Utente 4 abilitato</td>
<td>0 - non abilitato, 1 - abilitato</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60094</td>
<td>Utente 5 abilitato</td>
<td>0 - non abilitato, 1 - abilitato</td>
<td>R</td>
</tr>
<tr class="even">
<td>60095</td>
<td>Utente 6 abilitato</td>
<td>0 - non abilitato, 1 - abilitato</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60096</td>
<td>Utente 7 abilitato</td>
<td>0 - non abilitato, 1 - abilitato</td>
<td>R</td>
</tr>
<tr class="even">
<td>60097</td>
<td>Utente 8 abilitato</td>
<td>0 - non abilitato, 1 - abilitato</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60098</td>
<td>Nome utente 1</td>
<td>32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60114</td>
<td>Nome utente 2</td>
<td>32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60130</td>
<td>Nome utente 3</td>
<td>32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60146</td>
<td>Nome utente 4</td>
<td>32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60162</td>
<td>Nome utente 5</td>
<td>32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60178</td>
<td>Nome utente 6</td>
<td>32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60194</td>
<td>Nome utente 7</td>
<td>32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60210</td>
<td>Nome utente 8</td>
<td>32 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60226</td>
<td>Password utente 1</td>
<td>16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60234</td>
<td>Password utente 2</td>
<td>16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60242</td>
<td>Password utente 3</td>
<td>16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60250</td>
<td>Password utente 4</td>
<td>16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60258</td>
<td>Password utente 5</td>
<td>16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60266</td>
<td>Password utente 6</td>
<td>16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60274</td>
<td>Password utente 7</td>
<td>16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60282</td>
<td>Password utente 8</td>
<td>16 caratteri, visualizzazione ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60290</td>
<td>tempo dello screen saver</td>
<td>Mostra il tempo dello screen saver impostato nella configurazione, intervallo 0~60</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60291</td>
<td>Periodo di lampeggio degli indicatori</td>
<td>Periodo di lampeggio dell'oggetto indicatore luminoso, valore minimo 0,1, unità: s</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60292</td>
<td>Posizione X al tocco</td>
<td>Coordinata X del punto toccato</td>
<td>R</td>
</tr>
<tr class="even">
<td>60293</td>
<td>Posizione Y al tocco</td>
<td>Coordinata Y del punto toccato</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60294</td>
<td>Posizione X al rilascio</td>
<td>Coordinata X al rilascio del tocco</td>
<td>R</td>
</tr>
<tr class="even">
<td>60295</td>
<td>Posizione Y al rilascio</td>
<td>Coordinata Y al rilascio del tocco</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60296</td>
<td>stato del tocco</td>
<td>1-toccato, 0-rilasciato</td>
<td>R</td>
</tr>
<tr class="even">
<td>60297</td>
<td>Parità di COM1</td>
<td>Parametri di comunicazione, parità: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60298</td>
<td>Baud rate di COM1</td>
<td>Parametri di comunicazione, baud rate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60299</td>
<td>Bit di stop di COM1</td>
<td>Parametri di comunicazione, bit di stop: 0-1 bit, 1-2 bit</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60300</td>
<td>Lunghezza dati di COM1</td>
<td>Parametri di comunicazione, lunghezza dati: 0-7 bit, 1-8 bit</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60301</td>
<td>Indirizzo HMI di COM1</td>
<td>Parametri di comunicazione, indirizzo HMI</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60302</td>
<td>Indirizzo PLC di COM1</td>
<td>Parametri di comunicazione, indirizzo PLC</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60303</td>
<td>COM1: intervallo di indirizzi PLC consecutivi</td>
<td>Lunghezza massima di indirizzi consecutivi leggibili in una singola comunicazione</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60304</td>
<td>COM1: tempo di comunicazione</td>
<td>Tempo di ritardo della comunicazione</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60305</td>
<td>COM1: tentativi</td>
<td>Numero di ritrasmissioni del sistema in caso di comunicazione anomala</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60306</td>
<td>COM1: modalità indirizzo</td>
<td>Modalità indirizzo: 0-standard, 1-estesa</td>
<td>R</td>
</tr>
<tr class="even">
<td>60307</td>
<td>COM1: timeout di comunicazione</td>
<td>Imposta il timeout di comunicazione, in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60308</td>
<td>COM1: tempo di attesa corrente della comunicazione</td>
<td>Tempo di attesa corrente della comunicazione, in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60309</td>
<td>COM1: posizione HMI</td>
<td>0-locale 1-remoto</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60312</td>
<td>Parità di COM2</td>
<td>Parametri di comunicazione, parità: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60313</td>
<td>Baud rate di COM2</td>
<td>Parametri di comunicazione, baud rate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60314</td>
<td>Bit di stop di COM2</td>
<td>Parametri di comunicazione, bit di stop: 0-1 bit, 1-2 bit</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60315</td>
<td>Lunghezza dati di COM2</td>
<td>Parametri di comunicazione, lunghezza dati: 0-7 bit, 1-8 bit</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60316</td>
<td>Indirizzo HMI di COM2</td>
<td>Parametri di comunicazione, indirizzo HMI</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60317</td>
<td>Indirizzo PLC di COM2</td>
<td>Parametri di comunicazione, indirizzo PLC</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60318</td>
<td>COM2: intervallo di indirizzi PLC consecutivi</td>
<td>Lunghezza massima di indirizzi consecutivi leggibili in una singola comunicazione</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60319</td>
<td>COM2: tempo di comunicazione</td>
<td>Tempo di ritardo della comunicazione</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60320</td>
<td>COM2: tentativi</td>
<td>Numero di ritrasmissioni del sistema in caso di comunicazione anomala</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60321</td>
<td>COM2: modalità indirizzo</td>
<td>Modalità indirizzo: 0-standard, 1-estesa</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60322</td>
<td>COM2: timeout di comunicazione</td>
<td>Imposta il timeout di comunicazione, in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60323</td>
<td>COM2: tempo di attesa corrente della comunicazione</td>
<td>Tempo di attesa corrente della comunicazione, in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60324</td>
<td>COM2: posizione HMI</td>
<td>0-locale, 1-remoto</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61270</td>
<td>Parità di COM3</td>
<td>Parametri di comunicazione, parità: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61271</td>
<td>Baud rate di COM3</td>
<td>Parametri di comunicazione, baud rate: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61272</td>
<td>Bit di stop di COM3</td>
<td>Parametri di comunicazione, bit di stop: 0-1 bit, 1-2 bit</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61273</td>
<td>Lunghezza dati di COM3</td>
<td>Parametri di comunicazione, lunghezza dati: 0-7 bit, 1-8 bit</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61274</td>
<td>Indirizzo HMI di COM3</td>
<td>Parametri di comunicazione, indirizzo HMI</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61275</td>
<td>Indirizzo PLC di COM3</td>
<td>Parametri di comunicazione, indirizzo PLC</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61276</td>
<td>COM3: intervallo di indirizzi PLC consecutivi</td>
<td>Lunghezza massima di indirizzi consecutivi leggibili in una singola comunicazione</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61277</td>
<td>COM3: tempo di comunicazione</td>
<td>Tempo di ritardo della comunicazione</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61278</td>
<td>COM3: tentativi</td>
<td>Numero di ritrasmissioni del sistema in caso di comunicazione anomala</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61279</td>
<td>COM3: modalità indirizzo</td>
<td>Modalità indirizzo: 0-standard, 1-estesa</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61280</td>
<td>COM3: timeout di comunicazione</td>
<td>Imposta il timeout di comunicazione, in ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61281</td>
<td>COM3: tempo di attesa corrente della comunicazione</td>
<td>Tempo di attesa corrente della comunicazione, in ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61282</td>
<td>COM3: posizione HMI</td>
<td>0-locale, 1-remoto</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60327</td>
<td>Numero di allarmi storici</td>
<td>Numero totale di allarmi storici registrati</td>
<td>R/doppia word</td>
</tr>
<tr class="even">
<td>60329</td>
<td>Numero di record storici</td>
<td>Numero totale di record di dati storici registrati</td>
<td>R/doppia word</td>
</tr>
<tr class="odd">
<td>60333</td>
<td>cambio lingua della tastiera</td>
<td>1-tastiera cinese, 0-tastiera inglese, per la tastiera standard</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60334</td>
<td>Utilizzo della CPU</td>
<td>Utilizzo della CPU del sistema corrente</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60335</td>
<td>Luminosità attuale della retroilluminazione</td>
<td>Luminosità attuale della retroilluminazione (140~450)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60337</td>
<td>Data di creazione del progetto: anno</td>
<td>Anno di creazione del file di progetto corrente</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60338</td>
<td>Data di creazione del progetto: mese</td>
<td>Mese di creazione del file di progetto corrente</td>
<td>R</td>
</tr>
<tr class="even">
<td>60339</td>
<td>Data di creazione del progetto: giorno</td>
<td>Giorno di creazione del file di progetto corrente</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60340</td>
<td>lingua utente corrente</td>
<td>imposta la lingua corrente</td>
<td>W</td>
</tr>
<tr class="even">
<td>60359</td>
<td>Se uguale a 1, copia su chiavetta USB gli allarmi storici dell'intervallo di numeri di sequenza specificato</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60361</td>
<td>Se uguale a 1, copia su chiavetta USB gli allarmi storici dell'intervallo di tempo specificato</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60363</td>
<td>Esportazione allarmi storici: numero di sequenza iniziale</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60365</td>
<td>Esportazione allarmi storici: numero di sequenza finale</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60367</td>
<td>Esportazione allarmi storici: ora di inizio</td>
<td>Lunghezza 6 word: anno, mese, giorno, ora, minuto e secondo.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60373</td>
<td>Esportazione allarmi storici: ora di fine</td>
<td>Lunghezza 6 word: anno, mese, giorno, ora, minuto e secondo.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60379</td>
<td>Nome del file per l'esportazione degli allarmi storici su chiavetta USB</td>
<td>lunghezza 22 caratteri</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60408</td>
<td>Indirizzo di controllo del numero di gruppo corrente dei dati storici</td>
<td>Specifica il numero di gruppo corrente dei dati storici</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60409</td>
<td>Se uguale a 1, copia su chiavetta USB i dati storici dell'intervallo di numeri di sequenza specificato</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60411</td>
<td>Se uguale a 1, copia su chiavetta USB i dati storici dell'intervallo di tempo specificato</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60413</td>
<td>Esportazione dati storici: numero di sequenza iniziale</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60415</td>
<td>Esportazione dati storici: numero di sequenza finale</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60417</td>
<td>Esportazione dati storici: ora di inizio</td>
<td>Lunghezza 6 word: anno, mese, giorno, ora, minuto e secondo.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60423</td>
<td>Esportazione dati storici: ora di fine</td>
<td>Lunghezza 6 word: anno, mese, giorno, ora, minuto e secondo.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60429</td>
<td>Nome del file per l'esportazione dei dati storici su chiavetta USB</td>
<td>lunghezza 24 caratteri</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60441</td>
<td>Buffer di modifica della password utente 1</td>
<td>lunghezza 16 caratteri, visualizzazione ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60449</td>
<td>Abilita la modifica della password utente 1</td>
<td>Se vale 1, la password dell'utente 1 viene sostituita da quella presente nel buffer; il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60451</td>
<td>Buffer di modifica della password utente 2</td>
<td>lunghezza 16 caratteri, visualizzazione ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60459</td>
<td>Abilita la modifica della password utente 2</td>
<td>Se vale 1, la password dell'utente 2 viene sostituita da quella presente nel buffer; il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60461</td>
<td>Buffer di modifica della password utente 3</td>
<td>lunghezza 16 caratteri, visualizzazione ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60469</td>
<td>Abilita la modifica della password utente 3</td>
<td>Se vale 1, la password dell'utente 3 viene sostituita da quella presente nel buffer; il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60471</td>
<td>Buffer di modifica della password utente 4</td>
<td>lunghezza 16 caratteri, visualizzazione ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60479</td>
<td>Abilita la modifica della password utente 4</td>
<td>Se vale 1, la password dell'utente 4 viene sostituita da quella presente nel buffer; il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60481</td>
<td>Buffer di modifica della password utente 5</td>
<td>lunghezza 16 caratteri, visualizzazione ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60489</td>
<td>Abilita la modifica della password utente 5</td>
<td>Se vale 1, la password dell'utente 5 viene sostituita da quella presente nel buffer; il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60491</td>
<td>Buffer di modifica della password utente 6</td>
<td>lunghezza 16 caratteri, visualizzazione ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60499</td>
<td>Abilita la modifica della password utente 6</td>
<td>Se vale 1, la password dell'utente 6 viene sostituita da quella presente nel buffer; il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60501</td>
<td>Buffer di modifica della password utente 7</td>
<td>lunghezza 16 caratteri, visualizzazione ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60509</td>
<td>Abilita la modifica della password utente 7</td>
<td>Se vale 1, la password dell'utente 7 viene sostituita da quella presente nel buffer; il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60511</td>
<td>Buffer di modifica della password utente 8</td>
<td>lunghezza 16 caratteri, visualizzazione ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60519</td>
<td>Abilita la modifica della password utente 8</td>
<td>Se vale 1, la password dell'utente 8 viene sostituita da quella presente nel buffer; il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60520</td>
<td>Modello HMI</td>
<td>40 caratteri</td>
<td>R</td>
</tr>
<tr class="even">
<td>60540</td>
<td>versione del bootloader</td>
<td>40 caratteri</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60560</td>
<td>versione del sistema operativo</td>
<td>40 caratteri</td>
<td>R</td>
</tr>
<tr class="even">
<td>60580</td>
<td>versione del software</td>
<td>40 caratteri</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60600</td>
<td>Abilitazione registro operazioni</td>
<td>Se vale 1, la registrazione delle operazioni è abilitata</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60601</td>
<td>Numero di record operazioni</td>
<td>Mostra il numero attuale di record operazioni</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60602</td>
<td>Abilitazione cattura schermata</td>
<td>Se vale 1, esegue la cattura della schermata e si azzera automaticamente</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60603</td>
<td>Posizione di salvataggio delle pagine</td>
<td>0-chiavetta USB</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60604</td>
<td>Abilita protezione HMI</td>
<td>Se vale 1, usa la protezione HMI</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60605</td>
<td>Imposta il numero totale di livelli di password della protezione HMI</td>
<td>Imposta il numero totale di livelli di password della protezione HMI; si possono impostare fino a 15 password</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60606-60835</td>
<td>Impostazione della scadenza della protezione HMI</td>
<td>60606-60628: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 1, più la password di sblocco (lunghezza 16 caratteri)<br />
60629-60651: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 2, più la password di sblocco (lunghezza 16 caratteri)<br />
60652-60674: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 3, più la password di sblocco (lunghezza 16 caratteri)<br />
60675-60697: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 4, più la password di sblocco (lunghezza 16 caratteri)<br />
60698-60720: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 5, più la password di sblocco (lunghezza 16 caratteri)<br />
60721-60743: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 6, più la password di sblocco (lunghezza 16 caratteri)<br />
60744-60766: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 7, più la password di sblocco (lunghezza 16 caratteri)<br />
60767-60789: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 8, più la password di sblocco (lunghezza 16 caratteri)<br />
60790-60812: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 9, più la password di sblocco (lunghezza 16 caratteri)<br />
60813-60835: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 10, più la password di sblocco (lunghezza 16 caratteri)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63000-63114</td>
<td>Impostazione della scadenza della protezione HMI</td>
<td>63000-63022: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 11, più la password di sblocco (lunghezza 16 caratteri)<br />
63023-63045: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 12, più la password di sblocco (lunghezza 16 caratteri)<br />
63046-63068: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 13, più la password di sblocco (lunghezza 16 caratteri)<br />
63069-63091: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 14, più la password di sblocco (lunghezza 16 caratteri)<br />
63092-63114: anno, mese, giorno, ora, minuto, secondo e pagina di avviso di scadenza della password di livello 15, più la password di sblocco (lunghezza 16 caratteri)</td>
<td></td>
</tr>
<tr class="odd">
<td>63115~63130</td>
<td>Indirizzo di immissione per modificare la password di livello massimo</td>
<td>63115~63131: indirizzo di modifica della password di livello massimo (lunghezza 16 caratteri); al termine dell'immissione, scrivere 1 in LW63131 per rendere effettiva la password impostata</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63131</td>
<td>Indirizzo di abilitazione della password di livello massimo</td>
<td>63115~63130: al termine dell'immissione della password di livello massimo, scrivere 1 in questo indirizzo per renderla effettiva</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60836</td>
<td>Abilita salvataggio nell'HMI</td>
<td>Se vale 1, le impostazioni di protezione HMI vengono salvate nell'HMI e il registro si azzera automaticamente.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60837</td>
<td>Inizializza lo stato della protezione HMI</td>
<td>Riporta la protezione HMI allo stato iniziale. Gli utenti già sbloccati dovranno sbloccare di nuovo</td>
<td>W</td>
</tr>
<tr class="odd">
<td>60997</td>
<td>Assegnazione della funzione di ingresso USB.</td>
<td>Default 0: tastiera USB o mouse USB. Se vale 1: ingresso da lettore di codici a barre</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60998</td>
<td>Carattere di fine lettura del codice a barre 2D via USB: 0-ENTER, 1-TAB+ENTER</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60999</td>
<td>Lunghezza del codice letto dal lettore di codici 2D via USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61000 - 61127</td>
<td>Memorizzazione e uso del codice 2D letto</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61128</td>
<td>Uso dei parametri della stampante</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61138</td>
<td>Importazione ricetta: ID della ricetta sorgente</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61139</td>
<td>Importazione ricetta: ID della ricetta di destinazione</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61140</td>
<td>ID della ricetta da cancellare</td>
<td>-1 se il valore iniziale è visualizzato come intero a 16 bit; altrimenti 65535</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61141</td>
<td>Cambia il numero di gruppo ricette corrente durante il funzionamento dell'HMI</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61143</td>
<td>Specifica il numero di gruppo per l'importazione/esportazione delle ricette da/verso chiavetta USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61146</td>
<td>Numero della finestra da stampare quando la stampa è attivata da registro</td>
<td>Inserire il numero della finestra da stampare, impostare LB60175 per avviare la stampa (azzeramento automatico)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62020-62039</td>
<td>Nome della ricetta corrente</td>
<td>Oggetto di visualizzazione ASCII, codifica Unicode, lunghezza 20; mostra il nome della ricetta corrente</td>
<td>R</td>
</tr>
<tr class="odd">
<td>62040</td>
<td>Selezione del livello utente per l'accesso</td>
<td>Imposta il livello utente con cui accedere; corrisponde al livello utente selezionato in "Impostazione parametri touch screen" → "Impostazione password utente"</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62041~62056</td>
<td>Indirizzo di immissione della password di accesso</td>
<td>Inserire correttamente la password del livello utente impostato in 62040. La password di livello massimo sblocca tutti i livelli (lunghezza 16 caratteri) e completa l'accesso dell'utente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>62057</td>
<td>Registro del limite di proroghe dell'HMI</td>
<td>Se è selezionata l'opzione di proroga nelle impostazioni di protezione HMI, qui si può modificare il numero di proroghe; valore predefinito 1</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63141~63146</td>
<td>Impostazione della scadenza della password dinamica</td>
<td>Anno, mese, giorno, ora, minuto, secondo: LW63141~63146, tipo di dati: intero a 16 bit. Dopo aver impostato la data, attivare LB60182 per renderla effettiva (azzeramento automatico)</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63147~63152</td>
<td>Indirizzo di impostazione della chiave della password dinamica</td>
<td>Modifica la chiave della password dinamica, indirizzo: LW63147, tipo di dati: ASCII, lunghezza: 6. Dopo l'impostazione attivare LB60179 per renderla effettiva (azzeramento automatico)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63153~63184</td>
<td>Modifica del nome della ricetta</td>
<td>Oggetto di immissione ASCII, lunghezza 32; la modifica diventa effettiva con LB60180</td>
<td>W</td>
</tr>
<tr class="odd">
<td>63186~63189</td>
<td>Indirizzo IP del dispositivo Ethernet</td>
<td>Indirizzo IP del dispositivo Ethernet in modalità standard, tipo di dati: intero a 16 bit. Dopo aver impostato IP, porta e numero di stazione, attivare LB60178 per renderli effettivi</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63190</td>
<td>Numero di stazione del dispositivo Ethernet</td>
<td>Numero di stazione del dispositivo Ethernet in modalità standard, tipo di dati: intero a 16 bit. IP, porta e numero di stazione diventano effettivi attivando LB60178</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63191</td>
<td>Numero di porta del dispositivo Ethernet</td>
<td>Numero di porta del dispositivo Ethernet in modalità standard, tipo di dati: intero a 16 bit. Dopo aver impostato IP, porta e numero di stazione, attivare LB60178 per renderli effettivi</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60838~60853</td>
<td>Nome dell'utente attualmente connesso</td>
<td>Funzione permessi utente: mostra il nome dell'utente connesso; oggetto: visualizzazione ASCII, lunghezza 32</td>
<td>R</td>
</tr>
<tr class="odd">
<td>63200~63215</td>
<td>Gruppo dell'utente attualmente connesso</td>
<td>Funzione permessi utente: mostra il nome del gruppo dell'utente connesso (il primo gruppo di appartenenza); oggetto: visualizzazione ASCII, lunghezza 32</td>
<td>R</td>
</tr>
</tbody>
</table>
