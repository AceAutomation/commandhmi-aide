# Driver per dispositivi Koyo

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Koyo serie SN. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Koyo serie SN. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Koyo serie SN.</p></td>
</tr>
<tr class="even">
<td><p> Come collegare un PLC Koyo serie SN</p>
<p><strong>1.</strong> <strong>Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232 (porta seriale, protocollo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI HM COM1/COM2</p></td>
<td colspan="2"><p>Koyo serie SN</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>4</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/koyo.files/image006.gif" width="278" /><img src="../../drivers/koyo.files/image007.gif" width="130" /><img src="../../drivers/koyo.files/image008.gif" width="90" />

Il connettore dell'HMI è DB9F, quello del PLC Koyo serie SN è un jack modulare a 6 pin.

**2. Impostazioni software**

Selezionare Koyo Electronics nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Koyo serie SN.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Koyo SN Series | Koyo SN Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 | 7/8 |
| **Parità** | ODD | EVEN/ODD/NONE |
| **Bit di stop** | 1 | 1/2 |
| **Numero di stazione PLC** | 1 | 0~255 |
| **Numero di stazione HMI** | 0 | 0~255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | Sì |

**3. Koyo serie SN**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | ooo | 0~377 | Bit: relè di ingresso, sola lettura |
| **O** | ooo | 0~377 | Bit: relè di uscita |
| **M** | oooo | 0~1177 | Bit: relè ausiliario |
| **SP** | ooo | 0~777 | Bit: relè ausiliario speciale |
| **S** | ooo | 0~177 | Bit: relè di passo |
| **T** | ooo | 0~177 | Bit: timer |
| **C** | ooo | 0~177 | Bit: contatore |
| **R** | ooooo | 0~13777 | Word: registro dati |
| **TR** | ooooo | 0~13777 | Word: valore corrente del timer |
| **CR** | ooooo | 0~13777 | Word: valore corrente del contatore |
| **SR** | ooooo | 0~13777 | Word: registro dati speciale |

**4. Koyo serie DIRECT**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | ooo | 0~3777 | Bit: relè di ingresso, sola lettura |
| **Y** | ooo | 0~3777 | Bit: relè di uscita |
| **GX** | oooo | 0~7777 | Bit: relè di ingresso, sola lettura |
| **GY** | oooo | 0~7777 | Bit: relè di uscita |
| **C** | oooo | 0~7777 | Bit: contatore |
| **S** | oooo | 0~1777 | Bit: relè di passo |
| **SP** | oooo | 0~1777 | Bit: relè ausiliario speciale |
| **CT** | ooo | 0~777 | Bit: contatore |
| **T** | ooo | 0~777 | Bit: timer |
| **V** | oooo | 0~77777 | Word: registro dati speciale |
| **TV** | ooo | 0~777 | Word: valore corrente del timer |
| **CV** | ooo | 0~777 | Word: valore corrente del contatore |

KV-Nano

|                |              |              |                                            |
|----------------|--------------|--------------|--------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **R** | ddddd | 0~59915 | Bit: relè |
| **B** | DDDD | 0~1FFF | Bit: relè di collegamento |
| **MR** | ddddd | 0~59915 | Bit: relè ausiliario interno |
| **LR** | ddddd | 0~19915 | Bit: relè a ritenuta |
| **CR** | dddd | 0~8915 | Bit: relè di controllo |
| **VB** | DDDD | 0~1FFF | Bit: relè di lavoro |
| **T** | ddd | 0~511 | Bit: timer |
| **C** | ddd | 0~255 | Bit: contatore |
| **DM** | dddd | 0~32767 | Word: memoria dati |
| **W** | DDDD | 0~3FFF | Word: registro di collegamento |
| **TM** | dddd | 0~511 | Word: memoria dati temporanea |
| **Z** | dddd | 1~12 | Word: registro indice |
| **TC** | dddd | 0~511 | Double word: timer (valore corrente) |
| **TS** | dddd | 0~511 | Double word: timer (valore impostato) |
| **CC** | ddd | 0~255 | Double word: contatore (valore corrente) |
| **CS** | ddd | 0~255 | Double word: contatore (valore impostato) |
| **CTH** | d | 0~3 | Double word: contatore veloce |
| **CTC** | d | 0~7 | Double word: comparatore del contatore veloce |
| **CM** | dddd | 0~8999 | Word: memoria di controllo |
| **VM** | dddd | 0~9999 | Word: memoria di lavoro |

<img src="../../drivers/koyo.files/image009.gif" width="595" />

Nota:

o indica il sistema ottale, cifre da 0 a 7;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/koyo.files/image010.gif" width="595" />
