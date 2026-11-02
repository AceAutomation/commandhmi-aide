# Driver per dispositivi Xinje

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Xinje (Thinget) serie XC/XCM/XD. La comunicazione seriale avviene tra la porta seriale del touch screen e quella del PLC Thinget serie XC/XCM/XD. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Thinget serie XC/XCM/XD.</p></td>
</tr>
<tr class="even">
<td><p>Come collegare un PLC Thinget serie XC/XCM/XD</p>
<p><strong>1.  Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Touch screen serie HMI COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Thinget serie XC/XCM/XD</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
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
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/xinje.files/image006.gif" width="130" /><img src="../../drivers/xinje.files/image007.gif" width="280" /><img src="../../drivers/xinje.files/image008.gif" width="146" /></p></td>
</tr>
</tbody>
</table>

Il connettore dell'HMI è DB9F, quello del PLC Thinget serie XC/XCM/XD è MD8M.

**2. Impostazioni software**

Selezionare Xinje Electronic nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Thinget serie XC/XCM/XD.

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parametro** | **Valore predefinito** | **Valori ammessi** |
| **Tipo di PLC** | Thinget XC Series | Thinget XC/XCM/XD Series |
| **Tipo di porta di comunicazione** | RS232 | RS232/RS422/RS485 |
| **Velocità (baud)** | 19200 | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Modalità estesa** | Sì |

**3. Registri utilizzabili e intervalli di indirizzi**

Thinget serie XC/XCM

|                   |                    |                 |                                    |
|-------------------|--------------------|-----------------|------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | dddd | da 0 a 1037 | Bit: ingresso |
| **Y** | dddd | da 0 a 1037 | Bit: uscita |
| **M** | dddd | da 0 a 8767 | Bit: relè interno |
| **S** | dddd | da 0 a 1023 | Bit: passo di processo |
| **T** | ddd | da 0 a 639 | Bit: stato del timer |
| **C** | ddd | da 0 a 639 | Bit: stato del contatore |
| **D** | dddd | da 0 a 9023 | Word: registro dati |
| **TD** | ddd | da 0 a 639 | Word: valore corrente del timer |
| **CD** | ddd | da 0 a 639 | Word: valore corrente del contatore |
| **FD** | dddd | da 0 a 9023 | Word: registro FlashROM |
| **ED** | ddddd | da 0 a 16383 | Word: registro interno esteso |

Thinget serie XD2

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Nome registro</strong></p></td>
<td><p><strong>Formato indirizzo</strong></p></td>
<td><p><strong>Intervallo</strong></p></td>
<td><p><strong>Note</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>X</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Ingresso</p></td>
</tr>
<tr class="odd">
<td><p><strong>Y</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Uscita</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Relè interno</p></td>
</tr>
<tr class="odd">
<td><p><strong>HM</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~959</p></td>
<td><p>Relè interno</p></td>
</tr>
<tr class="even">
<td><p><strong>SM</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Relè interno speciale</p></td>
</tr>
<tr class="odd">
<td><p><strong>S</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Passo di processo</p></td>
</tr>
<tr class="even">
<td><p><strong>HS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~127</p></td>
<td><p>Passo di processo</p></td>
</tr>
<tr class="odd">
<td><p><strong>T</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Timer</p></td>
</tr>
<tr class="even">
<td><p><strong>TD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Valore corrente del timer</p></td>
</tr>
<tr class="odd">
<td><p><strong>HT</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Timer</p></td>
</tr>
<tr class="even">
<td><p><strong>ET</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Timer di precisione</p></td>
</tr>
<tr class="odd">
<td><p><strong>ETD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~31</p></td>
<td><p>Registro interno esteso</p></td>
</tr>
<tr class="even">
<td><p><strong>C</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Contatore</p></td>
</tr>
<tr class="odd">
<td><p><strong>CD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Valore corrente del contatore</p></td>
</tr>
<tr class="even">
<td><p><strong>HC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Contatore</p></td>
</tr>
<tr class="odd">
<td><p><strong> HSC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Contatore veloce</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Registro dati</p></td>
</tr>
<tr class="odd">
<td><p><strong>HD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~999</p></td>
<td><p>Registro dati</p></td>
</tr>
<tr class="even">
<td><p><strong>SD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Registro dati speciale</p></td>
</tr>
<tr class="odd">
<td><p><strong>HSD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~499</p></td>
<td><p>Registro dati speciale</p></td>
</tr>
<tr class="even">
<td><p><strong>FD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~4095</p></td>
<td><p>Registro FlashROM</p></td>
</tr>
<tr class="odd">
<td><p><strong>SFD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1999</p></td>
<td><p>Registro FlashROM</p></td>
</tr>
<tr class="even">
<td><p><strong>FS</strong></p></td>
<td><p>dd</p></td>
<td><p>0~47</p></td>
<td><p>Registro di sicurezza speciale</p></td>
</tr>
<tr class="odd">
<td><p><strong>SEM</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Bobina del comando WAIT<br />
dei blocchi funzione sequenziali</p></td>
</tr>
</tbody>
</table>

