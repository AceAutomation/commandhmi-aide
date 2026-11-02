# Telecamera

L'oggetto Telecamera permette di registrare video o acquisire immagini da una telecamera esterna; la pagina dell'oggetto è la seguente:

![](../../../configuration-guide/new_add_control/camera.files/001.png)

USB: per usare una telecamera collegata via USB occorre un HMI con sistema Linux 4.9.84 (001) o successivo;

Telecamera di rete: il flusso di ingresso è in formato RTSP; per esempio, il flusso di una telecamera Hikvision è:

admin:xl123456@192.168.1.63:554/ch1/sub/av_stream;

La sequenza del flusso è: nome account:password@indirizzo IP: le prime quattro voci sono impostate dall'utente in base ai parametri della telecamera, il resto è fisso e dipende dalla marca.

Suggerimento!

Sia con telecamere USB sia di rete, se la risoluzione è troppo alta la riproduzione sul touch screen presenta ritardi o scatti: occorre ridurre risoluzione, frame rate, ecc. del flusso. Le telecamere USB supportano il flusso video mjpeg, quelle di rete devono supportare il flusso con codifica h264. Le telecamere Hikvision sono state testate e verificate; per altre marche occorre verificare con prove pratiche.

Acquisizione immagini: attivando l'acquisizione tramite indirizzo, sulla chiavetta USB viene creata una cartella "video" in cui vengono salvati i video o le immagini acquisiti.

Formato di registrazione (Record Format): con il formato video la durata massima di registrazione è di 60 s. Il formato video salvato dalla telecamera di rete è MP4, quello della telecamera USB è AVI.

Immagine (Picture): con il formato immagine, il file viene salvato in formato JPG.

\[Avvio/arresto importazione\]: con valore 1 la telecamera collegata viene attivata e il flusso video importato; con valore 0 la telecamera viene disattivata e il flusso chiuso. \[Controllo pausa\]: sospende la visualizzazione del contenuto della telecamera, mentre il video continua a essere trasmesso. Nell'impostazione dell'indirizzo di controllo basta indicare l'indirizzo di avvio/arresto: l'indirizzo di pausa è l'indirizzo di avvio più 1.

Per esempio, se l'indirizzo di avvio/importazione è LW N, l'indirizzo di pausa è LW N+1.

Per la scheda di visualizzazione, vedere il pulsante "Position Switch".
