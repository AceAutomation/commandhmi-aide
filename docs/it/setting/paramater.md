# Impostazione dei parametri HMI

Il modello di HMI si sceglie alla creazione del progetto e si può modificare durante la configurazione tramite Impostazione parametri HMI nel gestore di progetto.

Fare doppio clic su "Impostazione parametri HMI" nel gestore di progetto: compare la finestra mostrata nella Figura 7-3:

**Impostazione parametri:**

1\. Le impostazioni si possono modificare tramite Preferenze nel menu Impostazioni, oppure facendo doppio clic su Impostazione parametri HMI in Impostazioni, nel gestore di progetto. Compare la finestra mostrata nella Figura 7-3:

<img src="../../setting/paramater.files/image002.jpg" width="643" alt="ScreenShot00218.jpg" />

Figura 7-3 Finestra Impostazione parametri HMI

Modello HMI: cambia il modello di HMI

Significato del modello:

Es.: HM-043BE

HM: serie HM di CommandHMI

043: dimensione del display dell'HMI

BE: tipo B (esiste anche il tipo E); tipi diversi hanno risoluzioni diverse.

Modalità di visualizzazione: schermo orizzontale o verticale.

Impostazioni di avvio HMI

Pagina iniziale: pagina mostrata dall'HMI all'accensione

Tempo screen saver: imposta il tempo dello screen saver

Frequenza di lampeggio: imposta la frequenza di lampeggio degli oggetti che possono lampeggiare; si può modificare inserendo direttamente un valore o con le frecce.

Suono allarme: quando si verifica un allarme, il touch screen può avvisare l'utente con un suono; il menu a discesa a destra offre due opzioni, con o senza avviso sonoro.

Suono al tocco: con il menu a discesa a destra si sceglie con o senza avviso sonoro.

Pagina screen saver: sceglie una delle pagine esistenti come screen saver; basta toccare lo schermo per tornare alla pagina precedente.

Pagina di caricamento: se si sceglie questa opzione, all'accensione l'HMI mostra per un certo tempo la pagina di caricamento selezionata, poi passa alla pagina iniziale; l'utente può così mostrare suggerimenti o note.

Lampeggio dello schermo in caso di allarme: alterna il colore di sfondo dell'oggetto Allarme o della Barra allarmi con il colore di sfondo della pagina, con la frequenza di lampeggio impostata sopra. Non funziona se lo sfondo è un'immagine o se il motivo di sfondo è trasparente.

• Altre impostazioni

• Nascondi cursore del mouse: indica se mostrare il mouse

• Impostazione virgola mobile:

• \[Standard\]: word alta del numero in virgola mobile prima, word bassa dopo;

• \[Personalizzato\]: l'ordine è definito dall'utente.

• Tocco non valido: selezionando "Usa etichetta personalizzata", gli oggetti non toccabili vengono contrassegnati con l'immagine scelta dall'utente.

• Modalità operativa: scegliere tra il tradizionale funzionamento a tocco e il funzionamento con mouse USB.

• Mostra effetto di pressione degli oggetti: novità di CommandHMI. Con l'effetto di pressione attivo, quando l'utente tocca un oggetto compare un contorno rettangolare, del colore scelto dall'utente. Attualmente supportano questo effetto gli oggetti Interruttore bit, Interruttore word, Pulsante di pagina, Pulsante funzione, Immissione numerica e Immissione ASCII. Il valore predefinito è Nessun effetto.

<img src="../../setting/paramater.files/paramater2873.png" width="130" />

Nota: per gli oggetti ellittici l'effetto di pressione resta rettangolare.

2、Impostazione password utente:

<img src="../../setting/paramater.files/paramater2964.png" width="605" />

Figura 7-4      Impostazione password utente

• Questa funzione supporta 8 password utente, ciascuna con otto livelli tra cui scegliere.

• Livello utente predefinito: il livello utente predefinito corrente è NULL.

• Consenti caricamento della configurazione: se selezionato, il progetto può essere caricato dall'HMI al PC; altrimenti no.

• Password per il caricamento: indica se il caricamento del progetto richiede una password.

• Password per l'aggiornamento della configurazione da chiavetta USB: se impostata, è necessaria per aggiornare il progetto dell'HMI tramite chiavetta USB.

• Password di massima autorità: questa password consente di operare su tutti gli oggetti limitati per livello.

• Caricamento: indica se questa password consente di caricare i progetti dall'HMI al PC.

• Permessi: indica se questa password consente tutte le operazioni soggette a limitazioni.

3、**Impostazioni di collegamento alla stampante e di download**

Fare clic sul pulsante "Impostazioni di collegamento tra HMI e stampante", come mostrato nella Figura 7-5:

<img src="../../setting/paramater.files/paramater3938.png" width="605" />

Figura 7-5      Parametri di collegamento tra stampante e HMI

Questa scheda contiene i parametri di collegamento tra la stampante e l'HMI; scegliere i parametri in base al modello di stampante.

Impostazioni di download:

Modalità di download: scegliere il collegamento USB o Ethernet. Con Ethernet occorre impostare indirizzo IP e numero di porta (quelli dell'HMI).

Cancella registro allarmi storici: indica se cancellare gli allarmi storici prima del download.

Cancella registro dati storici: indica se cancellare i dati storici prima del download.

Scarica ricette: indica se scaricare nell'HMI le ricette del progetto corrente.

Opzioni di download delle immagini:

Mantieni formato originale: le immagini vengono scaricate senza cambiarne il formato.

Converti in JPG: tutte le immagini vengono convertite in JPG prima del download nell'HMI.

(Nota: poiché le immagini BMP occupano molto spazio, si consiglia di selezionare questa opzione.)

**4. Posizione di memorizzazione e sistema di allarme, come mostrato di seguito**

<img src="../../setting/paramater.files/paramater5054.png" width="605" />

Figura 7-6      Posizione di memorizzazione e sistema di allarme

• Posizione di memorizzazione: posizione di dati storici, allarmi storici e catture di schermata. Le opzioni sono "Locale (FLASH)" e "Chiavetta USB", da scegliere secondo necessità. Il valore predefinito è Locale (FLASH).

• Sistema di allarme

• Usa il sistema di allarme: indica se usare l'allarme di sistema. Quando si verifica un allarme, il sistema mostra il messaggio di allarme corrente in alto o in basso in ogni pagina, secondo le opzioni impostate.

• Colore di sfondo, colore del testo, carattere e dimensione del carattere sono le proprietà della visualizzazione degli allarmi di sistema, impostabili secondo necessità.

• Modalità di visualizzazione: "Sempre visibile" mostra l'allarme in permanenza; "Visualizzazione ciclica" fa comparire e scomparire l'allarme a intervalli, con effetto lampeggiante.

• Posizione della barra allarmi: sceglie dove compare la barra allarmi.

**5. Altro, come mostrato di seguito**

<img src="../../setting/paramater.files/paramater5969.png" width="691" />

Figura 7-6      Password di sblocco dello screen saver

Usa password di sblocco dello screen saver: per uscire dallo screen saver occorre inserire la password impostata.

<img src="../../setting/paramater.files/paramater6121.png" width="130" />

Nota: la modifica del tempo dello screen saver ha effetto solo se è scelta una "Pagina screen saver"; basta toccare lo screen saver per tornare alla pagina precedente.
