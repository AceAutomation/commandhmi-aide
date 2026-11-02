# Proprietà della porta di comunicazione

Le proprietà della porta di comunicazione servono a impostare i parametri di comunicazione tra l'HMI e i dispositivi collegati.

Fare doppio clic su "Collegamento" (Link) e su Collegamento 1, come mostrato nella Figura 7-1:

<img src="../../setting/com.files/image004.jpg" width="532" />

Figura 7-1      Finestra delle proprietà della porta COM1

Nella scheda "Collegamento" (Link) sono disponibili varie marche e modelli di PLC, oltre al "Nome collegamento" e all'"Intervallo di indirizzi PLC consecutivi"

Fare clic sulla scheda Parametri della finestra, come mostrato nella Figura 7-2:

<img src="../../setting/com.files/image005.jpg" width="532" />

Figura 7-2      Impostazione dei parametri della porta di comunicazione COM1

**Impostazione dei parametri:**

Servizi dispositivo: produttore, marca del PLC e modello di CPU.

Porta: RS232 / 485/ 422

Baud rate: 1200/2400/4800/9600/19200/38400/57600/115200 / 187.5k

Parità: Odd / Even / None

Bit di dati: 7/8

Bit di stop: 1/2

Modello: modello del PLC

Numero di stazione HMI: imposta il numero di stazione dell'HMI

Tempo di comunicazione: l'HMI invia dati al PLC e ne riceve i dati; non può inviare di nuovo prima che sia trascorso il tempo di comunicazione impostato.

Timeout 1 e Timeout 2: il periodo di timeout si ottiene dividendo Timeout 1 per Timeout 2; nella figura sopra il timeout è di 200 ms. Si ha un timeout se l'HMI non ha ricevuto i dati 200 ms dopo l'invio.

Numero di tentativi: numero di ritrasmissioni dei dati dopo un timeout

Modalità indirizzo: ① Modalità standard: una porta seriale collega un solo PLC; ② Modalità estesa: una porta seriale collega più PLC dello stesso tipo

Intervallo di indirizzi PLC consecutivi: numero massimo di word che il PLC può leggere in una sola volta
