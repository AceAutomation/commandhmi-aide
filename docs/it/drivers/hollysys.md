# Driver per dispositivi HollySys

Questo driver permette ai touch screen di leggere e scrivere dati o stati dei registri dei PLC HollySys serie LM. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC HollySys serie LM. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC HollySys serie LM.

**Come collegare un PLC HOLLYSYS**

**1.  Collegamento hardware**

Cavo di collegamento:

RS232 (porta seriale, protocollo RS232)

|                             |     |                        |     |
|-----------------------------|-----|------------------------|-----|
| **HMI serie HM COM1/COM2** |     | **HollySys serie LM** |     |
| 2                           | RX  | 3                      | TX  |
| 3                           | TX  | 2                      | RX  |
| 5                           | GND | 5                      | GND |

<img src="../../drivers/hollysys.files/image002.gif" width="130" /><img src="../../drivers/hollysys.files/image003.gif" width="290" /><img src="../../drivers/hollysys.files/image004.gif" width="130" />

Il connettore dell'HMI serie HM è DB9F, quello del PLC HollySys serie LM è DB9M.

**2. Impostazioni software**

Selezionare HollySys Group nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC HollySys serie LM.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | HollySys LM Series | HollySys LM Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 38400 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | NONE | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 51 | 0~255 |
| **Numero di stazione HMI** | 0 | 0~255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | No |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                                                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **IX** | ddd.o | 0.0~511.7 | Bit: area di memoria I, sola lettura |
| **QX** | ddd.o | 0.0~511.7 | Bit: area di memoria Q |
| **MX** | dddd.o | 0.0~7816.7 | Bit: area di memoria M |
| **IW** | ddd | 0~510 | Word:<span id="OLE_LINK284"></span> area di memoria I, registro a 8 bit, ogni word occupa due indirizzi |
| **QW** | ddd | 0~510 | Word: <span id="OLE_LINK285"></span>area di memoria Q, registro a 8 bit, ogni word occupa due indirizzi |
| **MW** | dddd | 0~8190 | Word: area di memoria M, registro a 8 bit, ogni word occupa due indirizzi |

<img src="../../drivers/hollysys.files/image005.gif" width="600" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

Registro a 8 bit nelle note: la distanza tra gli indirizzi di due word adiacenti del registro è 2;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/hollysys.files/image005.gif" width="600" />
