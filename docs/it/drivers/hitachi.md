# Driver per dispositivi Hitachi

Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Hitachi serie E/EH. La comunicazione seriale avviene tra la porta seriale dell'HMI e quella del PLC Hitachi serie E/EH. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Hitachi serie E/EH.

**1. Collegamento hardware**

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
<td colspan="3"><p><strong>Hitachi serie E/EH</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td colspan="2"><p>SD</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>6</p></td>
<td colspan="2"><p>RD</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>1</p></td>
<td colspan="2"><p>SG</p></td>
</tr>
<tr class="odd">
<td colspan="2" rowspan="2"></td>
<td><p>4</p></td>
<td><p>PHL</p></td>
<td rowspan="2"><p>4-7</p>
<p>Ponticello</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>DR</p></td>
</tr>
</tbody>
</table>

|     |                                                      |     |                                                      |     |                                                     |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|-----------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     | <img src="../../drivers/hitachi.files/image002.gif" width="91" /> |
|     | <img src="../../drivers/hitachi.files/image003.gif" width="130" /> |     |                                                      |     |                                                     |
|     |                                                      |     | <img src="../../drivers/hitachi.files/image004.gif" width="278" /> |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |

Il connettore dell'HMI serie HM è DB9F, quello del dispositivo è RJ45.

**2. Impostazioni software**

Selezionare Hitachi Industrial nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Hitachi serie E/EH.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Hitachi E/EH Series | Hitachi E/EH Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 19200 | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Modalità estesa** | Sì |

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                                                    |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | hhhh | 0~ffff | Bit: ingresso digitale esterno, sola lettura |
| **Y** | hhhh | 0~ffff | Bit: <span id="OLE_LINK247"></span>uscita digitale esterna |
| **M** | hhhh | 0~ffff | Bit: relè interno |
| **R** | hhhh | 0~ffff | Bit: registro interno |
| **T** | hhhh | 0~ffff | Bit: stato del timer |
| **L** | hhhh | 0~ffff | Bit: relè di collegamento |
| **WX** | hhhh | 0~ffff | Word: ingressi digitali esterni |
| **WY** | hhhh | 0~ffff | Word: uscite digitali esterne |
| **WM** | hhhh | 0~ffff | Word: relè interni |
| **WR** | hhhh | 0~ffff | Word: registro interno |
| **WL** | hhhh | 0~ffff | Word: relè di collegamento |
| **TC** | hhhh | 0~ffff | Word: valore corrente di timer/contatore |

<img src="../../drivers/hitachi.files/image005.gif" width="595" />

Nota:

h indica il sistema esadecimale, cifre da 0 a 9 e da a a f;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/hitachi.files/image006.gif" width="595" />
