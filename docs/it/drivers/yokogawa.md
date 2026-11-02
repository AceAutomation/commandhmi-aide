# Driver per dispositivi Yokogawa

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Yokogawa serie FA-M3. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Yokogawa serie FA-M3. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Yokogawa serie FA-M3.

Come collegare un PLC Yokogawa serie FA-M3

**1. Collegamento hardware**

Cavo di collegamento:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

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
<td colspan="2"><p>Serie HM COM1/COM2</p></td>
<td colspan="3"><p><strong>Yokogawa serie FA-M3</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>5</strong></p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>SG</p></td>
<td rowspan="2"><p>Ponticello 4-5</p>
<p>Resistenza da 220Ω in serie</p></td>
</tr>
<tr class="odd">
<td><p><strong>6</strong></p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>SDB</p></td>
</tr>
<tr class="even">
<td><p><strong>7</strong></p></td>
<td><p>RX+</p></td>
<td><p>3</p></td>
<td><p>SDA</p></td>
<td rowspan="2"><p>Ponticello 2-3</p>
<p>Resistenza da 220Ω in serie</p></td>
</tr>
<tr class="odd">
<td><p><strong>8</strong></p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>RDB</p></td>
</tr>
<tr class="even">
<td><p><strong>9</strong></p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td colspan="2"><p>RDA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>6</p></td>
<td><p>CSA</p></td>
<td rowspan="2"><p>Ponticello 6-7</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>ERA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>8</p></td>
<td><p>CSB</p></td>
<td rowspan="2"><p>Ponticello 8-9</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>9</p></td>
<td><p>ERB</p></td>
</tr>
</tbody>
</table>

Il connettore dell'HMI è DB9F, quello del PLC Yokogawa serie FA-M3 è SIO.

**2. Impostazioni software**

Selezionare Yokogawa Electric Corp. nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Yokogawa serie FA-M3.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Yokogawa FA-M3 | Yokogawa FA-M3 |
| **Tipo di porta di comunicazione** | RS422 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | EVEN | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 1 | da 0 a 255 |
| **Numero di stazione HMI** | 0 | da 0 a 255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | No |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | ddddd | da 0 a 71664 | Bit: ingresso, non continuo, dipende dal numero di slot |
| **Y** | ddddd | da 0 a 71664 | Bit: uscita, non continua, dipende dal numero di slot |
| **M** | ddddd | da 0 a 16384 | Bit: relè speciale |
| **I** | ddddd | da 0 a 71024 | Bit: relè interno |
| **L** | ddddd | da 0 a 9984 | Bit: relè di collegamento, non continuo |
| **D** | ddddd | da 0 a 8192 | Word: registro dati |
| **B** | ddddd | da 0 a 32768 | Word: registro file |
| **V** | ddddd | da 0 a 64 | Word: uscita digitale esterna |
| **W** | ddddd | da 0 a 71024 | Word: registro di collegamento, non continuo |
| **Z** | ddddd | da 0 a 512 | Word: registro speciale |

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />
