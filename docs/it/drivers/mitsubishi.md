# Driver per dispositivi Mitsubishi

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Melsec serie FXxn/Q00J/C24N. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Melsec serie FXxn/Q00J/C24N. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Melsec serie FXxn/Q00J/C24N.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Melsec serie FXxn/Q00J/Q00U/C24N</p>
<p><strong>1.  Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS422- Melsec-FXxn/FX3U/3G<span id="OLE_LINK1"></span><span id="OLE_LINK3"></span><span id="OLE_LINK2"></span> <span id="OLE_LINK24"></span><span id="OLE_LINK26"></span><span id="OLE_LINK25"></span>(porta seriale)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Melsec-FXxn</strong></p></td>
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

<img src="../../drivers/mitsubishi.files/image002.gif" width="145" /><img src="../../drivers/mitsubishi.files/image003.gif" width="280" /><img src="../../drivers/mitsubishi.files/image004.gif" width="130" />

Il connettore del touch screen serie HMI è DB9F, quello del PLC Melsec serie FXxn è MD8M.

**RS232- Melsec-Q00J/Q00U**

|                                                                                       |     |              |     |
|---------------------------------------------------------------------------------------|-----|--------------|-----|
| <span id="OLE_LINK32"></span><span id="OLE_LINK33"></span>**HMI serie HM COM1/COM2** |     | **Q00J CPU** |     |
| **2**                                                                                 | RX  | 2            | TX  |
| **3**                                                                                 | TX  | 1            | RX  |
| **5**                                                                                 | GND | 3            | GND |

<img src="../../drivers/mitsubishi.files/image005.gif" width="146" /><img src="../../drivers/mitsubishi.files/image006.gif" width="280" /><img src="../../drivers/mitsubishi.files/image007.gif" width="130" />

Il connettore del touch screen serie HMI è DB9F, quello del PLC Melsec serie FXxn è MD8M.

Nota: istruzioni di collegamento per Q00U

Q00U: ponticello tra i pin 5 e 6 del connettore a 6 pin

Nel software di programmazione MITSUBISHI: Parameters &gt; PLC parameters -- &gt; Serial communication settings

Abilitare la comunicazione seriale, selezionare la velocità 115200, abilitare il controllo (checksum) e la scrittura in RUN

Usare il cavo di comunicazione MITSUBISHI, collegato direttamente all'HMI

**RS232 - modulo Melsec-QC24N**

|                             |     |              |     |
|-----------------------------|-----|--------------|-----|
| **HMI serie HM COM1/COM2** |     | **Q00J CPU** |     |
| **2**                       | RX  | 3            | TX  |
| **3**                       | TX  | 2            | RX  |
| **5**                       | GND | 5            | GND |

<img src="../../drivers/mitsubishi.files/image008.gif" width="130" /><img src="../../drivers/mitsubishi.files/image009.gif" width="290" /><img src="../../drivers/mitsubishi.files/image010.gif" width="130" />

Il connettore del touch screen serie HMI è DB9F, quello del modulo Melsec QC24N è DB9M.

**2. Impostazioni software**

Selezionare MITSUBISHI nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Melsec serie FXxn/Q00J/C24N.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Melsec-FX2N | Melsec-FX/ FX2N/ FX3U/3G /Q_C24N Q00J |
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

Melsec-FXxn/FX3U/3G/ FX3U-Ethernet

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
| **D_Bit** | dddd.dd | 0.00~7999.15 | Bit: bit di un registro a 16 bit |
| **D** | dddd | 0~7999 | Word: registro |
| **SD** | dddd | 8000~8999 | Word: registro speciale |
| **TV** | dddd | 0~255 | Word: valore corrente del timer |
| **CV** | dddd | 0~199 | Word: valore corrente del contatore |
| **CV32** | dddd | 200~255 | Double word: valore corrente del contatore a 32 bit |

FX5U/FX5U-Ethernet

