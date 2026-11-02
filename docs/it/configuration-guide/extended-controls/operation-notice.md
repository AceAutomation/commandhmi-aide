# Istruzioni sugli oggetti di CommandHMI

Il software di configurazione CommandHMI offre oggetti di base completi. L'utente può impostarne le proprietà facendo doppio clic o clic con il tasto destro sull'oggetto nell'area di visualizzazione. Posizione e dimensioni degli oggetti possono essere modificate manualmente nella barra di stato in basso oppure trascinando con il mouse.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/image002.jpg" width="829" alt="2018_11_20_08_51_35.jpg" />

Inserimento degli indirizzi degli oggetti: per operare su un indirizzo del PLC è possibile digitarlo direttamente da tastiera. Il nome dell'indirizzo non distingue maiuscole e minuscole.

Casella di stato: nella barra degli strumenti una casella combinata visualizza e permette di cambiare lo stato di pulsante di bit, spia di bit, pulsante multistato, spia multistato, movimento grafico, visualizzazione messaggi e visualizzazione immagini.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice675.png" width="92" />

Quando è selezionato un oggetto di questi tipi, il suo stato corrente compare nella casella di stato, da cui l'utente può sceglierne un altro.

Ricerca indirizzi (Address Search): mostra dove viene usato un indirizzo, elencando gli oggetti che lo occupano; fare doppio clic su una voce per selezionare l'oggetto.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice997.png" width="299" />

Inserire l'indirizzo e selezionare "Find": la finestra di output elenca i risultati della ricerca:

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1102.png" width="406" />

Fare doppio clic su un risultato per selezionare l'oggetto che occupa l'indirizzo.

Visualizzazione indirizzi (Address Display): fare clic su "Address Display" per visualizzare l'elenco degli indirizzi usati nel progetto; facendo doppio clic su una voce si apre la pagina delle proprietà dell'oggetto che usa quell'indirizzo, per modificarne rapidamente le impostazioni.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1461.png" width="719" />

In Display Mode si può scegliere se visualizzare gli indirizzi selezionati o quelli di tutte le pagine.

Sovrapposizione degli oggetti: sovrapponendo più oggetti è possibile eseguirli con un'unica operazione. CommandHMI supporta la sovrapposizione di fino a 32 oggetti. Quando si toccano oggetti sovrapposti, le relative operazioni vengono eseguite nell'ordine di sovrapposizione, come mostrato nella figura seguente:

Sovrapponendo gli oggetti 1, 2 e 3, al tocco vengono eseguiti in sequenza i comandi 1, 2 e 3.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1966.png" width="435" />

Se tra gli oggetti sovrapposti c'è un pulsante di cambio pagina, la pagina cambia quando arriva il suo turno e i comandi dei pulsanti sovrapposti successivi non vengono eseguiti. Analogamente, se compare una tastiera di inserimento, la tastiera viene visualizzata e i comandi successivi non vengono eseguiti.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice2303.png" width="494" />
