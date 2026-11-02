# Gerätetreiber Techwayson

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie TaiLing DX. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie TaiLing DX herstellen</p>
<p><strong>1.  Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232 <span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>(serielle Schnittstelle, Protokoll RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie TaiLing DX</strong></p></td>
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
<p><img src="../../drivers/techwayson.files/image002.gif" width="130" /><img src="../../drivers/techwayson.files/image003.gif" width="290" /><img src="../../drivers/techwayson.files/image004.gif" width="129" /></p></td>
</tr>
</tbody>
</table>

Der Anschluss des HMI ist DB9F, der der SPS der Serie TaiLing DX MD8M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ TaiLing Electric.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie TaiLing DX.

Standard-Verbindungsparameter des HM-HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie Techwayson V80       | Serie Techwayson V80                        |
| **Schnittstellentyp** | RS232                       | RS232                                        |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 1                           | 0~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation**  | Ja                         |
| **Online-Simulation**   | Ja                         |
| **Erweiterter Modus**       | Ja                         |

**3. Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                  |
| **X**             | oooo               | 0 bis 377        | Bit: Eingangsspule, nur lesen                   |
| **Y**             | oooo               | 0 bis 377        | Bit: Ausgangsspule                             |
| **M**             | dddd               | 0 bis 7999       | Bit: Zwischenrelais (Merker)                      |
| **SM**            | dddd               | 8000 bis 8999    | Bit: Sonderzwischenrelais              |
| **S**             | dddd               | 0 bis 999        | Bit: Statusbit                               |
| **T**             | dddd               | 0 bis 256        | Bit: Timerstatus                             |
| **C**             | dddd               | 0 bis 256        | Bit: Zählerstatus                           |
| **D**             | dddd               | 0 bis 7999       | Wort: Register                               |
| **SD**            | dddd               | 8000 bis 8999    | Wort: Sonderregister                       |
| **TV**            | dddd               | 0 bis 255        | Wort: Istwert des Timers             |
| **CV**            | dddd               | 0 bis 199        | Wort: Istwert des Zählers           |
| **CV32**          | dddd               | 200 bis 255      | Doppelwort: Istwert des 32-Bit-Zählers |

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                            |
| **0x**            | dddd               | 1~9984          | Bit: Ausgangsspule                       |
| **1x**            | dddd               | 1~2048          | Bit: Eingangsspule, nur lesen             |
| **3x**            | dddd               | 1~512           | Wort: 16-Bit-Eingangsregister, nur lesen |
| **4x**            | dddd               | 1~9999          | Wort: 16-Bit-Halteregister          |

<img src="../../drivers/techwayson.files/image005.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/techwayson.files/image006.gif" width="595" />
