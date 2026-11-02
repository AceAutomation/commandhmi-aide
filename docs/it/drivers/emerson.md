# Driver per dispositivi Emerson

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei <span id="OLE_LINK120"></span><span id="OLE_LINK121"></span>PLC Emerson serie EC. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del PLC Emerson serie EC. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Emerson serie EC.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Emerson serie EC</p>
<p>1.  Collegamento hardware</p>
<p>Cavo di collegamento:</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Emerson EC</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>3</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/emerson.files/image002.gif" width="146" /><img src="../../drivers/emerson.files/image003.gif" width="281" /><img src="../../drivers/emerson.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Il connettore dell'HMI è DB9F, quello del PLC Emerson serie EC è MD8M.

**2. Impostazioni software**

Selezionare Emerson Network Power nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Emerson serie EC.

Parametri di collegamento predefiniti del touch screen serie HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | EC Series (RTU) | EC Series (RTU) |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
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

|                   |                    |                 |                                             |
|-------------------|--------------------|-----------------|---------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| X | ooo | 0~377 | Bit: ingresso, sola lettura |
| Y | ooo | 0~377 | Bit: uscita |
| M | dddd | 0~7999 | Bit: relè interno |
| SM | ddd | 0~255 | Bit: relè interno speciale |
| S | ddd | 0~999 | Bit: relè di passo |
| T | ddd | 0~255 | Bit: stato del timer |
| C | ddd | 0~255 | Bit: stato del contatore |
| D | dddd | 0~7999 | Word: registro dati |
| SD | ddd | 0~255 | Word: registro dati speciale |
| TV | ddd | 0~255 | Word: valore corrente del timer |
| CV | ddd | 0~255 | Word: valore corrente del contatore |
| Z | dd | 0~15 | Word: registro di indirizzamento indicizzato |
| D_Double | dddd | 0~7999 | Double word: registro dati |
| CV_Double | ddd | 200~255 | Double word: valore corrente del contatore |
| SD_Double | ddd | 0~255 | Double word: registro dati speciale |

<img src="../../drivers/emerson.files/image005.gif" width="600" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/emerson.files/image006.gif" width="600" />
