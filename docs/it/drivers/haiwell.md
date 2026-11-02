# Driver per dispositivi HaiWell

|                                                                                                                                                                                                                                                                                                                                                                                                                                                     |     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Haiwell serie E/S/H. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Haiwell serie E/S/H. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Haiwell serie E/S/H. |     |

<span id="OLE_LINK217"></span><span id="OLE_LINK218"></span><span id="OLE_LINK219"></span>Come collegare un dispositivo HAIWELL<span id="OLE_LINK221"></span>

<span id="OLE_LINK222"></span><span id="OLE_LINK223"></span><span id="OLE_LINK224"></span>**1. Collegamento hardware**

<span id="OLE_LINK225"></span><span id="OLE_LINK226"></span><span id="OLE_LINK227"></span>Cavo di collegamento:

RS232 (porta seriale, protocollo RS232)

|                                                                                                                       |     |                          |     |
|-----------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| <span id="OLE_LINK228"></span><span id="OLE_LINK229"></span><span id="OLE_LINK230"></span>**HMI serie HM COM1/COM2** |     | **HaiWell serie E/S/H** |     |
| 2                                                                                                                     | RX  | 2                        | TX  |
| 3                                                                                                                     | TX  | 1                        | RX  |
| 5                                                                                                                     | GND | 3                        | GND |

|     |                                                      |     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                      |
|     | <img src="../../drivers/haiwell.files/image002.gif" width="129" /> |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     | <img src="../../drivers/haiwell.files/image003.gif" width="140" /> |
|     |                                                      |     | <img src="../../drivers/haiwell.files/image004.gif" width="280" /> |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |

<span id="OLE_LINK231"></span>Il connettore dell'HMI serie HM è DB9F, quello del PLC Haiwell serie E/S/H è MD4M.

<span id="OLE_LINK237"></span>**2. Impostazioni software**

Selezionare Haiwell Technology Corp. nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Haiwell serie E/S/H.

<span id="OLE_LINK242"></span>Parametri di collegamento predefiniti del touch screen serie HMI

|                             |                             |                             |                                              |     |
|-----------------------------|-----------------------------|-----------------------------|----------------------------------------------|-----|
| **Parametro** | **Valore predefinito** |                             | **Valori ammessi** |     |
| **Tipo di porta di comunicazione** | RS232 |                             | RS232/RS422/RS485 |     |
| **Velocità (baud)** | 19200 |                             | 1200/2400/4800/9600/19200/38400/57600/115200 |     |
| **Bit di dati** | 8 |                             | 7/8 |     |
| **Parità** | NONE |                             | EVEN/ODD/NONE |     |
| **Bit di stop** | 2 |                             | 1/2 |     |
| **Numero di stazione PLC** | 1 |                             | 1~31 |     |
| **Numero di stazione HMI** | 0 |                             | 0~255 |     |
| **Funzione** |                             | **Supportata** |                                              |     |
| **Simulazione offline** |                             | Sì |                                              |     |
| **Simulazione online** |                             | Sì |                                              |     |
| **Modalità estesa** |                             | Sì |                                              |     |
|                             |                             |                             |                                              |     |

3\. **Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| X | ddd | 0~1023 | Bit: ingresso digitale esterno |
| Y | ddd | 0~1023 | Bit: uscita digitale esterna |
| M | ddd | 0~12287 | Bit: relè interno |
| SM | ddd | 0~215 | Bit:<span id="OLE_LINK153"></span> stato del sistema |
| S | ddd | 0~2047 | Bit: stato di passo |
| T | ddd | 0~1023 | Bit: stato del timer |
| C | ddd | 0~255 | Bit: stato del contatore |
| AI | ddd | 0~255 | Word: registro di ingresso analogico |
| AQ | ddd | 0~255 | Word: registro di uscita analogica |
| V | ddd | 0~14847 | Word: registro interno |
| TCV | ddd | 0~1023 | Word: <span id="OLE_LINK154"></span>valore corrente del timer |
| CCV | ddd | 0~47, 80~255 | Word: valore corrente del contatore |
| SV | ddd | 0~154 | Word: registro di sistema |
| CCV32 | ddd | 0~31 | Double word: valore corrente del contatore |

<img src="../../drivers/haiwell.files/image010.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/haiwell.files/image011.gif" width="595" />
