# Protezione HMI

La protezione HMI serve a stabilire un periodo di tempo durante il quale l'HMI funziona normalmente. Superato il periodo impostato, l'HMI passa a una pagina specifica dove è necessaria una password per continuare a usarlo.

Fare doppio clic sulla voce "Protezione HMI" (HMI protection) nel "Gestore di progetto" per aprire la finestra mostrata nella Figura 7-14:

<img src="../../setting/hmi-protect.files/hmi-protect343.png" width="622" />

Figura 7-14    Finestra Protezione HMI

Esempio di applicazione di questa funzione:

➢Selezionare "Password di sblocco": la volta successiva sarà richiesta una password per accedere alla protezione HMI.

➢Selezionare "Sblocca tutti i livelli": se si inserisce questa password per sbloccare la protezione HMI, vengono sbloccati tutti i livelli di protezione.

➢Selezionare "Protezione HMI": si passa automaticamente alla scheda "Impostazioni protezione", come mostrato di seguito:

<img src="../../setting/hmi-protect.files/hmi-protect743.png" width="623" />

Figura 7-15    Impostazioni protezione HMI

Impostare il "Numero totale di livelli di password" a 3; selezionare il pulsante 1, scegliere 2009-04-01 e 12-00-00 nella colonna Limite di tempo in "Impostazione parametri"; scegliere la pagina 1 come "Pagina di avviso"; impostare la "Password di sblocco" a 1111. La protezione di livello 1 è così impostata.

Allo stesso modo, impostare limiti di tempo e password per i livelli 2 e 3.

• Sblocca tutti i livelli

Abilitando questa funzione e impostando la password, questa password permette di rimuovere tutti i livelli della protezione HMI

•  Password di accesso alle impostazioni di protezione

Abilitando questa funzione e impostando la password, la volta successiva sarà necessario inserirla per aprire la protezione HMI e visualizzarne le informazioni

•  Abilita protezione con password

Abilitando questa funzione si attiva la protezione HMI. I dettagli si impostano nelle impostazioni di protezione.

• Impostazioni di protezione

Numero totale di livelli di password: fino a 15 livelli di protezione HMI per periodi diversi, secondo necessità

Livello di password corrente: i parametri seguenti si riferiscono al livello di password corrente

Impostazione parametri:

Periodo di utilizzo: data di scadenza della protezione HMI

Pagina di avviso scadenza: pagina mostrata alla scadenza della protezione HMI

Password di sblocco: password che rimuove la protezione HMI alla scadenza

Impostazioni avanzate:

Visualizza giorni rimanenti: mostra i giorni che mancano alla scadenza impostata della protezione HMI

Anticipo:

Imposta con quanti giorni di anticipo rispetto alla scadenza della protezione HMI deve comparire l'avviso

Proroga:

Dopo la scadenza della protezione HMI, per il numero di giorni impostato, la pagina specificata viene mostrata a intervalli regolari

Priorità tra anticipo e proroga

Anticipo selezionato, proroga selezionata: vale l'anticipo

Anticipo non selezionato, proroga selezionata: vale la proroga

Anticipo selezionato, proroga selezionata, pulsante funzione "sblocco proroga protezione HMI" non usato: vale l'anticipo

Anticipo selezionato, proroga selezionata, pulsante funzione "sblocco proroga protezione HMI" usato: vale la proroga

•  Esempio d'uso della funzione:

Si supponga di impostare in questa finestra un numero totale di livelli di password pari a 3. Selezionare quindi 0 in "Livello di password corrente". In "Impostazione parametri", scegliere la data nella colonna "Periodo di utilizzo", per esempio 2009/04/01. Nella colonna successiva inserire l'ora, per esempio 12:00:00. In "Pagina di avviso scadenza" scegliere la pagina da mostrare alla scadenza, per esempio la pagina 1. In "Password di sblocco" inserire la password per rimuovere la protezione, per esempio 1111. La protezione HMI di livello 1 è impostata.

Poi selezionare 1 in "Livello di password corrente" e, in "Impostazione parametri", scegliere la data nella colonna "Periodo di utilizzo", per esempio 2009-04-05. Nella colonna successiva inserire l'ora, per esempio 12-00-00. In "Pagina di avviso scadenza" scegliere la pagina da mostrare alla scadenza, per esempio la pagina 2. In "Password di sblocco" inserire la password, per esempio 2222. La protezione HMI di livello 2 è impostata.

Poi selezionare 2 in "Livello di password corrente" e, in "Impostazione parametri", scegliere la data nella colonna "Periodo di utilizzo", per esempio 2009-04-10. Nella colonna successiva inserire l'ora, per esempio 12-00-00. In "Pagina di avviso scadenza" scegliere la pagina di avviso, per esempio la pagina 3. In "Password di sblocco" inserire la password, per esempio 3333. La protezione HMI di livello 3 è impostata.

Dopo aver impostato i 3 livelli di protezione HMI, fare clic su "OK".

Si supponga che oggi sia il 2009-04-01 alle 08-00-00. Il periodo di utilizzo della protezione di livello 1 scade alle 12-00-00 del 2009-04-01: poiché la scadenza non è ancora arrivata, l'HMI si può usare normalmente. Dopo 4 ore, alle 12-00-00 del 2009-04-01, l'HMI passa automaticamente alla pagina impostata per questo periodo. Per continuare a usare l'HMI e operare sulle altre pagine, l'utente può aggiungere in questa pagina (pagina 1) un pulsante funzione con la funzione "Sblocca HMI". Alla scadenza del livello 1, fare clic sul pulsante e inserire nella finestra la password di sblocco del livello 1: inserendo 1111 la protezione viene rimossa.

Sbloccata la password di livello 1, l'HMI si può usare normalmente. Dopo un certo tempo, alle 12-00-00 del 2009-04-05, scade la protezione di livello 2 e l'HMI passa automaticamente alla pagina di protezione impostata (pagina 2). Allo stesso modo, l'utente deve usare il pulsante funzione con la funzione "Sblocca HMI" e inserire la password di livello 2 (2222) per poter usare normalmente l'HMI.

Poiché è stata impostata anche la protezione di livello 3, alle 12-00-00 del 2009-04-10 l'utente dovrà allo stesso modo usare il pulsante funzione con la funzione "Sblocca HMI" e inserire la password di sblocco di livello 3 (3333) per poter usare normalmente l'HMI.

Una volta sbloccati tutti e 3 i livelli, la protezione HMI non è più attiva e l'HMI si può usare normalmente.

Gli esempi precedenti illustrano l'uso della funzione di protezione HMI. Per impostare un numero diverso di livelli di password la procedura è analoga; fare riferimento all'esempio sopra.
