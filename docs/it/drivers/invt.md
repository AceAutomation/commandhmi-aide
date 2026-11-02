# Dispositivi Invt

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei <span id="OLE_LINK121"></span>PLC Invt. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del PLC Invt. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Invt.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Invt</p>
<p>1.  Collegamento hardware</p>
<p>Cavo di collegamento:</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p>Invt</p></td>
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
<p><img src="../../drivers/invt.files/image005.gif" width="145" /><img src="../../drivers/invt.files/image006.gif" width="281" /><img src="../../drivers/invt.files/image007.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Il connettore dell'HMI è DB9F, quello del PLC Invt è MD8M.

**2. Impostazioni software**

Selezionare Invt nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Invt.

Parametri di collegamento predefiniti del touch screen serie HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **PLC type**                | IVC1,IVC1L,IVCIS,IVC2L,IVC3 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                  |
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

**3. (IVC1, IVC1L, IVCIS, IVC2L, IVC3, IVC3 TCP) Registri utilizzabili e intervalli di indirizzi**

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
| CV_Double | ddd | 0~255 | Double word: valore corrente del contatore |
| SD_Double | ddd | 0~255 | Double word: registro dati speciale |
| R | ddd | 0~32767 | Word: registro a 16 bit |
| RD | ddd | 32766 | Double word: registro R a 32 bit |
|                   |                    |                 |                                             |
| D_Bit | dddd.dd | 0.0~7999.15 | Bit: bit del registro D |
| SD_Bit | ddd.dd | 0.0~255.15 | Bit: bit del registro SD |
| Z_Bit | dd.dd | 0.0~15.15 | Bit: bit del registro Z |
| R_Bit | dddd.dd | 0.0~32767.15 | Bit: bit del registro R |

AX70 RTU/AX70 TCP

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **IX** | ddd.o | 0.0~511.7 | Bit: area I, accesso a bit (sola lettura) |
| **QX** | ddd.o | 0.0~511.7 | Bit: area Q, accesso a bit |
| **MX** | ddd.o | 0.0~7566.7 | Bit: area M, accesso a bit |
| **IB** | ddd | 0~511 | Byte: area I, accesso a byte (sola lettura) |
| **QB** | ddd | 0~511 | Byte: area Q, accesso a byte |
| **MB** | dddd | 0~7566 | Byte: area M, accesso a byte |
| **IW** | ddd | 0~511 | Word: area I, accesso a word (sola lettura) |
| **QW** | ddd | 0~511 | Word: area Q, accesso a word |
| **MW** | dddd | 0~3783 | Word: area M, accesso a word |
| **ID** | ddd | 0~127 | Double word: area I, accesso a double word (sola lettura) |
| **QD** | ddd | 0~127 | Double word: area Q, accesso a double word |
| **MD** | dddd | 0~1891 | Double word: area M, accesso a double word |

<img src="../../drivers/invt.files/image004.gif" width="600" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/invt.files/image004.gif" width="600" />
