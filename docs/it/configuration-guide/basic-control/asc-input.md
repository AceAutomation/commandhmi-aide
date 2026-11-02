# Inserimento ASCII

Fare clic sull'icona del pulsante ASCII Input<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input38.png" width="30" />: si apre la finestra di dialogo mostrata nella Figura 4-100:

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input93.png" width="665" />

Figura 4-100 Finestra di dialogo ASCII Input

• Indirizzo di scrittura (Write address): indirizzo in cui scrivere il testo ASCII.

• Monitoraggio (Monitor): valore dell'indirizzo letto e visualizzato dall'oggetto.

• Indirizzo di monitoraggio uguale all'indirizzo di scrittura (Monitor address identical to write address): l'indirizzo di monitoraggio coincide con quello di scrittura.

• Indirizzo di monitoraggio (Monitor address): indirizzo da leggere

• Totale (Total): numero massimo di caratteri visualizzabili.

• Dimensione carattere (Font Size): dimensione dei caratteri visualizzati

• Scambia byte alto e basso dell'input (Exchange high and low bytes of input): il byte alto del valore inserito dall'utente viene scambiato con il byte basso, quindi il dato risultante viene memorizzato nell'indirizzo word monitorato.

• Password: se selezionata, l'oggetto non mostra i caratteri ma degli asterischi (\*)

• Usa UNICODE (Use UNICODE): il valore dell'indirizzo monitorato viene visualizzato con codifica Unicode

Allineamento:

• Sinistra (Left): il testo è visualizzato nella parte sinistra dell'area di visualizzazione.

• Centro (Center): il testo è visualizzato al centro dell'area di visualizzazione.

• Destra (Right): il testo è visualizzato nella parte destra dell'area di visualizzazione.

• Usa macro (Use Macro): selezionando "Use Macro" viene visualizzato l'elenco delle macro; l'utente può sceglierne una da eseguire alla pressione del pulsante. Nell'elenco a discesa compaiono solo le macro compilate.

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input1310.png" width="130" />

Nota: per esempio, se si seleziona il tipo di dato a 32 bit, l'indirizzo di memorizzazione occupa 2 word. Se si scrivono dati nel registro dati di un PLC SIEMENS all'indirizzo V10, vengono occupati i registri V10 e V11; se l'utente monitora anche V11 con un altro oggetto, si verifica un errore. Prestare attenzione all'uso dei tipi di dato a 32 bit per evitare errori di dati e di indirizzo.

Nota: le altre funzioni della scheda General sono le stesse della visualizzazione ASCII, a cui si rimanda.

Nota: per l'uso delle schede "Advanced" e "Visibility", vedere il Pulsante di bit.
