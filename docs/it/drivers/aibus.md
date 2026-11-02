# Driver per dispositivi AIBUS

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei dispositivi AIBUS tramite il protocollo AIBUS. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del dispositivo AIBUS. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del dispositivo AIBUS.

**1.  Collegamento hardware**

Cavo di collegamento:

RS232 (porta seriale, protocollo RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Dispositivo AIBUS** |     |
| 2 | RX | Pin definiti dall'utente | TX |
| 3 | TX | Pin definiti dall'utente | RX |
| 5 | GND | Pin definiti dall'utente | GND |

<img src="../../drivers/aibus.files/image002.gif" width="157" /><img src="../../drivers/aibus.files/image003.gif" width="130" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>La porta del touch screen serie HMI è un connettore trapezoidale femmina a 9 pin. La piedinatura del dispositivo AIBUS dipende dal dispositivo specifico.</p>
<p><strong>RS422 (porta seriale, protocollo RS422)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Dispositivo AIBUS</strong></p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table>
<table>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><img src="../../drivers/aibus.files/image004.gif" width="280" /></td>
</tr>
</tbody>
</table>
 &#10;<br />
&#10;<p>La porta del touch screen serie HMI è un connettore trapezoidale femmina a 9 pin. La piedinatura del dispositivo AIBUS dipende dal dispositivo specifico.</p>
<p><strong>RS485 (porta seriale, protocollo RS485)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Touch screen serie HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Dispositivo AIBUS</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>D-</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>D+</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p>La porta del touch screen serie HMI è un connettore trapezoidale femmina a 9 pin. La piedinatura del dispositivo AIBUS dipende dal dispositivo specifico.</p></td>
</tr>
</tbody>
</table>

**2. Impostazioni software**

ü Selezionare AIBUS Protocol nel servizio del dispositivo collegato.

ü Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

ü Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del dispositivo AIBUS.

ü Per le impostazioni del dispositivo AIBUS, consultare la relativa documentazione tecnica.

Parametri di collegamento predefiniti del touch screen serie HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | AIBUS Protocol | AIBUS Protocol |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | NONE | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 1 | 1~255 |
| **Numero di stazione HMI** | 0 | 0~255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | Sì |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                      |
|-------------------|--------------------|-----------------|----------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **Parameter** | ddd | 0~255 | Word: parametro |
| **PV** | d | 0 | Word: valore di processo |
| **SV** | d | 0 | Word: valore impostato |
| **MV** | d | 0 | Word: valore manipolato |
| **Status** | d | 0 | Word: valore di stato |

<img src="../../drivers/aibus.files/image005.gif" width="595" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Nota: </p>
<p>• d indica il sistema decimale, cifre da 0 a 9;</p>
<p>• "Word" nelle note indica che il registro può essere usato solo come word;</p>
<p>• I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.</p>
<p>Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/aibus.files/image006.gif" width="595" />
