# Modbus TCP/IP

È possibile eseguire la comunicazione remota e il controllo dell'HMI tramite MODBUS TCP.

**Impostazioni** con l'HMI configurato come stazione master:

Dopo aver creato un progetto, fare doppio clic su "Connessione 1" (Connection 1), come mostrato di seguito:

<img src="../../multpoint/modbustcpip.files/modbustcpip209.png" width="248" />

Viene visualizzata la finestra "Proprietà porta di comunicazione" (Communication Port Properties), mostrata di seguito.

<img src="../../multpoint/modbustcpip.files/modbustcpip286.png" width="590" />

Fare clic su "Parametri" (Parameter) nella finestra "Proprietà porta" per accedere alla finestra seguente e impostare l'indirizzo IP e il numero di porta (quelli del dispositivo monitorato). Scegliere la modalità indirizzo standard; fare clic su "OK" per completare le impostazioni.

<img src="../../multpoint/modbustcpip.files/modbustcpip544.png" width="588" />

Se come modalità indirizzo si seleziona "Modalità estesa" (Extended Mode), l'indirizzo IP e il numero di porta impostati qui non hanno effetto: si impostano invece in runtime tramite il pulsante funzione "Configurazione IP dispositivi slave" (Slave devices IP config).

Durante il runtime, fare clic sul pulsante per aprire la finestra di immissione del numero di stazione; inserire il numero di stazione e accedere all'interfaccia di impostazione dell'IP e della porta dello slave, come mostrato nella figura seguente:

<img src="../../multpoint/modbustcpip.files/modbustcpip985.png" width="445" />

Dopo queste impostazioni, scaricare il progetto nell'HMI; collegare master e slave direttamente o tramite un router per eseguire il monitoraggio e il controllo.

**Impostazioni della stazione slave:**

**1. Impostare l'IP**

Per prima cosa, impostare gli interruttori DIP 1 e 3 per accedere all'impostazione dell'indirizzo IP dell'HMI; nella pagina che compare, inserire l'indirizzo IP. In questo esempio l'indirizzo IP della stazione slave è 192.168.1.31. 2.

**2. Creare le connessioni**

Dopo aver creato il progetto, fare doppio clic su "Connessione 1" (Connection 1), come mostrato di seguito:

<img src="../../multpoint/modbustcpip.files/modbustcpip1527.png" width="229" />

Viene visualizzata la finestra "Proprietà porta di comunicazione" (Communication Port Properties), mostrata di seguito.

<img src="../../multpoint/modbustcpip.files/modbustcpip1604.png" width="588" />

Nella finestra mostrata sopra, eseguire le seguenti impostazioni:

\* Porta di connessione: "Ethernet" (come mostrato).

<img src="../../multpoint/modbustcpip.files/modbustcpip1711.png" width="543" />

\* Posizione HMI: selezionare "Locale" (Local) (come mostrato).

<img src="../../multpoint/modbustcpip.files/modbustcpip1752.png" width="163" />

\* Servizio di connessione: selezionare "Modbus" - "Modbus Slave TCP / IP" (come mostrato).

<img src="../../multpoint/modbustcpip.files/modbustcpip1830.png" width="531" />

Fare clic su "Parametri" (Parameter) nella finestra "Proprietà porta" per accedere alla finestra seguente e impostare l'indirizzo IP (della stazione slave) e il numero di porta. Fare clic su "OK" per completare le impostazioni.

<img src="../../multpoint/modbustcpip.files/modbustcpip2039.png" width="589" />

Scaricare il progetto nell'HMI; collegare master e slave direttamente o tramite un router per eseguire il monitoraggio e il controllo.

<img src="../../multpoint/modbustcpip.files/modbustcpip2198.png" width="130" />

L'indirizzo è l'indirizzo interno quando l'HMI è configurato come stazione slave.
