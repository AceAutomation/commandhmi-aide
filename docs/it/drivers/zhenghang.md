# Driver per dispositivi ZhengHang

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC ZhengHang serie A5. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC ZhengHang serie A5. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC ZhengHang serie A5.

Come collegare un PLC ZhengHang serie A5

**1. Collegamento hardware**

Cavo di collegamento:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

|                           |     |                    |     |
|---------------------------|-----|--------------------|-----|
| **HM　ＨＭＩ　COM1/COM2** |     | **ZhengHang A5　** |     |
| 2                         | RX  | 2                  | TX  |
| 3                         | TX  | 3                  | RX  |
| 5                         | GND | 5                  | GND |

<img src="../../drivers/zhenghang.files/image002.gif" width="130" /><img src="../../drivers/zhenghang.files/image003.gif" width="290" /><img src="../../drivers/zhenghang.files/image004.gif" width="130" />

Il connettore dell'HMI è DB9F, quello del PLC ZhengHang serie A5 è DB9M.

**2. Impostazioni software**

Selezionare ZhengHang Electronics nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC ZhengHang serie A5.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | A5 Series | A5 Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | NONE | EVEN/ODD/NONE |
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

|                   |                    |                 |                                                                           |
|-------------------|--------------------|-----------------|---------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | dd.o | da 0.0 a 15.7 | Bit: immagine degli ingressi, sola lettura |
| **Q** | dd.o | da 0.0 a 15.7 | Bit: immagine delle uscite |
| **M** | dddd.o | da 0.0 a 4095.7 | Bit: memoria a bit |
| **VW** | dddd | da 0 a 1998 | Word: memoria variabili, registro a 8 bit, ogni word occupa due indirizzi |
| **AIW** | d | da 0 a 9 | Word: ingresso analogico, sola lettura |
| **AQW** | d | da 0 a 9 | Word: uscita analogica, sola scrittura |

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />
