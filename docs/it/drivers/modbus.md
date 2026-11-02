# Driver per dispositivi Modbus

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei <span id="OLE_LINK37"></span><span id="OLE_LINK38"></span>dispositivi MODBUS. La comunicazione seriale avviene tra la porta seriale del touch screen serie HMI e quella del dispositivo MODBUS. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del dispositivo MODBUS.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC MODBUS</p>
<p><strong>1.</strong> <strong>Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232<span id="OLE_LINK24"></span><span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK62"></span><span id="OLE_LINK63"></span><span id="OLE_LINK64"></span><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Dispositivo Modbus</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>Pin definiti dall'utente</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modbus.files/image002.gif" width="157" /><img src="../../drivers/modbus.files/image003.gif" width="130" />

Il connettore dell'HMI è DB9F. La piedinatura del dispositivo Modbus dipende dal dispositivo specifico.

**RS422**

|                                                                                                                    |     |                   |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-------------------|-----|
| <span id="OLE_LINK72"></span><span id="OLE_LINK73"></span><span id="OLE_LINK74"></span>**HMI serie HM COM1/COM2** |     | **Dispositivo Modbus** |     |
| 6 | RX- | Pin definiti dall'utente | TX- |
| 7 | RX+ | Pin definiti dall'utente | TX+ |
| 8 | TX- | Pin definiti dall'utente | RX- |
| 9 | TX+ | Pin definiti dall'utente | RX+ |

<img src="../../drivers/modbus.files/image004.gif" width="157" /><img src="../../drivers/modbus.files/image005.gif" width="130" />

Il connettore dell'HMI è DB9F. La piedinatura del dispositivo Modbus dipende dal dispositivo specifico.

**RS485**

|                                                                                       |     |                   |     |
|---------------------------------------------------------------------------------------|-----|-------------------|-----|
| <span id="OLE_LINK78"></span><span id="OLE_LINK79"></span>**HMI serie HM COM1/COM2** |     | **Dispositivo Modbus** |     |
| 8 | D- | Pin definiti dall'utente | B |
| 9 | D+ | Pin definiti dall'utente | A |

<img src="../../drivers/modbus.files/image006.gif" width="157" /><img src="../../drivers/modbus.files/image007.gif" width="130" />

Il connettore dell'HMI è un connettore trapezoidale femmina a 9 pin. La piedinatura del dispositivo Modbus dipende dal dispositivo specifico.

**TCP/IP (collegamento diretto RJ45)**

|                                                                                                                    |      |                   |      |
|--------------------------------------------------------------------------------------------------------------------|------|-------------------|------|
| <span id="OLE_LINK82"></span><span id="OLE_LINK83"></span><span id="OLE_LINK84"></span>**HMI serie HM COM1/COM2** |      | **Dispositivo Modbus** |      |
| 1                                                                                                                  | TX+  | 3                 | RX+  |
| 2                                                                                                                  | TX-  | 6                 | RX-  |
| 3                                                                                                                  | RX+  | 1                 | TX+  |
| 4                                                                                                                  | BD4+ | 4                 | BD4+ |
| 5                                                                                                                  | BD4- | 5                 | BD4- |
| 6                                                                                                                  | RX-  | 2                 | TX-  |
| 7                                                                                                                  | BD3+ | 7                 | BD3+ |
| 8                                                                                                                  | BD3- | 8                 | BD3- |

|     |                                                    |     |                                                     |     |                                                    |
|-----|----------------------------------------------------|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                     |     |                                                    |
|     | <img src="../../drivers/modbus.files/image008.gif" width="95" /> |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     | <img src="../../drivers/modbus.files/image009.gif" width="95" /> |
|     |                                                    |     | <img src="../../drivers/modbus.files/image010.gif" width="267" /> |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |

<span id="OLE_LINK68"></span><span id="OLE_LINK69"></span><span id="OLE_LINK70"></span>

Il connettore dell'HMI è RJ45, quello del dispositivo Modbus è RJ45.

**TCP/IP (collegamento RJ45 tramite router)**

|                       |      |               |      |
|-----------------------|------|---------------|------|
| **HMI HM COM1/COM2** |      | Dispositivo Modbus |      |
| 1                     | TX+  | 3             | RX+  |
| 2                     | TX-  | 6             | RX-  |
| 3                     | RX+  | 1             | TX+  |
| 4                     | BD4+ | 4             | BD4+ |
| 5                     | BD4- | 5             | BD4- |
| 6                     | RX-  | 2             | TX-  |
| 7                     | BD3+ | 7             | BD3+ |
| 8                     | BD3- | 8             | BD3- |

<img src="../../drivers/modbus.files/image011.gif" width="95" />

|     |                                                     |     |                                                    |
|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                     |     |                                                    |
|     |                                                     |     | <img src="../../drivers/modbus.files/image012.gif" width="95" /> |
|     | <img src="../../drivers/modbus.files/image013.gif" width="267" /> |     |                                                    |
|     |                                                     |     |                                                    |

Il connettore dell'HMI è RJ45, quello del dispositivo Modbus è RJ45.

**2. Impostazioni software**

Selezionare Modbus nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del dispositivo Modbus.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | RTU Master | RTU/RTU_S/ASCII/ASCII_S Master |
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

<img src="../../drivers/modbus.files/image014.gif" width="595" />

Nota: con RTU_S e ASCII_S il codice funzione usato per la scrittura dei dati è 0x10 (indipendentemente dalla lunghezza dei dati scritti);

·Se il numero di stazione PLC è 0, il sistema è in modalità broadcast.

**3. Registri utilizzabili e intervalli di indirizzi**

|                   |                    |                 |                                                                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| 0x | ddddd | 0~65535 | Bit: bobina |
| 1x | ddddd | 0~65536 | Bit: ingresso discreto, sola lettura |
| 3x_Bit | ddddd.DD | 0.00~65535.15 | Bit: <span id="OLE_LINK100"></span>bit di un registro di ingresso a 16 bit, sola lettura |
| 4x_Bit | ddddd.DD | 0.00~65535.15 | Bit: bit di un registro di uscita (holding) a 16 bit |
| 3x | ddddd | 0~65535 | Word: registro di ingresso a 16 bit, sola lettura |
| 4x | ddddd | 0~65535 | Word: registro di uscita (holding) a 16 bit |
| 3x_D | ddddd | 0~65535 | Double word: registro di ingresso, con inversione dei 16 bit alti e bassi della double word 3x, sola lettura |
| 4x_D | ddddd | 0~65535 | Double word: registro di uscita, con inversione dei 16 bit alti e bassi della double word 4x |

Modbus Slave

|                       |                             |                 |                                                                |
|-----------------------|-----------------------------|-----------------|----------------------------------------------------------------|
| **Registro interno** | **Codici funzione supportati** | **Intervallo** | **Note** |
| LB | 01/02/05/15 | 0~59999 | Bit: lettura e scrittura degli indirizzi interni LB del touch screen |
| LW | 03/04/06/16 | 0~59999 | Word: lettura e scrittura degli indirizzi interni LW del touch screen |

<img src="../../drivers/modbus.files/image015.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

DD indica i 16 bit, cifre da 0 a 15;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/modbus.files/image016.gif" width="595" />
