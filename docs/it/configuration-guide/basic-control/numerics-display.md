# Visualizzazione numerica

La visualizzazione numerica è un oggetto di uso comune che visualizza i valori memorizzati nei registri dati del PLC o di altri dispositivi collegati, come velocità, corrente, pressione, ecc.

Selezionare l'icona di visualizzazione<img src="../../../configuration-guide/basic-control/numerics-display.files/image002.jpg" width="30" /> nella barra degli strumenti: il sistema apre la finestra di dialogo mostrata nella Figura 4-91:

Figura 4-91 Finestra di dialogo Numeric Display

In questa finestra si impostano le modalità di visualizzazione del valore memorizzato nel registro dati del PLC o di altri dispositivi collegati: numero di cifre, decimali, dimensione del carattere, colore, allineamento e formato del testo.

• Tipo di dato (Data type): l'utente sceglie il tipo di dato in base al valore del registro da monitorare.

• Tipo di visualizzazione (Display Type): l'utente sceglie il tipo di visualizzazione in base alle esigenze del progetto.

• Indirizzo di monitoraggio (Monitor address): indirizzo di lettura, cioè l'indirizzo del registro dati del PLC o di altri dispositivi collegati che contiene il dato da visualizzare.

• Decimali (Decimal Place): numero di cifre decimali visualizzate.

• Carattere (Font): scegliere un carattere normale o un carattere digitale.

• Dimensione carattere (Font size): scegliere la dimensione del carattere visualizzato.

• Allineamento (Alignment): l'impostazione predefinita è Center.

• Sinistra (Left): il valore è visualizzato nella parte sinistra dell'area di visualizzazione.

• Centro (Center): il valore è visualizzato al centro dell'area di visualizzazione.

• Destra (Right): il valore è visualizzato nella parte destra dell'area di visualizzazione.

• Formato (Justification): l'impostazione predefinita è la soppressione degli zeri.

• Soppressione degli zeri (Zero-suppression): gli zeri prima delle cifre significative non vengono visualizzati. <span id="OLE_LINK668"></span><span id="OLE_LINK669"></span>Se il valore dell'indirizzo monitorato è 00123, intero positivo a 16 bit, viene visualizzato 123.

• Zeri iniziali (Zero Header): vengono visualizzati gli zeri iniziali fino al numero di cifre impostato. Se il valore dell'indirizzo monitorato è 00123, intero positivo a 16 bit, viene visualizzato 00123.

• Spazi iniziali (Space Header): al posto degli zeri iniziali vengono visualizzati degli spazi. Se il valore dell'indirizzo monitorato è 00123, intero positivo a 16 bit, viene visualizzato   123.

• Colore testo (Text Color): colore del carattere dei dati visualizzati;

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Nota: per forma, colore bordo, colore primo piano, colore sfondo e stile, vedere l'oggetto "Pulsante di bit".

Nota: <span id="OLE_LINK678"></span><span id="OLE_LINK679"></span>fare doppio clic sulla casella di visualizzazione per modificarne contenuto e proprietà. Quando l'oggetto è attivo nell'HMI, compare una tastiera a schermo che permette all'utente di inserire i dati.

Nota: <span id="OLE_LINK684"></span><span id="OLE_LINK685"></span>il numero di decimali influisce sulla visualizzazione. Se il tipo di dato è intero positivo o intero a 16/32 bit, il valore visualizzato si ottiene spostando il punto decimale del valore letto del numero di cifre impostato: se il valore letto è 212 e i decimali sono 2, viene visualizzato 2.12. Se il tipo di dato è virgola mobile a 32 bit, il valore non viene spostato ma vengono visualizzate solo le cifre decimali impostate: se il valore letto è 2.123 e i decimali sono 2, viene visualizzato 2.12.

Nota: il numero totale di cifre è la somma delle cifre della parte intera e della parte decimale. Se la parte intera del valore è più lunga di quella impostata, viene visualizzata la lunghezza effettiva. Per esempio, per il valore 2123 con lunghezza 2 e 1 decimale, viene visualizzato 212.3.

La scheda Advanced della visualizzazione numerica offre funzioni avanzate, tra cui la scalatura e la visualizzazione per intervalli, come mostrato nella Figura 4-92:

<img src="../../../configuration-guide/basic-control/numerics-display.files/image005.jpg" width="675" />

Figura 4-92    Scheda Advanced della visualizzazione numerica

• Scalatura (Scaling): se selezionata, il dato visualizzato è: valore dell'indirizzo monitorato (letto) × guadagno + offset

<span id="OLE_LINK696"></span><span id="OLE_LINK697"></span>• Visualizza intervallo (Display Range): selezionando questa opzione, l'utente può impostare i limiti inferiore e superiore e i colori di sfondo per il livello basso e alto. Il valore letto dall'oggetto viene rappresentato con colori diversi in base ai limiti impostati.

• Intervallo variabile (Variable range): i valori di "Lower Limit" e "Higher Limit" variano dinamicamente in base all'indirizzo inserito dall'utente

• Limite inferiore (Lower limit): imposta il limite inferiore. Quando il valore visualizzato è inferiore a questo limite, lo sfondo assume il colore impostato in Low Level Background Color.

• Limite superiore (Higher limit): imposta il limite superiore. Quando il valore visualizzato è superiore a questo limite, lo sfondo assume il colore impostato in High Level Background Color.

Per esempio, impostando il colore di sfondo e del testo nella scheda General e selezionando i colori di visualizzazione per intervalli come nella Figura 4-93:

<img src="../../../configuration-guide/basic-control/numerics-display.files/image006.jpg" width="673" />

<img src="../../../configuration-guide/basic-control/numerics-display.files/image007.jpg" width="349" />

Figura 4-93 Impostazione della visualizzazione per intervalli

Al variare del valore dell'indirizzo monitorato, il testo e lo sfondo della visualizzazione numerica cambiano di conseguenza, come mostrato nella Figura 4-94:

<img src="../../../configuration-guide/basic-control/samdra93.gif" width="508" />

Figura 4-94    Esempio di visualizzazione numerica

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Nota: per la scheda Visibility, vedere l'uso dell'oggetto "Pulsante di bit".

Nota: <span id="OLE_LINK682"></span><span id="OLE_LINK683"></span>se si seleziona il tipo di dato a 32 bit, l'indirizzo di memorizzazione occupa 2 word. Per esempio, se si scrivono dati nel registro dati di un PLC SIEMENS all'indirizzo V10, vengono occupati i registri V10 e V11; se l'utente monitora anche V11 con un altro oggetto, si verifica un errore. Prestare attenzione all'uso dei tipi di dato a 32 bit per evitare errori di dati e di indirizzo.

Dopo l'impostazione, fare clic su "OK" per aggiungere l'oggetto all'area di visualizzazione (cioè la pagina)
