# Gerätetreiber Yokogawa

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Yokogawa FA-M3. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

Verbindung mit einer SPS der Serie Yokogawa FA-M3 herstellen

**1.Hardwareanschluss**

Verbindungskabel:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

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
<td colspan="2"><p>HM-Serie COM1/COM2</p></td>
<td colspan="3"><p><strong>Serie Yokogawa FA-M3</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>5</strong></p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>SG</p></td>
<td rowspan="2"><p>4-5 gebrückt</p>
<p>220-Ω-Widerstand in Reihe</p></td>
</tr>
<tr class="odd">
<td><p><strong>6</strong></p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>SDB</p></td>
</tr>
<tr class="even">
<td><p><strong>7</strong></p></td>
<td><p>RX+</p></td>
<td><p>3</p></td>
<td><p>SDA</p></td>
<td rowspan="2"><p>2-3 gebrückt</p>
<p>220-Ω-Widerstand in Reihe</p></td>
</tr>
<tr class="odd">
<td><p><strong>8</strong></p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>RDB</p></td>
</tr>
<tr class="even">
<td><p><strong>9</strong></p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td colspan="2"><p>RDA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>6</p></td>
<td><p>CSA</p></td>
<td rowspan="2"><p>6-7 gebrückt</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>ERA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>8</p></td>
<td><p>CSB</p></td>
<td rowspan="2"><p>8-9 gebrückt</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>9</p></td>
<td><p>ERB</p></td>
</tr>
</tbody>
</table>

Der Anschluss des HMI ist DB9F, der der SPS der Serie Yokogawa FA-M3 SIO.

**2.Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Yokogawa Electric Corp.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Yokogawa FA-M3.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Yokogawa FA-M3              | Yokogawa FA-M3                               |
| **Schnittstellentyp** | RS422                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 1                           | 0 bis 255                                     |
| **HMI-Stationsnummer**      | 0                           | 0 bis 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation**  | Ja                         |
| **Online-Simulation**   | Ja                         |
| **Erweiterter Modus**       | Nein                          |

**3.Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                               |
| **X**             | ddddd              | 0 bis 71664      | Bit: Eingang, nicht fortlaufend, abhängig von der Steckplatznummer  |
| **Y**             | ddddd              | 0 bis 71664      | Bit: Ausgang, nicht fortlaufend, abhängig von der Steckplatznummer |
| **M**             | ddddd              | 0 bis 16384      | Bit: Sonderrelais                                        |
| **I**             | ddddd              | 0 bis 71024      | Bit: Internes Relais (Merker)                                       |
| **L**             | ddddd              | 0 bis 9984       | Bit: Link-Relais, nicht fortlaufend                            |
| **D**             | ddddd              | 0 bis 8192       | Wort: Datenregister                                       |
| **B**             | ddddd              | 0 bis 32768      | Wort: Dateiregister                                       |
| **V**             | ddddd              | 0 bis 64         | Wort: externer Schaltausgang                     |
| **W**             | ddddd              | 0 bis 71024      | Wort: Link-Register, nicht fortlaufend                        |
| **Z**             | ddddd              | 0 bis 512        | Wort: Sonderregister                                    |

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />
