# Driver per dispositivi Nanda

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Nanda serie NA-200/400. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Nanda serie NA-200/400. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Nanda serie NA-200/400.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Nanda serie NA-200/400</p>
<p><strong>1.  Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Nanda NA-200/400</strong></p></td>
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
<p><img src="../../drivers/nanda.files/image002.gif" width="130" /><img src="../../drivers/nanda.files/image003.gif" width="290" /><img src="../../drivers/nanda.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Il connettore dell'HMI è DB9F, quello del PLC Nanda serie NA-200/400 è DB9M.

**2. Impostazioni software**

Selezionare Nanda Auto Technology nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Nanda serie NA-200/400.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **PLC type**                | Nanda NA-200                | Nanda NA-200/400                             |
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

Nanda NA-200

|                   |                    |                 |                                                                                                                               |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | ddd | 1~128 | Bit: <span id="OLE_LINK54"></span><span id="OLE_LINK55"></span><span id="OLE_LINK56"></span>ingresso digitale, sola lettura |
| **Q** | ddd | 1~128 | Bit: uscita digitale |
| **M** | dddd | 1~1024 | Bit: registro a bit |
| **S** | ddd | 1~256 | Bit: registro a bit di sistema |
| **N** | ddd | 1~256 | Bit: registro a bit con ritenzione in caso di mancanza di alimentazione |
| **IW** | dd | 1~32 | Word: ingresso analogico |
| **QW** | dd | 1~32 | Word: uscita analogica |
| **MW** | dddd | 1~1024 | Word: registro a word |
| **SW** | ddd | 1~256 | Word: registro a word di sistema |
| **NW** | ddd | 1~256 | Word: registro a word con ritenzione in caso di mancanza di alimentazione |

Nanda NA-400

|                   |                    |                 |                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | ddd | 1~2048 | Bit: ingresso digitale, sola lettura |
| **Q** | ddd | 1~2048 | Bit: uscita digitale |
| **M** | dddd | 1~8192 | Bit: registro a bit |
| **S** | ddd | 1~4096 | Bit: registro a bit di sistema |
| **N** | ddd | 1~2048 | Bit: registro a bit con ritenzione in caso di mancanza di alimentazione |
| **IW** | dd | 1~512 | Word: ingresso analogico |
| **QW** | dd | 1~512 | Word: uscita analogica |
| **MW** | dddd | 1~8192 | Word: registro a word |
| **SW** | ddd | 1~2048 | Word: registro a word di sistema |
| **NW** | ddd | 1~2048 | Word: registro a word con ritenzione in caso di mancanza di alimentazione |

<img src="../../drivers/nanda.files/image005.gif" width="596" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/nanda.files/image006.gif" width="595" />
