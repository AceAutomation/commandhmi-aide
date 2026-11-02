# Pulsante di pagina

Il pulsante di pagina serve al cambio di pagina, alla modifica del livello utente, all'apertura di finestre popup e ad altre operazioni. Una volta configurato, permette di passare da una pagina o finestra a un'altra, eventualmente cambiando al tempo stesso il livello utente.

• Fare clic sull'icona <img src="../../../configuration-guide/basic-control/screen-button.files/screen-button293.png" width="30" /> nella barra degli strumenti per aprire la finestra di dialogo mostrata nella Figura 4-80.

<img src="../../../configuration-guide/basic-control/screen-button.files/screen-button364.png" width="671" />

Figura 4-80 Finestra di dialogo Screen Button

<img src="../../../configuration-guide/basic-control/screen-button.files/screen-button404.png" width="130" />

Per forma, colore bordo, colore primo piano, colore sfondo e motivo, vedere il "Pulsante di bit".

**Funzioni:**

• Apri pagina (Open Screen): facendo clic sul pulsante si passa alla pagina selezionata. Funziona sia in una pagina sia in una finestra.

• Apri pagina precedente (Open Previous Screen): facendo clic sul pulsante si torna alla pagina precedente. Funziona solo in una pagina.

• Chiudi e apri (Close Open Screen): funziona solo in una finestra; chiude la finestra corrente e apre un'altra finestra o pagina.

• Chiudi (Close Screen): funziona solo in una finestra; chiude la finestra corrente.

**Cambio del livello utente:**

• Disconnessione (Logout): riporta il livello utente corrente al livello predefinito

• Livello utente specificato (Specified User Level): imposta il livello utente corrente sul livello specificato

**Attivazione:**

• Alla pressione (Press): il cambio di pagina avviene quando l'utente preme il pulsante.

• Al rilascio (Release): il cambio di pagina avviene quando l'utente rilascia il pulsante.

**Accesso richiesto se il livello è insufficiente:**

Se nella scheda "Advanced" della finestra "Screen Button" è selezionata l'opzione "Controlled by User Level" ed è stato modificato il livello minimo abilitato ("Effective Lowest Level"), l'oggetto è attivo solo se il livello utente corrente è maggiore o uguale a tale livello. Se il livello utente corrente è inferiore, quando l'utente tocca l'oggetto sul touch screen compare la finestra di inserimento password, come mostrato nella Figura 4-81:

![](../../../configuration-guide/basic-control/screen-button.files/001.png)

Figura 4-81 Tastiera di inserimento password

La pagina si apre solo se il livello corrispondente alla password inserita è sufficiente; il livello utente corrente diventa quello della password appena inserita.

**Macro:**

"Open macros" mostra l'elenco delle macro; l'utente può sceglierne una da eseguire alla pressione del pulsante. Nell'elenco a discesa compaiono solo le macro compilate.

<img src="../../../configuration-guide/basic-control/screen-button.files/screen-button2377.png" width="130" />

La scheda "Label" del pulsante di pagina è simile a quella del "Pulsante di bit". Poiché il pulsante di pagina ha un solo stato, la sua scheda Label contiene solo Status 1 Text e Status 1 Picture; per il resto le funzioni sono le stesse.

Le schede "Advanced" e "Visibility" del pulsante di pagina sono uguali a quelle del "Pulsante di bit", a cui si rimanda.

Dopo aver impostato tutte le proprietà, fare clic su "OK": il cursore assume la forma di una croce. Fare clic con il tasto sinistro nell'area di visualizzazione per aggiungere l'oggetto alla pagina.
