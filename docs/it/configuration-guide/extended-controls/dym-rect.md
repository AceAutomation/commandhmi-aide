# Rettangolo dinamico

Le funzioni del rettangolo dinamico sono simili a quelle del cerchio dinamico: entrambi rappresentano in tempo reale lo stato degli indirizzi monitorati, cambiando posizione o dimensioni dell'elemento grafico in base ai loro valori.

Selezionare l'icona del rettangolo dinamico<img src="../../../configuration-guide/extended-controls/dym-rect.files/image002.jpg" width="34" /> nella barra degli strumenti per aprire la finestra di dialogo mostrata nella Figura 4-57.

Figura 4-57    Finestra del rettangolo dinamico

Il rettangolo dinamico legge quattro gruppi di valori, che rappresentano rispettivamente coordinata x, coordinata y, larghezza e altezza del rettangolo. La modalità di lettura dipende dal tipo di dato selezionato.

• Spessore linea (Line Width): spessore della linea

• Tipo (Type): angolo retto, smussato o arrotondato.

• Nota: il tipo ha effetto solo se lo spessore della linea è maggiore di 1.

Esempio:

Con tipo di dato "intero a 16 bit" e indirizzo di monitoraggio LW1, vengono letti i quattro indirizzi LW1, LW2, LW3 e LW4, con il significato seguente:

Il valore di LW1 è la coordinata x <span id="OLE_LINK558"></span><span id="OLE_LINK559"></span>del rettangolo;

Il valore di LW2 è la coordinata y del rettangolo;

Il valore di LW3 è la larghezza del rettangolo;

Il valore di LW4 è l'altezza del rettangolo.

Con tipo di dato "intero a 16 bit", vengono letti quattro dati consecutivi, secondo il formato di indirizzo del modello di PLC, che rappresentano coordinata x, coordinata y, larghezza e altezza del rettangolo.

Con tipo di dato "intero a 32 bit" e indirizzo di monitoraggio LW1, vengono letti LW1, LW3, LW5 e LW7.

Il valore di LW1 è la coordinata x del rettangolo;

Il valore di LW3 è la coordinata y del rettangolo;

Il valore di LW5 è la larghezza del rettangolo;

Il valore di LW7 è l'altezza del rettangolo;

Con tipo di dato "intero a 32 bit", secondo il formato di indirizzo del modello di PLC, i quattro dati (coordinate x e y, larghezza e altezza) si trovano a intervalli di 2 a partire dall'indirizzo di monitoraggio.

**Controllo (Control):**

• Posizione (Position): altezza e larghezza del rettangolo non cambiano, mentre la posizione segue i valori degli indirizzi delle coordinate x e y.

• Dimensioni (Size): altezza e larghezza del rettangolo cambiano rispetto a uno dei quattro punti fissi seguenti, mentre la posizione non cambia.

• In alto a sinistra (Upper Left): <span id="OLE_LINK562"></span><span id="OLE_LINK563"></span>il punto fisso è l'angolo in alto a sinistra e il rettangolo si estende verso l'angolo in basso a destra.

• In alto a destra (Upper right): il punto fisso è l'angolo in alto a destra e il rettangolo si estende verso l'angolo in basso a sinistra.

• In basso a sinistra (Lower Left): il punto fisso è l'angolo in basso a sinistra e il rettangolo si estende verso l'angolo in alto a destra.

• In basso a destra (Lower right): il punto fisso è l'angolo in basso a destra e il rettangolo si estende verso l'angolo in alto a sinistra.

**Pieno (Solid):**

Se Solid non è selezionato, il rettangolo è vuoto, cioè senza colore di sfondo; altrimenti è pieno e il colore di sfondo si imposta con l'opzione relativa.

**Bordo (Border):**

Se questa opzione non è selezionata, il rettangolo non ha bordo e il colore del bordo non è modificabile; altrimenti il rettangolo ha un bordo, il cui colore si imposta con l'opzione colore bordo.

Trasparenza (Transparency): trasparenza del colore di sfondo del rettangolo dinamico.

<span id="OLE_LINK570"></span><span id="OLE_LINK571"></span><img src="../../../configuration-guide/extended-controls/dym-rect.files/image004.jpg" width="130" />

Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".
