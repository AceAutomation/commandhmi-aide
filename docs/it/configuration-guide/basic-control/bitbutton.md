# Pulsante di bit

Il pulsante di bit serve a comandare e visualizzare lo stato ON/OFF (o 1/0) di un indirizzo bit del dispositivo collegato al touch screen. È l'oggetto più semplice e più utilizzato.

Procedura per configurare un pulsante di bit:

1\. Fare clic sull'icona Bit Button<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton263.png" width="30" /> nella barra degli strumenti per aprire la finestra di dialogo delle proprietà del pulsante di bit, come mostrato nella Figura 4-68:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton381.png" width="664" />

Figura 4-68 Finestra di dialogo Bit Button

2\. La finestra di dialogo comprende quattro schede: General, Mark, Advanced e Visibility.

Forma (Shape): fare clic sul pulsante Shape per scegliere la forma grafica dell'oggetto, come mostrato nella Figura 4-69

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton600.png" width="472" />

Figura 4-69 Finestra di selezione della forma

• Colore bordo (Border Color): se si è scelta una forma con bordo, fare clic su questo pulsante per scegliere un altro colore del bordo.

• Colore primo piano (Foreground Color): per cambiare il colore di primo piano, fare clic su questo pulsante e sceglierlo nella tavolozza a discesa. (Il colore di primo piano ha effetto solo se è selezionato uno stile con sfumatura).

• Colore sfondo (Background Color): per cambiare il colore di sfondo, fare clic sul pulsante e sceglierlo nella tavolozza a discesa.

• Motivo (Pattern): fare clic sull'elenco a discesa, che contiene 21 motivi, come mostrato nella Figura 4-70:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton1213.png" width="662" />

Figura 4-70 Modifica della forma e del motivo

• Set: se si sceglie la funzione Set, dopo il download nell'HMI, facendo clic sul pulsante di bit il valore dell'indirizzo di scrittura viene impostato a 1. In altre parole, l'indirizzo di scrittura del dispositivo collegato viene portato a ON e viene visualizzato lo stato 1/ON.

• Reset: se si sceglie la funzione Reset, dopo il download nell'HMI, facendo clic sul pulsante di bit il valore dell'indirizzo di scrittura viene impostato a 0. In altre parole, l'indirizzo di scrittura del dispositivo collegato viene portato a OFF e viene visualizzato lo stato 0/OFF.

• Impulsivo (Inching): con la funzione Inching si può scegliere "1 alla pressione" oppure "0 alla pressione". Con "1 alla pressione", dopo il download nell'HMI, quando si preme il pulsante di bit l'indirizzo di scrittura del dispositivo collegato viene portato a 1/ON e viene visualizzato lo stato 1/ON; quando il pulsante viene rilasciato, l'indirizzo di scrittura viene portato a 0/OFF e viene visualizzato lo stato 0/OFF. Con "0 alla pressione", dopo il download nell'HMI, quando si preme il pulsante di bit l'indirizzo di scrittura del dispositivo collegato viene portato a 0/OFF e viene visualizzato lo stato 0/OFF; quando il pulsante viene rilasciato, l'indirizzo di scrittura viene portato a 1/ON e viene visualizzato lo stato 1/ON.

• Alternato (Alternate): con la funzione Alternate, dopo il download nell'HMI, se lo stato corrente del pulsante di bit è 0/OFF, toccando il pulsante l'indirizzo di scrittura viene portato a 1/ON e viene visualizzato lo stato 1/ON; se lo stato corrente è 1/ON, toccando il pulsante l'indirizzo di scrittura viene portato a 0/OFF e viene visualizzato lo stato 0/OFF. Lo stato cambia a ogni tocco.

• Indirizzo di scrittura (Write Address): fare clic sull'icona della tastiera accanto a "Write Address" per inserire l'indirizzo. Il software CommandHMI propone i simboli di indirizzo corrispondenti al dispositivo collegato. Per esempio, per i PLC MITSUBISHI serie FX-2N: X indica l'indirizzo di un ingresso; Y di un'uscita; M di un relè interno; C di un contatore (visualizzazione dello stato); T di un timer (visualizzazione dello stato); D di un registro dati; C \* di un contatore (valore di conteggio); T \* di un timer (valore di conteggio). Un altro esempio è la serie SIEMENS S7-200: I indica l'indirizzo di ingresso; Q l'indirizzo di uscita; M l'indirizzo di un relè interno; V l'indirizzo di un registro dati. Come mostrato nella Figura 4-71:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton3963.png" width="251" />

Figura 4-71 Inserimento dell'indirizzo

In questo modo l'utente può scrivere lo stato corrente del pulsante di bit all'indirizzo del PLC o di altri dispositivi collegati, usando i diversi simboli di indirizzo. Quando il pulsante di bit è nello stato 0/OFF, il valore dell'indirizzo di scrittura o di visualizzazione è 0/OFF; quando l'oggetto è nello stato 1/ON, il valore è 1/ON.

