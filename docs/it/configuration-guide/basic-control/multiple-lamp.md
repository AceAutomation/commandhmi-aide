# Spia multistato

La spia multistato serve principalmente a visualizzare stati diversi in base al valore dell'indirizzo di monitoraggio. Può visualizzare fino a 32 stati.

Fare clic sul pulsante Multi-state indicator<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image002.jpg" width="28" /> nella barra degli strumenti per aprire la finestra di dialogo mostrata nella Figura 4-83.

Figura 4-83    Finestra di dialogo della spia multistato

1\. Generale (General):

• Stato (State): l'utente può modificare il valore di stato per impostare, per ciascuno stato, il colore del bordo, di primo piano, di sfondo e il motivo dell'oggetto

• Tipo di stato (State Type): (supponendo che il valore inserito dall'utente sia n)

• Valore (Value): il valore scritto va da zero al numero totale di stati meno 1.

• Bit di registro (Register Bit): il valore scritto è 2 elevato alla n.

E.g.:

<span id="OLE_LINK657"></span><span id="OLE_LINK511"></span><span id="OLE_LINK510"></span>Indirizzo di monitoraggio (lettura) LW3 e numero totale di stati 8. Fare clic su OK per aggiungere l'oggetto alla pagina, quindi aggiungere alla pagina un oggetto di inserimento numerico con indirizzo di scrittura e di monitoraggio LW3 e infine salvare il progetto.

In simulazione o sull'HMI, l'utente fa clic sull'oggetto di inserimento numerico e inserisce un valore di stato con la tastiera. Se il valore inserito è 2, il valore dell'indirizzo di monitoraggio (lettura) corrisponde allo stato 1 e l'oggetto mostra il testo dello stato 1 (impostato nella scheda Text); analogamente, se in LW3 viene inserito 8, l'oggetto mostra il testo dello stato 3. Se in LW3 viene inserito 3, la spia multistato non passa ad alcuno stato.

• Valori di stato personalizzati (Customize status value): selezionando questa opzione compare il pulsante "Defined status value"; facendo clic si apre la finestra "Customize status value", come mostrato nella Figura 4-84:

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image004.jpg" width="333" />

Figura 4-84    Finestra dei valori di stato definiti dall'utente

In questa finestra la colonna "S \#" indica lo stato: il valore selezionato corrisponde al valore dello stato. Fare doppio clic su un valore per inserire il valore da associare allo stato.

Per esempio: indirizzo di monitoraggio (lettura) LW3 e numero totale di stati 8. Fare clic su OK per aggiungere l'oggetto alla pagina, quindi aggiungere alla pagina un oggetto di inserimento numerico con indirizzo di scrittura e di monitoraggio LW3 e infine salvare il progetto.

In simulazione o sull'HMI, l'utente fa clic sull'oggetto di inserimento numerico e inserisce un valore di stato con la tastiera. Se il valore inserito è 1, l'oggetto mostra il testo dello stato 1 (impostato nella scheda Text); analogamente, se in LW3 viene inserito 33, l'oggetto mostra il testo dello stato 2. Se in LW3 viene inserito 2, la spia multistato non passa ad alcuno stato.

• Tipo di dato (Data Type): tipo di dato dell'indirizzo di scrittura e dell'indirizzo di monitoraggio (lettura)

• Indirizzo di monitoraggio (Monitor address): indirizzo di lettura, il cui valore determina lo stato visualizzato dall'oggetto.

• Numero totale di stati (Total states): l'utente può impostare il numero totale di stati secondo necessità, fino a 32 stati (dallo stato 0 allo stato 31).

Per esempio, con tipo di dato intero positivo a 16 bit e 32 stati, quando il valore memorizzato nell'indirizzo di monitoraggio è 0 la spia multistato mostra il testo e l'immagine dello stato 0; se il valore è 5 mostra il testo e l'immagine dello stato 5. Se il valore è 60, la spia continua a mostrare lo stato 31, perché il numero massimo di stati è 32.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Nota: per forma, colore bordo, colore primo piano, colore sfondo e motivo, vedere l'oggetto "Pulsante di bit".

Nota: se per la spia multistato si seleziona il tipo di dato a 32 bit, l'indirizzo di memorizzazione occupa 2 word. <span id="OLE_LINK673"></span><span id="OLE_LINK672"></span>Per esempio, se si scrivono dati nel registro dati di un PLC SIEMENS all'indirizzo V10, vengono occupati i registri V10 e V11; se l'utente monitora anche V11 con un altro oggetto, si verifica un errore. Prestare attenzione all'uso dei tipi di dato a 32 bit per evitare errori di dati e di indirizzo.

Nota: il tipo di dato deve corrispondere ai dati da visualizzare.

2\. Testo (Text):

Fare clic sulla scheda "Text" della finestra delle proprietà della spia multistato per visualizzare le impostazioni del testo, come mostrato nella Figura 4-85:

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image006.jpg" width="675" />

Figura 4-85 Scheda Text della spia multistato

Tutte le lingue usano il testo della prima lingua: opzione usata nei progetti multilingua, quando in "Language" di Gestione progetto il numero totale di lingue è maggiore di 1; in questo caso il testo dell'oggetto non cambia al cambio di lingua.

<span id="OLE_LINK737"></span><span id="OLE_LINK736"></span>• Lingua (Language): opzione usata nei progetti multilingua. Selezionando una lingua si possono inserire testi diversi per i vari stati, realizzando così la gestione multilingua. (In un pulsante funzione, selezionare l'opzione "Switch language" e la lingua di destinazione: in simulazione o sull'HMI, facendo clic sul pulsante tutti gli oggetti con testo passano alla lingua specificata). Per ogni lingua testo, carattere e dimensione possono essere diversi, mentre colore, spaziatura e posizione sono comuni.

• Carattere (Font): tipo di carattere del testo; stati diversi e lingue diverse possono usare caratteri diversi.

• Dimensione carattere (Font Size): dimensione del testo; stati diversi e lingue diverse possono usare dimensioni diverse.

• Colore, spaziatura, posizione (Color, Kerning, Position): impostano colore, spaziatura e allineamento del testo selezionato. Se in Gestione progetto le lingue sono più di una e nella scheda Text si seleziona una lingua diversa dalla lingua 1, queste tre impostazioni non sono modificabili perché coincidono con quelle della lingua 1.

3\. Immagine (Picture):

Fare clic sulla scheda Picture della finestra delle proprietà della spia multistato per visualizzare le impostazioni mostrate nella Figura 4-86.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image007.jpg" width="675" />

Figura 4-86 Scheda Picture della spia multistato

Questa scheda serve principalmente ad associare immagini ai diversi stati. Per impostazione predefinita gli stati non hanno immagini, che possono essere aggiunte secondo necessità.

• Procedura: selezionare nell'elenco lo stato di cui modificare l'immagine, quindi scegliere l'immagine nella libreria di sistema oppure tramite un percorso di Windows. Selezionando i diversi stati, le immagini corrispondenti vengono visualizzate sotto. L'utente può inoltre decidere se adattare l'immagine all'oggetto: in caso contrario può modificarne margine e posizione per migliorarne l'aspetto.

• Adatta all'oggetto (Fit to Object): se selezionata, l'immagine ha le stesse dimensioni dell'oggetto nella scheda General e le opzioni Margin e Position sono nascoste; altrimenti sono visibili.

Se si importa un'immagine da un file esterno, compare l'opzione "Transparent", che rende trasparente un colore specificato

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Nota: per la scheda Visibility, vedere l'oggetto "Pulsante di bit".

Dopo aver impostato tutte le proprietà, fare clic su "OK" per aggiungere l'oggetto alla pagina
