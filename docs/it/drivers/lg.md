# Driver per dispositivi LG

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC LG serie Master-K. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC LG serie Master-K. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC LG serie Master-K.

Come collegare un PLC LG serie Master-K

**1. Collegamento hardware**

Cavo di collegamento:

RS232 con protocollo CNet<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> (porta seriale, protocollo RS232)

|                                                                                                                    |     |                 |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-----------------|-----|
| <span id="OLE_LINK60"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span>**HMI serie HM COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                                                  | RX  | 7               | TX  |
| 3                                                                                                                  | TX  | 4               | RX  |
| 5                                                                                                                  | GND | 5               | GND |

<img src="../../drivers/lg.files/image002.gif" width="130" /><img src="../../drivers/lg.files/image003.gif" width="291" /><img src="../../drivers/lg.files/image004.gif" width="130" />

Il connettore dell'HMI è DB9F, quello del PLC LG serie Master-K è DB9M.

RS232 con protocollo KLoader

|                                                                                       |     |                 |     |
|---------------------------------------------------------------------------------------|-----|-----------------|-----|
| <span id="OLE_LINK65"></span><span id="OLE_LINK66"></span>**HMI serie HM COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                     | RX  | 3               | TX  |
| 3                                                                                     | TX  | 2               | RX  |
| 5                                                                                     | GND | 5               | GND |

<img src="../../drivers/lg.files/image005.gif" width="291" /><img src="../../drivers/lg.files/image006.gif" width="130" /><img src="../../drivers/lg.files/image007.gif" width="130" />

Il connettore dell'HMI è DB9F, quello del PLC LG serie Master-K è DB9M.

RS<span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>485

|                                                          |     |                 |
|----------------------------------------------------------|-----|-----------------|
| <span id="OLE_LINK67"></span>**HMI serie HM COM1/COM2** |     | **LG Master-K** |
| 8                                                        | D-  | B               |
| 9                                                        | D+  | A               |

 <img src="../../drivers/lg.files/image008.gif" width="157" /><img src="../../drivers/lg.files/image009.gif" width="130" />

Il connettore dell'HMI è DB9F, quello del PLC LG serie Master-K è una morsettiera a due fili.

RS232-K10S1

|                             |     |                 |     |
|-----------------------------|-----|-----------------|-----|
| **HMI serie HM COM1/COM2** |     | **LG Master-K** |     |
| 2                           | RX  | 4               | TX  |
| 3                           | TX  | 1               | RX  |
| 5                           | GND | 6               | GND |

Il connettore dell'HMI è DB9F, quello del PLC LG serie Master-K è MD6M.

|     |                                                 |     |                                                 |
|-----|-------------------------------------------------|-----|-------------------------------------------------|
|     |                                                 |     |                                                 |
|     |                                                 |     | <img src="../../drivers/lg.files/image010.gif" width="146" /> |
|     | <img src="../../drivers/lg.files/image011.gif" width="401" /> |     |                                                 |
|     |                                                 |     |                                                 |

**2. Impostazioni software**

Selezionare LG Industrial Systems nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC LG serie Master-K.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | LG Master-K Cnet | LG Master-K Cnet/K Loader/K10s1 |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 19200 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | NONE | EVEN/ODD/NONE |
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

Intervallo di indirizzi utilizzabili dei PLC serie Kxxx:

|               |                |             |                                |
|---------------|----------------|-------------|--------------------------------|
| Nome registro | Formato indirizzo | Intervallo | Note |
| P_Bit | dddh | 0~255f | Bit: area di ingresso/uscita |
| M_Bit | dddh | 0~255f | Bit: relè ausiliario |
| K_Bit | dddh | 0~255f | Bit: relè protetto |
| L_Bit | dddh | 0~255f | Bit: relè di collegamento |
| F_Bit | dddh | 0~255f | Bit: relè speciale |
| P | dddh | 0~255f | Word: area di ingresso/uscita |
| M | dddh | 0~255f | Word: relè ausiliario |
| K | dddh | 0~255f | Word: relè protetto |
| L | dddh | 0~255f | Word: relè di collegamento |
| F | dddh | 0~255f | Word: relè speciale |
| T | ddd | 0~255 | Bit: relè del timer |
| C | ddd | 0~255 | Bit: relè del contatore |
| S | dddd | 0~9999 | Word: registro di passo |
| D | dddd | 0~9999 | Word: registro dati |
| TV | ddd | 0~255 | Word: valore corrente del timer |
| CV | ddd | 0~255 | Word: valore corrente del contatore |

