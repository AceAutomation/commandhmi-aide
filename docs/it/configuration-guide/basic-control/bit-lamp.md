# Spia di bit

La spia di bit permette di monitorare lo stato ON/OFF di un contatto bit del dispositivo collegato e di visualizzarlo sullo schermo dell'HMI.

Come mostrato nella Figura 4-78:

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image007.jpg" width="554" alt="2018_11_20_14_25_09.jpg" />

Figura 4-78

Configurazione di una spia di bit:

1\. Selezionare l'icona Bit Lamp<img src="../../../configuration-guide/basic-control/bit-lamp.files/image002.jpg" width="31" /> nella barra degli strumenti: si apre la finestra di dialogo mostrata nella Figura 4-79:

Figura 4-79    Finestra di dialogo Bit Lamp

• Tipo di dato (Data Type): l'elenco a discesa offre tre opzioni: Bit, Word Bit e Double-word Bit. Con "Bit" l'indirizzo monitorato (letto) è un indirizzo bit; con Double-word Bit è un indirizzo double word.

• Numero di bit (Bit Number): se il tipo di dato è "Word Bit" o "Double-word Bit", il valore dell'indirizzo monitorato (stato ON/OFF) è dato dal bit indicato. Va da 0 a 15 per Word Bit e da 0 a 31 per Double-word Bit.

Per esempio, con "Word Bit" selezionato e indirizzo monitorato LW1 di valore 23, se il numero di bit è 3 lo stato è 0, perché 23 in binario è 10111 e il quarto bit da destra (bit 3) vale 0.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Nota: <span id="OLE_LINK707"></span><span id="OLE_LINK706"></span>per Forma, Colore bordo, Colore primo piano, Colore sfondo e Motivo, vedere l'oggetto Pulsante di bit.

2\. Nella scheda "General" delle proprietà della spia di bit, scegliere l'indirizzo da monitorare. Nella scheda "Mark" si impostano testi e immagini da visualizzare e l'eventuale lampeggio.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Nota: la scheda "Mark" della spia di bit è uguale a quella del pulsante di bit, a cui si rimanda.

3\. Per modificare le proprietà della spia, fare doppio clic su di essa e reimpostarle nella finestra delle proprietà.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Nota: la scheda Visibility della spia di bit è uguale a quella del pulsante di bit, a cui si rimanda.

Dopo aver impostato le proprietà, fare clic su "OK" per aggiungere l'oggetto all'area di visualizzazione (cioè la pagina)