|                   |                    |                               |                                         |
|-------------------|--------------------|-------------------------------|-----------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | oooo | 0~1777 | Bit: ingresso, sola lettura |
| **Y** | oooo | 0~1777 | Bit: uscita |
| **M** | dddd | 0~7679 | Bit: relè interno |
| **L** | dddd | 0~7679 | Bit: relè a ritenuta |
| **F** | ddd | 0~127 | Bit: relè di allarme |
| **TS** | ddd | 0~511 | Bit: contatto del timer |
| **CS** | ddd | 0~255 | Bit: contatto del contatore |
| **S** | dddd | 0~4095 | Bit: relè di passo |
| **SM** | dddd | 0~9999 | Bit: relè speciale |
| **B** | hh | 0-ff (esadecimale) | Bit: relè di collegamento |
| **D_Bit** | dddd.dd | 0.0~7999.15 | Bit: bit di un registro a 16 bit |
| **D** | dddd | 0~7999 | Word: registro |
| **R** | ddddd | 0~32767 | Word: registro file |
| **W** | hhh | 0-1ff (esadecimale) | Word: registro di collegamento |
| **CN** | ddd | 0~255 | Word: valore corrente del contatore |
| **TN** | ddd | 0~511 | Word: valore corrente del timer |
| **SD** | ddddd | 0~11999 | Word: registro speciale |

  Melsec-Q00J/QC24N

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | hhh | 0~7ff | Bit: relè di ingresso, sola lettura |
| **Y** | hhh | 0~7ff | Bit: relè di uscita |
| **M** | dddd | 0~8191 | Bit: relè interno |
| **L** | dddd | 0~2047 | Bit: relè a ritenuta |
| **F** | dddd | 0~2047 | Bit: allarme |
| **V** | dddd | 0~2047 | Bit: relè di fronte |
| **S** | dddd | 0~2047 | Bit: relè di passo |
| **B** | hhh | 0~7ff | Bit: relè di collegamento |
| **SB** | hhh | 0~3ff | Bit: relè di collegamento speciale |
| **T** | ddd | 0~511 | Bit: stato del timer |
| **C** | ddd | 0~511 | Bit: stato del contatore |
| **D** | ddddd | 0~11135 | Word: registro dati |
| **W** | hhh | 0~7ff | Word: registro di collegamento |
| **SW** | hhh | 0~3ff | Word: registro di collegamento speciale |
| Z | d | 0~9 | Word: registro indice |
| TV | ddd | 0~511 | Word: valore corrente del timer |
| CV | ddd | 0~511 | Word: valore corrente del contatore |

Q00U

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | hhhh | 0~1fff | Bit: relè di ingresso, sola lettura |
| **Y** | hhhh | 0~1fff | Bit: relè di uscita |
| **M** | dddd | 0~8191 | Bit: relè interno |
| **L** | dddd | 0~8191 | Bit: relè a ritenuta |
| **F** | dddd | 0~2047 | Bit: relè di allarme |
| **V** | dddd | 0~2047 | Bit: relè di fronte |
| **B** | ffff | 0~1fff | Bit: relè di collegamento |
| **T** | ddd | 0~2047 | Bit: stato del timer |
| **C** | dddd | 0~1023 | Bit: stato del contatore |
| **SB** | hhh | 0~7ff | Bit: relè di collegamento speciale |
| **SM** | ddd | 0~2047 | Bit: relè speciale |
| **D_Bit** | Dddd.h | 0.0~12287.f | Bit: bit di un registro a 16 bit |
| **D** | Dddd | 0~12287 | Word: registro dati |
| **W** | Hhhh | 0~1fff | Word: registro di collegamento |
| **TV** | Dddd | 0~2047 | Word: valore corrente del timer |
| **CV** | Dddd | 0~1023 | Word: valore corrente del contatore |
| **SW** | Hhh | 0~7ff | Word: registro di collegamento speciale |
| **SD** | Dddd | 0~2047 | Word: registro speciale |
| **Z** | Dd | 0~19 | Word: registro indice |

