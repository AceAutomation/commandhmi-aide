# Orologio

L'impostazione dell'orologio comprende tre funzioni: download dell'ora di sistema nell'HMI, scrittura dell'ora nel PLC e sincronizzazione con il PLC.

Fare doppio clic su "Orologio" (Clock) nel gestore di progetto per aprire la finestra delle proprietà dell'orologio.

<img src="../../setting/clock.files/image004.jpg" width="388" />

<img src="../../setting/clock.files/image005.jpg" width="388" />

Figura 7-11 Finestra Impostazione orologio

Scarica l'orologio di sistema nell'HMI: indica se scaricare le informazioni dell'orologio di sistema nell'HMI.

• Scrivi ora/data nel PLC:

• Tipo di dati e Lunghezza sono valori predefiniti.

• Ora: anno-mese-giorno-ora-minuto-secondo-giorno della settimana. Per i dettagli vedere LW 60000~LW 60006 negli indirizzi dei registri. Il giorno della settimana dell'ora di sistema non è modificabile.

Indirizzo di scrittura: l'ora di sistema verrà scritta in questo indirizzo del PLC.

• Modalità di avvio:

Periodica: scrive periodicamente l'ora di sistema nell'indirizzo PLC specificato, all'intervallo specificato.

Su trigger: l'ora di sistema viene scritta nell'indirizzo PLC specificato quando l'indirizzo di trigger vale 1.

Reset automatico: riporta automaticamente a 0 l'indirizzo di trigger quando vale 1.

**Sincronizzazione con l'ora del PLC:**

Tipo di dati e Lunghezza sono valori predefiniti.

 Ora: anno-mese-giorno-ora-minuto-secondo-giorno della settimana. Per i dettagli vedere LW 60000~LW 60006 negli indirizzi dei registri. Il giorno della settimana dell'ora di sistema non è modificabile.

• Indirizzo di lettura: vengono lette le informazioni contenute nell'indirizzo del PLC.

• Modalità di avvio:

Periodica: scrive periodicamente l'ora di sistema nell'indirizzo PLC specificato, all'intervallo specificato.

Trigger: l'ora di sistema viene sincronizzata con il PLC quando l'indirizzo di trigger vale 1.

Reset automatico: riporta automaticamente a 0 l'indirizzo di trigger quando vale 1.
