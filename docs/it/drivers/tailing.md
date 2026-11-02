# Driver per dispositivi TaiLing

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC TaiLing serie DX. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC TaiLing serie DX. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC TaiLing serie DX.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC TaiLing serie DX</p>
<p><strong>1.  Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232 <span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>(porta seriale, protocollo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>TaiLing</strong> <strong>serie DX</strong></p></td>
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
<td><p>5</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/tailing.files/image002.gif" width="130" /><img src="../../drivers/tailing.files/image003.gif" width="290" /><img src="../../drivers/tailing.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Il connettore dell'HMI è DB9F, quello del PLC TaiLing serie DX è DB9M.

**2. Impostazioni software**

Selezionare TaiLing Electric nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC TaiLing serie DX.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | DX Series | DX Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | NONE | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 1 | da 1 a 31 |
| **Numero di stazione HMI** | 0 | da 0 a 255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | No |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | oooo | da 0 a 377 | Bit: ingresso, sola lettura |
| **Y** | oooo | da 0 a 377 | Bit: uscita |
| **M** | dddd | da 0 a 7999 | Bit: relè interno |
| **SM** | dddd | da 8000 a 8999 | Bit: relè interno speciale |
| **S** | dddd | da 0 a 999 | Bit: bit di stato |
| **T** | dddd | da 0 a 256 | Bit: stato del timer |
| **C** | dddd | da 0 a 256 | Bit: stato del contatore |
| **D** | dddd | da 0 a 7999 | Word: registro |
| **SD** | dddd | da 8000 a 8999 | Word: registro speciale |
| **TV** | dddd | da 0 a 255 | Word: valore corrente del timer |
| **CV** | dddd | da 0 a 199 | Word: valore corrente del contatore |
| **CV32** | dddd | da 200 a 255 | Double word: valore corrente del contatore a 32 bit |

<img src="../../drivers/tailing.files/image005.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo;

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/tailing.files/image005.gif" width="595" />