Intervallo di indirizzi utilizzabili dei PLC serie XGB CPU (comunicazione tramite la porta di download RS232 del PLC):

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| P_Bit | ddddh | 0-1023f | Bit: area di ingresso/uscita |
| M_Bit | ddddh | 0-1023f | Bit: relè ausiliario |
| F_Bit | ddddh | 0-1023f | Bit: relè speciale |
| L_Bit | ddddh | 0-2047f | Bit: relè di collegamento |
| K_Bit | ddddh | 0-4095f | Bit: relè protetto |
| D_Bit          | ddddh        | 0-10239f     |                                   |
| T | dddd | 0-1023 | Bit: relè del timer |
| C | dddd | 0-1023 | Bit: relè del contatore |
| TV | dddd | 0-1023 | Word: valore corrente del timer |
| CV | dddd | 0-1023 | Word: valore corrente del contatore |
| P | dddd | 0-1023 | Word: area di ingresso/uscita |
| M | dddd | 0-1023 | Word: relè ausiliario |
| F | dddd | 0-1023 | Word: relè speciale (sola lettura) |
| L | dddd | 0-2047 | Word: relè di collegamento |
| K | dddd | 0-4095 | Word: relè protetto |
| D | dddd | 0-10239 | Word: registro dati |
| R | dddd | 0-10239 | Word: registro di passo |
| ZR             | dddd         | 0-10239      | Word:                             |
| S | ddd | 0-127 | Word: registro di passo |
| Z              | ddd          | 0-127        | Word:                             |
| U | dd.dd | 0.0-10.31 | Word: (sola lettura) |

Intervallo di indirizzi utilizzabili dei PLC serie XGB CNET:

|               |                |             |                         |
|---------------|----------------|-------------|-------------------------|
| Nome registro | Formato indirizzo | Intervallo | Note |
| P | dddh | 0~127f | Word: area di ingresso/uscita |
| M | dddh | 0~255f | Word: relè ausiliario |
| K | dddh | 0~2559f | Word: relè protetto |
| L | dddh | 0~1279f | Word: relè di collegamento |
| F | dddh | 0~255f | Word: relè speciale |
| T | ddd | 0~255 | Bit: relè del timer |
| C | ddd | 0~255 | Bit: relè del contatore |
| S | ddd | 0~127.99 | Word: registro di passo |
| D | dddd | 0~5119 | Word: registro dati |
| N             | dddd           | 0~3935      |                         |
| Z             | ddd            | 0~127       |                         |
| ZR            | dddd           | 0~1023      |                         |
| U             | d              | 0~7.31      |                         |

XGB TCP/IP

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| P_Bit | ddddh | 0-2047f | Bit: area di ingresso/uscita |
| M_Bit | ddddh | 0-2047f | Bit: relè ausiliario |
| F_Bit | ddddh | 0-2047f | Bit: relè speciale |
| L_Bit | ddddh | 0-4095f | Bit: relè di collegamento |
| K_Bit | ddddh | 0-8191f | Bit: relè protetto |
| T | dddd | 0-2047 | Bit: relè del timer |
| C | dddd | 0-2047 | Bit: relè del contatore |
| TV | dddd | 0-2047 | Word: valore corrente del timer |
| CV | dddd | 0-2047 | Word: valore corrente del contatore |
| P | dddd | 0-2047 | Word: area di ingresso/uscita |
| M | dddd | 0-2047 | Word: relè ausiliario |
| F | dddd | 0-2047 | Word: relè speciale (sola lettura) |
| L | dddd | 0-4095 | Word: relè di collegamento |
| K | dddd | 0-8191 | Word: relè protetto |
| D | ddddd | 0-19999 | Word: registro dati |
| R              | ddddd        | 0-16383      |                                   |
| S | ddd | 0-127 | Word: registro di passo |
| Z              | ddd          | 0-127        |                                   |
| U              | dd.dd        | 0.0-11.31    |                                   |
| N | ddddd | 0-10239 | Word: (sola lettura) |

<img src="../../drivers/lg.files/image012.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

h indica il sistema esadecimale, cifre da 0 a 9 e da a a f;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/lg.files/image013.gif" width="595" />
