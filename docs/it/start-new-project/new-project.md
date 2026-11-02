# Creare un nuovo progetto

Questa operazione serve a creare un nuovo progetto. Selezionare Nuovo progetto nel menu File oppure il pulsante Nuovo progetto <img src="../../start-new-project/new-project.files/new-project136.png" width="28" /> nella barra degli strumenti: CommandHMI apre la finestra "Nuovo progetto", in cui si indicano nome e percorso di salvataggio del progetto. Selezionare il modello di HMI; fare clic su OK per creare il progetto e passare alla finestra delle impostazioni della porta di comunicazione; fare clic su Annulla per uscire.

**1. Finestra Nuovo progetto**

Nome progetto:

Percorso: percorso di salvataggio del nuovo file di progetto; il valore predefinito è C: \\

Modello: modelli disponibili per i progetti:

HM-035AE(320\*240)        HM-035UE(320\*240)        HM-043AE()480\*272        HM-043D(480\*272)        HM-043AD(480-272)        HM-043BE(480\*272)        HM-043BS(480\*272)        HM-043QE(480\*272)        HM-043UE(480\*272)        HM-043TE(480\*272)        HM-050AS(480\*272)        HM-050AE(480\*272)        HM-050BS(800\*480)        HM-050BE(800\*480)        HM-057AE(640\*480)        HM-070AS(800\*480)        HM-070AE(800\*480)        HM-070BS(800\*480)        HM-070BE(800\*480)        HM-070GS(800\*480)        HM-070GE(800\*480)        HM-070QS(800\*480)        HM-070QE(800\*480)        HM-070GG(800\*480)        HM-070GW(800\*480)        HM-070MS(800\*480)        HM-070ME(800\*480)        HM-070MG(800\*480)        HM-070MW(800\*480)        HM-T070XS(1024\*600)        HM-102AS(800\*480)        HM-102AE(800\*480)        HM-102BS(1024\*600)        HM-102BE(1024\*600)        HM-102CW(1024\*600)        HM-102CG(1024\*600)        HM-102HE(1024\*600)        HM-102HS(1024\*600)        HM-121AS(800\*600)        HM-121AE(800\*600)        HM-H150AS(1024\*768)        HM-156QS(1920\*1080)

Il modello predefinito è HM-070AE(800\*480); la risoluzione tra parentesi (800 \* 480) non viene mostrata nella finestra.

Modalità di visualizzazione: orientamento del touch screen usato dal progetto. Le opzioni sono:

Orizzontale: configurazione con il touch screen in orizzontale.

Verticale: configurazione con il touch screen in verticale.

La modalità predefinita è Orizzontale.

<img src="../../start-new-project/new-project.files/image002.jpg" width="547" alt="ScreenShot00217.jpg" />

Figura 3-1      Finestra Nuovo progetto

La figura sopra mostra la finestra Nuovo progetto, in cui si indicano Nome, Percorso, Modello e Modalità di visualizzazione; poi fare clic su Avanti per impostare la porta di comunicazione.

Il modello da scegliere dipende dall'HMI in possesso dell'utente.

<img src="../../start-new-project/new-project.files/new-project1533.png" width="130" />

Il nome del nuovo progetto non può contenere i caratteri seguenti: \\ /: \* "&lt;&gt; \|?.

Il percorso del nuovo progetto non può contenere i caratteri seguenti: \\ /: \* "&lt;&gt; \|?.

## 2. Finestra Impostazioni di comunicazione

La finestra Impostazioni di comunicazione serve a impostare i parametri della porta di comunicazione dell'HMI. Solo parametri corretti garantiscono una comunicazione regolare tra PLC e touch screen. I parametri dipendono dal modello di PLC da collegare.

Nome connessione: nome della porta di comunicazione.

Servizio dispositivo: selezione della marca del PLC e del tipo di CPU.

Interfaccia di connessione: scegliere una porta COM o la porta Ethernet.

Intervallo di indirizzi PLC consecutivi: imposta lo spazio di indirizzi consecutivi del PLC; si consiglia il valore predefinito.

##

<img src="../../start-new-project/new-project.files/new-project2298.png" width="624" />

Figura 3-2      Finestra Impostazioni di comunicazione

La figura sopra mostra la finestra delle impostazioni della porta di comunicazione, in cui si sceglie il servizio dispositivo in base al tipo di dispositivo collegato. Per una connessione Ethernet, scegliere "Collegamento diretto (Ethernet)" in "Tipo di connessione".

ID connessione: parametro interno, non modificabile!

Le proprietà di comunicazione si possono impostare anche in seguito dalla connessione nel gestore di progetto, dove si impostano gli altri parametri.

**3.       Finestra Proprietà pagina**

Fare clic su "Avanti" nella finestra Impostazioni di comunicazione per aprire la finestra Nuova pagina, in cui si impostano nome e colore di sfondo della pagina. Il nome predefinito è il numero della pagina; il colore di sfondo predefinito è il blu. A ogni nuova pagina, CommandHMI assegna un numero che indica l'ordine della pagina nel progetto. La numerazione parte da 1: la prima pagina è la 1, la quinta è la 5. Per cambiare il colore di sfondo, fare clic sul rettangolo accanto a Colore di sfondo per aprire la tavolozza dei colori. Con oltre duecento colori pronti, CommandHMI offre un'ampia scelta. Se non basta, fare clic in basso a destra nella tavolozza per definire un colore personalizzato: nella finestra Colori personalizzati scegliere prima il colore di base, poi il colore nell'area quadrata centrale, trascinando il mouse per regolarlo; si può anche agire sulla barra verticale a destra trascinando il mouse, poi fare clic su OK. Si possono anche inserire direttamente i valori del colore.

<img src="../../start-new-project/new-project.files/new-project4278.png" width="626" />

Figura 3-3      Finestra Nuova pagina

<img src="../../start-new-project/new-project.files/new-project4313.png" width="506" />

Figura 3-4      Finestra di selezione del colore

Si può anche scegliere un'immagine come sfondo della pagina. Fare clic sull'icona del percorso per trovare l'immagine.

<img src="../../start-new-project/new-project.files/new-project4463.png" width="331" />

Figura 3-5      Impostazione del percorso dell'immagine

Fare clic su OK per completare questi passaggi: il sistema apre subito la pagina appena creata. La preparazione del nuovo progetto è terminata e si può iniziare a modificare il progetto.
