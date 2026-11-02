# Uso di HMIManager

Andare alla pagina degli strumenti di download

![](../../appendix/hmimanageer.files/002.png)

Pagina Download:

Impostazione della comunicazione:
USB: il PC è collegato all'HMI tramite USB
WAN: il PC è collegato all'HMI tramite Ethernet

È anche possibile fare clic sul pulsante Scan per eseguire la scansione degli indirizzi IP

![](../../appendix/hmimanageer.files/a1.png)

È possibile verificare l'indirizzo IP trovato e modificarlo nel campo di modifica sottostante

![](../../appendix/hmimanageer.files/a2.png)

Fare clic sul pulsante a destra per applicare le modifiche alle informazioni visualizzate: al termine compare una finestra di conferma.

![](../../appendix/hmimanageer.files/a3.png)

Fare quindi clic su Rescan: le modifiche risultano visibili nell'elenco.

![](../../appendix/hmimanageer.files/a4.png)

Selezionare l'indirizzo IP da utilizzare e fare clic sul pulsante Select per confermare l'IP di destinazione; le informazioni IP vengono riportate automaticamente nella finestra di download.

**Attenzione!**

Per usare la funzione di scansione IP devono essere soddisfatti i tre requisiti seguenti:

1. I pannelli prodotti prima del 30 dicembre 2024 richiedono l'aggiornamento manuale con il pacchetto patch per la scansione IP: se il file "hmi.patch" non è presente nella cartella di installazione, contattare l'assistenza tecnica per ottenerlo.
     2. La versione del software di configurazione non deve essere inferiore a HMITOOLV7.1_022
     3. La versione del firmware non deve essere inferiore a Simulator 8.1.0.10.

Selezione del download:
Download della configurazione: occorre generare il file di progetto u-disk-prj.bin; nel software di configurazione selezionare Download-&gt;Extract Project Save As-&gt;Generate u-disk-prj.bin, fare clic su Browse per selezionare il file, quindi su Start per scaricarlo e aggiornare la configurazione nell'HMI.
Download delle ricette: compilare il progetto HMI, aprire la cartella compile nella cartella di installazione del software, dove si trovano i due file recipe60.bin e recipe62.bin: per versioni fino alla 6.0 selezionare recipe60.bin, per versioni superiori alla 6.0 selezionare recipe62.bin. Fare clic su Browse per selezionare il file, quindi su Start Download.

![](../../appendix/hmimanageer.files/003.png)

Pagina Upload:

Impostazione della comunicazione:
Come per il download.

Selezione dell'upload:
Area di selezione dell'upload: è possibile caricare la configurazione se le impostazioni del pannello lo consentono; ricette, dati storici e allarmi storici possono essere caricati solo se presenti nel programma in esecuzione sull'HMI.
Upload dei dati storici: fare clic su Browse per impostare percorso e nome del file da salvare, quindi su Start Upload per caricare il file zip dei dati storici e il file .csv; per i dettagli vedere "Upload dei dati storici".
Upload della configurazione: fare clic su Browse per impostare percorso e nome del file da salvare, quindi su Start Upload per caricare il file zip della configurazione; una volta decompresso, il progetto può essere visualizzato e modificato normalmente. Vedere "Upload del progetto".
Upload delle ricette: fare clic su Browse per impostare percorso e nome del file da salvare, quindi su Start Upload per caricare il file delle ricette presente nell'HMI.
Upload degli allarmi storici: fare clic su Browse per impostare percorso e nome del file da salvare, quindi su Start Upload per caricare il file degli allarmi presente nell'HMI.

![](../../appendix/hmimanageer.files/004.png)

Pagina Version:

Impostazione della comunicazione:
Come per il download.

Informazioni sulla versione: versione dell'HMI attualmente collegato.

![](../../appendix/hmimanageer.files/005.png)

Pagina Firmware:

Impostazione della comunicazione:
Come per il download.

Firmware Info
Informazioni firmware: fare clic su Browse per selezionare il firmware da aggiornare, quindi su Upgrade

![](../../appendix/hmimanageer.files/006.png)

Pagina Simulation:

Selezionare con Browse il file di progetto .vpm per eseguire la simulazione online o offline.

![](../../appendix/hmimanageer.files/007.png)

Pagina Address:

Service: selezionare il produttore del dispositivo.
Model: selezionare il modello del dispositivo
Vengono visualizzate tutte le informazioni sugli indirizzi del dispositivo selezionato.
