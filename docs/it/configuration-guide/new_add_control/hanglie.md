# Matrice

Questo elemento visualizza i dati impostati dall'utente in una griglia, offrendo un'interfaccia semplice per selezionarli e modificarli. Le funzioni comprendono il cambio pagina automatico, l'inserimento, l'eliminazione, la copia e l'incolla.

Scheda General

![](../../../configuration-guide/new_add_control/hanglie.files/001.png)

Impostazione dei dati

Numero totale di campi (Total Fields): numero di colonne della tabella

Numero iniziale di voci: numero iniziale di righe della tabella

Voci per pagina: numero di righe visualizzate in una pagina

Indirizzo iniziale: indirizzo corrispondente al primo elemento della tabella

Offset indirizzo: offset dell'indirizzo di ogni riga della colonna

Anteprima indirizzi

Mostra la distribuzione degli indirizzi della tabella

Impostazione dei campi

Campo corrente (Current Field): colonna corrente

Tipo di campo (Field type): stato, stringa o numero

Larghezza campo (Field Width): larghezza della colonna

Allineamento (Alignment): allineamento degli elementi della colonna

Numero totale di stati: numero totale di stati degli elementi della colonna

Avanzate

![](../../../configuration-guide/new_add_control/hanglie.files/002.png)

Stato

Voci selezionate (Selected Items): elementi selezionati

Numero effettivo di voci: numero effettivo di elementi

Voci visibili (Total Visible Items): numero totale di elementi visibili

Pagina corrente (Current page): numero della pagina corrente

Pagine totali (Total Pages): numero totale di pagine

Aggiornamento automatico dei dati della pagina corrente: Sì = aggiornamento automatico; altrimenti è comandato dall'indirizzo impostato

Aggiorna dati: indirizzo di aggiornamento

Operazioni

Bit di invisibilità: rende invisibili i dati

Livello di invisibilità: condizione per cui il bit di invisibilità ha effetto

Indirizzo di trigger pagina precedente: passa alla pagina precedente

Indirizzo di trigger pagina successiva: passa alla pagina successiva

Indirizzo di trigger voce precedente: seleziona la voce precedente della colonna

Indirizzo di trigger voce successiva: seleziona la voce successiva della colonna

Indirizzo di trigger copia: copia la voce corrente

Indirizzo di trigger incolla: incolla i dati

Indirizzo di trigger sostituisci: sovrascrive la voce corrente con i dati incollati

Indirizzo di trigger inserisci: inserisce una voce nella posizione corrente

Indirizzo di trigger taglia: taglia i dati

Bit di protezione tocco: protezione contro il tocco

Indirizzo di impostazione della voce selezionata: imposta la voce da selezionare

Trigger di impostazione della voce selezionata: rende effettiva la voce selezionata impostata

Indirizzo di impostazione del numero totale di voci: imposta il numero totale di voci

Trigger di impostazione del numero totale di voci: rende effettivo il numero totale di voci impostato

Avanzate 2

L'area temporanea è un buffer in cui l'elemento può memorizzare temporaneamente dei dati. I dati del buffer possono essere inseriti, aggiunti e scritti nelle voci selezionate, e i dati della voce selezionata possono essere letti nel buffer.

![](../../../configuration-guide/new_add_control/hanglie.files/003.png)

Area temporanea

Indirizzo iniziale: indirizzo iniziale dell'area temporanea

Bit di inserimento della voce selezionata: quando è a ON, i dati del buffer (indirizzo: indirizzo iniziale del buffer + offset della voce) vengono inseriti nella voce selezionata e il numero effettivo di voci aumenta di 1. Se il numero effettivo di voci ha già raggiunto il massimo, l'inserimento non è possibile.

Bit di aggiunta alla voce selezionata: quando è a ON, i dati del buffer (indirizzo: indirizzo iniziale del buffer + offset della voce) vengono aggiunti alla voce selezionata e il numero effettivo di voci aumenta di 1. Se il numero effettivo di voci ha già raggiunto il massimo, l'aggiunta non è possibile.

Aggiungi in fondo: quando è a ON, i dati del buffer (indirizzo: indirizzo iniziale del buffer + offset della voce) vengono aggiunti in fondo e il numero effettivo di voci aumenta di 1. Se il numero effettivo di voci ha già raggiunto il massimo, l'aggiunta non è possibile.

Lettura della voce selezionata: quando è a ON, il contenuto della voce selezionata viene letto nel buffer (indirizzo: indirizzo iniziale del buffer + offset della voce)

Scrittura della voce selezionata: quando è a ON, i dati del buffer (indirizzo: indirizzo iniziale del buffer + offset della voce) vengono scritti nella voce selezionata

Aspetto

![](../../../configuration-guide/new_add_control/hanglie.files/004.png)

Impostazione dei campi

Impostazione del numero della tabella, ecc.

Stile

Linee della griglia, colore di sfondo, colore di sfondo della selezione, ecc.
