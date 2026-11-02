# Visualizzazione immagini

La visualizzazione immagini è un'estensione dell'oggetto Immagine statica: l'immagine statica può mostrare una sola immagine, mentre la visualizzazione immagini può mostrarne fino a 32. Il comportamento dipende dal tipo di stato selezionato dall'utente.

La procedura è la seguente:

Fare clic sull'icona Picture display<img src="../../../configuration-guide/basic-control/picture-display.files/image002.jpg" width="32" /> nella barra degli strumenti: si apre la finestra di dialogo mostrata nella Figura 4-110:

Figura 4-110   Finestra di dialogo Picture Display

• Bit: con Bit selezionato, gli stati sono solo due, 0 e 1, e l'indirizzo di monitoraggio deve essere un indirizzo bit. L'oggetto mostra l'immagine corrispondente allo stato 0 o 1 dell'indirizzo monitorato.

• Valore (Value): con Value selezionato, gli stati possono essere fino a 2048 e l'immagine visualizzata dipende dal valore dell'indirizzo monitorato: con valore 0 viene mostrata l'immagine dello stato 0, e così via.

• Cambio automatico (Auto-switching): con questa opzione gli stati possono essere fino a 2048 e l'oggetto non cambia immagine in base all'indirizzo monitorato: basta impostare il numero totale di stati e la frequenza di cambio. Durante l'esecuzione nell'HMI, l'oggetto cambia automaticamente le immagini nell'intervallo impostato.

<img src="../../../configuration-guide/basic-control/picture-display.files/image004.jpg" width="130" />

Nota: la scheda "Picture" della visualizzazione immagini è simile a quella della "Spia multistato", a cui si rimanda.

Nota: per l'uso della scheda "Visibility", vedere l'oggetto "Pulsante di bit".

Dopo le impostazioni, fare clic su "OK" per aggiungere l'oggetto all'area di visualizzazione (la pagina).
