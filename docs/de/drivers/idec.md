# Gerätetreiber IDEC

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Macro Smart FC4A/FC5A/FC6A. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

**Verbindung mit der Serie Macro Smart FC4A/FC5A herstellen**

1\. Hardwareanschluss

Verbindungskabel:

RS232 (serielle Schnittstelle, Protokoll RS232)

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
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="3"><p><strong>Macro Smart FC4A/FC5A</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td colspan="2"><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td colspan="2"><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>6</p></td>
<td><p>GND</p></td>
<td rowspan="2"><p>6-7</p>
<p>Kurzschluss</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>

|     |                                                   |     |                                                   |     |                                                   |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|---------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     | <img src="../../drivers/idec.files/image002.gif" width="146" /> |
|     | <img src="../../drivers/idec.files/image003.gif" width="129" /> |     |                                                   |     |                                                   |
|     |                                                   |     | <img src="../../drivers/idec.files/image004.gif" width="280" /> |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |

Der Anschluss des HMI ist DB9F, der der SPS der Serie Macro Smart FC4A/FC5A MD8M.

**2.Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Allen-Bradley.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Macro Smart FC4A/FC5A/FC6A.

Standard-Verbindungsparameter des HM-HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Macro Smart FC4A            | Macro Smart FC4A/ Macro Smart FC5A           |
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

**3.Verwendbare Register und Adressbereiche**

Macro Smart FC4A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                    |
| **I**             | ddd                | 0~255           | Bit: externer Schalteingang, nur lesen |
| **Q**             | ddd                | 0~255           | Bit: externer Schaltausgang           |
| **M**             | dddd               | 0~1023          | Bit: Internes Relais (Merker)                            |
| **SM**            | ddd                | 0~215           | Bit: Internes Register                         |
| **R**             | ddd                | 0~255           | Wort: Schieberegister                           |
| **D**             | ddd                | 0~1299          | Wort: Datenregister                            |
| **TV**            | ddd                | 0~127           | Wort: Istwert des Timers                   |
| **CV**            | ddd                | 0~127           | Wort: Istwert des Zählers                 |

Macro Smart FC5A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                    |
| **I**             | ddd                | 0~255           | Bit: externer Schalteingang, nur lesen |
| **Q**             | ddd                | 0~255           | Bit: externer Schaltausgang           |
| **M**             | dddd               | 0~2047          | Bit: Internes Relais (Merker)                            |
| **SM**            | ddd                | 0~215           | Bit: Internes Register                         |
| **R**             | ddd                | 0~255           | Wort: Schieberegister                           |
| **D**             | ddd                | 0~42000         | Wort: Datenregister                            |
| **TV**            | ddd                | 0~255           | Wort: Istwert des Timers                   |
| **CV**            | ddd                | 0~255           | Wort: Istwert des Zählers                 |

Macro Smart FC6A Tcp/IP

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Registername</strong></p></td>
<td><p><strong>Adressformat</strong></p></td>
<td><p><strong>Eingabebereich</strong></p></td>
<td><p><strong>Bemerkungen</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>I</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit: externer Schalteingang, nur lesen</p></td>
</tr>
<tr class="odd">
<td><p><strong>Q</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit：Bit: externer Schaltausgang</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>Dddo</p></td>
<td><p>0~7997</p>
<p>8000~8317</p>
<p>10000~17497</p></td>
<td><p>Bit：internes Relais (Merker)</p></td>
</tr>
<tr class="odd">
<td><p><strong>R</strong></p></td>
<td><p>Ddd</p></td>
<td><p>0~255</p></td>
<td><p>Bit：Schieberegister</p></td>
</tr>
<tr class="even">
<td><p><strong>T</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Bit: Timerstatus (nur lesen)</p></td>
</tr>
<tr class="odd">
<td><p><strong>C</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~511</p></td>
<td><p>Bit: Zählerstatus (nur lesen)</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>ddddd</p></td>
<td><p>0~8499</p>
<p>10000~55999</p></td>
<td><p>Wort: Register</p></td>
</tr>
<tr class="odd">
<td><p><strong>TV</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Wort: Istwert des Timers (nur lesen)</p></td>
</tr>
<tr class="even">
<td><p><strong>CV</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Wort: Istwert des Zählers (nur lesen)</p></td>
</tr>
<tr class="odd">
<td><p><strong>TS</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>• Wort: Sollwert des Timers (nur lesen)</p></td>
</tr>
<tr class="even">
<td><p><strong>CS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Wort: Sollwert des Zählers (nur lesen)</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/idec.files/image009.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/idec.files/image010.gif" width="595" />
