# Driver per dispositivi Delta

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei <span id="OLE_LINK42"></span><span id="OLE_LINK43"></span>PLC Delta serie DVP. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del PLC Delta serie DVP. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Delta serie DVP.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Delta serie DVP</p>
<p><strong>1.  Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK53"></span><span id="OLE_LINK2"></span> (porta seriale, protocollo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI serie HM  COM1/COM2</p></td>
<td colspan="2"><p>Delta serie DVP</p></td>
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
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/delta.files/image008.gif" width="281" /><img src="../../drivers/delta.files/image009.gif" width="146" /><img src="../../drivers/delta.files/image010.gif" width="130" />  </p>
<p><span id="OLE_LINK54"></span>Il connettore dell'HMI serie HM è DB9F, quello del PLC Delta serie DVP è MD8M.</p>
<p>RS485 (porta seriale, protocollo RS485)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI serie HM COM1/COM2</p></td>
<td><p>Delta serie DVP</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/delta.files/image011.gif" width="130" /><img src="../../drivers/delta.files/image012.gif" width="156" /></p>
<p>Il connettore dell'HMI serie HM è DB9F, quello del PLC Delta serie DVP è una morsettiera a due fili.</p></td>
</tr>
</tbody>
</table>

**2. Impostazioni software**

ü Selezionare Delta Corporation nel servizio del dispositivo collegato.

ü Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

ü Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

ü Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Delta serie DVP.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Delta DVP Series | Delta DVP Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 19200 | 1200/2400/4800/9600/19200/38400/57600/115200 |
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

|                   |                    |                 |                                               |
|-------------------|--------------------|-----------------|-----------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | ooo | 0~377 | Bit: ingresso, sola lettura |
| **Y** | ooo | 0~377 | Bit: uscita |
| **M** | dddd | 0~4095 | Bit: relè ausiliario |
| **S** | dddd | 0~1023 | Bit: relè interno |
| **T** | ddd | 0~255 | Bit: stato del timer |
| **C** | ddd | 0~255 | Bit: stato del contatore |
| **D** | dddd | 0~9999 | Word: registro dati |
| **TV** | ddd | 0~255 | Word: valore corrente del timer |
| **CV** | ddd | 0~199 | Word: valore corrente del contatore |
| **CV32** | ddd | 200~255 | Double word: valore corrente del contatore a 32 bit |

<img src="../../drivers/delta.files/image013.gif" width="595" />

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Nota:</p>
<p>d indica il sistema decimale, cifre da 0 a 9;</p>
<p>o indica il sistema ottale, cifre da 0 a 7;</p>
<p>Bit nelle note: il registro può essere usato solo come bit;</p>
<p>Word nelle note: il registro può essere usato solo come word;</p>
<p>Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;</p>
<p>Sola lettura nelle note: il registro può essere letto ma non scritto;</p>
<p>I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.</p>
<p>Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.</p></td>
</tr>
</tbody>
</table>
