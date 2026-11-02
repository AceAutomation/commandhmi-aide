# Ricette

Nel settore manifatturiero, la ricetta descrive le proporzioni dei materiali usati per realizzare un prodotto ed è un insieme di valori di parametri usati durante la produzione. Per esempio, per fare il pane serve una ricetta di base che elenca i pesi o le proporzioni di tutti gli ingredienti: acqua, farina, zucchero, uova, olio e così via. Può anche elencare ingredienti facoltativi come frutta, frutta secca, cioccolato, che si possono aggiungere alla ricetta di base per ottenere pane di gusti diversi. Un altro esempio è un'acciaieria, dove una ricetta può essere un insieme di parametri macchina. Per le macchine a lotti, una ricetta può descrivere le diverse fasi della lavorazione.

Una macchina può produrre sia pane sia torte, con pane di gusti diversi e torte di varie forme. Qui chiamiamo ricetta le proporzioni degli ingredienti del pane, e file le diverse proporzioni per i vari gusti di pane. I record di ricetta sono quindi contenuti nei file di ricetta.

CommandHMI offre la funzione di configurazione delle ricette, accessibile dalla voce Ricette della barra dei menu o dal gestore di progetto: si apre la finestra di configurazione delle ricette, dove si può aggiungere un nuovo gruppo di ricette. Come mostrato nella Figura 7-32:

<img src="../../setting/formula.files/formula1334.png" width="515" />

Figura 7-32 Finestra delle proprietà delle ricette continue

• Nome: nome del file di ricetta corrente.

• Descrizione: descrizione del file di ricetta corrente;

• Lunghezza ricetta: imposta la lunghezza e il numero degli indirizzi di record letti dalla ricetta corrente. Gli indirizzi della tabella di record sono disposti automaticamente in sequenza dal sistema e non sono modificabili. La lunghezza massima della ricetta è 4096.

• Numero totale: numero di ricette, fino a 512;

• Gruppo di ricette modificabile nell'HMI: consente di modificare la ricetta nell'HMI.

<img src="../../setting/formula.files/formula1872.png" width="794" />

Figura 7-33 Finestra delle proprietà delle ricette discrete

• Nome gruppo: nome del file di ricetta corrente.

• Descrizione ricetta: descrizione del file di ricetta corrente;

• Flag di scrittura ricetta completata: dopo la scrittura della ricetta corrente nel PLC, l'indirizzo bit impostato viene messo a 1;

• Gruppo di ricette modificabile nell'HMI: consente di modificare la ricetta nell'HMI.

<img src="../../setting/formula.files/formula2225.png" width="130" />

Nota: lunghezza ricetta \* byte occupati dal tipo di dati \* numero totale &lt;= 512KB

• Tipo di dati: tipo di dati del registro;

• Scrivi ricetta nel PLC: imposta l'indirizzo del registro dati del PLC associato alla ricetta;

• Leggi ricetta dal PLC: imposta l'indirizzo del registro dati del PLC associato alla ricetta;

• Memoria ricette: intervallo di indirizzi di memoria della ricetta nell'HMI, generato automaticamente e non modificabile;

• Ricetta corrente: l'indirizzo di memoria della ricetta nell'HMI e il registro dati del PLC sono generati automaticamente in ordine e non sono modificabili;

• Registro numero ricetta: le ricette sono ordinate automaticamente per numero progressivo, non modificabile; corrisponde all'ordine dei nomi di ricetta nella voce dati.

La voce dati delle ricette continue è mostrata nella Figura 7-33:

<img src="../../setting/formula.files/formula2990.png" width="514" />

Figura 7-34 Scheda Dati delle ricette continue

• Nome: nome della ricetta corrente;

• Dati: scrive e mostra il valore di ogni indirizzo della ricetta corrente;

• Copia dati ricetta: copia i dati dalla ricetta sorgente alla ricetta di destinazione. Fare clic su OK per salvare o su Annulla per uscire dalla finestra. Una volta completata la configurazione delle ricette, si può progettare l'interfaccia per gestirle nell'HMI.

Esempio di applicazione delle ricette:

1\. Creare una configurazione di ricette come descritto sopra. Il risultato è mostrato nella Figura 7-34:

<img src="../../setting/formula.files/formula3531.png" width="515" />

Figura 7-35  Funzione di copia dei dati delle ricette continue