Thinget serie XD3

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | ooooo | 0~20077 | Ingressi (X10000~X11177: moduli di espansione; X20000~X20277: modulo BD di espansione) |
| **Y** | ooooo | 0~20077 | Uscite (Y10000~Y11177: moduli di espansione; Y20000~Y20277: modulo BD di espansione) |
| **M** | dddd | 0~7999 | Relè interno |
| **HM** | ddd | 0~959 | Relè interno |
| **SM** | dddd | 0~2047 | Relè interno speciale |
| **S** | dddd | 0~1023 | Passo di processo |
| **HS** | ddd | 0~127 | Passo di processo |
| **T** | ddd | 0~575 | Timer |
| **TD** | ddd | 0~575 | Valore corrente del timer |
| **HT** | dd | 0~95 | Timer |
| **ET** | dd | 0~31 | Timer di precisione |
| **ETD** | ddd | 0~31 | Registro interno esteso |
| **C** | ddd | 0~575 | Contatore |
| **CD** | ddd | 0~575 | Valore corrente del contatore |
| **HC** | dd | 0~95 | Contatore |
| **HSC** | dd | 0~31 | Contatore veloce |
| **D** | dddd | 0~7999 | Registro dati |
| **HD** | ddd | 0~999 | Registro dati |
| **SD** | dddd | 0~2047 | Registro dati speciale |
| **HSD** | ddd | 0~499 | Registro dati speciale |
| **FD** | dddd | 0~4095 | Registro FlashROM |
| **SFD** | dddd | 0~1999 | Registro FlashROM |
| **FS** | dd | 0~47 | Registro di sicurezza speciale |
| **ID** | ddddd | 0~20099 | Unità base (ID10000~ID10999: moduli di espansione; ID20000~20099: modulo BD di espansione) |
| **QD** | ddddd | 0~20099 | Unità base (QD10000~QD10999: moduli di espansione; QD20000~QD20099: modulo BD di espansione) |
| **SEM** | dd | 0~31 | Bobina del comando WAIT dei blocchi funzione sequenziali |

Thinget serie XD5/XDM

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **X** | ooooo | 0~20077 | Ingressi (X10000~X11177: moduli di espansione; X20000~X20277: modulo BD di espansione) |
| **Y** | ooooo | 0~20077 | Uscite (Y10000~Y11177: moduli di espansione; Y20000~Y20277: modulo BD di espansione) |
| **M** | ddddd | 0~20479 | Relè interno |
| **HM** | ddddd | 0~11999 | Relè interno |
| **SM** | dddd | 0~4095 | Relè interno speciale |
| **S** | dddd | 0~7999 | Passo di processo |
| **HS** | ddd | 0~999 | Passo di processo |
| **T** | dddd | 0~4095 | Timer |
| **TD** | ddd | 0~575 | Valore corrente del timer |
| **HT** | dddd | 0~1023 | Timer |
| **ET** | dd | 0~39 | Timer di precisione |
| **ETD** | ddd | 0~39 | Registro interno esteso |
| **C** | dddd | 0~4095 | Contatore |
| **CD** | ddd | 0~4095 | Valore corrente del contatore |
| **HC** | dddd | 0~1023 | Contatore |
| **HSC** | dd | 0~36 | Contatore veloce |
| **D** | ddddd | 0~20479 | Registro dati |
| **HD** | ddddd | 0~6143 | Registro dati |
| **SD** | dddd | 0~4095 | Registro dati speciale |
| **HSD** | dddd | 0~1023 | Registro dati speciale |
| **FD** | dddd | 0~4095 | Registro FlashROM |
| **SFD** | dddd | 0~5999 | Registro FlashROM |
| **FS** | dd | 0~47 | Registro di sicurezza speciale |
| **ID** | ddddd | 0~20099 | Unità base (ID10000~ID10999: moduli di espansione; ID20000~20099: modulo BD di espansione) |
| **QD** | ddddd | 0~20099 | Unità base (QD10000~QD10999: moduli di espansione; QD20000~QD20099: modulo BD di espansione) |
| **SEM** | ddd | 0~127 | Bobina del comando WAIT dei blocchi funzione sequenziali |

<img src="../../drivers/xinje.files/image009.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

Word nelle note: il registro può essere usato solo come word;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/xinje.files/image011.gif" width="595" />
