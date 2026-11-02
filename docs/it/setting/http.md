# HTTP

<img src="../../setting/lisanbaojing.files/image007.jpg" width="133" alt="lisanbaojing2414" /> Solo lo schermo remoto supporta questa funzione

![](../../setting/http.files/open.png)

Con questa funzione l'utente può configurare facilmente i parametri del server HTTP

Ø  Scheda Generale

<img src="../../setting/http.files/general.png" width="606" />

- Nome

Nome della connessione

- URL

URL di destinazione della richiesta HTTP

- Metodo

Metodo della richiesta HTTP: GET o POST

- Codifica

Formato di codifica

- Intestazione della richiesta

Intestazione della richiesta HTTP

- Timeout

Tempo di risposta HTTP

- Formati

comprende: JSON (generale) o JSON (avanzato), [come per 【MQTT】](mqtttheme.md#anchor-name)

- Modalità di trasmissione

comprende: automatica e su trigger bit

Ø  Scheda Indirizzo (JSON generale)

Configurabile quando nella scheda \[Generale\] si sceglie il formato \[JSON generale\].

Aggiunge un valore. Può essere di tipo bit o word, con valore fisso o letto da un indirizzo specificato. [Vedere 【MQTT】](mqtttheme.md#anchor-name1)

Ø  Scheda Invio JSON (JSON avanzato)

Configurabile quando nella scheda \[Generale\] si sceglie il formato \[JSON avanzato\].
<img src="../../setting/http.files/sendjson.png" width="606" />

Imposta i dati da inviare; l'impostazione degli indirizzi supporta una struttura ad albero, con componenti, array e altre forme; anche il timestamp e i nomi dei dati sono personalizzabili. [Vedere 【MQTT】](mqtttheme.md#anchor-name1)

Ø  Scheda Ricezione JSON

<img src="../../setting/http.files/receivejson.png" width="606" />

Imposta i dati da ricevere; l'impostazione degli indirizzi supporta una struttura ad albero, con componenti, array e altre forme; anche il timestamp e i nomi dei dati sono personalizzabili. Vedere [【Invio JSON】](#anchor-name)

Ø  Scheda Sicurezza

Vedere la scheda \[Sicurezza\] in [\[MQTT\].](mqtttheme.md#anchor-name2)
