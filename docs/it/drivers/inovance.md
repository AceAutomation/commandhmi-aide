# Driver per dispositivi Inovance

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Inovance serie H1u/H2u. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del PLC Inovance serie H1u/H2u. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Inovance serie H1u/H2u.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Inovance serie H1u/H2u</p>
<p><strong>1.  Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232 (porta seriale, protocollo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI HM COM1/COM2</p></td>
<td colspan="2"><p>Inovance serie H1u/H2u</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>7</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>1</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>2</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/inovance.files/image002.gif" width="281" /><img src="../../drivers/inovance.files/image003.gif" width="130" /><img src="../../drivers/inovance.files/image004.gif" width="145" />

Il connettore dell'HMI è DB9F, quello del PLC Inovance serie H1u/H2u è DB9M.

**2. Impostazioni software**

Selezionare Inovance Technology Corp. nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Inovance serie H1u/H2u.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | H1u/H2u | H1u/H2u |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 7 | 7/8 |
| **Parità** | EVEN | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 0 | 0~255 |
| **Numero di stazione HMI** | 0 | 0~255 |

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
| **X** | oooo | 0~377 | Bit: ingresso, sola lettura |
| **Y** | oooo | 0~377 | Bit: uscita |
| **M** | dddd | 0~7999 | Bit: relè interno |
| **SM** | dddd | 8000~8999 | Bit: relè interno speciale |
| **S** | dddd | 0~999 | Bit: bit di stato |
| **T** | dddd | 0~256 | Bit: stato del timer |
| **C** | dddd | 0~256 | Bit: stato del contatore |
| **D** | dddd | 0~7999 | Word: registro |
| **SD** | dddd | 8000~8999 | Word: registro speciale |
| **TV** | dddd | 0~255 | Word: valore corrente del timer |
| **CV** | dddd | 0~199 | Word: valore corrente del contatore |
| **CV32** | dddd | 200~255 | Double word: valore corrente del contatore a 32 bit |

<img src="../../drivers/inovance.files/image005.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/inovance.files/image006.gif" width="595" />
