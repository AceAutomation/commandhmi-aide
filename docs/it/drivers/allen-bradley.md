# Driver per dispositivi Allen-Bradley

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei dispositivi AIBUS tramite il protocollo AIBUS. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del dispositivo AIBUS. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del dispositivo AIBUS.

**Come collegare un dispositivo AIBUS**

**1. Collegamento hardware**

Cavo di collegamento:

RS232 (porta seriale, protocollo RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Dispositivo AIBUS** |     |
| 2 | RX | Pin definiti dall'utente | TX |
| 3 | TX | Pin definiti dall'utente | RX |
| 5 | GND | Pin definiti dall'utente | GND |

<img src="../../drivers/allen-bradley.files/image002.gif" width="130" /><img src="../../drivers/allen-bradley.files/image003.gif" width="280" /><img src="../../drivers/allen-bradley.files/image004.gif" width="145" />

ControlLogix/CompactLogix:

|                             |     |                         |     |
|-----------------------------|-----|-------------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Allen-Bradley (AB)** |     |
| 2                           | RX  | 3                       | TX  |
| 3                           | TX  | 2                       | RX  |
| 5                           | GND | 5                       | GND |

<img src="../../drivers/allen-bradley.files/image005.gif" width="129" /><img src="../../drivers/allen-bradley.files/image006.gif" width="290" /><img src="../../drivers/allen-bradley.files/image007.gif" width="130" />

La porta dell'HMI serie HM è DB9F, quella del dispositivo AB è MD8M.

**2. Impostazioni software**

ü Selezionare Allen-Bradley nel servizio del dispositivo collegato.

ü Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

ü Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

ü Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Allen-Bradley.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | MicroLogix DF1_CRC | MicroLogix DF1_CRC/MicroLogix DF1_BCC |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 19200 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | NONE | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 1 | 1~31 |
| **Numero di stazione HMI** | 0 | 0~255 |
| **Controllo** | CRC | BCC |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | No |

**3. Registri utilizzabili e intervalli di indirizzi**

Serie SLC/MicroLogix:

|                   |                    |                        |                                |
|-------------------|--------------------|------------------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | 1:ddd/o | 1:0/0~1:255/15 | Bit: immagine degli ingressi |
| **O** | 0:ddd/o | 0:0/0~0:255/15 | Bit: immagine delle uscite |
| **B** | ddd:ddd/o | 3:0/0~255:255/15 | Bit: memoria a bit |
| **S_Bit** | 2:ddd/o | 2:0/0~2:255/15 | Bit: bit di stato del sistema |
| **N_Bit** | ddd:ddd/o | 7:0、10:0/0~255:255/15 | Bit: bit di una word del registro dati |
| **S** | 2:ddd | 2:0~2:255 | Word: word di stato del sistema |
| **ST** | ddd:ddd.dd | 0:0.0~255:255.40 | Word: word di stato del sistema |
| **N** | ddd:ddd | 7:0、10:0~255:255 | Word: registro dati |
| **F** | ddd:ddd | 8:0~255:255 | Word: registro in virgola mobile |
| **T_ACC** | ddd:ddd | 4:0~255:255 | Word: valore ACC del timer |
| **T_PRE** | ddd:ddd | 4:0~255:255 | Word: valore PRE del timer |
| **C_ACC** | ddd:ddd | 5:0~255:255 | Word: valore ACC del contatore |
| **C_PRE** | ddd:ddd | 5:0~255:255 | Word: valore PRE del contatore |

ControlLogix/CompactLogix:

|                   |                    |                  |                                |
|-------------------|--------------------|------------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **B-Bit** | ddd:ddd/dd | 3~225:0~255/0~15 | Bit: bit di una word del registro dati |
| **N_Bit** | ddd:ddd/dd | 7~225:0~255/0~15 | Bit: bit di una word del registro dati |
| **N_Bit** | ddd:ddd/o | 7:0/0~255:255/7 | Bit: bit di una word del registro dati |
| **S** | 2:ddd | 2:0~2:255 | Word: word di stato del sistema |
| **N** | ddd:ddd | 7:0~255:255 | Word: registro dati |
| **F** | ddd:ddd | 8:0~255:255 | Word: registro in virgola mobile |

CompactLogix_L16ER_TCP (porta: 44818)

|               |                    |                 |                                        |
|---------------|--------------------|-----------------|----------------------------------------|
| Nome registro | **Formato indirizzo** | **Intervallo** | **Note** |
| **B** | ddd.ddd | 0.0~255.255 | Bit: indirizzo di tipo bool |
| **I** | Ddd.ddd | 0.0~255.255 | Word: registro int a 16 bit |
| **F** | ddd.ddd | 0.0~255.99 | Double word: registro float a 32 bit |

MicroLogix DF1_TCP            (porta: 44818)

|               |                    |                  |                                                    |
|---------------|--------------------|------------------|----------------------------------------------------|
| Nome registro | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | ddd.ddd/dd | 0.0/0~255.255/15 | Bit: immagine degli ingressi, sola lettura |
| **O** | ddd.ddd/dd | 0.0/0~255.255/15 | Bit: immagine delle uscite |
| **B** | ddd.ddd/dd | 0.0/0~255.255/15 | Bit: memoria a bit |
| **T** | ddd.ddd | 0.0~255.255 | Bit: stato del timer |
| **C** | ddd.ddd | 0.0~255.255 | Bit: stato del contatore |
| **S_Bit** | ddd.ddd/dd | 0.0/0~255.255/15 | Bit: bit del registro di sistema |
| **N_Bit** | ddd.ddd/dd | 0.0/0~255.255/15 | Bit: bit di un registro dati |
| **S** | ddd.ddd | 0.0~255.255 | Word: registro di sistema |
| **N** | ddd.ddd | 0.0~255.255 | Word: registro intero a 16 bit |
| **F** | ddd.ddd | 0.0~255.255 | Double word: registro in virgola mobile a 32 bit |
| **TV** | ddd.ddd | 0.0~255.255 | Word: valore corrente del timer |
| **CV** | ddd.ddd | 0.0~255.255 | Word: valore corrente del contatore |
| **TS** | ddd.ddd | 0.0~255.255 | Word: valore impostato del timer |
| **CS** | ddd.ddd | 0.0~255.255 | Word: valore impostato del contatore |

**4. Collegamento degli HMI serie HM ai PLC Allen-Bradley ControlLogix e CompactLogix**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Aprire RSLinx e configurare il driver di comunicazione del PLC</p>
<p><img src="../../drivers/allen-bradley.files/image008.gif" width="349" /></p>
<p>Creare un driver; selezionare collegamento seriale e dispositivi RS-232 DF1</p>
<p><img src="../../drivers/allen-bradley.files/image009.gif" width="425" /></p>
<p>Dopo la configurazione, se PC e PLC sono collegati con un cavo, il PLC è visibile in RSLinx</p>
<p><img src="../../drivers/allen-bradley.files/image010.gif" width="430" /></p>
<p>Aprire il software di programmazione del PLC RSLogix 5000, creare il progetto e i nuovi tag</p>
<p><img src="../../drivers/allen-bradley.files/image011.gif" width="282" /></p>
<p>Creare i tag B003, N007 e F008</p>
<p><img src="../../drivers/allen-bradley.files/image012.gif" width="390" /></p>
<p>Elenco dei tag dopo la creazione:</p>
<p><img src="../../drivers/allen-bradley.files/image013.gif" width="633" /></p>
<p>Creare la <a href="javascript:;">mappatura degli indirizzi</a></p>
<p><img src="../../drivers/allen-bradley.files/image014.gif" width="428" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image015.gif" width="410" /><strong></strong></p>
<p><strong>Impostare i parametri del PLC</strong></p>
<p><img src="../../drivers/allen-bradley.files/image016.gif" width="807" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image017.gif" width="552" /><strong></strong></p>
<p>·d indica il sistema decimale, cifre da 0 a 9;</p>
<p>·o indica il sistema ottale, cifre da 0 a 7;</p>
<p>·Bit nelle note: il registro può essere usato solo come bit;</p>
<p>·Word nelle note: il registro può essere usato solo come word;</p>
<p>·Sola lettura nelle note: il registro può essere letto ma non scritto;</p>
<p>·I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.</p>
<p>Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato </p></td>
</tr>
</tbody>
</table>

Collegamento ai PLC CompactLogix serie 1769

Nuovi tag di indirizzo nel PLC

Corrispondenza tra indirizzi e tag

Registro        tipo di tag     dimensione array

B                          bool             255

I                           int                 255

F                          real               100

Il nome del tag deve avere 3 caratteri, per esempio B003, I004 e F005

<img src="../../drivers/allen-bradley.files/image018.jpg" width="314" alt="ab_guanli.jpg" />

<img src="../../drivers/allen-bradley.files/image019.jpg" width="390" alt="ab_guanli2.jpg" />

Collegamento ai MicroLogix serie 1766 DF1_TCP

Tranne i registri di I/O, la cui dimensione non è impostabile, la dimensione degli array degli altri registri è 256. Il primo numero del formato dell'indirizzo è il numero di file: per esempio, il numero di file di F8 è 8, quello di I1 è 1, e così via.
