# Driver per dispositivi Keyence

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Keyence serie KV/VisualKV. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Keyence serie KV/VisualKV. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Keyence serie KV/VisualKV.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Keyence serie KV/VisualKV</p>
<p><strong>1. Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232 (porta seriale, protocollo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Keyence serie KV/VisualKV</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>2</p></td>
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
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/keyence.files/image002.gif" width="130" /><img src="../../drivers/keyence.files/image003.gif" width="90" /><img src="../../drivers/keyence.files/image004.gif" width="278" />

Il connettore dell'HMI è DB9F, quello del PLC Keyence serie KV/VisualKV è un jack modulare a 6 pin.

**2. Impostazioni software**

Selezionare Keyence Corporation nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Keyence serie KV/VisualKV.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | KV-1000/700 KV-L20(R) | KV-1000/700 KV-L20(R)/ KV-/40 KV-P16 |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
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

l  KV-1000/700 KV-L20(R)

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **R** | dddDD | 0~99915 | Bit: relè di ingresso/uscita |
| **MR** | dddDD | 0~3915 | Bit: relè ausiliario interno |
| **LR** | dddDD | 0~3999 | Bit: relè a ritenuta |
| **CR** | ddDD | 0~3999 | Bit: relè di controllo |
| **T** | dddd | 0~65534 | Bit: timer |
| **C** | dddd | 0~65534 | Bit: contatore |
| **DM** | ddddd | 0~32766 | Word: memoria dati |
| **EM** | ddddd | 0~511 | Word: memoria dati estesa |
| **FM** | ddddd | 0~11998 | Word: registro file |
| **TM** | ddd | 0~3999 | Word: memoria dati temporanea |
| **CM** | ddddd | 0~3999 | Word: memoria di controllo |
| **TV** | dddd | 0~99915 | Word: valore corrente del timer |
| **CV** | dddd | 0~3915 | Word: valore corrente del contatore |

l  KV-10/16/24/40 KV-P16

|                   |                    |                 |                                           |
|-------------------|--------------------|-----------------|-------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| RLY | dddDD | 0~99915 | Bit: relè |
| T | dddd | 0~999 | Bit: timer |
| C | dddd | 0~999 | Bit: contatore |
| DM | ddddd | 0~9999 | Word: memoria dati |
| TM | ddd | 0~99 | Word: memoria dati temporanea |
| TV_c | dddd | 0~999 | Word: valore corrente del timer |
| TV_p | dddd | 0~999 | Word: valore preimpostato del timer |
| CV_c | dddd | 0~999 | Word: valore corrente del contatore |
| CV_p | dddd | 0~999 | Word: valore preimpostato del contatore |
| CTH | dddd | 0~9 | Word: valore corrente del contatore veloce |

l  KV-Nano

|                   |                    |                 |                                      |
|-------------------|--------------------|-----------------|--------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **R** | ddddd | 0~59915 | Bit: relè |
| **B** | DDDD | 0~1FFF | Relè di collegamento |
| **MR** | ddddd | 0~59915 | Relè ausiliario interno |
| **LR** | ddddd | 0~19915 | Relè a ritenuta |
| **CR** | dddd | 0~8915 | Relè di controllo |
| **VB** | DDDD | 0~1FFF | Relè di lavoro |
| **T** | ddd | 0~511 | Bit: timer |
| **C** | ddd | 0~255 | Bit: contatore |
| **DM** | dddd | 0~32767 | Memoria dati |
| **W** | DDDD | 0~3FFF | Registro di collegamento |
| **TM** | dddd | 0~511 | Memoria dati temporanea |
| **Z** | dddd | 1~12 | Registro indice |
| **TC** | dddd | 0~511 | Double word: timer (valore corrente) |
| **TS** | dddd | 0~511 | Double word: timer (valore impostato) |
| **CC** | ddd | 0~255 | Double word: contatore (valore corrente) |
| **CS** | ddd | 0~255 | Double word: contatore (valore impostato) |
| **CTH** | d | 0~3 | Contatore veloce |
| **CTC** | d | 0~7 | Double word: comparatore veloce |
| **CM** | dddd | 0~8999 | Memoria di controllo |
| **VM** | dddd | 0~9999 | Memoria di lavoro |

<img src="../../drivers/keyence.files/image005.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

DD indica i 16 bit, cifre da 0 a 15;

Bit nelle note: il registro può essere usato solo come bit;

Word nelle note: il registro può essere usato solo come word;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato.

<img src="../../drivers/keyence.files/image005.gif" width="595" />
