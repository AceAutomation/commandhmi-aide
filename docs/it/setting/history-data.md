# Raccolta dati storici

La raccolta dati storici funziona insieme all'oggetto [Visualizzazione dati storici](../configuration-guide/extended-controls/history-record.md) della barra degli strumenti. La prima serve principalmente a impostare i parametri, il secondo a visualizzare i dati storici.

Per creare una raccolta dati storici, fare clic con il tasto destro su "Raccolta dati storici" e selezionare "Nuova raccolta dati storici" nel menu.

Nota: CommandHMI supporta ora più gruppi di dati storici; si possono creare fino a quattro raccolte dati storici.

Non è possibile creare più di quattro gruppi; altrimenti compare il seguente messaggio di errore:

<img src="../../setting/history-data.files/image008.jpg" width="456" />

Fare doppio clic su "Raccolta dati storici 0" nel "Gestore di progetto" per aprire la finestra mostrata nella Figura 7-19:

<img src="../../setting/history-data.files/image009.jpg" width="627" />

Figura 7-19     Finestra Raccolta dati storici

• Nome: imposta il nome mostrato nel gestore di progetto.

• Lunghezza campionamento: numero di dati letti dalla memoria a ogni campionamento.

• Numero totale di campioni: numero di volte in cui i dati vengono acquisiti.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Nota: memoria richiesta = (20 + byte totali dei tipi di dati di tutte le voci) \* numero totale di campioni.

"20" sono i byte occupati da data e ora;

"Byte totali dei tipi di dati di tutte le voci" è la somma dei tipi di dati scelti per ogni voce nella scheda Voci dati.

Per esempio, come mostrato nella Figura 7-20:

a. Se il tipo di dati di ogni voce è "intero positivo a 16 bit", i "byte totali dei tipi di dati di tutte le voci" = 2 + 2 + 2 + 2 + 2 = 10; la memoria richiesta è (20 + 10) \* 2 = 60. Un "dato a 16 bit" occupa 2 byte, un "dato a 32 bit" ne occupa 4.

b\. Se per "LH1" e "LH3" si sceglie il tipo "intero positivo a 32 bit" (in questo caso gli indirizzi delle "Voci dati" risultano LH0, LH1, LH3, LH5, LH6), i "byte totali occupati da tutte le voci" = 2 + 4 + 4 + 2 + 2 = 14; la memoria richiesta è quindi (20 + 14) \* 2 = 68.

Indirizzo di lettura: indirizzo iniziale da cui leggere i dati (per i dettagli vedere Voci dati)

Metodo di campionamento:

• Periodico: legge i dati all'intervallo impostato.

• Su trigger: legge i dati quando l'indirizzo di trigger vale 1.

• Orologio: inizia a leggere i dati a un intervallo di tempo impostato dall'utente.

Gestione a campionamento pieno: comportamento quando il campionamento raggiunge il numero totale massimo.

Arresta campionamento: interrompe il campionamento quando è pieno; se l'opzione non è selezionata, i nuovi dati letti sostituiscono i più vecchi.

Notifica: imposta a 1 un indirizzo quando il numero di campioni raggiunge il massimo.

Fare clic sulla scheda "Voci dati" e impostare le proprietà, come mostrato nella Figura 7-20:

<img src="../../setting/history-data.files/image002.jpg" width="627" />

Figura 7-20 Voci dati della raccolta dati storici

Se è selezionato il multilingua, quando si aggiungono nuove voci occorre impostare il nome per ogni lingua; altrimenti non è possibile aggiungerle.

In CommandHMI gli indirizzi di ogni gruppo di dati storici possono essere non consecutivi, in base all'uso effettivo dei registri LW, per esempio: S1 è LW1, S2 è LW89, S3 è LW8905.

Fare clic su una voce qualsiasi dell'elenco per impostarne le proprietà.

Esempio dettagliato:

Nella scheda Generale impostare l'indirizzo di lettura su LW1, con indirizzi di registro consecutivi e lunghezza di campionamento 5; fare clic sulla scheda Voci dati e aggiungere 5 colonne di dati (LH0-LH4). Selezionarle una per una per impostarne le proprietà: nome, indirizzo, tipo di dati, numero di cifre totali e decimali, scalatura.

