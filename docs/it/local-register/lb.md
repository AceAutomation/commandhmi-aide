# LB

LB

| Indirizzo | Funzione | Note | Lettura/scrittura |
|-------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| 60000-60099 | Impostazione iniziale a ON | Questi bit possono essere inizializzati a ON all'avvio del sistema | R/W |
| 60100 | Download ricetta | Attivando questo bit, i dati dell'RWI corrente vengono scritti nel dispositivo; si azzera al termine | R/W |
| 60101 | Upload ricetta | Attivando questo bit, la ricetta viene letta dal dispositivo nell'area dei registri RWI; si azzera al termine | R/W |
| 60102 | Salvataggio ricetta | Attivando questo bit, la ricetta viene scritta da RWI nella memoria FLASH; si azzera al termine | R/W |
| 60103 | Indicazione di download ricetta in corso | Questo bit è a ON mentre la ricetta viene scritta nel dispositivo e torna a OFF al termine del download | R |
| 60104 | Indicazione di upload ricetta in corso | Questo bit è a ON mentre la ricetta viene letta dal dispositivo e torna a OFF al termine | R |
| 60105 | Riavvio dell'HMI | Attivando questo bit il sistema si riavvia | R |
| 60106 | Controllo della retroilluminazione | ON: spegne la retroilluminazione dell'LCD; OFF: la accende | R/W |
| 60107 | Stato della comunicazione COM1 | ON: comunicazione normale o assente; OFF: errore di comunicazione | R |
| 60108 | Stato della comunicazione COM2 | ON: comunicazione normale o assente; OFF: errore di comunicazione | R |
| 60186 | Stato della comunicazione COM3 | ON: comunicazione normale o assente; OFF: errore di comunicazione | R |
| 60109 | Salvataggio delle modifiche ai parametri di comunicazione COM1 | Attivando questo bit, i parametri di comunicazione modificati vengono scritti nella memoria FLASH; torna a OFF al termine | R/W |
| 60110 | Salvataggio delle modifiche ai parametri di comunicazione COM2 | Attivando questo bit, i parametri di comunicazione modificati vengono scritti nella memoria FLASH; torna a OFF al termine | R/W |
| 60187 | Salvataggio delle modifiche ai parametri di comunicazione COM3 | Attivando questo bit, i parametri di comunicazione modificati vengono scritti nella memoria FLASH; torna a OFF al termine | R |
| 60111 | Conferma della modifica dei parametri di sistema | Attivando questo bit, i parametri di sistema modificati vengono scritti nella memoria FLASH; torna a OFF al termine | R/W |
| 60112 | Finestra di errore di comunicazione | ON: la finestra di errore può comparire; OFF: la finestra di errore è disabilitata | R/W |
| 60113 | Controllo del cursore del mouse | ON: il cursore del mouse è visibile; OFF: il cursore è disattivato (solo con uso touch) | R/W |
| 60114 | Stato della connessione USB | ON: è collegato un dispositivo USB; OFF: nessun dispositivo USB collegato | R |
| 60115 | Controllo della finestra della chiavetta USB | ON: impedisce la comparsa della finestra della chiavetta USB | R/W |
| 60116 | Suono al tocco | Abilita il suono al tocco o al clic del mouse | R/W |
| 60117 | Suono di allarme | Abilita il suono quando si verifica un allarme | R/W |
| 60118 | Cancellazione dello storico allarmi | Azzera le registrazioni dello storico allarmi (reset automatico) | R/W |
| 60119 | Cancellazione del registro operazioni | Azzera le registrazioni delle operazioni (reset automatico) | R/W |
| 60120 | Cancellazione dei dati storici | Azzera le registrazioni dei dati storici (reset automatico) | R/W |
| 60121 | Ricarica ricetta | Ricarica i dati della ricetta corrispondente al numero corrente; il bit è a ON durante la ricarica e torna a OFF al termine | R/W |
| 60123 | Salvataggio dello storico allarmi | ON: salva lo storico allarmi nella memoria flash; torna automaticamente a OFF dopo il salvataggio | R/W |
| 60124 | Salvataggio dei dati storici | ON: salva i dati storici nella memoria flash; torna automaticamente a OFF dopo il salvataggio | R/W |
| 60127 | Invio dei file dello storico allarmi alla chiavetta USB | Invia i file dello storico allarmi alla chiavetta USB; torna automaticamente a OFF dopo l'invio | R/W |
| 60128 | Invio dei file dei dati storici alla chiavetta USB | Invia i file dei dati storici alla chiavetta USB; torna automaticamente a OFF dopo l'invio | R/W |
| 60129 | Invio del progetto corrente alla chiavetta USB | Invia il file di progetto alla chiavetta USB; torna automaticamente a OFF dopo l'invio | R/W |
| 60133 | Disconnessione dell'utente corrente | ON: annulla l'accesso dell'utente; si azzera automaticamente al termine | R/W |
| 60141 | Allarme in tempo reale in corso | Questo bit è a ON quando si verifica un allarme in tempo reale | R |
| 60142 | Sistema in screen saver | Questo bit è a ON quando è attivo lo screen saver | R |
| 60143 | Copia del registro operazioni sulla chiavetta USB | ON: invia il file del registro operazioni alla chiavetta USB; torna automaticamente a OFF dopo l'invio | R/W |
| 60145 | Copia di tutte le ricette sulla chiavetta USB | ON: invia il file delle ricette alla chiavetta USB; torna automaticamente a OFF dopo l'invio | W |
| 60147 | Fine scansione del lettore USB di codici bidimensionali | ON: attivazione | R/W |
| 60148 | Importazione dei dati storici dalla chiavetta USB | ON: attivazione; reset automatico. Il file dei dati storici importato deve chiamarsi hisdata+numero di gruppo.csv, altrimenti la funzione non ha effetto. | R/W |
| 60150 | Esportazione della ricetta con ID specificato sulla chiavetta USB | ON: attivazione; reset automatico | R/W |
| 60152 | Importazione della ricetta con ID specificato dalla chiavetta USB nell'HMI | ON: attivazione; reset automatico | R/W |
| 60154 | Cancellazione della ricetta con ID specificato | ON: attivazione; reset automatico | R/W |
| 60155 | Sovrascrittura della ricetta | ON: attivazione; reset automatico | R/W |
| 60156 | Lettura e salvataggio della ricetta | ON: attivazione; reset automatico | R/W |
| 60163 | Esportazione delle ricette per gruppo sulla chiavetta USB | ON: attivazione; reset automatico | R/W |
| 60165 | Stato della comunicazione Ethernet | ON: comunicazione normale; OFF: errore di comunicazione | R |
| 60167 | Scansione dei file della chiavetta USB | ON: attivazione; reset automatico. Cerca i file .csv nella cartella principale e nelle sottocartelle della chiavetta USB e li mostra in una finestra per l'importazione e l'esportazione dei file delle ricette | R/W |
| 60168 | Esportazione dei dati storici per gruppo sulla chiavetta USB | ON: attivazione; reset automatico. LW60408 imposta il numero del gruppo di dati storici da esportare | R/W |
| 60169 | Modalità di disabilitazione dei numeri di stazione | ON: modalità automatica; OFF: modalità manuale (predefinita). Disabilitazione e sblocco automatici: quando il touch screen comunica con più dispositivi in modalità estesa e un dispositivo non risponde, il programma disabilita automaticamente la comunicazione con quel numero di stazione; un meccanismo interno di riconnessione sblocca automaticamente la stazione e ripristina la comunicazione quando il dispositivo torna a comunicare normalmente | R/W |
| 60175 | Stampa della finestra controllata da registro | A ON, il sistema esegue la stampa e si azzera automaticamente. Il numero della finestra da stampare va indicato in LW61146 (non il numero di pagina) | R/W |
| 60178 | Abilitazione della modifica dei parametri di comunicazione TCP | Con un dispositivo Ethernet collegato in modalità standard, permette di modificare dinamicamente IP, porta, numero di stazione e altri parametri del dispositivo collegato. Per i dettagli vedere gli indirizzi 63186~63191 di \[LW\]. | R/W |
| 60179 | Abilitazione della modifica della chiave della password dinamica | Imposta la chiave della password dinamica, che diventa effettiva; reset automatico. Indirizzo della chiave: LW63147, tipo di dato ASCII, lunghezza 6 | R/W |
| 60180 | Modifica del nome della ricetta | LW63153 (oggetto di inserimento ASCII, lunghezza 32): dopo l'inserimento del nome della ricetta, questo bit rende effettiva la modifica; si azzera automaticamente al termine | R/W |
| 60181 | Abilitazione della password dinamica | Abilita la funzione di password dinamica: 0 = disabilitata, 1 = abilitata | R/W |
| 60182 | Impostazione della scadenza della password dinamica | Imposta la data di scadenza della password dinamica (anno, mese, giorno, ora) in LW63141 ~ 63146, tipo di dato intero a 16 bit; dopo l'impostazione della data, LB60182 la rende effettiva e si azzera automaticamente. Nota: durante la protezione con password non è consentito aggiornare il firmware né modificare l'ora di sistema con i DIP 1 e 3; il firmware può essere aggiornato dopo aver inserito la super password | R/W |
| 60183 | Salvataggio immediato dell'area con ritenzione | Sui touch screen serie Q i dati dell'area con ritenzione vengono salvati automaticamente ogni minuto. Attivando questo indirizzo i dati vengono salvati immediatamente; reset automatico. | R/W |
