# Server

• **Scheda Generale**

<img src="../../setting/mqtt.files/server-general.png" width="706" />

- IP (nome di dominio)

IP del server MQTT

- Porta

Numero di porta del server MQTT

- ID client

ID del client; si possono usare alcuni caratteri speciali

- Nome utente

Imposta il nome utente (richiede l'autenticazione abilitata)

- Password

Imposta la password utente (richiede l'autenticazione abilitata)

- Durata del test di connessione

Se il server MQTT supera questo valore senza ricevere il messaggio di test dall'HMI, considera l'HMI disconnesso.

• **Scheda Indirizzo**

<img src="../../setting/mqtt.files/server-addr.png" width="706" />

- Indirizzo di stato

Imposta un gruppo di indirizzi word per verificare lo stato della connessione.

**\[indirizzo di stato\](indicazione di stato)**

Valore 0: server online arrestato.

Valore 1: disconnesso dal server.

Valore 2: connessione al server riuscita.

**■   \[indirizzo di stato + 1\](indicazione di errore)**

|                      |                                                                                                                                                                                                                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Valore indicato** | **Descrizione**                                                                                                                                                                                                                                                                             |
| 0                    | Operazione completata correttamente                                                                                                                                                                                                                                                         |
| -1                   | Operazione del client MQTT non riuscita                                                                                                                                                                                                                                                     |
| -2                   | Errore di persistenza                                                                                                                                                                                                                                                                       |
| -3                   | Client disconnesso                                                                                                                                                                                                                                                                          |
| -4                   | È stato raggiunto il numero massimo di messaggi consentiti contemporaneamente                                                                                                                                                                                                              |
| -5                   | Rilevata stringa UTF-8 non valida                                                                                                                                                                                                                                                           |
| -6                   | È stato fornito un parametro vuoto non valido                                                                                                                                                                                                                                               |
| -7                   | Il topic è stato troncato (la stringa del topic contiene caratteri NULL); usare il valore della lunghezza del topic per accedere al topic completo                                                                                                                                         |
| -8                   | Il parametro di struttura non ha l'identificatore (eye catcher) e il numero di versione corretti                                                                                                                                                                                           |
| -9                   | Il parametro qos non è 0, 1 o 2                                                                                                                                                                                                                                                             |
| -10                  | Tutti i 65535 msgid MQTT sono in uso                                                                                                                                                                                                                                                        |
| -11                  | La richiesta non è completa e viene scartata                                                                                                                                                                                                                                                |
| -12                  | Impossibile mettere in buffer altri messaggi                                                                                                                                                                                                                                                |
| -13                  | Tentativo di usare la versione non SSL della libreria per una connessione SSL                                                                                                                                                                                                               |
| -14                  | Il prefisso del protocollo nel serverURI deve essere: tcp:// o mqtt:// (TCP non sicuro), ssl:// o mqtts:// (SSL/TLS cifrato), ws:// (WebSocket non sicuro) o wss:// (WebSocket sicuro). I prefissi TLS (ssl, mqtts, wss) sono validi solo se è collegata la versione TLS della libreria |
| -15                  | Non usare altre versioni dell'opzione MQTT                                                                                                                                                                                                                                                  |
| -16                  | La chiamata non è applicabile alla versione MQTT del client                                                                                                                                                                                                                                 |
| -17                  | La lunghezza del topic del messaggio "will" è zero                                                                                                                                                                                                                                          |
| -18                  | Il comando di connessione o disconnessione viene ignorato perché in testa alla coda c'è già un comando di connessione o disconnessione. Usare le callback onSuccess/onFailure per attendere il completamento del comando precedente                                                         |
| -19                  | maxBufferedMessages nelle opzioni di connessione deve essere &gt;=0                                                                                                                                                                                                                           |

- Indirizzo di controllo

**Il tipo di dati del registro è un intero a 16 bit.**

Se il valore è minore o uguale a 0, si disconnette dal server MQTT.

Se il valore è maggiore di 0, mantiene la connessione con il server MQTT.
