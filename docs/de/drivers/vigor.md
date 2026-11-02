# Gerätetreiber Vigor

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Vigor V/VH/VB/M. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Vigor V/VH/VB/M herstellen</p>
<p><strong>1.  Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Vigor V/VH/VB/M</strong></p></td>
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
<td><p>4</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/vigor.files/image002.gif" width="63" /><img src="../../drivers/vigor.files/image003.gif" width="318" /><img src="../../drivers/vigor.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Der Anschluss des HMI ist DB9F, der der SPS der Serie Vigor V/VH/VB/M DB9M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Vigor Electric Corp.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Vigor V/VH/VB/M.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie V/VH/VB/M            | Serie V/VH/VB/M                             |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 7                           | 7/8                                          |
| **Parität**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 0                           | 0 bis 255                                     |
| **HMI-Stationsnummer**      | 0                           | 0 bis 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation**  | Ja                         |
| **Online-Simulation**   | Ja                         |
| **Erweiterter Modus**       | Nein                          |

**3. Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                       |
|-------------------|--------------------|-----------------|---------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                           |
| **X**             | ooo                | 0 bis 777        | Bit: Eingangskontakt                    |
| **Y**             | ooo                | 0 bis 777        | Bit: Ausgangskontakt                   |
| **M**             | dddd               | 0 bis 8999       | Bit: Internes Relais (Merker)                   |
| **SM**            | dddd               | 9000 bis 9255    | Bit: Internes Sonderrelais           |
| **S**             | dddd               | 0 bis 999        | Bit: Schrittrelais                   |
| **T**             | ddd                | 0 bis 255        | Bit: Timerstatus                      |
| **C**             | ddd                | 0 bis 255        | Bit: Zählerstatus                    |
| **D**             | dddd               | 0 bis 8999       | Wort: Datenregister                   |
| **SD**            | dddd               | 9000 bis 9255    | Wort: Sonderdatenregister           |
| **TV**            | ddd                | 0 bis 255        | Wort: Istwert des Timers      |
| **CV**            | ddd                | 0 bis 199        | Wort: Istwert des Zählers    |
| **CV32**          | ddd                | 200 bis 255      | Wort: Istwert des 32-Bit-Zählers |

<img src="../../drivers/vigor.files/image005.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein;

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/vigor.files/image005.gif" width="595" />
