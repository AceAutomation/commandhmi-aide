# Impostare i parametri e aggiungere oggetti grafici

**Impostazione dei parametri:**

1\. Le impostazioni si possono modificare tramite Preferenze nel menu Impostazioni, oppure facendo doppio clic su [Impostazione parametri HMI](../setting/paramater.md) in Impostazioni, nel gestore di progetto. Compare la finestra mostrata nella Figura 3-6:

<img src="../../start-new-project/setting-parameter.files/image001.jpg" width="643" alt="ScreenShot00218.jpg" />

Figura 3-6     Finestra Impostazione parametri generali

• Modello HMI: con questa opzione si cambia il modello di HMI.

• Modalità di visualizzazione: schermo orizzontale o verticale.

• Impostazioni di avvio HMI

• Pagina iniziale: pagina mostrata dall'HMI all'accensione

• Tempo screen saver: imposta il tempo dello screen saver

• Frequenza di lampeggio: imposta la frequenza di lampeggio degli oggetti che possono lampeggiare; si può modificare inserendo direttamente un valore o con le frecce.

• Suono allarme: quando si verifica un allarme, il touch screen può avvisare l'utente con un suono; il menu a discesa a destra offre due opzioni, con o senza avviso sonoro.

• Suono al tocco: con il menu a discesa a destra si sceglie con o senza avviso sonoro.

• Pagina screen saver: sceglie una delle pagine esistenti come screen saver; basta toccare lo schermo per tornare alla pagina precedente.

• Pagina di caricamento: se si sceglie questa opzione, all'accensione l'HMI mostra per un certo tempo la pagina di caricamento selezionata, poi passa alla pagina iniziale; l'utente può così mostrare suggerimenti o note.

• Altre impostazioni

• Nascondi cursore del mouse: indica se mostrare il mouse

• Impostazione virgola mobile:

\[Standard\]: word alta del numero in virgola mobile prima, word bassa dopo;

\[Personalizzato\]: l'ordine è definito dall'utente.

• Tocco non valido: selezionando "Usa etichetta personalizzata", gli oggetti non toccabili vengono contrassegnati con l'immagine scelta dall'utente.

• Mostra effetto di pressione degli oggetti: novità di CommandHMI. Con l'effetto di pressione attivo, quando l'utente tocca un oggetto compare un contorno rettangolare, del colore scelto dall'utente. Attualmente supportano questo effetto gli oggetti Interruttore bit, Interruttore word, Pulsante di pagina, Pulsante funzione, Immissione numerica e Immissione ASCII. Il valore predefinito è Nessun effetto.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2109.png" width="130" />

Per gli oggetti ellittici l'effetto di pressione resta rettangolare.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2172.png" width="230" />

Figura 3-7

2、Impostazione password utente

<img src="../../start-new-project/setting-parameter.files/setting-parameter2206.png" width="692" />

Figura 3-8     Impostazione password utente nella finestra Impostazione parametri HMI

Questa funzione prevede 8 password utente, ciascuna con otto livelli tra cui scegliere.

• Livello utente predefinito: il livello utente predefinito corrente è NULL.

• Consenti caricamento della configurazione: se selezionato, il progetto può essere caricato dall'HMI al PC; altrimenti no.

• Password per il caricamento: indica se il caricamento del progetto richiede una password.

• Password per l'aggiornamento della configurazione da chiavetta USB: se impostata, è necessaria per aggiornare il progetto dell'HMI tramite chiavetta USB.

• Password di massima autorità: questa password consente di operare su tutti gli oggetti limitati per livello.

• Caricamento: indica se questa password consente di caricare i progetti dall'HMI al PC.

• Permessi: indica se questa password consente tutte le operazioni soggette a limitazioni.

**3. Impostazioni di collegamento <span id="OLE_LINK247"></span><span id="OLE_LINK246"></span>alla stampante e di download**

Fare clic sul pulsante "Impostazioni di collegamento tra HMI e stampante", come mostrato nella Figura 3-9:

<img src="../../start-new-project/setting-parameter.files/setting-parameter3209.png" width="693" />

Figura 3-9      Impostazioni di collegamento tra HMI e stampante

<span id="OLE_LINK245"></span><span id="OLE_LINK244"></span>Questa scheda contiene i parametri di collegamento tra la stampante e l'HMI; scegliere i parametri in base al modello di stampante.

**Impostazioni di download:**

• Modalità di download: scegliere il collegamento USB o Ethernet. Con Ethernet occorre impostare indirizzo IP e numero di porta (quelli dell'HMI).

• Cancella registro allarmi storici: indica se cancellare gli allarmi storici prima del download.

• Cancella registro dati storici: indica se cancellare i dati storici prima del download.

• Scarica ricette: indica se scaricare nell'HMI le ricette del progetto corrente.

**Opzioni di download delle immagini:**

• Mantieni formato originale: le immagini vengono scaricate senza cambiarne il formato.

• Converti in JPG: tutte le immagini vengono convertite in JPG prima del download nell'HMI.

(Nota: poiché le immagini BMP occupano molto spazio, si consiglia di selezionare questa opzione.)

4. Posizione di memorizzazione e sistema di allarme, come mostrato di seguito

<img src="../../start-new-project/setting-parameter.files/setting-parameter4305.png" width="692" />

Figura 3-10   Finestra Posizione di memorizzazione e allarmi di sistema

• Posizione di memorizzazione: posizione di dati storici, allarmi storici e catture di schermata. Le opzioni sono "Locale (FLASH)" e "Chiavetta USB", da scegliere secondo necessità. Il valore predefinito è Locale (FLASH).

• IP HMI: imposta i parametri di rete del touch screen

• Sistema di allarme

Usa il sistema di allarme: indica se usare l'allarme di sistema. Quando si verifica un allarme, il sistema mostra il messaggio di allarme corrente in alto o in basso in ogni pagina, secondo le opzioni impostate.

Colore di sfondo, colore del testo, carattere e dimensione del carattere sono le proprietà della visualizzazione degli allarmi di sistema, impostabili secondo necessità.

Modalità di visualizzazione: "Sempre visibile" mostra l'allarme in permanenza; "Visualizzazione ciclica" fa comparire e scomparire l'allarme a intervalli, con effetto lampeggiante.

Posizione della barra allarmi: sceglie dove compare la barra allarmi.

5. Altre impostazioni, come mostrato di seguito

<img src="../../start-new-project/setting-parameter.files/setting-parameter5287.png" width="690" />

Figura 3-11   Password per sbloccare lo screen saver

• Se questa opzione è selezionata, per uscire dallo screen saver l'utente deve inserire la password.

<img src="../../start-new-project/setting-parameter.files/setting-parameter5429.png" width="130" />

La modifica del tempo dello screen saver ha effetto solo se è scelta una "Pagina screen saver"; basta toccare lo screen saver per tornare alla pagina precedente.