Questa configurazione comprende in totale 4 ricette, ciascuna con 16 voci. Gli indirizzi di memorizzazione vanno da RWI: 1 a RWI: 16 nella memoria dell'HMI.

2. Dopo la configurazione, la ricetta può essere mostrata sullo schermo, modificata o scaricata direttamente nel PLC. A tale scopo si usano i seguenti oggetti funzionali essenziali.

• Visualizzazione ricetta: fare clic su visualizzazione/immissione numerica <img src="../../setting/formula.files/formula3946.png" width="23" /> (vedere "Visualizzazione/immissione numerica")

Selezionare l'indirizzo di memoria interna RWI: 0 per creare sullo schermo un oggetto di visualizzazione e immissione numerica. Il valore immesso e visualizzato è il numero della ricetta: il valore 0 di RWI0 indica la ricetta numero 1, il valore 1 la ricetta numero 2, ecc.

• Fare clic sul pulsante funzione <img src="../../setting/formula.files/formula4264.png" width="21" />: per l'uso vedere "Pulsante funzione".

Con il pulsante funzione, impostando la funzione appropriata, si possono creare pulsanti per scrivere la ricetta nel PLC, leggerla dal PLC, salvarla, selezionare la ricetta precedente o quella successiva.

Gestione di più gruppi di ricette: CommandHMI offre la funzione multi-gruppo, che però supporta solo dieci gruppi; oltre questo limite compare un messaggio, come mostrato in 7-34-2

<img src="../../setting/formula.files/formula4682.png" width="248" />

Figura 7-35-1

<img src="../../setting/formula.files/formula4698.png" width="321" />

Figura 7-35-2

LW61141 serve a inserire il gruppo di ricette, mentre RWI0 serve ancora a inserire il numero di ricetta. Per selezionare una ricetta occorre quindi impostare sia LW61141 sia RWI0. Per esempio: inserendo 0 in LW61141 e 2 in RWI0 si selezionano i dati della ricetta 2 del gruppo 0.

3. Seguendo la procedura sopra, si può creare una pagina come quella della Figura 7-35:

Si supponga che l'indirizzo di monitoraggio da scrivere sia D0, la lunghezza della ricetta 16 e il numero totale 4.

<img src="../../setting/formula.files/formula5250.png" width="746" />

Figura 7-36 Risultato della ricetta

Con i pulsanti funzione e gli oggetti di visualizzazione/immissione numerica è facile modificare, salvare, leggere e scrivere le ricette. Occorre però prestare attenzione ai punti seguenti:

• Prima di usare le funzioni ricetta occorre creare l'elenco delle ricette.

• Quando si scrivono i parametri nell'elenco ricette, fare attenzione al tipo di dati: un dato a 16 bit occupa una word, un dato a 32 bit ne occupa due. Scegliere un tipo di dati coerente. Prestare particolare attenzione agli indirizzi a 32 bit: poiché occupano due word, evitare sovrapposizioni tra indirizzo di scrittura e indirizzo di monitoraggio.

• L'indirizzo RWI0 ha un uso fisso e serve solo a cambiare il numero di ricetta. Se RWI0 vale 0, indica la prima ricetta, e così via.

• Gli indirizzi dei parametri di ricetta sono consecutivi.

La voce dati delle ricette discrete è mostrata nella Figura 7-33:

<img src="../../setting/formula.files/formula6181.png" width="795" />

Figura 7-41  Scheda Dati delle ricette discrete

• Numero totale di ricette: numero di ricette, fino a 128;

• Lingua: l'utente può impostare nomi di elementi e ricette in lingue diverse.

• Nome ricetta: modifica il nome della ricetta corrente, ad esempio "recipe1", "recipe2".

• Nuovo (New): apre la finestra "Elemento ricetta" per creare un elemento, come mostrato nella figura seguente.

  <img src="../../setting/formula.files/formula6495.png" width="517" />

Figura 7-42  Finestra Nuovo elemento di ricetta discreta

• Elimina (Delete): elimina l'elemento di ricetta corrente.

• Elimina tutto (Delete All): elimina tutti gli elementi di questa ricetta.

• Modifica (Alter): apre la finestra Elemento ricetta dell'elemento corrente per modificarne le informazioni.

• Esporta (Export): apre la finestra Salva con nome; salva la ricetta come file \*.csv nel percorso e con il nome indicati.

• Importa (Import): apre la finestra Apri; scegliere un file \*.csv da usare come ricetta corrente.
