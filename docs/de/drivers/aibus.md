# Gerätetreiber AIBUS

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände von AIBUS-Geräten über das AIBUS-Protokoll. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der des AIBUS-Geräts hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen des AIBUS-Geräts sorgfältig.

**1.  Hardwareanschluss**

Verbindungskabel:

RS232 (serielle Schnittstelle, Protokoll RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **AIBUS-Gerät**  |     |
| 2                           | RX  | Benutzerdefinierter Pin | TX  |
| 3                           | TX  | Benutzerdefinierter Pin | RX  |
| 5                           | GND | Benutzerdefinierter Pin | GND |

<img src="../../drivers/aibus.files/image002.gif" width="157" /><img src="../../drivers/aibus.files/image003.gif" width="130" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Der Anschluss des Touchscreens ist eine 9-polige Sub-D-Buchse. Die Anschlussbelegung des AIBUS-Geräts hängt vom jeweiligen Gerät ab.</p>
<p><strong>RS422 (serielle Schnittstelle, Protokoll RS422)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>AIBUS-Gerät</strong></p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table>
<table>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><img src="../../drivers/aibus.files/image004.gif" width="280" /></td>
</tr>
</tbody>
</table>
 &#10;<br />
&#10;<p>Der Anschluss des Touchscreens ist eine 9-polige Sub-D-Buchse. Die Anschlussbelegung des AIBUS-Geräts hängt vom jeweiligen Gerät ab.</p>
<p><strong>RS485 (serielle Schnittstelle, Protokoll RS485)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Touchscreen COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>AIBUS-Gerät</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>D-</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>D+</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p>Der Anschluss des Touchscreens ist eine 9-polige Sub-D-Buchse. Die Anschlussbelegung des AIBUS-Geräts hängt vom jeweiligen Gerät ab.</p></td>
</tr>
</tbody>
</table>

**2. Softwareeinstellungen**

ü Wählen Sie unter „Geräteservice“ das AIBUS-Protokoll.

ü Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

ü Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit dem AIBUS-Gerät übereinstimmen.

ü Zu den Einstellungen des AIBUS-Geräts siehe dessen technische Unterlagen.

Standard-Verbindungsparameter des Touchscreens

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | AIBUS Protocol              | AIBUS Protocol                               |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**              | NONE                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 1                           | 1~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation** | Ja                         |
| **Online-Simulation**  | Ja                         |
| **Erweiterter Modus**       | Ja                         |

**3. Verwendbare Register und Adressbereiche**

|                   |                    |                 |                      |
|-------------------|--------------------|-----------------|----------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**          |
| **Parameter**     | ddd                | 0~255           | Wort: Parameter |
| **PV**            | d                  | 0               | Wort: Istwert   |
| **SV**            | d                  | 0               | Wort: Sollwert      |
| **MV**            | d                  | 0               | Wort: Stellwert    |
| **Status**        | d                  | 0               | Wort: Zustandswert    |

<img src="../../drivers/aibus.files/image005.gif" width="595" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Hinweis: </p>
<p>• ·d: dezimal, Eingabebereich 0-9;</p>
<p>• ·„Wort“ in den Bemerkungen: Das Register ist nur als Wort verwendbar;</p>
<p>• Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.</p>
<p>Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/aibus.files/image006.gif" width="595" />
