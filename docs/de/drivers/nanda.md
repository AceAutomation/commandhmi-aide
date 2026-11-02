# Gerätetreiber Nanda

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Nanda NA-200/400. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Nanda NA-200/400 herstellen</p>
<p><strong>1.  Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Nanda NA-200/400</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>2</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/nanda.files/image002.gif" width="130" /><img src="../../drivers/nanda.files/image003.gif" width="290" /><img src="../../drivers/nanda.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Der Anschluss des HMI ist DB9F, der der SPS der Serie Nanda NA-200/400 DB9M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Nanda Auto Technology.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Nanda NA-200/400.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Nanda NA-200                | Nanda NA-200/400                             |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**              | NONE                        | EVEN/ODD/NONE                                |
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

Nanda NA-200

|                   |                    |                 |                                                                                                                               |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                                                                   |
| **I**             | ddd                | 1~128           | Bit: Digitaleingang, nur lesen |
| **Q**             | ddd                | 1~128           | Bit: Digitalausgang                                                                                                  |
| **M**             | dddd               | 1~1024          | Bit: Bitregister                                                                                                             |
| **S**             | ddd                | 1~256           | Bit: System-Bitregister                                                                                                      |
| **N**             | ddd                | 1~256           | Bit: Remanentes Bitregister (spannungsausfallsicher)                                                                                |
| **IW**            | dd                 | 1~32            | Wort: Analogeingang                                                                                                   |
| **QW**            | dd                 | 1~32            | Wort: Analogausgang                                                                                                  |
| **MW**            | dddd               | 1~1024          | Wort: Wortregister                                                                                                           |
| **SW**            | ddd                | 1~256           | Wort: System-Wortregister                                                                                                    |
| **NW**            | ddd                | 1~256           | Wort: Remanentes Wortregister (spannungsausfallsicher)                                                                              |

Nanda NA-400

|                   |                    |                 |                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                      |
| **I**             | ddd                | 1~2048          | Bit: Digitaleingang, nur lesen           |
| **Q**             | ddd                | 1~2048          | Bit: Digitalausgang                     |
| **M**             | dddd               | 1~8192          | Bit: Bitregister                                |
| **S**             | ddd                | 1~4096          | Bit: System-Bitregister                         |
| **N**             | ddd                | 1~2048          | Bit: Remanentes Bitregister (spannungsausfallsicher)   |
| **IW**            | dd                 | 1~512           | Wort: Analogeingang                      |
| **QW**            | dd                 | 1~512           | Wort: Analogausgang                     |
| **MW**            | dddd               | 1~8192          | Wort: Wortregister                              |
| **SW**            | ddd                | 1~2048          | Wort: System-Wortregister                       |
| **NW**            | ddd                | 1~2048          | Wort: Remanentes Wortregister (spannungsausfallsicher) |

<img src="../../drivers/nanda.files/image005.gif" width="596" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/nanda.files/image006.gif" width="595" />
