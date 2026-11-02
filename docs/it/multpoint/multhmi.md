# Collegamento "un dispositivo con più HMI"

I touch screen HMI serie CommandHMI consentono il collegamento "un dispositivo con più HMI" a un PLC tramite protocollo MODBUS. I touch screen sono collegati in cascata e il primo schermo è collegato al PLC. Tutti i touch screen possono essere configurati come stazioni slave e il PLC come stazione master: fare doppio clic su "Connessione COM1" nel gestore di progetto per aprire la finestra delle proprietà della porta di comunicazione; nella voce Servizio dispositivo della scheda Generale scegliere Modbus RTU e a destra Modbus RTU Slave. In alternativa, il primo touch screen collegato al PLC può essere configurato come stazione master, e il PLC e gli altri schermi come stazioni slave. In questo caso, nelle proprietà della porta di comunicazione del primo schermo scegliere Modbus RTU nella voce Servizio dispositivo della scheda Generale e a destra Modbus RTU Master; nella scheda Parametri impostare la modalità estesa e assegnare gli indirizzi dei touch screen. In questo modo i touch screen configurati come slave possono comunicare con il PLC attraverso il primo touch screen. In entrambe le configurazioni solo la stazione master può comunicare con le stazioni slave; le stazioni slave non possono comunicare tra loro.

Con il PLC configurato come stazione master e tutti i touch screen come stazioni slave:

1. La porta di comunicazione del PLC collegato è RS232; i metodi di collegamento e le impostazioni di sistema sono mostrati nelle Figure 8-1, 8-2 e 8-3:

<img src="../../multpoint/multhmi.files/multhmi1428.png" width="577" />

Figura 8-1  Schema "un dispositivo con più HMI" con PLC (RS232) come stazione master

<img src="../../multpoint/multhmi.files/multhmi1528.png" width="589" />

Figura 8-2 Scelta del protocollo MODBUS e impostazione come stazione slave

<img src="../../multpoint/multhmi.files/multhmi1593.png" width="588" />

Figura 8-3 Assegnazione dell'indirizzo di stazione dell'HMI

2. La porta di comunicazione del PLC collegato è RS485; il metodo di collegamento è mostrato nella Figura 8-4:

<img src="../../multpoint/multhmi.files/multhmi1744.png" width="598" />

Figura 8-4  Schema "un dispositivo con più HMI" con PLC (RS485) come stazione master

Quando la porta di comunicazione del PLC è RS485 e tutti i touch screen sono stazioni slave, le impostazioni di sistema sono le stesse del caso RS232. Vedere la Figura 8-2 e la Figura 8-3.

Quando tutti gli schermi HMI sono configurati come stazioni slave, si possono collegare fino a 255 schermi. Tuttavia, con molti touch screen collegati la risposta diventa lenta.

 Con il primo touch screen configurato come stazione master, e il PLC e tutti gli altri schermi come stazioni slave:

1. La porta di comunicazione del PLC collegato è RS232; i metodi di collegamento e le impostazioni di sistema sono mostrati nelle Figure 8-5, 8-6 e 8-7:

<img src="../../multpoint/multhmi.files/multhmi2462.png" width="579" />

Figura 8-5   Schema "un dispositivo con più HMI" con PLC (RS232) come stazione slave

<img src="../../multpoint/multhmi.files/multhmi2563.png" width="588" />

Figura 8-6 Scelta del protocollo MODBUS per il primo schermo e impostazione come stazione master

<img src="../../multpoint/multhmi.files/multhmi2650.png" width="590" />

Figura 8-7 La modalità estesa è necessaria quando il primo touch screen è stazione master

Le impostazioni di sistema dei touch screen configurati come stazioni slave sono simili a quelle mostrate nella Figura 8-2 e nella Figura 8-3.

<img src="../../multpoint/multhmi.files/multhmi2852.png" width="130" />

Nota: poiché RS232 non supporta il collegamento multipunto, se nel collegamento "un dispositivo con più HMI" il PLC non dispone di porta RS485, occorre un adattatore di comunicazione per convertire il segnale RS485 in RS232.

Nota: quando un touch screen HMI è stazione master nel collegamento "un dispositivo con più HMI", per il touch screen master occorre impostare la modalità indirizzo multiprotocollo (estesa).

Con Modbus configurato come stazione master si possono aggiungere in teoria fino a 255 stazioni slave; tuttavia, più stazioni slave si impostano, più lenta sarà la comunicazione.
