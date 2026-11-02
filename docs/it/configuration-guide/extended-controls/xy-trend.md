# Grafico di tendenza XY

**Presentazione del grafico di tendenza XY:**

Visualizzazione dinamica e continua dei valori delle variabili.

Traccia più curve di riferimento, usando i valori di due registri consecutivi come coordinate orizzontale e verticale, per osservarne l'andamento in modo preciso e intuitivo.

Possono essere visualizzate fino a 8 linee spezzate (grafico a linee).

L'aggiunta e la modifica delle proprietà del grafico di tendenza XY sono simili a quelle del grafico di tendenza, a cui si rimanda. Aprire l'icona<img src="../../../configuration-guide/extended-controls/xy-trend.files/image002.jpg" width="36" />

Aprire la finestra delle proprietà del grafico di tendenza XY; per le impostazioni vedere il "Grafico di tendenza". Nel grafico di tendenza ogni linea rappresenta il valore di indirizzi consecutivi a partire dall'indirizzo indicato, mentre nel grafico XY ogni linea rappresenta il valore di due indirizzi consecutivi a partire dall'indirizzo indicato.

**Uso del grafico di tendenza XY:**

Colore (Color): colore della linea di rilevamento (linea di riferimento).

Indirizzo di rilevamento (Detection address): il valore della linea di rilevamento corrente viene scritto in questo indirizzo.

Per esempio, con tipo di dato a 16 bit e 4 gruppi di dati, se l'indirizzo inserito è LW3 vengono letti 8 indirizzi consecutivi:

LW3: linea 1, valore sull'asse X

LW4: linea 1, valore sull'asse Y

LW5: linea 2, valore sull'asse X

LW6: linea 2, valore sull'asse Y

LW7: linea 3, valore sull'asse X

LW8: linea 3, valore sull'asse Y

LW9: linea 4, valore sull'asse X

LW10: linea 4, valore sull'asse Y

Gli indirizzi letti sono LW3-LW10, cioè 8 indirizzi. Quindi, con dati a 16 bit e N gruppi, vengono letti 2 \* N indirizzi consecutivi secondo le regole di indirizzamento del modello di PLC.

Con tipo di dato a 32 bit e 3 gruppi di dati, se l'indirizzo inserito è LW3 occorre leggere in sequenza 12 word.

LW3: linea 1, valore sull'asse X

LW5: linea 1, valore sull'asse Y

LW7: linea 2, valore sull'asse X

LW9: linea 2, valore sull'asse Y

LW11: linea 3, valore sull'asse X

LW13: linea 3, valore sull'asse Y

Gli indirizzi letti sono LW3-LW14, cioè 12 word. Quindi, con dati a 32 bit e N gruppi, vengono letti 2 \* N valori a intervalli di 2 indirizzi secondo le regole di indirizzamento del modello di PLC.
