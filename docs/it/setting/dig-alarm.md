# Registrazione allarmi digitali

L'impostazione allarmi serve a visualizzare le informazioni di allarme; solo con essa l'oggetto allarme e la barra allarmi funzionano correttamente (infatti l'oggetto allarme e la barra allarmi mostrano i messaggi della "registrazione allarmi digitali" e della "registrazione allarmi analogici").

Fare clic con il tasto destro su "Registrazione allarmi" (Alarm landing) nel gestore di progetto e selezionare "Nuovo allarme digitale", come mostrato nella Figura 7-22:

<img src="../../setting/dig-alarm.files/image001.jpg" width="274" alt="ScreenShot00094.jpg" />

Figura 7-22    Selezione della registrazione allarmi

Fare doppio clic sulla voce "Registrazione allarmi digitali" per aprire la finestra delle impostazioni degli allarmi digitali, come mostrato nella Figura 7-23:

<img src="../../setting/dig-alarm.files/dig-alarm508.png" width="558" />

Figura 7-23    Selezione di bit consecutivi

Per creare una registrazione di allarmi digitali, procedere come segue:

• Inserire prima l'indirizzo di lettura; in questo esempio si usa l'indirizzo interno LB1.

• Nella colonna "Dimensione" (Size) selezionare il numero totale di allarmi, cioè il numero totale di indirizzi bit, che sono consecutivi. In questo esempio il valore è sei.

• Impostare il "Tempo di scansione" (Scanning time) degli allarmi bit, cioè la frequenza di scansione.

• Fare clic su una voce dell'elenco, poi spostare il mouse a destra sul riquadro "Messaggio" e inserire il testo dell'allarme nel campo "Testo" (Text). Si supponga che i messaggi di allarme siano quelli della Figura 7-23.

• Se "Usa" (Use) è selezionato, il messaggio di allarme viene mostrato nell'"Oggetto allarme" o nella "Barra allarmi". Altrimenti il messaggio non compare anche se l'indirizzo corrispondente vale 1. Se l'indirizzo di questa voce vale 0, il messaggio non viene mostrato.

• Allarme su OFF (OFF Alarm): se questa opzione è selezionata, l'allarme scatta quando l'indirizzo corrispondente vale 0 (OFF). Altrimenti scatta quando l'indirizzo vale 1 (ON). Per impostazione predefinita, l'allarme scatta quando l'indirizzo vale 1 (ON).

• Esporta U (U export): esporta le impostazioni degli allarmi

• Importa U (U import): importa le impostazioni degli allarmi

Esempio: si supponga di scegliere il tipo "Bit consecutivi" (Continuous bit).

• Se l'indirizzo LB1 vale 0, il messaggio di allarme non viene mostrato nell'"Oggetto allarme" né nella "Barra allarmi", indipendentemente dall'opzione "Usa".

• Se l'indirizzo LB1 vale 1 e l'opzione "Usa" non è selezionata, il messaggio di allarme non viene mostrato nell'"Oggetto allarme" né nella "Barra allarmi".

• Se l'indirizzo LB1 vale 1 e l'opzione "Usa" è selezionata, il messaggio di allarme viene mostrato nell'"Oggetto allarme" e nella "Barra allarmi".

Fare clic su "OK" per completare le impostazioni degli allarmi digitali. Si possono aggiungere 6 pulsanti bit con funzione di commutazione sugli indirizzi LB1-LB6, posizionare sulla pagina gli oggetti "Allarme" e "Barra allarmi" ed eseguire la simulazione offline per verificare che i messaggi di allarme vengano mostrati.

Di seguito un esempio di simulazione offline, mostrato nella Figura 7-24:

<img src="../../setting/dig-alarm.files/dig-alarm2644.png" width="1182" />

Figura 7-24    Esempio di simulazione offline di allarmi digitali

Quando come tipo si seleziona "Bit consecutivi di word" (Continuous Bit of Word), come mostrato nella Figura 7-25:

<img src="../../setting/dig-alarm.files/dig-alarm2789.png" width="559" />

Figura 7-25    Selezione di bit consecutivi di word

Se l'opzione "Usa" di un certo bit è selezionata, l'allarme scatta quando quel bit vale 1.

<img src="../../setting/dig-alarm.files/dig-alarm2952.png" width="130" />

Nota: quando si copiano testi di allarme da altri documenti nei messaggi degli allarmi digitali e analogici, verificare che il testo non contenga interruzioni di riga (invisibili). Si consiglia di digitare i messaggi manualmente invece di copiarli e incollarli, per evitare errori di visualizzazione.

Se come tipo si seleziona "Valore word" (Word value), come mostrato nella Figura 7-26:

<img src="../../setting/dig-alarm.files/dig-alarm3352.png" width="556" />

Figura 7-26    Finestra di allarme digitale "Valore word"

Selezionato un valore, l'allarme scatta quando il valore dell'indirizzo è uguale al valore selezionato nell'elenco.

Posizionare un oggetto Allarme con 7 righe, come nell'esempio della Figura 7-24, e una Barra allarmi dinamica con le proprietà impostate come nella Figura 7-27:

<img src="../../setting/dig-alarm.files/dig-alarm3691.png" width="675" />

Figura 7-27    Finestra delle proprietà della Barra allarmi dinamica

Aggiungere infine sei pulsanti bit con indirizzo di scrittura LB1-LB6, impostando per ciascuno le funzioni "Commutazione" (Alternation), "Monitoraggio" (Monitor) e "Indirizzo di monitoraggio uguale all'indirizzo di scrittura". Fatto ciò, fare clic su "Salva" nella barra degli strumenti per salvare il progetto, eseguire il comando "Offline" della voce "Download" nella barra dei menu e fare clic sui pulsanti bit LB1, LB2, LB4 e LB6. L'oggetto Allarme e la Barra allarmi dinamica mostreranno i messaggi di LB1, LB2, LB4 e LB6 definiti in "Allarmi digitali". Facendo di nuovo clic sui pulsanti, l'"Oggetto allarme" e la "Barra allarmi dinamica" non mostrano più nulla, perché la funzione di commutazione riporta i valori a 0.

<img src="../../setting/dig-alarm.files/dig-alarm4400.png" width="130" />

Nota: con la funzione di cambio lingua sono disponibili messaggi di allarme diversi per ciascuna lingua.

Nota: gli HMI serie HM supportano fino a 10 allarmi digitali.
