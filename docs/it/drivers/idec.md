# Driver per dispositivi IDEC

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC IDEC (MicroSmart) serie FC4A/FC5A/FC6A. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del PLC. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC MicroSmart serie FC4A/FC5A/FC6A.

**Come collegare un PLC MicroSmart serie FC4A/FC5A**

1\. Collegamento hardware

Cavo di collegamento:

RS232 (porta seriale, protocollo RS232)

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="3"><p><strong>Macro Smart FC4A/FC5A</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td colspan="2"><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td colspan="2"><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>6</p></td>
<td><p>GND</p></td>
<td rowspan="2"><p>6-7</p>
<p>Ponticello</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>

|     |                                                   |     |                                                   |     |                                                   |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|---------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     | <img src="../../drivers/idec.files/image002.gif" width="146" /> |
|     | <img src="../../drivers/idec.files/image003.gif" width="129" /> |     |                                                   |     |                                                   |
|     |                                                   |     | <img src="../../drivers/idec.files/image004.gif" width="280" /> |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |

Il connettore dell'HMI è DB9F, quello del PLC MicroSmart serie FC4A/FC5A è MD8M.

**2. Impostazioni software**

Selezionare IDEC nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC MicroSmart serie FC4A/FC5A/FC6A.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Macro Smart FC4A | Macro Smart FC4A/ Macro Smart FC5A |
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

Macro Smart FC4A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | ddd | 0~255 | Bit: ingresso digitale esterno, sola lettura |
| **Q** | ddd | 0~255 | Bit: uscita digitale esterna |
| **M** | dddd | 0~1023 | Bit: relè interno |
| **SM** | ddd | 0~215 | Bit: registro interno |
| **R** | ddd | 0~255 | Word: registro a scorrimento |
| **D** | ddd | 0~1299 | Word: registro dati |
| **TV** | ddd | 0~127 | Word: valore corrente del timer |
| **CV** | ddd | 0~127 | Word: valore corrente del contatore |

Macro Smart FC5A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | ddd | 0~255 | Bit: ingresso digitale esterno, sola lettura |
| **Q** | ddd | 0~255 | Bit: uscita digitale esterna |
| **M** | dddd | 0~2047 | Bit: relè interno |
| **SM** | ddd | 0~215 | Bit: registro interno |
| **R** | ddd | 0~255 | Word: registro a scorrimento |
| **D** | ddd | 0~42000 | Word: registro dati |
| **TV** | ddd | 0~255 | Word: valore corrente del timer |
| **CV** | ddd | 0~255 | Word: valore corrente del contatore |

Macro Smart FC6A Tcp/IP

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Nome registro</strong></p></td>
<td><p><strong>Formato indirizzo</strong></p></td>
<td><p><strong>Intervallo</strong></p></td>
<td><p><strong>Note</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>I</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit: ingresso digitale esterno, sola lettura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Q</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit: uscita digitale esterna</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>Dddo</p></td>
<td><p>0~7997</p>
<p>8000~8317</p>
<p>10000~17497</p></td>
<td><p>Bit: relè interno</p></td>
</tr>
<tr class="odd">
<td><p><strong>R</strong></p></td>
<td><p>Ddd</p></td>
<td><p>0~255</p></td>
<td><p>Bit: registro a scorrimento</p></td>
</tr>
<tr class="even">
<td><p><strong>T</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Bit: stato del timer (sola lettura)</p></td>
</tr>
<tr class="odd">
<td><p><strong>C</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~511</p></td>
<td><p>Bit: stato del contatore (sola lettura)</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>ddddd</p></td>
<td><p>0~8499</p>
<p>10000~55999</p></td>
<td><p>Word: registro</p></td>
</tr>
<tr class="odd">
<td><p><strong>TV</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Word: valore corrente del timer (sola lettura)</p></td>
</tr>
<tr class="even">
<td><p><strong>CV</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Word: valore corrente del contatore (sola lettura)</p></td>
</tr>
<tr class="odd">
<td><p><strong>TS</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Word: valore impostato del timer (sola lettura)</p></td>
</tr>
<tr class="even">
<td><p><strong>CS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Word: valore impostato del contatore (sola lettura)</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/idec.files/image009.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/idec.files/image010.gif" width="595" />
