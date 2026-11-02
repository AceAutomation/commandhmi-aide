# Pulsante funzione

Il pulsante funzione è un oggetto fondamentale dell'HMI, che permette di realizzare in modo semplice e rapido numerose funzioni. Fare clic su <img src="../../../configuration-guide/basic-control/function-button.files/function-button143.png" width="28" /> per aprire la finestra delle proprietà del pulsante funzione, come mostrato nella Figura 4-82:

<img src="../../../configuration-guide/basic-control/function-button.files/function-button223.png" width="660" />

Figura 4-82 Finestra di dialogo Function Button

<img src="../../../configuration-guide/basic-control/function-button.files/function-button264.png" width="130" />

Nota: per Forma, Colore bordo, Colore primo piano, Colore sfondo e Motivo, vedere l'oggetto Pulsante di bit.

**1. Spegnere la retroilluminazione**

Scegliendo la funzione di spegnimento della retroilluminazione, premendo il pulsante sullo schermo la retroilluminazione si spegne mentre l'HMI continua a funzionare normalmente. Per riaccenderla basta toccare un punto qualsiasi del touch screen.

**2. Conferma allarme**

Scegliendo la funzione di conferma allarme, facendo clic sul pulsante si conferma l'allarme selezionato

**3. Riavvio**

Se il pulsante funzione è impostato su riavvio del sistema, toccandolo il touch screen si riavvia.

**4. Impostare il tempo dello screen saver**

Se il pulsante funzione è impostato su questa funzione, toccandolo compare una finestra per impostare il tempo di attivazione dello screen saver.

**5. Scrivere la ricetta nel PLC**

Questa funzione trasferisce la ricetta al PLC: toccando il pulsante, la ricetta memorizzata nell'HMI viene trasferita nei registri dati consecutivi corrispondenti del PLC o di altri dispositivi collegati. (L'indirizzo è quello di scrittura impostato dal progettista nella definizione della ricetta).

**6. Leggere la ricetta dal PLC**

