# Gerätetreiber Emerson

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der <span id="OLE_LINK120"></span><span id="OLE_LINK121"></span>Register von SPS der Serie Emerson EC. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Emerson EC herstellen</p>
<p>1.  Hardwareanschluss</p>
<p>Verbindungskabel:</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Emerson EC</strong></p></td>
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
<p><img src="../../drivers/emerson.files/image002.gif" width="146" /><img src="../../drivers/emerson.files/image003.gif" width="281" /><img src="../../drivers/emerson.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Der Anschluss des HMI ist DB9F, der der SPS der Serie Emerson EC MD8M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Emerson Network Power.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Emerson EC.

Standard-Verbindungsparameter des Touchscreens

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | EC Series (RTU)             | EC Series (RTU)                              |
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

**3. Verwendbare Register und Adressbereiche**

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
| CV_Double         | ddd                | 200~255         | Doppelwort: Istwert des Zählers       |
| SD_Double         | ddd                | 0~255           | Doppelwort: Sonder-Datenspeicher |

<img src="../../drivers/emerson.files/image005.gif" width="600" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/emerson.files/image006.gif" width="600" />
