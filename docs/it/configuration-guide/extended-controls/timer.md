# Timer

Il timer è un oggetto attivato in base al tempo. Nel software di configurazione CommandHMI il timer serve ad attivare le macro. Fare clic su <img src="../../../configuration-guide/extended-controls/timer.files/timer152.png" width="35" /> nella barra degli strumenti, oppure fare doppio clic su un timer esistente, per aprirne la pagina delle impostazioni:

<img src="../../../configuration-guide/extended-controls/timer.files/timer240.png" width="662" />

**Controllo**

• Modalità di esecuzione (Execution mode): Always Execute (esecuzione continua) oppure Address Triggered (attivazione tramite indirizzo).

1\. "Always Execute": la macro viene eseguita sempre, alla frequenza impostata dall'utente.

2\. "Address Triggered": la macro viene eseguita alla frequenza impostata quando il bit indicato vale 1 e non viene eseguita quando vale 0.

• Indirizzo (Address): con la modalità "Address Triggered" compare il campo in cui inserire l'indirizzo bit che comanda l'esecuzione della macro; quando il suo valore è 1, la macro viene eseguita.

• Frequenza (Frequency): intervallo di esecuzione della macro, da 0,1 a 60 s.

• Numero di esecuzioni (Execution Times): numero di volte in cui la macro viene eseguita. Con valore 0 la macro viene eseguita indefinitamente.

**Funzione**

• Tipo di funzione (Function type): tipo di funzione da eseguire; nel software di configurazione CommandHMI la funzione del timer è la macro.

• Nome (Name): nome della macro da eseguire. Se non esistono macro, il timer non può essere configurato.

<img src="../../../configuration-guide/extended-controls/timer.files/timer1240.png" width="130" />

Le dimensioni del timer non sono modificabili, la posizione sì. Durante l'esecuzione del progetto il timer non è visibile sull'HMI.