Questa funzione legge la ricetta dal PLC: toccando il pulsante, i dati della ricetta vengono letti dai registri dati consecutivi corrispondenti del PLC o di altri dispositivi collegati. (L'indirizzo è quello di scrittura impostato dal progettista nella definizione della ricetta).

**7. Impostare data e ora**

Questa funzione permette di impostare data e ora: toccando il pulsante si impostano data e ora interne.

**8. Cancellare gli allarmi**

Questa funzione cancella gli allarmi: toccando il pulsante si cancellano gli allarmi selezionati e confermati.

**9. Ricetta precedente**

Con questa funzione, facendo clic sul pulsante si apre la ricetta precedente a quella corrente. Se la ricetta corrente è la prima o se esiste una sola ricetta, i parametri della ricetta non cambiano.

**10. Ricetta successiva**

Con questa funzione, facendo clic sul pulsante si apre la ricetta successiva a quella corrente. Se la ricetta corrente è l'ultima o se esiste una sola ricetta, i parametri della ricetta non cambiano.

**11. Salvare la ricetta corrente**

Con questa funzione, toccando il pulsante si salvano i dati della ricetta provenienti dai registri dati consecutivi corrispondenti del PLC o di altri dispositivi collegati, impostati dal progettista nella definizione della ricetta.

**12. Screenshot**

Con la funzione Screenshot, facendo clic sul pulsante la pagina corrente viene salvata come immagine nella posizione indicata dall'utente. L'indirizzo del nome dell'immagine può essere inserito con un oggetto di inserimento ASCII; il nome non può contenere caratteri come ：#￥%&\*-+&lt;&gt; e la sua lunghezza non deve superare 20 caratteri.

**13. Parametri di sistema**

Imposta il pulsante funzione sui parametri di sistema: facendo clic sull'HMI si apre la pagina di impostazione dei parametri di sistema, in cui si possono modificare ora di sistema, tempo dello screen saver, contrasto della retroilluminazione, ecc.

**14. Accesso (Log on)**

Con la funzione di accesso, quando l'utente fa clic sul pulsante compare una finestra di login. Dopo aver scelto il nome utente compare una tastiera con cui inserire la password per ottenere i permessi di accesso.

**15. Disconnessione utente**

Con la funzione di disconnessione, toccando il pulsante l'utente corrente viene disconnesso e i suoi permessi annullati, in modo che il livello utente diventi il più basso.

**16. Segnale acustico di allarme (ON/OFF)**

Con questa funzione l'HMI emette un suono quando si verifica un allarme; il pulsante funzione permette di attivarlo o disattivarlo. Se il suono è attivo, facendo clic sul pulsante viene disattivato, e viceversa

**17. Suono al tocco (ON/OFF)**

Impostando il pulsante funzione su questa funzione, toccandolo si attiva o disattiva il suono al tocco. Se il suono al tocco è attivo, viene disattivato, e viceversa.

**18. Cancellare tutti i dati storici**

Vengono cancellati i dati storici memorizzati nell'HMI.

**19. Cancellare lo storico allarmi**

Viene cancellato lo storico allarmi memorizzato nell'HMI.

**20. Sbloccare la protezione HMI**

Inserire la password per disattivare la protezione dell'HMI.

**21. Lettura e salvataggio ricetta**

Legge e salva la ricetta.

**22. Funzione di riserva**

Solo funzione di riserva, non esegue alcuna operazione.

**23. Ricaricare la ricetta**

Ricarica i dati della ricetta dalla memoria flash negli indirizzi RWI corrispondenti.

**24. Cambio lingua**

Visualizza i testi di tutti gli oggetti in un'altra lingua specificata

**25. Stampa della pagina con stampante seriale**

Stampa la pagina impostata tramite una stampante seriale. Le impostazioni di collegamento del driver della stampante si trovano in "HMI Parameter settings" -&gt; "Printer and Download settings", nel riquadro sinistro dell'interfaccia del software.

**26. Configurazione IP dei dispositivi slave**

Questa funzione richiede la modalità estesa ("Extended Mode"), impostabile in "Communication Port Property". Per la comunicazione Ethernet con più dispositivi occorre aggiungere davanti all'oggetto corrispondente un numero di stazione e il registro che controlla il numero di stazione. Durante l'esecuzione del progetto nell'HMI, facendo clic sull'oggetto funzione, il numero di stazione impostato dall'utente viene mostrato nella finestra "IP config", in cui si impostano i parametri IP della stazione per realizzare la comunicazione Ethernet con più dispositivi.

**27. Funzioni degli interruttori DIP 1 e 3**

Corrisponde alle funzioni disponibili con gli interruttori DIP 1 e 3 dell'hardware in posizione ON: principalmente impostazione IP, impostazione dell'ora di sistema e parametri della retroilluminazione. Dopo l'impostazione, fare clic su OK per riavviare.

Usa macro (Use Macro): selezionando "Use macro" compare l'elenco delle macro; l'utente può sceglierne una da eseguire quando viene eseguita la funzione. Nell'elenco a discesa compaiono solo le macro compilate.

<img src="../../../configuration-guide/basic-control/function-button.files/function-button6119.png" width="130" />

Nota: passando alla pagina di sistema, il sistema chiude il progetto corrente; al ritorno dalla pagina di sistema, il progetto viene riavviato e si torna alla pagina iniziale impostata nel progetto.

Nota: la scheda "Mark" del pulsante funzione è simile a quella del "Pulsante di bit", a cui si rimanda, con la differenza che non ha Status Text 1 né Status Picture 1, perché il pulsante funzione ha un solo stato.

Nota: le schede Advanced e Visibility del pulsante funzione sono uguali a quelle del pulsante di bit, a cui si rimanda anche per l'uso dei tasti di scelta rapida.

Nota: le operazioni Ricetta precedente, Ricetta successiva, Salva ricetta e Lettura e salvataggio ricetta valgono solo per il gruppo di ricette corrente. Per operare su un altro gruppo, impostarlo prima in LW61141.

Nota: la cancellazione dei dati storici cancella tutti i gruppi di dati storici.

Dopo aver impostato tutte le proprietà, fare clic su "OK" per aggiungere il pulsante all'area di visualizzazione (cioè la pagina)
