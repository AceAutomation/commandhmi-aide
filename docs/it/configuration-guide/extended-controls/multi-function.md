# Pulsante multifunzione

Il pulsante multifunzione permette di eseguire con un solo oggetto una sequenza di operazioni personalizzate, semplificando l'uso da parte dell'operatore. Fare clic su<img src="../../../configuration-guide/extended-controls/multi-function.files/multi-function153.png" width="28" /> nella barra degli strumenti, oppure fare doppio clic su un pulsante multifunzione esistente, per aprire la pagina delle proprietà.

![](../../../configuration-guide/extended-controls/multi-function.files/multi-function249.png)

• Generale (General):

**1. Aspetto del pulsante: forma, colore, stile e altre impostazioni.**

**2. Funzioni disponibili**

L'utente può scegliere tra le funzioni elencate.

• Imposta bobina (Set Coil): porta a 1 l'indirizzo indicato.

• Resetta bobina (Reset Coil): porta a 0 l'indirizzo indicato.

• Inverti bobina (Coil Alternation): inverte il valore dell'indirizzo indicato: se è 0 diventa 1, se è 1 diventa 0;

• Bobina impulsiva (Coil Jog): l'indirizzo indicato è a 1 finché si tocca il pulsante e torna a 0 al rilascio;

• Cambio pagina (Screen Jump): passa alla pagina selezionata. Con Modify si sceglie la pagina di destinazione.

<img src="../../../configuration-guide/extended-controls/multi-function.files/multi-function746.png" width="201" />

• Imposta dato (Set data): scrive il valore impostato all'indirizzo indicato. Si scelgono il tipo di dato, l'indirizzo e il valore.

<img src="../../../configuration-guide/extended-controls/multi-function.files/multi-function885.png" width="231" />

• Inserimento utente (User input): l'utente inserisce un valore che viene scritto all'indirizzo indicato. Si scelgono il tipo di dato e l'indirizzo; all'esecuzione del comando compare l'interfaccia di inserimento dati.

<img src="../../../configuration-guide/extended-controls/multi-function.files/multi-function1141.png" width="231" />

Selezionare una funzione disponibile e fare clic su Add per aggiungerla all'elenco delle funzioni selezionate.

Cambio livello utente (User level switching): disconnette l'utente corrente e permette di accedere con un utente di altro livello. Gli altri utenti si specificano nella pagina delle impostazioni.

Chiudi finestra (Close Window): chiude la finestra corrente; utilizzabile solo all'interno di una finestra.

Lettura e salvataggio ricetta (Recipe Read & Save): legge e salva la ricetta corrente nell'HMI.

Cancella allarmi (Clear Alarms): cancella i messaggi di allarme esistenti. Dopo aver selezionato una voce nella visualizzazione storico allarmi, fare clic sul pulsante per cancellarla.

Download ricetta (Recipe Download): scrive nell'HMI i dati della ricetta presenti negli indirizzi RWI e si azzera al termine dell'operazione.

Upload ricetta (Recipe Upload): legge il contenuto della ricetta dall'HMI nell'area dei registri RWI e si azzera al termine dell'operazione.

Quattro operazioni (Four operations): esegue le operazioni aritmetiche di base sui valori; dopo aver selezionato la funzione, fare doppio clic su di essa per impostare tipo di operazione, tipo di dato, tipo di operando, ecc.

Se sono selezionate sia "User Input" sia "Coil Jog", viene eseguita solo User Input e non Coil Jog.

**3. Funzioni aggiunte**

Le funzioni selezionate vengono elencate qui. Fare doppio clic su una funzione o fare clic su "Modify" per impostarla o modificarla; fare clic su "Delete" per eliminarla.

Durante l'esecuzione del progetto, facendo clic sul pulsante multifunzione vengono eseguite tutte le funzioni selezionate.

**4. Macro**

Selezionare "Execute Macro" per visualizzare l'elenco delle macro. Scegliere una macro: durante l'esecuzione del progetto verrà eseguita facendo clic sul pulsante multifunzione.

<img src="../../../configuration-guide/extended-controls/multi-function.files/multi-function1803.png" width="130" />

Impostazioni Label, Advanced e Visibility: vedere il Pulsante di bit.

Per i tasti di scelta rapida della scheda Advanced, vedere "Bit Switch".