Si supponga che nomi, tipo di dati e scalatura di LH0-LH4 siano impostati come nella Figura 7-20 e che le altre proprietà abbiano i valori predefiniti:

LH0 - intero positivo a 16 bit, scalatura con guadagno 3 e offset 2

LH1 - intero positivo a 32 bit, scalatura con guadagno 2 e offset 1

LH2 - intero a 16 bit, scalatura non selezionata

LH3 - intero a 32 bit, scalatura non selezionata

LH4 - virgola mobile, scalatura con guadagno 4 e offset 5

Con queste impostazioni, poiché la lunghezza di campionamento è 5 (scheda Generale), vengono letti 5 valori consecutivi a partire dall'"Indirizzo di lettura". Gli indirizzi vengono letti in base al tipo di dati di ogni voce.

Con dati a 16 bit gli indirizzi letti sono consecutivi; con dati a 32 bit sono distanziati. Se è selezionata la scalatura, il valore finale è uguale al valore letto moltiplicato per il guadagno più l'offset.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Nota: il guadagno della scalatura deve essere maggiore di 1!

Impostati tipo di dati e scalatura di ogni voce, gli indirizzi letti sono i seguenti:

LH0-LW1 (dato a 16 bit, indirizzo di lettura + 1) Valore finale di LH0 = valore di LW1 × 3 + 2

LH1-LW2 (dato a 32 bit, indirizzo di lettura + 2) Valore finale di LH1 = valore di LW2 × 2 + 1

LH2-LW4 (dato a 16 bit, indirizzo di lettura + 1) Valore finale di LH2 = valore di LW4

LH3-LW5 (dato a 32 bit, indirizzo di lettura + 2) Valore finale di LH3 = valore di LW5

LH4-LW7 (dato a 32 bit, indirizzo di lettura + 2) Valore finale di LH4 = valore di LW7 × 4 + 5

Al termine fare clic su "OK". Fare clic sull'icona "Visualizzazione dati storici" nella barra degli strumenti, impostare il numero di righe a 5 nella finestra che compare e lasciare i valori predefiniti per le altre proprietà.

Fare clic su "OK": sullo schermo viene generata automaticamente una tabella, come mostrato nella Figura 7-21:

Figura 7-21 Tabella della visualizzazione dati storici

Uso della tabella:

• Data: data in cui è stato letto il valore dell'indirizzo

• Ora: ora in cui è stato letto il valore dell'indirizzo

• "LH0": mostra il valore di LW1 in un dato momento.

• "LH1": mostra il valore di LW2 in un dato momento.

• "LH2": mostra il valore di LW4 in un dato momento.

• "LH3": mostra il valore dell'indirizzo LW5 in un dato momento.

• "LH4": mostra il valore dell'indirizzo LW7 in un dato momento.

Per esempio: indirizzo di lettura LW1, lunghezza di campionamento 3, numero totale di campioni 10, metodo di campionamento su trigger, intervallo 1 secondo, tipo di dati predefinito per ogni dato;

1). L'opzione Arresta campionamento non è selezionata:

I valori di LW1, LW2 e LW3 vengono letti ogni secondo. Poiché il numero totale di campioni è 10, al decimo secondo sono stati letti 10 gruppi di dati. Non essendo selezionata l'opzione "Arresta campionamento", il processo continua. Per memorizzare i dati viene allocata un'area di memoria fissa, che dipende da lunghezza di campionamento, numero totale di campioni e tipo di dati; quando il numero di gruppi raggiunge il "numero totale di campioni", i nuovi dati sostituiscono i primi.

2). L'opzione Arresta campionamento è selezionata:

L'unica differenza è che il campionamento si interrompe al raggiungimento del numero totale di campioni.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Usare "[Tendenze storiche](../configuration-guide/extended-controls/histrendgraphics.md)" o "[Visualizzazione dati storici](../configuration-guide/extended-controls/history-record.md)" per leggere i valori in modo più intuitivo.