• Monitoraggio (Monitor): selezionando "Monitor" compare "Monitor Address": il pulsante di bit può allora monitorare le variazioni del valore dell'indirizzo di monitoraggio. Quando il pulsante di bit è nello stato 0/OFF, il valore dell'indirizzo di monitoraggio è 0/OFF; quando è nello stato 1/ON, il valore è 1/ON. Con "Monitor Address" selezionato, l'indirizzo di monitoraggio e quello di scrittura possono essere diversi. Per esempio, con la funzione Set, toccando l'oggetto l'indirizzo di scrittura viene portato a 1/ON; ma se in quel momento l'indirizzo di monitoraggio è a 0/OFF, il pulsante di bit continua a mostrare lo stato 0/OFF. In genere si seleziona "Monitor address identical to Write address" per visualizzare direttamente il valore scritto.

• Macro: selezionando "Use Macro" compare l'elenco delle macro; l'utente può sceglierne una da eseguire alla pressione del pulsante di bit. Nell'elenco a discesa compaiono solo le macro compilate.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5308.png" width="130" />

Se Monitor non è selezionato, lo stato visualizzato del pulsante non cambia anche quando l'oggetto viene toccato.

**Mark**

Selezionando la scheda Mark vengono visualizzate le proprietà del testo dello stato 0, come mostrato nella Figura 4-72:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5512.png" width="664" />

Figura 4-72 Scheda Label del pulsante di bit

La scheda comprende quattro elementi: "Status 0 Text", "Status 1 Text", "Status 0 Picture" e "Status 1 Picture".

• Testo stato 0, Testo stato 1 (Status 0 Text, Status 1 Text): permettono di modificare carattere, dimensione, margine, colore e posizione del testo dello stato 0 o 1. CommandHMI offre anche una funzione di copia, che consente di copiare gli attributi di uno stato sull'altro, con un notevole risparmio di tempo.

• Tutti i testi usano la prima lingua (All Texts use the first language): opzione usata nei progetti multilingua ("Language" in Gestione progetto). Se il numero totale di lingue è maggiore di 1, selezionando questa opzione il contenuto dell'oggetto non cambia al cambio di lingua.

• Lingua (Language): opzione usata nei progetti multilingua, per inserire il testo nelle diverse lingue. (In un pulsante funzione, selezionare l'opzione "Switch language" e la lingua di destinazione: in simulazione o sull'HMI tutti gli oggetti con testo vengono visualizzati nella lingua selezionata). Per ogni lingua il testo, il carattere e la dimensione possono essere diversi, mentre colore, spaziatura e posizione sono comuni

• Carattere (Font): sceglie il tipo di carattere del testo; lingue diverse possono usare caratteri diversi.

• Dimensione carattere (Font Size): sceglie la dimensione del testo; lingue diverse possono usare dimensioni diverse.

• Colore, margine, posizione (Color, Margin, Position): impostano colore, margine e allineamento del testo selezionato. Se le lingue sono più di una, queste opzioni sono quelle della lingua 1 e non sono modificabili per le altre lingue.

• Immagine stato 0, Immagine stato 1 (Status 0 Picture, Status 1 Picture): è possibile assegnare immagini di formati diversi ai diversi stati, in base alla "Picture source". L'immagine scelta viene aggiunta automaticamente alla scheda "General". Se è selezionato "Fit to Object Size", l'immagine assume le stesse dimensioni dell'oggetto.

• Adatta alle dimensioni dell'oggetto (Fit to Object Size): se selezionato, l'immagine assume le stesse dimensioni dell'oggetto e le opzioni Margin e Position vengono nascoste.

• Se si importa un'immagine da un file esterno, compare l'opzione "Transparency", che rende trasparente un colore specificato

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton7699.png" width="130" />

Selezionando "Flicker", l'oggetto lampeggia nello stato ON/OFF. La frequenza di lampeggio predefinita è 1 s. Per modificarla, fare doppio clic su "HMI parameter settings" in Gestione progetto e cambiare "Flashing frequency".

Selezionare la scheda "Advanced" per visualizzare le proprietà avanzate, come mostrato nella Figura 4-73

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8062.png" width="660" />

Figura 4-73  Scheda Advanced del pulsante di bit

• Controllato da bit (Controlled by Bit): se è selezionato "Controlled by Bit" e "Valid Status" è 1, il pulsante di bit è attivo solo quando il valore del "Control Bit" è 1. Se "Valid Status" è 0, il pulsante di bit è attivo solo quando il valore del "Control Bit" è 0. Negli altri casi il pulsante non ha alcun effetto.

