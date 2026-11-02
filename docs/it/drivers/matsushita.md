# Driver per dispositivi Matsushita

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Matsushita serie FP. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Matsushita serie FP. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Matsushita serie FP.

Come collegare un PLC Matsushita serie FP

**1.  Collegamento hardware**

Cavo di collegamento:

RS232-FP0/FP2/FP2SH/FPM

|                                                                                                                                                 |     |                          |     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| <span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span>**HMI serie HM COM1/COM2** |     | **Matsushita serie FP** |     |
| 2                                                                                                                                               | RX  | 3                        | TX  |
| 3                                                                                                                                               | TX  | 2                        | RX  |
| 5                                                                                                                                               | GND | 1                        | GND |

<img src="../../drivers/matsushita.files/image002.gif" width="280" /><img src="../../drivers/matsushita.files/image003.gif" width="129" /><img src="../../drivers/matsushita.files/image004.gif" width="145" />

Il connettore dell'HMI è DB9F, quello del PLC Matsushita serie FP è MD5M.

RS422-FP1

|                             |     |                      |     |
|-----------------------------|-----|----------------------|-----|
| **HMI serie HM COM1/COM2** |     | Matsushita serie FP |     |
| 6                           | RX- | 2                    | TX- |
| 7                           | RX+ | 5                    | TX+ |
| 8                           | TX- | 3                    | RX- |
| 9                           | TX+ | 6                    | RX+ |

<img src="../../drivers/matsushita.files/image005.gif" width="140" /><img src="../../drivers/matsushita.files/image006.gif" width="129" /><img src="../../drivers/matsushita.files/image007.gif" width="280" />

Il connettore dell'HMI è DB9F, quello del PLC Matsushita serie FP è MD8M.

**2. Impostazioni software**

Selezionare MATSUSHITA nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Matsushita serie FP.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | FP Series | FP Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | ODD | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 1 | 0~255 |
| **Numero di stazione HMI** | 0 | 0~255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | No |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | ddddh | 0~9999f | Bit: ingresso esterno, sola lettura |
| **Y** | ddddh | 0~9999f | Bit: uscita esterna |
| **R** | ddddh | 0~9999f | Bit: relè interno |
| **L** | ddddh | 0~9999f | Bit: relè di collegamento |
| **T** | dddd | 0~9999 | Bit: stato del timer, sola lettura |
| **C** | dddd | 0~9999 | Bit: stato del contatore, sola lettura |
| **WX** | dddd | 0~9999 | Word: ingresso esterno, sola lettura |
| **WY** | dddd | 0~9999 | Word: uscita esterna |
| **WR** | dddd | 0~9999 | Word: relè interno |
| **WL** | dddd | 0~9999 | Word: relè di collegamento |
| **DT** | ddddd | 0~99999 | Word: registro dati |
| **LD** | ddddd | 0~99999 | Word: registro di collegamento |
| **FL** | ddddd | 0~99999 | Word: registro file |
| **SV** | dddd | 0~9999 | Word: area dei valori impostati di timer/contatori |
| **EV** | dddd | 0~9999 | Word: area dei valori correnti di timer/contatori |

<img src="../../drivers/matsushita.files/image008.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

h indica il sistema esadecimale, cifre da 0 a 9 e da a a f;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/matsushita.files/image009.gif" width="595" />
