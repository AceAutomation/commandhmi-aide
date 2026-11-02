# Tema

Ø  Aggiungere un topic di pubblicazione

• Scheda Generale

![](../../setting/mqtttheme.files/addpublish.png)

- Nome

Imposta il nome di progetto del topic MQTT

- Topic

Topic ricevuto dal server MQTT all'invio di un messaggio

- Formato

\[JSON (generale)\]: dati in formato JSON con struttura a elenco.

\[JSON (avanzato)\]: formato JSON con struttura ad albero liberamente personalizzabile.

- Modalità di invio

**■  automatica**

Su variazione: quando il contenuto dell'indirizzo monitorato cambia, viene trasmesso automaticamente.

Ciclica: il contenuto dell'indirizzo monitorato viene trasmesso periodicamente.

**■  su trigger bit**

Il contenuto viene trasmesso quando si attiva l'indirizzo bit specificato.

• Indirizzo (JSON generale)

Configurabile quando nella scheda \[Generale\] si sceglie il formato \[JSON generale\].
<img src="../../setting/mqtttheme.files/addgeneraladdr.png" width="606" />

Aggiunge un valore. Può essere di tipo bit o word, con valore fisso o letto da un indirizzo specificato.

• Indirizzo (JSON avanzato)

Configurabile quando nella scheda \[Generale\] si sceglie il formato \[JSON avanzato\].
<img src="../../setting/mqtttheme.files/addextendaddr.png" width="606" />

L'impostazione degli indirizzi supporta una struttura ad albero, con componenti, array ecc.; anche il timestamp e i nomi dei dati sono personalizzabili.

- elemento

Aggiunge un elemento di dati. Un componente può contenere più formati di dati, ciascuno con nome e valore propri.

I dati dell'elemento sono racchiusi tra parentesi graffe { }.

- Array

Aggiunge un array di dati. Un array può contenere più formati di dati, ma ha un solo nome.

I dati dell'array sono racchiusi tra parentesi quadre \[ \].

- valore

Aggiunge un valore, una stringa o un timestamp. Valori e stringhe possono essere fissi o letti da un indirizzo specificato.

- modello

Converte il testo JSON personalizzato dall'utente in dati ad albero

- Anteprima

Converte i dati ad albero correnti in testo JSON

• Scheda Sicurezza

Se abilitato, ha effetto quando l'indirizzo bit impostato soddisfa la condizione di trigger.
<img src="../../setting/mqtttheme.files/publishsecurity.png" width="606" />

Ø  Aggiungere un topic di sottoscrizione

• Scheda Generale

<img src="../../setting/mqtttheme.files/addsubscribe.png" width="606" />

- Nome

Imposta il nome di progetto del topic MQTT

- Topic

Topic sottoscritto dal server MQTT

- Il formato è

[come per【Pubblicazione】](#anchor-name)

- Modalità operativa

■  automatica

automaticamente.

■  Manuale

Eseguita impostando manualmente l'indirizzo specificato.

• Scheda Indirizzo

[Come per【Pubblicazione】](#anchor-name)

• Scheda Sicurezza

[Come per【Pubblicazione】](#anchor-name)
