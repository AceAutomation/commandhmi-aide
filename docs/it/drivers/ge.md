# Driver per dispositivi GE

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC GE Fanuc. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del PLC GE Fanuc. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC GE Fanuc.

**1. Collegamento hardware**

Cavo di collegamento:

RS232 (porta seriale, protocollo RS232)

|                             |     |                     |     |
|-----------------------------|-----|---------------------|-----|
| **HMI serie HM COM1/COM2** |     | **GE Fanuc** |     |
| 2                           | RX  | 4                   | TX  |
| 3                           | TX  | 3                   | RX  |
| 5                           | GND | 8                   | GND |

|     |                                                 |     |                                                 |     |                                                |
|-----|-------------------------------------------------|-----|-------------------------------------------------|-----|------------------------------------------------|
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     | <img src="../../drivers/ge.files/image002.gif" width="97" /> |
|     | <img src="../../drivers/ge.files/image003.gif" width="130" /> |     |                                                 |     |                                                |
|     |                                                 |     | <img src="../../drivers/ge.files/image004.gif" width="278" /> |     |                                                |
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     |                                                |

Il connettore dell'HMI serie HM è DB9F, quello del PLC GE Fanuc è RJ45.

**2. Impostazioni software**

Selezionare GE Corporation nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC GE Fanuc.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | GE Fanuc SNP-X | GE Fanuc SNP-X/ GE Fanuc CCM |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 19200 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | ODD | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 0 | 0~255 |
| **Numero di stazione HMI** | 0 | 0~255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | No |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                            |
|-------------------|--------------------|-----------------|----------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **%I** | ddddd | 1~10000 | Bit: ingresso discreto |
| **%Q** | ddddd | 1~10000 | Bit: uscita discreta |
| **%M** | ddddd | 1~10000 | Bit: uso interno |
| **%S** | ddd | 1~128 | Bit: uso di sistema, sola lettura |
| **%SA** | ddd | 1~128 | Bit: uso di sistema, sola lettura |
| **%SB** | ddd | 1~128 | Bit: uso di sistema, sola lettura |
| **%SC** | ddd | 1~128 | Bit: uso di sistema, sola lettura |
| **%T** | ddd | 1~256 | Bit: stato temporaneo |
| **%G** | dddd | 1~7680 | Bit: Genius Global |
| **%AI** | ddddd | 1~10000 | Word: ingresso analogico |
| **%AQ** | ddddd | 1~10000 | Word: uscita analogica |
| **%R** | ddddd | 1~32640 | Word: memoria registri |

 <img src="../../drivers/ge.files/image005.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/ge.files/image005.gif" width="595" />
