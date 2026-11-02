# Collegamento "un HMI con più dispositivi"

Gli HMI consentono, tramite protocollo MODBUS, non solo il collegamento "un dispositivo con più HMI" ma anche il collegamento "un HMI con più dispositivi". In quest'ultima, un solo touch screen può operare direttamente sui registri di più PLC collegati, purché questi supportino il protocollo MODBUS. Nelle impostazioni di sistema, scegliere Modbus RTU nella voce Servizio dispositivo della scheda Generale e a destra Modbus RTU Master: il touch screen diventa stazione master e tutti i PLC stazioni slave. Il touch screen può quindi operare sui registri dei PLC. I nomi dei registri dei PLC corrispondono a quelli del protocollo MODBUS.

<img src="../../multpoint/multmachine.files/multmachine744.png" width="506" />

Figura 8-8      Collegamento "un HMI con più dispositivi"

<img src="../../multpoint/multmachine.files/multmachine805.png" width="590" />

Figura 8-9      Impostazione del touch screen come stazione master

<img src="../../multpoint/multmachine.files/multmachine857.png" width="588" />

Figura 8-10    La modalità estesa è necessaria quando il touch screen è stazione master

Dopo questa impostazione, gli indirizzi PLC nelle proprietà della porta di comunicazione non hanno più effetto. Quando l'utente fa clic su un oggetto per inserire un indirizzo, compare la finestra di immissione indirizzo mostrata nella Figura 8-11. A destra del nome del registro c'è un menu a discesa: il valore scelto è l'indirizzo della stazione slave (PLC).

<img src="../../multpoint/multmachine.files/multmachine1294.png" width="251" />

Figura 8-11    Finestra di immissione indirizzo

<img src="../../multpoint/multmachine.files/multmachine1326.png" width="130" />

**Indirizzi di controllo per abilitare la comunicazione con le stazioni in modalità estesa:**

Ogni porta seriale occupa 16 word per il controllo dei numeri di stazione, cioè al massimo 256 stazioni abilitabili, con LW59000 come indirizzo base

COM1 corrisponde a 59010~59025: LW59010 alle stazioni 0~15, LW59011 alle stazioni 16~31, e così via

COM2 corrisponde a 59026~59041: LW59026 alle stazioni 0~15, LW59027 alle stazioni 16~31, e così via

Ethernet corrisponde a 59026~59041: LW59026 alle stazioni 0~15, LW59027 alle stazioni 16~31, e così via

All'avvio dell'HMI tutte le stazioni sono abilitate per impostazione predefinita; con una macro si può controllare ogni bit per avviare o arrestare la comunicazione con il numero di stazione corrispondente.

<img src="../../multpoint/multmachine.files/multmachine1993.png" width="130" />

Nota: poiché RS232 non supporta il collegamento multipunto, se nel collegamento "un HMI con più dispositivi" il PLC non dispone di porta RS485, occorre un adattatore di comunicazione per convertire il segnale RS485 in RS232.
