# Grafico a barre

Il grafico, detto anche grafico a barre, serve principalmente a mostrare in tempo reale la variazione dei valori numerici sotto forma di barre, in modo più intuitivo. Può rappresentare la variazione dei registri dati del PLC o di altri dispositivi collegati, nonché la variazione in tempo reale di tutte le grandezze analogiche del processo. Vedere la figura seguente.

<img src="../../../configuration-guide/basic-control/bar.files/image006.jpg" width="535" alt="2018_11_20_14_27_19.jpg" />

Figura 4-101   Grafico a barre

Per aggiungere un grafico a barre e modificarne le proprietà, procedere come segue:

1\. Selezionare l'icona Bar Chart <img src="../../../configuration-guide/basic-control/samdra8.gif" width="20" />nella barra degli strumenti o nel menu Tools: compare la finestra di dialogo mostrata nella Figura 4-102.

2\. Impostare le proprietà del grafico a barre nella finestra delle proprietà, quindi fare clic su OK:

• Colore sfondo (Background color): colore di sfondo del grafico a barre

• Colore bordo (Border Color): imposta il colore del bordo della barra. Nella Figura 4-102 l'impostazione del colore del bordo non ha effetto; selezionando un'altra "forma" della barra la modifica diventa visibile.

• Trasparente (Transparent): rende trasparente lo sfondo della barra

• Direzione (Direction): direzione di riempimento della barra; sono disponibili quattro direzioni: verso l'alto, verso il basso, verso sinistra e verso destra.

• Verso l'alto (Upward): all'aumentare del valore dell'indirizzo monitorato, la barra si riempie dal basso verso l'alto

• Verso il basso (Downward): all'aumentare del valore dell'indirizzo monitorato, la barra si riempie dall'alto verso il basso

• Verso sinistra (Leftward): all'aumentare del valore dell'indirizzo monitorato, la barra si riempie da destra verso sinistra

• Verso destra (Rightward): all'aumentare del valore dell'indirizzo monitorato, la barra si riempie da sinistra verso destra

• Tipo di dato (Data type): tipo di dato del valore letto, cioè indirizzo word o double word.

• Indirizzo di monitoraggio (Monitor address): indirizzo del registro dati visualizzato nella barra, cioè l'indirizzo letto

• Massimo (Maximum): valore massimo dell'indirizzo monitorato (letto). Se il valore letto è superiore, la barra è piena e non varia più

• Minimo (Minimum): valore minimo dell'indirizzo monitorato (letto). Se il valore letto è inferiore, la barra è vuota e non varia più

• Intervallo variabile (Variable range): i valori massimo e minimo variano dinamicamente in base all'indirizzo inserito dall'utente; il tipo di dato dell'indirizzo è quello impostato in "Data type"

• Barra bipolare (Bipolar bar): la barra può estendersi su entrambi i lati in base al valore del registro.

• Punto centrale (Midpoint): punto centrale della barra bipolare.

<img src="../../../configuration-guide/basic-control/bar.files/image002.jpg" width="675" />

Figura 4-102   Finestra di dialogo del grafico a barre

Per esempio, con massimo 100, minimo 10 e riempimento verso l'alto, selezionando la barra bipolare e inserendo 70 come "Midpoint", l'aumento del valore dell'indirizzo monitorato a partire da 0 viene rappresentato come nella Figura 4-103.

<img src="../../../configuration-guide/basic-control/samdra10.gif" width="534" />

Figura 4-103 Grafico a barre bipolare

3\. Modifica del grafico a barre: facendo clic sul grafico compaiono otto piccoli punti verdi che si possono trascinare con il mouse per ridimensionarlo.

Scheda "Range":

Questa scheda serve a visualizzare con colori di primo piano e di sfondo diversi i valori dell'indirizzo monitorato che rientrano in intervalli specifici. Le proprietà sono mostrate nella Figura 4-104:

Figura 4-104   Scheda Range del grafico a barre

• Visualizza intervallo (Display Range): selezionando questa opzione, l'utente può impostare i limiti inferiore e superiore e i colori di sfondo per il livello basso e alto. Il valore letto dall'oggetto viene rappresentato con colori diversi in base ai limiti impostati.

• Intervallo variabile (Variable range): i valori di "Lower Limit" e "Higher Limit" variano dinamicamente in base all'indirizzo inserito dall'utente

• Limite inferiore (Lower limit): imposta il limite inferiore. Quando il valore visualizzato è inferiore a questo limite, lo sfondo assume il colore impostato in Low Level Background Color.

• Limite superiore (Higher limit): imposta il limite superiore. Quando il valore visualizzato è superiore a questo limite, lo sfondo assume il colore impostato in High Level Background Color.

<span id="OLE_LINK727"></span><span id="OLE_LINK726"></span>Dopo le impostazioni, fare clic su "OK" per aggiungere l'oggetto all'area di visualizzazione (la pagina)

<img src="../../../configuration-guide/basic-control/bar.files/image004.jpg" width="130" />

Nota: se il valore dell'indirizzo monitorato è compreso tra massimo e minimo, i colori di primo piano e di sfondo sono quelli impostati nella scheda "General".

Nota: per l'uso della scheda "Visibility", vedere il "Pulsante di bit".
