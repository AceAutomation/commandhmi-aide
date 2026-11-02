# Geräte Invt

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der <span id="OLE_LINK121"></span>Register von SPS der Serie Invt. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Invt herstellen</p>
<p>1.  Hardwareanschluss</p>
<p>Verbindungskabel:</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p>Invt</p></td>
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
<td><p>3</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/invt.files/image005.gif" width="145" /><img src="../../drivers/invt.files/image006.gif" width="281" /><img src="../../drivers/invt.files/image007.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Der Anschluss des HMI ist DB9F, der der SPS der Serie Invt MD8M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Invt Network Power.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Invt.

Standard-Verbindungsparameter des Touchscreens

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **PLC type**                | IVC1,IVC1L,IVCIS,IVC2L,IVC3 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                  |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 7                           | 7/8                                          |
| **Parität**              | EVEN                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 1                           | 0~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation** | Ja                         |
| **Online-Simulation**  | Ja                         |
| **Erweiterter Modus**       | Ja                         |

**3. (IVC1,IVC1L,IVCIS,IVC2L,IVC3,IVC3 TCP) Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                             |
|-------------------|--------------------|-----------------|---------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                 |
| X                 | ooo                | 0~377           | Bit: Eingang, nur lesen      |
| Y                 | ooo                | 0~377           | Bit: Ausgang                |
| M                 | dddd               | 0~7999          | Bit: Internes Relais (Merker)                         |
| SM                | ddd                | 0~255           | Bit: Internes Sonderrelais                 |
| S                 | ddd                | 0~999           | Bit: Schrittrelais                         |
| T                 | ddd                | 0~255           | Bit: Timerstatus                           |
| C                 | ddd                | 0~255           | Bit: Zählerstatus                         |
| D                 | dddd               | 0~7999          | Wort: Datenspeicher                |
| SD                | ddd                | 0~255           | Wort: Sonder-Datenspeicher        |
| TV                | ddd                | 0~255           | Wort: Istwert des Timers                |
| CV                | ddd                | 0~255           | Wort: Istwert des Zählers              |
| Z                 | dd                 | 0~15            | Wort: Register für indizierte Adressierung           |
| D_Double          | dddd               | 0~7999          | Doppelwort: Datenspeicher         |
| CV_Double         | ddd                | 0~255           | Doppelwort: Istwert des Zählers       |
| SD_Double         | ddd                | 0~255           | Doppelwort: Sonder-Datenspeicher |
| R                 | ddd                | 0~32767         | Wort: 16-Bit-Register                       |
| RD                | ddd                | 32766           | Doppelwort: 32-Bit-R-Register              |
|                   |                    |                 |                                             |
| D_Bit             | dddd.dd            | 0.0~7999.15     | Bit:D-Bitregister                        |
| SD_Bit            | ddd.dd             | 0.0~255.15      | Bit:SD-Bitregister                       |
| Z_Bit             | dd.dd              | 0.0~15.15       | Bit:Z-Bitregister                        |
| R_Bit             | dddd.dd            | 0.0~32767.15    | Bit:R-Bitregister                        |

AX70 RTU/AX70 TCP

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                |
| **IX**            | ddd.o              | 0.0~511.7       | Bit：Bitdarstellung des I-Bereichs (nur lesen)                 |
| **QX**            | ddd.o              | 0.0~511.7       | Bit：Bitdarstellung des Q-Bereichs                             |
| **MX**            | ddd.o              | 0.0~7566.7      | Bit：Bitdarstellung des M-Bereichs                             |
| **IB**            | ddd                | 0~511           | Byte：Bytedarstellung des I-Bereichs (nur lesen)              |
| **QB**            | ddd                | 0~511           | Byte：Bytedarstellung des Q-Bereichs                          |
| **MB**            | dddd               | 0~7566          | Byte：Bytedarstellung des M-Bereichs                          |
| **IW**            | ddd                | 0~511           | Wort：Wortdarstellung des I-Bereichs (nur lesen)              |
| **QW**            | ddd                | 0~511           | Wort：Wortdarstellung des Q-Bereichs                           |
| **MW**            | dddd               | 0~3783          | Wort：Wortdarstellung des M-Bereichs                           |
| **ID**            | ddd                | 0~127           | Doppelwort：Doppelwortdarstellung des I-Bereichs (nur lesen) |
| **QD**            | ddd                | 0~127           | Doppelwort：Doppelwortdarstellung des Q-Bereichs             |
| **MD**            | dddd               | 0~1891          | Doppelwort：Doppelwortdarstellung des M-Bereichs             |

<img src="../../drivers/invt.files/image004.gif" width="600" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/invt.files/image004.gif" width="600" />