Melsec-E71

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | hhhh | 0~1fff | Bit: relè di ingresso, sola lettura |
| **Y** | hhhh | 0~1fff | Bit: relè di uscita |
| **M** | dddd | 0~8191 | Bit: relè interno |
| **L** | dddd | 0~8191 | Bit: relè a ritenuta |
| **F** | dddd | 0~2047 | Bit: relè di allarme |
| **V** | dddd | 0~2047 | Bit: relè di fronte |
| **S** | dddd | 0~8191 | Bit: relè di passo |
| **B** | ffff | 0~1fff | Bit: relè di collegamento |
| **T** | ddd | 0~2047 | Bit: stato del timer |
| **C** | dddd | 0~1023 | Bit: stato del contatore |
| **SB** | hhh | 0~7ff | Bit: relè di collegamento speciale |
| **SM** | ddd | 0~2047 | Bit: relè speciale |
| **D_Bit** | Dddd.h | 0.0~12287.f | Bit: bit di un registro a 16 bit |
| **D** | Dddd | 0~12287 | Word: registro dati |
| **W** | Hhhh | 0~1fff | Word: registro di collegamento |
| **TV** | Dddd | 0~2047 | Word: valore corrente del timer |
| **CV** | Dddd | 0~1023 | Word: valore corrente del contatore |
| **SW** | Hhh | 0~7ff | Word: registro di collegamento speciale |
| **SD** | Dddd | 0~2047 | Word: registro speciale |
| **Z** | Dd | 0~19 | Word: registro indice |

Melsec-LCPU

|                |              |              |                                |
|----------------|--------------|--------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | hhhh | 0~1fff | Bit: relè di ingresso, sola lettura |
| **Y** | hhhh | 0~1fff | Bit: relè di uscita |
| **M** | dddd | 0~8191 | Bit: relè interno |
| **L** | dddd | 0~8191 | Bit: relè a ritenuta |
| **F** | dddd | 0~2047 | Bit: relè di allarme |
| **V** | dddd | 0~2047 | Bit: relè di fronte |
| **S** | dddd | 0~8191 | Bit: relè di passo |
| **B** | hhhh | 0~1fff | Bit: relè di collegamento |
| **SB** | hhh | 0~7ff | Bit: relè di collegamento speciale |
| **T** | dddd | 0~2047 | Bit: stato del timer |
| **C** | dddd | 0~1023 | Bit: stato del contatore |
| **D-bit** | ddddd.dd | 0~45055.15 | Bit: bit di un registro a 16 bit |
| **D** | ddddd | 0~45055 | Word: registro dati |
| **TV** | dddd | 0~2047 | Word: valore corrente del timer |
| **CV** | dddd | 0~1023 | Word: valore corrente del contatore |
| **W** | hhhh | 0~1fff | Word: registro di collegamento |
| **SW** | hhh | 0~7ff | Word: registro di collegamento speciale |
| **SD** | hhhh | 0~2047 | Word: registro speciale |
| **Z** | hh | 0~19 | Word: registro indice |

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

h indica il sistema esadecimale, cifre da 0 a 9 e da a a f;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

**4. Collegamento degli HMI serie HM ai PLC Mitsubishi FX5U**

Aprire GX Works3 - New file - Series FX5CPU - Type FX5U

<img src="../../drivers/mitsubishi.files/image012.gif" width="384" />

Navigation - Parameter - Module Parameter - Ethernet

<img src="../../drivers/mitsubishi.files/image013.gif" width="1092" />

External Device Configuration - impostazioni specifiche

<img src="../../drivers/mitsubishi.files/image014.gif" width="1024" />

Impostazioni generali nel software CommandHMI

<img src="../../drivers/mitsubishi.files/image015.gif" width="532" />

Parametri di collegamento

<img src="../../drivers/mitsubishi.files/image016.gif" width="532" />