• Controllato da livello utente (Controlled by User Level): l'utente può selezionare più opzioni secondo necessità. In simulazione o sull'HMI viene verificato se il livello dell'utente corrente dispone del permesso.

Per esempio, se nella scheda Advanced dell'oggetto sono selezionate le opzioni 2 e 3 del livello abilitato e le password utente nelle impostazioni parametri del touch screen sono quelle della Figura 4-74:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8900.png" width="692" />

Figura 4-74 Impostazione delle password utente nei parametri del touch screen

Se il livello utente predefinito è NULL, l'oggetto non è utilizzabile; in questo caso si può usare la funzione Change User Level di un pulsante funzione per cambiare il livello. Per esempio, se l'utente inserisce la password 6666, corrispondente al livello utente 6, che ha solo l'opzione 1 e non corrisponde né all'opzione 2 né alla 3, il sistema segnala che la password non è corretta; se l'utente inserisce 2222 o 3333, poiché entrambi questi utenti hanno l'opzione 2, che corrisponde alle opzioni 2 o 3, la password è valida e l'oggetto diventa utilizzabile. Se il livello utente predefinito è l'utente 2 o 3, entrambi hanno l'opzione 2 e soddisfano le condizioni, quindi l'oggetto è utilizzabile in simulazione o all'avvio; se il livello predefinito è l'utente 6, questo livello non soddisfa le condizioni e l'oggetto non è utilizzabile in simulazione o all'avvio. L'impostazione predefinita è mostrata nella figura seguente:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton9956.png" width="459" />

Selezionando "change the user level is insufficient", se il livello utente non è sufficiente compare una finestra di accesso in cui l'utente può scegliere un livello adeguato e accedere di nuovo, come mostrato di seguito:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton10150.png" width="466" />

In CommandHMI questa funzione è disponibile solo per i seguenti oggetti: pulsante di bit, casella combinata, inserimento ASCII, pulsante funzione, tastiera ASCII, pulsante multifunzione, pulsante multistato, selettore ricette, pulsante di pagina, pulsante di opzione, pulsante a passi, pulsante di word, cursore e inserimento numerico; per il loro uso vale quanto descritto per il pulsante di bit.

• Tempo minimo di pressione (Minimum press time): numero di secondi dopo i quali l'oggetto reagisce alla pressione, in simulazione o sull'HMI.

• Notifica (Notification): se l'oggetto è utilizzabile in simulazione o sull'HMI, facendo clic sull'oggetto e inserendo un valore con la tastiera che compare, lo stato (1 o 0) viene scritto all'indirizzo "Notification Bit" impostato.

• Registro di notifica (Notification Register): se l'oggetto è utilizzabile in simulazione o sull'HMI, facendo clic sull'oggetto e inserendo un valore con la tastiera che compare, il valore (cioè quello inserito dall'utente) viene scritto all'indirizzo del registro di notifica impostato.

• Tasto di scelta rapida (Hotkey): con questa funzione si può associare un numero o un carattere che produce lo stesso effetto della pressione. Per esempio, inserendo 1, premere il tasto 1 del tastierino numerico in simulazione o sull'HMI, oppure su una tastiera esterna, produce lo stesso effetto.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11418.png" width="161" />

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11420.png" width="130" />

Il livello utente predefinito è NULL, cioè il livello più basso. Il progettista può modificarlo con la funzione "Change User Level" di un pulsante funzione inserendo la password corrispondente.

Per tocco effettivo si intende un tocco che produce un effetto reale, come l'esecuzione di set, reset, impulsivo o alternato. Un altro esempio è l'inserimento numerico: quando l'utente tocca l'oggetto compare la tastiera, ma questo non genera una notifica, perché non viene scritto nulla all'indirizzo. Se si esce dalla tastiera con ESC non viene generata alcuna notifica. La notifica viene generata solo quando si inserisce un valore compreso tra minimo e massimo e si preme ENTER.

Selezionare la scheda "Show" per visualizzare le proprietà di visibilità, che stabiliscono se l'oggetto è visibile o nascosto. Come mostrato nella Figura 4-75

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12372.png" width="675" />

Figura 4-75 Scheda Visibility del pulsante di bit

• Controllato da bit (Controlled by bit): se questa opzione è selezionata e lo stato attivo è 1, il pulsante di bit è visibile sul touch screen solo quando il valore del bit di controllo è 1; se lo stato attivo è 0, è visibile solo quando il valore del bit di controllo è 0.

• Controllato da livello utente (Controlled by User Level): le condizioni sono le stesse dell'opzione omonima della scheda Advanced; il pulsante di bit è visibile sul touch screen solo se tali condizioni sono soddisfatte.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12995.png" width="130" />

Se nessuna delle due opzioni è selezionata, l'oggetto è sempre visibile sul touch screen.
