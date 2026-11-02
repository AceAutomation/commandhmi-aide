# Pulsante multistato

Il pulsante multistato e la spia multistato hanno funzioni sostanzialmente uguali; l'unica differenza è che il pulsante multistato permette di inserire valori, mentre la spia si limita a indicarli. Procedere come segue:

Fare clic sull'icona del pulsante<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button271.png" width="31" /> nella barra degli strumenti per aprire la finestra di dialogo mostrata nella Figura 4-87.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button336.png" width="663" />

Figura 4-87 Finestra di dialogo del pulsante multistato

• Stato (State): l'utente può modificare il valore di stato e, per ciascuno stato, il colore del bordo, di primo piano, di sfondo e il motivo dell'oggetto

• Tipo di stato (State type): (supponendo che il valore inserito sia n)

• Valore (Value): il valore scritto è un numero compreso tra zero e il numero totale di stati.

• Bit di registro (Register bit): il valore scritto è 2 elevato alla n.

E.g:

Selezionare "Value" come tipo di stato, "Keyboard Input" come modalità e LW3 come indirizzo di scrittura, selezionare l'opzione "Monitor Address Identical to Write Address" e impostare il numero totale di stati a 8. Fare quindi clic su OK per aggiungere l'oggetto alla pagina e salvare il progetto.

In simulazione o sull'HMI, facendo clic sull'oggetto compare una tastiera in cui l'utente inserisce un valore di stato. Se il valore inserito è 3, nel registro LW3 viene scritto 2 elevato alla 3 e viene visualizzato il testo dello stato 3 (impostato nella scheda Text dell'oggetto). Viceversa, se nell'indirizzo LW3 viene inserito il valore 8, l'oggetto visualizza il testo dello stato 3; se viene inserito 5, l'oggetto non visualizza alcuno stato.

• Valori di stato personalizzati (Customize Status Value): selezionando questa opzione compare il pulsante "Define Status Value...", come mostrato nella Figura 4-88:

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1611.png" width="662" />

Figura 4-88 Pulsante multistato con valori di stato personalizzati

Facendo clic sul pulsante "Define status value..." si apre la finestra "Customize status value", come mostrato nella Figura 4-89:

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1799.png" width="333" />

Figura 4-89 Finestra di definizione dei valori di stato

In questa finestra, la colonna "S #" indica lo stato; il valore nella riga selezionata corrisponde al valore dello stato. Fare doppio clic per inserire il valore dello stato corrente.

Per esempio, selezionare "Customize status value" come tipo di stato, "Keyboard Input" come modalità e LW3 come indirizzo di scrittura, selezionare l'opzione "Monitor Address Identical to Write Address" e impostare il numero totale di stati a 8. Fare quindi clic su OK per aggiungere l'oggetto alla pagina e salvare il progetto. In simulazione o sull'HMI, facendo clic sull'oggetto compare una tastiera in cui l'utente inserisce un valore di stato. Se il valore inserito è 1, nel registro LW3 viene scritto 22 e viene visualizzato il testo dello stato 1 (impostato nella scheda Text dell'oggetto). Viceversa, se nell'indirizzo LW3 viene inserito il valore 33, l'oggetto visualizza il testo dello stato 2; se viene inserito 2, l'oggetto non visualizza alcuno stato.

• Modalità (Mode): sono disponibili sei funzioni: "Keyboard Input", "Output constant", "Increase", "Decrease", "Loopback increase" e "Loopback decrease".

• Inserimento da tastiera (Keyboard input): sono selezionabili tutte e tre le opzioni di "State Type". In simulazione o sull'HMI, facendo clic sull'oggetto compare una tastiera per inserire il valore, come mostrato nella Figura 4-90:

![](../../../configuration-guide/basic-control/multiple-button.files/001.png)

Figura 4-90 Tastiera

• Costante in uscita (Output constant): tra le tre opzioni di "State Type" è selezionabile solo "Value". Selezionando questa opzione compare il campo "constant" in cui impostare la costante; in simulazione o sull'HMI, facendo clic sull'oggetto viene scritto il valore costante impostato

• Incremento (Increase): tra le tre opzioni di "State Type" è selezionabile solo "Value". In simulazione o sull'HMI, ogni clic sull'oggetto aumenta lo stato di 1; l'incremento si arresta al numero totale di stati.

• Decremento (Decrease): tra le tre opzioni di "State Type" è selezionabile solo "Value". In simulazione o sull'HMI, ogni clic sull'oggetto diminuisce lo stato di 1; il decremento si arresta al limite degli stati.

• Incremento ciclico (Loopback increase): tra le tre opzioni di "State Type" è selezionabile solo "Value". In simulazione o sull'HMI, ogni clic sull'oggetto aumenta lo stato di 1; superato il numero totale di stati si torna allo stato 0.

• Decremento ciclico (Loopback decrease): tra le tre opzioni di "State Type" è selezionabile solo "Value". In simulazione o sull'HMI, ogni clic sull'oggetto diminuisce lo stato di 1; superato il limite si torna allo stato massimo.

• Tipo di dato (Data Type): tipo di dato dell'indirizzo di scrittura e dell'indirizzo di monitoraggio (lettura)

• Indirizzo di monitoraggio (Monitor address): indirizzo di lettura, il cui valore determina lo stato visualizzato dall'oggetto.

• Numero totale di stati (Total number of states): numero massimo di stati

• Usa macro (Use Macro): se selezionata, facendo clic sull'oggetto in simulazione o sull'HMI viene eseguita la macro scelta dall'utente.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button5026.png" width="130" />

Nota: per forma, colore bordo, colore primo piano, colore sfondo e motivo, vedere l'oggetto "Pulsante di bit".

Nota: per le schede "Text" e "Picture", vedere l'oggetto "Spia multistato".

Nota: per le schede "Advanced" e "Appearance", vedere l'oggetto "Pulsante di bit", a cui si rimanda anche per i tasti di scelta rapida.

Dopo aver impostato le proprietà, fare clic su "OK" per aggiungere l'oggetto all'area di visualizzazione (cioè la pagina)
