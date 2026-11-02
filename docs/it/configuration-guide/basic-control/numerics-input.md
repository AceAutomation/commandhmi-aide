# Inserimento numerico

L'inserimento numerico è l'oggetto più utilizzato, praticamente indispensabile in ogni processo di controllo. Permette di inserire, visualizzare e memorizzare valori nei registri dati del PLC o di altri dispositivi collegati, come velocità, corrente, pressione, ecc.

L'inserimento numerico e la visualizzazione numerica hanno funzioni sostanzialmente uguali; l'unica differenza è che l'inserimento numerico permette anche di scrivere valori nei registri dati del PLC o di altri dispositivi collegati, oltre a visualizzarli.

Per creare un tasto di inserimento numerico procedere come segue:

Selezionare l'icona Numerical input<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input596.png" width="31" /> nella barra degli strumenti: compare una finestra di dialogo, come mostrato nella Figura 4-95.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input665.png" width="662" />

Figura 4-95 Finestra di dialogo Numeric Input

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input705.png" width="130" />

Nota: per forma, colore bordo, colore primo piano, colore sfondo e motivo, vedere l'oggetto "Pulsante di bit".

Nota: per "Alignment", "Justification", "Decimal Place" e "Total Digits", vedere l'oggetto "Visualizzazione numerica".

Nota: fare doppio clic sulla casella di visualizzazione per modificarne contenuto e proprietà. Quando l'oggetto è attivo nell'HMI, compare una tastiera a schermo che permette all'utente di inserire i dati, come mostrato nella Figura 4-96.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1192.png" width="693" />

Figura 4-96 Tastiera di inserimento numerico

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1228.png" width="130" />

Nota: se si seleziona il tipo di dato a 32 bit, l'indirizzo di memorizzazione occupa 2 word. Per esempio, se si scrivono dati nel registro dati di un PLC SIEMENS all'indirizzo V10, vengono occupati i registri V10 e V11; se l'utente monitora anche V11 con un altro oggetto, si verifica un errore. Prestare attenzione all'uso dei tipi di dato a 32 bit per evitare errori di dati e di indirizzo.

Nota: il numero di decimali influisce sulla visualizzazione. Se il tipo di dato è intero positivo o intero a 16/32 bit, il valore visualizzato si ottiene spostando il punto decimale del valore letto del numero di cifre impostato: se il valore letto è 212 e i decimali sono 2, viene visualizzato 2.12. Se il tipo di dato è virgola mobile a 32 bit, il valore non viene spostato ma vengono visualizzate solo le cifre decimali impostate: se il valore letto è 2.123 e i decimali sono 2, viene visualizzato 2.12.

Nota: il numero totale di cifre è la somma delle cifre della parte intera e della parte decimale. Se la parte intera del valore è più lunga di quella impostata, viene visualizzata la lunghezza effettiva. Per esempio, per il valore 2123 con lunghezza 2 e 1 decimale, viene visualizzato 212.3.

• Inserimento password (Password input): attiva l'inserimento di una password; i caratteri digitati dall'utente vengono visualizzati come "\*" durante l'inserimento e la visualizzazione.

• Usa macro (Use Macro): selezionando "Use Macro" compare l'elenco delle macro; l'utente può sceglierne una da eseguire alla pressione del tasto di inserimento numerico. Nell'elenco a discesa compaiono solo le macro compilate.

• Numero totale di cifre (Total digit): somma delle cifre della parte intera e della parte decimale; determina la dimensione dei valori visualizzati e inseriti. Con 4 cifre totali e 1 decimale, il valore massimo è 999.9, che è il massimo inseribile e visualizzabile dall'oggetto. Un valore inserito superiore genera un errore; un valore visualizzato superiore viene troncato alle cifre impostate. Per esempio, con 4 cifre totali, 1 decimale e valore effettivo 12345, l'oggetto visualizza 234.5.

Scheda "Advanced": serve principalmente a impostare guadagno, offset e controllo dell'intervallo dei dati inseriti (per verificare che il valore inserito non esca dall'intervallo impostato). La scheda contiene inoltre le opzioni "Touch availability" e "Notification", con le stesse funzioni dell'oggetto "Pulsante di bit", a cui si rimanda.

Fare clic sulla scheda "Advanced", come mostrato nella Figura 4-97:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input3958.png" width="675" />

Figura 4-97 Scheda Advanced dell'inserimento numerico

