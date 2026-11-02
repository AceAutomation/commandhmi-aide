# Driver per dispositivi Fuji

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Fuji serie NB. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del PLC Fuji serie NB. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Fuji serie NB.

**Come collegare un dispositivo Fuji**

**1. Collegamento hardware**

Cavo di collegamento:

RS422<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (porta seriale, protocollo RS422)

|                         |     |                |     |
|-------------------------|-----|----------------|-----|
| HMI serie HM COM1/COM2 |     | Fuji serie NB |     |
| 6                       | RX- | 4              | TX- |
| 7                       | RX+ | 3              | TX+ |
| 8                       | TX- | 6              | RX- |
| 9                       | TX+ | 5              | RX+ |

|     |                                                   |     |                                                   |     |                                                  |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|--------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     | <img src="../../drivers/fuji.files/image002.gif" width="95" /> |
|     | <img src="../../drivers/fuji.files/image003.gif" width="130" /> |     |                                                   |     |                                                  |
|     |                                                   |     | <img src="../../drivers/fuji.files/image004.gif" width="278" /> |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |

Il connettore dell'HMI serie HM è DB9F, quello del PLC Fuji serie NB è RJ45.

**2. Impostazioni software**

Selezionare Fuji Electric Corporation nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Fuji serie NB.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Fuji NB Series | Fuji NB Series |
| **Tipo di porta di comunicazione** | RS422 | RS422 |
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
| **Modalità estesa** | Sì |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | hhh | 0~7ff | Bit: ingresso, sola lettura |
| **Y** | hhh | 0~7ff | Bit: uscita |
| **M** | hhhh | 0~7fff | Bit: relè interno |
| **SM** | hhhh | 8000~81ff | Bit: relè interno |
| **L** | hhh | 0~5ff | Bit: relè a ritenuta |
| **S** | hh | 0~ff | Bit: relè di passo |
| **T** | hhh | 0~1ff | Bit: stato del timer |
| **C** | hh | 0~ff | Bit: stato del contatore |
| **D** | hhhh | 0~7fff | Word: registro dati |
| **SD** | hhhh | 8000~80ff | Word: registro dati |
| **TV** | hhh | 0~1ff | Word: valore corrente del timer |
| **CV** | hh | 0~ff | Word: valore corrente del contatore |

<img src="../../drivers/fuji.files/image005.gif" width="595" />

Nota:

h indica il sistema esadecimale, cifre da 0 a 9 e da a a f;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/fuji.files/image005.gif" width="595" />
