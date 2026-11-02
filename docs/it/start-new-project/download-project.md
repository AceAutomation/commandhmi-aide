# Download del progetto

<img src="../../start-new-project/download-project.files/image012.jpg" width="368" />

Figura 3-11    Messaggio di errore di compilazione

Si può correggere in base al messaggio di errore nella finestra di output, oppure fare doppio clic sull'errore: CommandHMI trova e seleziona automaticamente l'oggetto errato. Facendo doppio clic sull'oggetto se ne vedono le proprietà, si individua la causa dell'errore e si apportano le modifiche. Poi fare clic su Salva e compilare di nuovo. Se non ci sono errori, dopo poco compare una finestra che indica la compilazione riuscita. Fare clic su OK per terminare, come mostrato nella Figura 3-12:

<img src="../../start-new-project/download-project.files/image013.jpg" width="364" />

Figura 3-12    Finestra di output delle informazioni

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Prima del download occorre compilare, e prima di compilare occorre salvare; altrimenti la compilazione non riesce, come mostrato nella Figura 3-11. Se dopo la compilazione si apportano altre modifiche, occorre compilare di nuovo.

<img src="../../start-new-project/download-project.files/image014.jpg" width="425" />

Figura 3-13    Promemoria di compilazione

Infine eseguire il comando USB del menu Download per scaricare tramite cavo USB; in alternativa si può scegliere direttamente il comando Compila + Download del menu Download. Compare la finestra della Figura 3-14:

<img src="../../start-new-project/download-project.files/image015.jpg" width="716" />

Figura 3-14    Finestra di download

Fare clic per scaricare; la barra di avanzamento al centro mostra lo stato del download. Al termine, una finestra indica che il download USB è completato. Fare clic su OK per terminare, come mostrato nella Figura 3-15:

<img src="../../start-new-project/download-project.files/image005.jpg" width="720" alt="2018_11_20_09_02_42.jpg" />

Figura 3-15    Download completato

Il passo successivo è il collegamento al PLC per verificare che il progetto funzioni correttamente nell'HMI.

I modi di collegamento tra HMI e PLC o PC sono descritti in "Collegamento" nel manuale hardware.

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Durante il trasferimento non togliere l'alimentazione all'HMI o al PC, non scollegare il cavo USB ed evitare altre operazioni, per non compromettere il trasferimento.

Installare i driver USB prima del download; altrimenti il PC non si collega all'HMI e non è possibile completare il download.

<img src="../../start-new-project/download-project.files/image017.jpg" width="716" />

Figura 3-16    Messaggio relativo al driver USB

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

La finestra della Figura 3-16 indica che il PC non riconosce l'HMI. Occorre verificare che il driver USB sia installato: collegare il PC e accendere l'HMI, poi cercare "CommandHMI HMI Tech Corp USB drive" in Windows, in "Risorse del computer" - "Proprietà" - "Hardware" - "Gestione dispositivi" - "Controller USB (Universal Serial Bus)" (si può provare a scollegare il cavo USB per verificare se il PC riconosce l'HMI):

**Download della configurazione tramite Ethernet**

• Impostare i parametri di rete dell'HMI

Attivare insieme gli interruttori DIP 1 e 3; impostare l'IP (qui 192.168.1.100), il gateway, la subnet e la porta. La porta è fissa a 12345.

• Compilare la configurazione

Se si sceglie il download tramite Ethernet, occorre inserire indirizzo IP e numero di porta nel campo di immissione. L'IP è quello dell'HMI di destinazione: qui 192.168.1.100, come sopra, con porta fissa 12345. Poi fare clic per riavviare e scaricare, come mostrato nella Figura 3-18:

![](../../start-new-project/download-project.files/001.png)

Figura 3-18 Download della configurazione tramite Ethernet

È anche possibile fare clic sul pulsante Scan per eseguire la scansione degli indirizzi IP

![](../../start-new-project/download-project.files/002.png)

È possibile verificare l'indirizzo IP trovato e modificarlo nel campo di modifica sottostante

![](../../start-new-project/download-project.files/003.png)

Fare clic sul pulsante a destra per applicare le modifiche alle informazioni visualizzate: al termine compare una finestra di conferma.

![](../../start-new-project/download-project.files/004.png)

Fare quindi clic su Rescan: le modifiche risultano visibili nell'elenco.

![](../../start-new-project/download-project.files/005.png)

Selezionare l'indirizzo IP da utilizzare e fare clic sul pulsante Select per confermare l'IP di destinazione; le informazioni IP vengono riportate automaticamente nella finestra di download.

**Attenzione!**

Per usare la funzione di scansione IP devono essere soddisfatti i tre requisiti seguenti:

1. I pannelli prodotti prima del 30 dicembre 2024 richiedono l'aggiornamento manuale con il pacchetto patch per la scansione IP: se il file "hmi.patch" non è presente nella cartella di installazione, contattare l'assistenza tecnica per ottenerlo.
     2. La versione del software di configurazione non deve essere inferiore a HMITOOLV7.1_022
     3. La versione del firmware non deve essere inferiore a Simulator 8.1.0.10.

![](../../start-new-project/download-project.files/006.png)
