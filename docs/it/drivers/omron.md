# Driver per dispositivi Omron

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC SYSMAC serie C/CPM/CS/CJ. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC SYSMAC serie C/CPM/CS/CJ. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC SYSMAC serie C/CPM/CS/CJ.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC SYSMAC serie C/CPM/CS/CJ</p>
<p>1.  Collegamento hardware</p>
<p>Cavo di collegamento:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>Touch screen serie HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>SYSMAC CS/CJ</strong></p></td>
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
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>9</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/omron.files/image002.gif" width="130" /><img src="../../drivers/omron.files/image003.gif" width="290" /><img src="../../drivers/omron.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Il connettore dell'HMI è DB9F, quello del PLC SYSMAC serie C/CPM/CS/CJ è DB9M.

**2. Impostazioni software**

Selezionare OMRON nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC SYSMAC serie C/CPM/CS/CJ.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | SYSMAC C/CPM Series | SYSMAC C/CPM/CS/CJ Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 9600 | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 7 | 7/8 |
| **Parità** | EVEN | EVEN/ODD/NONE |
| **Bit di stop** | 2 | 1/2 |
| **Numero di stazione PLC** | 0 | 0~255 |
| **Numero di stazione HMI** | 0 | 0~255 |

|                         |                             |
|-------------------------|-----------------------------|
| **Funzione** | **Supportata** |
| **Simulazione offline** | Sì |
| **Simulazione online** | Sì |
| **Modalità estesa** | No |

**3. Registri utilizzabili e intervalli di indirizzi**

SYSMAC serie C/CPM

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **IR_Bit** | dddd.DD | 0.0~4095.15 | Bit: relè di ingresso/uscita |
| **HR_Bit** | dddd.DD | 0.0~4095.15 | Bit: relè a ritenuta |
| **LR_Bit** | dddd.DD | 0.0~4095.15 | Bit: relè di collegamento |
| **AR_Bit** | dddd.DD | 0.0~4095.15 | Bit: relè di memoria ausiliaria |
| **T** | ddd | 0~255 | Bit: stato del timer |
| **C** | ddd | 0~255 | Bit: stato del contatore |
| **IR** | dddd | 0~4095 | Word: relè di ingresso/uscita |
| **HR** | dddd | 0~4095 | Word: relè a ritenuta |
| **LR** | dddd | 0~4095 | Word: relè di collegamento |
| **AR** | dddd | 0~4095 | Word: relè di memoria ausiliaria |
| **TC** | ddd | 0~255 | <span id="OLE_LINK234"></span>Word: valore del timer |
| **DM** | dddd | 0~9999 | Word: <span id="OLE_LINK235"></span><span id="OLE_LINK236"></span><span id="OLE_LINK237"></span>area dati comune |

SYSMAC serie CS/CJ

|                   |                    |                 |                                                                                         |
|-------------------|--------------------|-----------------|-----------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **CIO_Bit** | dddd.DD | 0.0~3189.15 | Bit: <span id="OLE_LINK238"></span>area I/O (CIO) |
| **W_Bit** | dddd.DD | 0.0~6143.15 | Bit:<span id="OLE_LINK239"></span> area di lavoro |
| **H_Bit** | dddd.DD | 0.0~511.15 | Bit:<span id="OLE_LINK240"></span> area a ritenuta |
| **A_Bit** | dddd.DD | 0.0~959.15 | Bit: <span id="OLE_LINK241"></span>area ausiliaria, sola lettura: 7.168 bit: A00000～A447.15 |
| **D_Bit** | dddd.DD | 0.0~32767.15 | Bit:<span id="OLE_LINK242"></span> area dati comune |
| **T** | dddd | 0~4095 | Bit: stato del timer |
| **C** | dddd | 0~4095 | Bit: stato del contatore |
| **CIO** | dddd | 0~3189 | Word: area I/O (CIO) |
| **W** | dddd | 0~6143 | Word: area di lavoro |
| **H** | dddd | 0~511 | Word: area a ritenuta |
| **A** | dddd | 0~959 | Word: area ausiliaria, sola lettura: 448 word: A000～A447 |
| **D** | dddd | 0~32767 | Word: area dati comune |
| **TV** | dddd | 0~4095 | Word: valore corrente del timer |
| **CV** | dddd | 0~4095 | Word: valore corrente del contatore |

CP1L Tcp/Ip       / Fins-udp

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **CIO_Bit** | dddd.DD | 0.0~3189.15 | Bit: area I/O (CIO) |
| **W_Bit** | dddd.DD | 0.0~6143.15 | Bit: area di lavoro |
| **H_Bit** | dddd.DD | 0.0~511.15 | Bit: area a ritenuta |
| **A_Bit** | dddd.DD | 0.0~959.15 | Bit: area ausiliaria, sola lettura: 7.168 bit: A00000～A447.15 |
| **D_Bit** | dddd.DD | 0.0~32767.15 | Bit: area dati comune |
| **T** | dddd | 0~4095 | Bit: stato del timer |
| **C** | dddd | 0~4095 | Bit: stato del contatore |
| **CIO** | dddd | 0~3189 | Word: area I/O (CIO) |
| **W** | dddd | 0~6143 | Word: area di lavoro |
| **H** | dddd | 0~511 | Word: area a ritenuta |
| **A** | dddd | 0~959 | Word: area ausiliaria, sola lettura: 448 word: A000～A447 |
| **D** | dddd | 0~32767 | Word: area dati comune |
| **TV** | dddd | 0~4095 | Word: valore corrente del timer |
| **CV** | dddd | 0~4095 | Word: valore corrente del contatore |

<img src="../../drivers/omron.files/image010.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

DD indica i 16 bit; cifre da 0 a 15;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/omron.files/image011.gif" width="595" />

 Specifiche di collegamento CP1L TCP/IP: impostazione

-&gt; Ethernet integrata -&gt; impostare IP e numero di porta. Nota:

si consiglia la comunicazione FINS-UDP, che permette di collegare più touch screen allo stesso PLC; prima della comunicazione normale è necessaria una fase di handshake che richiede un certo tempo

Istruzioni di collegamento FINS-UDP:

Impostazioni -&gt; Ethernet integrata -&gt; impostare IP e numero di porta

Il numero di nodo della configurazione FINS-UDP deve corrispondere al numero di nodo impostato nelle opzioni Ethernet di Omron

<img src="../../drivers/omron.files/image008.jpg" width="500" alt="image009.jpg" />
