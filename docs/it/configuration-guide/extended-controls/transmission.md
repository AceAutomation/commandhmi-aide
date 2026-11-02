# Trasmissione dati

Serve a trasferire dati tra PLC e HMI o tra PLC e PLC. Fare clic su "Data Transmission" in Gestione progetto per visualizzare l'elenco dei trasferimenti dati.

<img src="../../../configuration-guide/extended-controls/transmission.files/image005.jpg" width="564" />

Figura 7-36

L'elenco riporta i dettagli di tutti i trasferimenti configurati, che l'utente può creare, eliminare e modificare. Il software di configurazione CommandHMI supporta fino a 512 trasferimenti dati.

Per creare un nuovo trasferimento o modificarne uno esistente, aprire la pagina delle proprietà:

<img src="../../../configuration-guide/extended-controls/transmission.files/image006.jpg" width="339" />

Figura 7-37

**1. Attributi**

Temporizzato / A trigger (Timing / Trigger): modalità di attivazione del trasferimento.

Temporizzato (Timing): il trasferimento avviene all'intervallo impostato.

A trigger (Triggering): il trasferimento è comandato da un indirizzo specificato e avviene quando il suo valore è 1.

Reset automatico (Automatic reset): quando l'indirizzo di trigger vale 1, viene riportato automaticamente a 0.

Tipo di indirizzo (Address Type): tipo di indirizzo dei dati trasferiti: Bit / Word / Double Word.

Word / Bit: lunghezza dei dati da trasferire, da 1 a 64.

**2. Indirizzi**

Indirizzo sorgente (Source Address): indirizzo di origine dei dati trasferiti, <span id="OLE_LINK497"></span><span id="OLE_LINK498"></span>che deve essere dello stesso tipo impostato in "Property".

Indirizzo di destinazione (Destination Address): indirizzo di destinazione dei dati trasferiti, che deve essere dello stesso tipo impostato in "Property".

<img src="../../../configuration-guide/extended-controls/transmission.files/image004.jpg" width="130" />

Indirizzo sorgente e indirizzo di destinazione non possono trovarsi sullo stesso PLC.
