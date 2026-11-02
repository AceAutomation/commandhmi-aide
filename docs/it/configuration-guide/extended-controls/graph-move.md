# Movimento grafico

L'oggetto Movimento grafico permette di spostare nella pagina, in una direzione specifica, un elemento della galleria o un file grafico, in base al valore delle variabili associate. Permette di creare effetti di animazione nella pagina.

Per aggiungere l'oggetto Movimento grafico e modificarne le proprietà:

Selezionare il pulsante Graphic Move<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move351.png" width="35" /> nella barra degli strumenti, impostare le proprietà nella finestra che compare e fare clic su OK, come mostrato nella Figura 4-61:

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move459.png" width="662" />

Figura 4-61 Finestra Graphic Move

• Selezione dell'immagine:

Nella scheda Pictures, selezionare l'immagine da muovere, che può anche essere personalizzata.

• Indirizzo di monitoraggio (Monitor Address):

L'indirizzo di monitoraggio del movimento occupa tre indirizzi, corrispondenti al numero di stato, al valore sull'asse X e al valore sull'asse Y. Per esempio, con indirizzo di monitoraggio LW1 nella memoria interna e tipo di dato a 16 bit, i valori di LW1, LW2 e LW3 controllano direttamente lo stato, lo spostamento sull'asse X e lo spostamento sull'asse Y; con tipo di dato a 32 bit, lo stato è in LW1, la coordinata X in LW3 e la coordinata Y in LW5.

• Modalità (Method): gli esempi seguenti usano tutti LW1 della memoria interna come indirizzo di monitoraggio, con tipo di dato a 16 bit, per illustrare ciascun tipo di movimento:

• Movimento orizzontale lungo l'asse X: l'elemento si sposta solo orizzontalmente, non verticalmente, senza superare i limiti inferiore e superiore dell'asse X. Lo stato è il valore di LW1, la coordinata X il valore di LW2.

• Movimento verticale lungo l'asse Y: l'elemento si sposta solo verticalmente, non orizzontalmente, senza superare i limiti inferiore e superiore dell'asse Y. Lo stato è il valore di LW1, la coordinata Y il valore di LW2.

• Movimento orizzontale e verticale contemporaneo: l'elemento può spostarsi in orizzontale e in verticale, senza superare i limiti degli assi X e Y. Lo stato è il valore di LW1, la coordinata X il valore di LW2 e la coordinata Y il valore di LW3.

• Movimento orizzontale proporzionale lungo l'asse X: l'elemento si sposta solo orizzontalmente, non verticalmente, senza superare i limiti inferiore e superiore dell'asse X. Lo stato è il valore di LW1, la coordinata X il valore di LW2.

• Movimento verticale proporzionale lungo l'asse Y: l'elemento si sposta solo verticalmente, non orizzontalmente, senza superare i limiti inferiore e superiore dell'asse Y. Lo stato è il valore di LW1, la coordinata il valore di LW2.

• Movimento orizzontale proporzionale inverso lungo l'asse X: l'elemento si sposta solo orizzontalmente, non verticalmente, senza superare i limiti inferiore e superiore dell'asse X. Lo stato è il valore di LW1, la coordinata X il valore di LW2.

• Movimento verticale proporzionale inverso lungo l'asse Y: l'elemento si sposta solo verticalmente, non orizzontalmente, senza superare i limiti inferiore e superiore dell'asse Y. Lo stato è il valore di LW1, la coordinata il valore di LW2.

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move3614.png" width="130" />

• Per le schede "Text" e "Picture", vedere l'oggetto "Spia multistato".

• Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".

• La posizione dell'elemento in movimento si controlla modificando i valori degli ultimi due indirizzi di monitoraggio.

• La coordinata massima degli assi X / Y corrisponde alle dimensioni massime della pagina.
