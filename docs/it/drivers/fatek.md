# Driver per dispositivi Fatek

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei <span id="OLE_LINK158"></span><span id="OLE_LINK159"></span>PLC Fatek serie FB. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Fatek serie FB. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Fatek serie FB.

**Come collegare un dispositivo Fatek**

**1. Collegamento hardware**

Cavo di collegamento:

RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (porta seriale, protocollo RS232)

|                         |     |                 |     |
|-------------------------|-----|-----------------|-----|
| HMI serie HM COM1/COM2 |     | Fatek serie FB |     |
| 2                       | RX  | 1               | TX  |
| 3                       | TX  | 2               | RX  |
| 5                       | GND | 4               | GND |

|     |                                                    |     |                                                    |     |                                                    |
|-----|----------------------------------------------------|-----|----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     | <img src="../../drivers/fatek.files/image006.gif" width="146" /> |
|     | <img src="../../drivers/fatek.files/image007.gif" width="129" /> |     |                                                    |     |                                                    |
|     |                                                    |     | <img src="../../drivers/fatek.files/image008.gif" width="280" /> |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |

Il connettore dell'HMI serie HM è DB9F, quello del PLC Fatek serie FB è MD4M.

**2. Impostazioni software**

Selezionare Fatek Automation Corp. nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Fatek serie FB.

Parametri di collegamento predefiniti del touch screen serie HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Fatek FB Series | Fatek FB Series |
| **Tipo di porta di comunicazione** | RS232 | RS232 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 7 | 7/8 |
| **Parità** | EVEN | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 1 | 0~255 |
| **Numero di stazione HMI** | 0 | 0~255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | Sì |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                                   |
|-------------------|--------------------|-----------------|---------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| X | dddd | 0~9999 | Bit: ingresso, sola lettura |
| Y | dddd | 0~9999 | Bit: relè di uscita |
| M | dddd | 0~9999 | Bit: relè interno |
| S | dddd | 0~9999 | Bit: relè di passo |
| T | dddd | 0~9999 | Bit: stato del timer |
| C | dddd | 0~9999 | Bit: stato del contatore |
| R | dddd | 0~9999 | <span id="OLE_LINK198"></span>Word: registro dati |
| D | dddd | 0~9999 | Word: registro dati |
| TR | dddd | 0~9999 | Word: valore corrente del timer |
| CR | dddd | 0~9999 | Word: valore corrente del contatore |
| F | dddd | 0~9999 | Word: registro file |
| DRC | ddd | 200~255 | Double word: valore corrente del contatore a 32 bit |

<img src="../../drivers/fatek.files/image009.gif" width="600" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/fatek.files/image009.gif" width="600" />
