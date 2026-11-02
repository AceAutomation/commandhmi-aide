# Collegamento passante (pass-through)

Il touch screen HMI consente un tipo di connessione speciale in cui un HMI remoto può monitorare o controllare un PLC o un altro dispositivo attraverso la porta seriale di un altro HMI collegato al PLC o al dispositivo. In questo modo si hanno due o più terminali di controllo per lo stesso dispositivo. Il collegamento passante è una funzione molto utile dell'HMI.

Prima di usare il collegamento passante, è necessario conoscere i seguenti termini:

• HMI locale: l'HMI collegato al PLC o ad altro dispositivo.

• HMI remoto: l'HMI collegato all'HMI locale, che controlla i dispositivi tramite il collegamento passante.

Per realizzare il collegamento passante, l'HMI locale deve disporre di due porte seriali. Lo schema del collegamento passante è mostrato nella Figura 8-12 e nella Figura 8-13:

Collegamento passante con due schermi:

<img src="../../multpoint/penetrate.files/penetrate789.png" width="578" />

Figura 8-12    Schema del collegamento passante con due schermi

Collegamento passante con più schermi:

<img src="../../multpoint/penetrate.files/penetrate913.png" width="792" />

Figura 8-13    Schema del collegamento passante con più schermi

HMI locale: impostazioni software:

Fare doppio clic sulla connessione creata per aprire la finestra delle proprietà della porta di comunicazione. Scegliere COM1 come porta di connessione. Prendendo come esempio il collegamento passante MITSUBISHI, la COM1 dell'HMI locale è collegata a un PLC MITSUBISHI FX2N. I parametri impostati in Parametri di comunicazione devono corrispondere a quelli del PLC o del dispositivo collegato. Vedere la Figura 8-14 e la Figura 8-15:

<img src="../../multpoint/penetrate.files/penetrate1423.png" width="589" />

Figura 8-14    Scheda Generale delle proprietà della porta di comunicazione dell'HMI locale

<img src="../../multpoint/penetrate.files/penetrate1500.png" width="587" />

Figura 8-15: scheda COM1 delle proprietà della porta di comunicazione dell'HMI locale

Creare una nuova connessione, scegliere COM2 come porta, non aggiungere alcun protocollo in Connessione, impostare le proprietà come segue e impostare gli stessi parametri seriali della porta 1. I parametri consigliati sono 9600, 8, None, 1. Come proprietà passante scegliere "Connetti porta schermo slave" (Connect Slave Screen Port) e impostare il numero di schermi in base alla situazione reale. Vedere la Figura 8-16 e la Figura 8-17.

<img src="../../multpoint/penetrate.files/image001.jpg" width="598" alt="ScreenShot00093.jpg" />

Figura 8-16    Scheda Generale delle proprietà della porta di comunicazione dell'HMI locale

<img src="../../multpoint/penetrate.files/penetrate2042.png" width="589" />

Figura 8-17    Scheda Parametri delle proprietà della porta di comunicazione dell'HMI locale

Lasciare i valori predefiniti per gli altri parametri. A questo punto la configurazione dell'HMI locale è completata.

HMI remoto: impostazioni software:

Fare doppio clic sulla connessione creata per aprire la finestra delle proprietà della porta di comunicazione. Scegliere COM1 come porta, "Remoto" (Remote) come posizione HMI e impostare gli stessi parametri di comunicazione della scheda parametri COM2 dell'HMI locale (vedere sopra), come mostrato nella Figura 8-18 e nella Figura 8-19.

<img src="../../multpoint/penetrate.files/penetrate2646.png" width="589" />

Figura 8-18    Scheda Generale delle proprietà della porta di comunicazione dell'HMI remoto

<img src="../../multpoint/penetrate.files/penetrate2724.png" width="588" />

Figura 8-19    Scheda Parametri delle proprietà della porta di comunicazione dell'HMI remoto

Lasciare i valori predefiniti per gli altri parametri. A questo punto la configurazione dell'HMI remoto è completata.

<img src="../../multpoint/penetrate.files/penetrate2924.png" width="130" />

Nota: le impostazioni precedenti riguardano il collegamento passante con due schermi.

Nota: nel collegamento passante con più schermi, l'impostazione COM dell'HMI remoto è la stessa di quella dell'HMI locale.

Nota: poiché tutti i dati di comunicazione vengono scambiati con il PLC attraverso la COM1 dell'HMI locale, nel collegamento passante con più schermi la velocità di comunicazione è ridotta.
