# Driver per dispositivi Modicon

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Modicon serie NEZA/TWIDO/M218. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Modicon serie NEZA/TWIDO/M218. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Modicon serie NEZA/TWIDO/M218.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Modicon serie NEZA/TWIDO/M218</p>
<p><strong>1.  Collegamento hardware</strong></p>
<p><span id="OLE_LINK19"></span><span id="OLE_LINK20"></span>Cavo di collegamento:</p>
<p>RS<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>485</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><span id="OLE_LINK60"></span><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Modicon NEZA/TWIDO/M218</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modicon.files/image002.gif" width="281" /><img src="../../drivers/modicon.files/image003.gif" width="130" /><img src="../../drivers/modicon.files/image004.gif" width="145" />

Il connettore dell'HMI è DB9F, quello del PLC Modicon serie NEZA/TWIDO/M218 è MD8M.

**2. Impostazioni software**

Selezionare Modicon Corp. nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Modicon serie NEZA/TWIDO/M218.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | NEZA Series | NEZA/TWIDO/M218 Series |
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

**3. Registri utilizzabili e intervalli di indirizzi**

Serie NEZA

|                   |                    |                 |                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **%MW** | ddddd | 0~65535 | Word: <span id="OLE_LINK50"></span>registro dati word |

Serie TWIDO

|                   |                    |                 |                                                                                    |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **%M** | ddddd | 0~65535 | Bit: <span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>registro dati bit |
| **%MW** | ddddd | 0~65535 | Word: <span id="OLE_LINK53"></span><span id="OLE_LINK54"></span>registro dati word |

Serie M218

|                   |                    |                 |                          |
|-------------------|--------------------|-----------------|--------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **%MX** | ddddd.o | 0~131071.7 | Bit: registro dati bit |
| **%MW** | ddddd | 0~65535 | Word: registro dati word |

<img src="../../drivers/modicon.files/image005.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/modicon.files/image006.gif" width="595" />
