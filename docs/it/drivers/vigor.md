# Driver per dispositivi Vigor

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Vigor serie V/VH/VB/M. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Vigor serie V/VH/VB/M. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Vigor serie V/VH/VB/M.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Vigor serie V/VH/VB/M</p>
<p><strong>1.  Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Vigor serie V/VH/VB/M</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>2</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>4</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/vigor.files/image002.gif" width="63" /><img src="../../drivers/vigor.files/image003.gif" width="318" /><img src="../../drivers/vigor.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Il connettore dell'HMI è DB9F, quello del PLC Vigor serie V/VH/VB/M è DB9M.

**2. Impostazioni software**

Selezionare Vigor Electric Corp. nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Vigor serie V/VH/VB/M.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | V/VH/VB/M Series | V/VH/VB/M Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 19200 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 7 | 7/8 |
| **Parità** | EVEN | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 0 | da 0 a 255 |
| **Numero di stazione HMI** | 0 | da 0 a 255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | No |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                       |
|-------------------|--------------------|-----------------|---------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | ooo | da 0 a 777 | Bit: contatto di ingresso |
| **Y** | ooo | da 0 a 777 | Bit: contatto di uscita |
| **M** | dddd | da 0 a 8999 | Bit: relè interno |
| **SM** | dddd | da 9000 a 9255 | Bit: relè interno speciale |
| **S** | dddd | da 0 a 999 | Bit: relè di passo |
| **T** | ddd | da 0 a 255 | Bit: stato del timer |
| **C** | ddd | da 0 a 255 | Bit: stato del contatore |
| **D** | dddd | da 0 a 8999 | Word: registro dati |
| **SD** | dddd | da 9000 a 9255 | Word: registro dati speciale |
| **TV** | ddd | da 0 a 255 | Word: valore corrente del timer |
| **CV** | ddd | da 0 a 199 | Word: valore corrente del contatore |
| **CV32** | ddd | da 200 a 255 | Word: valore corrente del contatore a 32 bit |

<img src="../../drivers/vigor.files/image005.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo;

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/vigor.files/image005.gif" width="595" />
