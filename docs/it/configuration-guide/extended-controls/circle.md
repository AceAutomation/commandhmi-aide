# Cerchio dinamico

Il cerchio dinamico è un elemento grafico posizionato nella pagina che si sposta e cambia dimensione secondo un percorso determinato dal valore dell'indirizzo di monitoraggio. Per aggiungere l'oggetto e modificarne le proprietà:

Selezionare l'icona del cerchio dinamico<img src="../../../configuration-guide/extended-controls/circle.files/image002.jpg" width="32" /> nella barra degli strumenti, come mostrato nella Figura 4-56:

Figura 4-56    Finestra del cerchio dinamico

Il cerchio dinamico legge tre gruppi di valori, che rappresentano rispettivamente la coordinata x e la coordinata y del centro e il raggio del cerchio. La modalità di lettura di questi indirizzi dipende dal tipo di dato selezionato.

• Controllo (Control):

• Centro (Center): il cerchio si sposta seguendo la posizione del centro, con raggio invariato.

• Raggio (Radius): cambia solo il raggio, senza spostamento.

• Centro e raggio (Center & Radius): cambiano sia il raggio, in base all'indirizzo del raggio, sia la posizione del centro, in base agli indirizzi delle coordinate x e y.

• Trasparenza (Transparency): trasparenza del colore di sfondo del cerchio dinamico.

<span id="OLE_LINK564"></span><span id="OLE_LINK565"></span>• Pieno (Solid):

Se Solid non è selezionato, il cerchio è vuoto, cioè senza colore di sfondo; altrimenti è pieno e il colore di sfondo si imposta con l'opzione relativa.

• Bordo

Se questa opzione non è selezionata, il cerchio non ha bordo e il colore del bordo non è modificabile; altrimenti il cerchio ha un bordo, il cui colore si imposta con l'opzione colore bordo.

Esempio:

Con tipo di dato "intero a 16 bit", vengono letti tre dati consecutivi, secondo il formato di indirizzo del modello di PLC, che rappresentano coordinata x e y del centro e raggio. Con indirizzo di monitoraggio LW1, <span id="OLE_LINK548"></span><span id="OLE_LINK549"></span>vengono letti LW1, LW2 e LW3, con il significato seguente:

Il valore di LW1 è la coordinata x del centro.

<span id="OLE_LINK552"></span><span id="OLE_LINK553"></span>         Il valore di LW2 è la coordinata y del centro.

Il valore di LW3 è il raggio del cerchio.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Qualunque sia l'opzione di controllo selezionata (Center o Radius), l'HMI legge comunque i tre indirizzi, con lo stesso significato. Per esempio, selezionando Radius con indirizzo di monitoraggio LW1, il raggio resta comunque controllato solo da LW3.

Con tipo di dato "intero a 32 bit" e indirizzo di monitoraggio LW1, vengono letti LW1, LW3 e LW5, con il significato seguente:

<span id="OLE_LINK550"></span><span id="OLE_LINK551"></span>Il valore di LW1 è la coordinata x del centro.

Il valore di LW3 è la coordinata y del centro.

Il valore di LW5 è il raggio del cerchio.

Con tipo di dato "intero a 32 bit", secondo il formato di indirizzo del modello di PLC, i tre dati (coordinate x e y del centro e raggio) si trovano a intervalli di 2 a partire dall'indirizzo di monitoraggio.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".
