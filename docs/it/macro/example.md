# Un semplice blocco macro

Creare un nuovo progetto e selezionare il modello di HMI appropriato. Il modulo di script realizzerà le seguenti semplici funzioni aritmetiche: inizializzare gli oggetti "Visualizzazione numerica" con i valori degli elementi dell'array char source \[4\] = {2, 3, 4, 5} tramite lo script Init; leggere i dati inseriti dall'esterno tramite gli oggetti di visualizzazione numerica; premendo il pulsante "=" viene quindi eseguito lo script ADDSUM, il cui risultato viene mostrato tramite questo oggetto.

I passaggi dettagliati sono i seguenti:

**Passo 1: <Creare un nuovo script>**

Fare clic sul pulsante di scelta rapida "Script editor" sul lato sinistro della barra degli strumenti: si apre una finestra di dialogo.

**Passo 2: <Creare la macro Init>**

Fare clic sul pulsante <img src="../../macro/example.files/example866.png" width="25" /> nell'interfaccia dell'editor di script: nell'elenco "Non salvati" compare un nuovo script, come mostrato nella Figura 5-7. Modificare il nome dello script nel campo Script e scrivere il codice sorgente nella finestra di modifica, come mostrato nella Figura 5-8

<img src="../../macro/example.files/example1100.png" width="886" />

Figura 5-7      Nuovo script

<img src="../../macro/example.files/example1126.png" width="1087" />

Figura 5-8 Modifica dello script Init

<img src="../../macro/example.files/example1156.png" width="130" />

I nomi delle macro possono contenere solo cifre arabe (0-9), lettere dell'alfabeto inglese (a-z, A-Z) e il carattere di sottolineatura (_). Inserire il contenuto mostrato in Figura 5-9:

**Passo 3: <Impostazione delle variabili>**

Registrare le impostazioni degli attributi, come nome e tipo delle variabili, nella finestra mostrata in Figura 5-9. Fare doppio clic nella finestra "Variable Setting", oppure fare clic con il tasto destro per aprire il menu contestuale e selezionare "New Variable": si apre la finestra di dialogo mostrata in Figura 5-10, in cui impostare i valori delle variabili esterne.

<img src="../../macro/example.files/example1677.png" width="499" />

Figura 5-9 Codice dello script

Nome: inserire rispettivamente LW0, LW1, LW2, LW3 come nome della variabile;

Tipo di dato: impostare intero a 16 bit;

Lettura/scrittura: selezionare lettura e scrittura;

Gli indirizzi sono: LW0 = 0, LW1 = 1, LW2 = 2, LW3 = 3;

Al termine delle impostazioni, il risultato è quello mostrato in Figura 5-10.

<img src="../../macro/example.files/example1981.png" width="843" />

Figura 5-10     Impostazione delle variabili

**Passo 4: <Compilare il file sorgente>**

Completati i passaggi precedenti, si passa alla compilazione: fare clic sul pulsante di compilazione mostrato in Figura 5-11; il software salva, compila, collega e controlla automaticamente eventuali altri errori.

<img src="../../macro/example.files/example2223.png" width="800" />

Figura 5-11    Output delle informazioni

Quando la finestra dei messaggi visualizza "0 errors! Compile successfully", la macro è stata creata correttamente e viene aggiunta automaticamente all'elenco delle macro compilate; in caso contrario viene visualizzato un messaggio di errore e la macro viene aggiunta automaticamente all'elenco delle compilazioni non riuscite. L'utente può modificare la macro fino a ottenere una compilazione corretta.

**Passo 5: <Creare lo script ADDSUM>**

Ripetere i passi 2 - 4 per creare lo script ADDSUM, come mostrato in Figura 5-13

<1>: Inserire "ADDSUM" come nome dello script.

<2>: Inserire il contenuto cerchiato nella finestra di modifica del codice.

<3>: Impostare i valori degli attributi delle variabili nella finestra di impostazione delle variabili.

<4>: Fare clic sul pulsante Compile.

<img src="../../macro/example.files/example2991.png" width="1168" />

Figura 5-13    Creazione dello script ADDSUM

**Passo 6: <Modificare gli oggetti>**

<1>. Posizionare gli oggetti nella pagina del progetto e regolarne le dimensioni, come mostrato in Figura 5-14.

<img src="../../macro/example.files/example3164.png" width="558" />

Figura 5-14    Disposizione degli oggetti

<2>. Impostare i parametri degli attributi degli oggetti

Fare clic con il tasto destro sull'oggetto "Numeric Input" e impostare l'indirizzo e gli attributi di ciascun oggetto, come mostrato in Figura 5-15.

<img src="../../macro/example.files/example3375.png" width="660" />

Figura 5-15    Proprietà dell'oggetto di immissione numerica

È fondamentale che gli indirizzi delle variabili LW0, LW1, LW2, LW3 e SumLW corrispondano all'"indirizzo di scrittura" (mostrato in Figura 5-15) di ciascun oggetto. Fare clic su "OK" per salvare le impostazioni.

<3>. Impostare le proprietà dell'oggetto Bit Button

<img src="../../macro/example.files/example3658.png" width="661" />

Figura 5-16 (Impostazione delle proprietà di Bit Button)

<4>. Impostazione delle proprietà del Timer

Selezionare lo script Init e fare clic su "OK" per salvare le impostazioni.

<img src="../../macro/example.files/example3792.png" width="661" />

Figura 5-17    Proprietà del timer

<5>. Selezionare la pagina "Label" -> "Text" del Function Button e inserire il carattere "+" nella casella di testo, come mostrato in Figura 5-18.

<img src="../../macro/example.files/example3963.png" width="662" />

Figura 5-18    Proprietà del pulsante funzione

**Passo 7: Compilare e scaricare nell'HMI**

<1>: Fare clic sull'icona di compilazione per eseguire l'operazione.

<img src="../../macro/example.files/example4101.png" width="64" />

Figura 5-19    Compilazione generale del progetto

<2>: Selezionare "Download (D) -> USB download (D)", quindi fare clic su "Download" nella finestra di dialogo che si apre. Riavviare l'HMI.

È anche possibile fare clic sul pulsante di scelta rapida Compile Download.

**Passo 8: <Verifica del risultato>**

Dopo il riavvio dell'HMI compare la pagina seguente (Figura 5-20).

Questo perché all'avvio la prima istruzione eseguita dal timer è Init.

<img src="../../macro/example.files/example4642.png" width="484" />

Figura 5-20    Visualizzazione del valore iniziale

Inserire per esempio i dati "31,42,53,64" negli oggetti "Visualizzazione numerica", quindi fare clic sul pulsante "=" per eseguire lo script ADDSUM: il risultato visualizzato sarà 190, come mostrato in Figura 5-21:

<img src="../../macro/example.files/example5009.png" width="481" />

Figura 5-21     Visualizzazione del risultato

A questo punto la modifica, la compilazione, il download e il test dello script sono stati completati con successo, con tutte le funzioni necessarie.