• Controllato da bit (Controlled by Bit): se selezionata, l'oggetto è disponibile solo in determinate condizioni. Se "Valid Status" è 1, l'oggetto è attivo solo quando il valore del "Control Bit" è 1; se "Valid Status" è 0, è attivo solo quando il valore del "Control Bit" è 0. Negli altri casi l'oggetto non ha alcun effetto.

• Controllato da livello utente (Controlled by User Level): l'utente può selezionare più opzioni secondo necessità. In simulazione o sull'HMI viene verificato se il livello dell'utente corrente dispone del permesso.

• Usa tasti di scelta rapida (Use Hot Keys): vedere il Pulsante di bit.

• Mostra valore (Show value): se selezionata, durante l'inserimento la tastiera mostra il valore corrente dell'oggetto. Per esempio, se il valore visualizzato è 389, facendo clic sull'oggetto di inserimento numerico l'area di inserimento mostra 389; altrimenti l'area è vuota, come mostrato di seguito:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4972.png" width="93" />

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4974.png" width="630" />

Per esempio, se nella scheda Advanced dell'oggetto sono selezionate le opzioni 2 e 3 del livello abilitato e le password utente nelle impostazioni parametri del touch screen sono quelle della Figura 4-98:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input5185.png" width="605" />

Figura 4-98 Impostazione delle password utente nei parametri del touch screen

Se il livello utente predefinito è NULL, l'oggetto non è utilizzabile; in questo caso si può usare la funzione Change User Level di un pulsante funzione per cambiare il livello. Per esempio, se l'utente inserisce la password 6666, corrispondente al livello utente 6, che ha solo l'opzione 1 e non corrisponde né all'opzione 2 né alla 3, il sistema segnala che la password non è corretta; se l'utente inserisce 2222 o 3333, poiché entrambi questi utenti hanno l'opzione 2, la password è valida e l'oggetto diventa utilizzabile. Se il livello utente predefinito è l'utente 2 o 3, entrambi hanno l'opzione 2 e soddisfano le condizioni, quindi l'oggetto è utilizzabile in simulazione o all'avvio; se il livello predefinito è un utente che non soddisfa le condizioni, l'oggetto non è utilizzabile in simulazione o all'avvio. L'impostazione predefinita è mostrata nella figura seguente:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6241.png" width="266" />

Selezionando "change the user level is insufficient", se il livello utente non è sufficiente compare una finestra di accesso in cui l'utente può scegliere un livello adeguato e accedere di nuovo, come mostrato di seguito:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6435.png" width="268" />

• Notifica (Notification): se l'oggetto è utilizzabile, in simulazione o sull'HMI, facendo clic sull'oggetto e inserendo un valore con la tastiera che compare, lo stato impostato (1 o 0) viene scritto all'indirizzo del bit di notifica.

• Scalatura (Scaling): se selezionata, il valore scritto all'indirizzo = (valore inserito dall'utente con la tastiera - offset) / guadagno; il valore visualizzato (cioè il valore dell'indirizzo monitorato) = valore dell'indirizzo monitorato × guadagno + offset

• Visualizza intervallo (Display Range): selezionando questa opzione, l'utente può impostare i limiti inferiore e superiore e i colori di sfondo per il livello basso e alto. Il valore letto dall'oggetto viene rappresentato con colori diversi in base ai limiti impostati.

• Intervallo variabile (Variable range): i valori di "Lower Limit" e "Higher Limit" variano dinamicamente in base all'indirizzo inserito dall'utente

• Limite inferiore (Lower limit): imposta il limite inferiore. Quando il valore visualizzato è inferiore a questo limite, lo sfondo assume il colore impostato in Low Level Background Color.

• Limite superiore (Higher limit): imposta il limite superiore. Quando il valore visualizzato è superiore a questo limite, lo sfondo assume il colore impostato in High Level Background Color.

• Controllo intervallo (Range check): verifica che il valore inserito non superi il massimo o il minimo impostati.

Dopo le impostazioni, fare clic su "OK" per aggiungere l'oggetto all'area di visualizzazione (cioè la pagina)

• Con la scheda General impostata come nella figura seguente, il numero viene visualizzato in binario mentre l'inserimento avviene in decimale. Con gli altri tipi di visualizzazione, il tipo di inserimento coincide con il tipo di visualizzazione.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input8099.png" width="663" />

• Dopo aver impostato le proprietà, fare clic su OK: il cursore del mouse assume la forma di una croce. Tracciare un rettangolo nella pagina con il mouse per aggiungere l'oggetto.
