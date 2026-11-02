# Gerätetreiber Delta

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der <span id="OLE_LINK42"></span><span id="OLE_LINK43"></span>Register von SPS der Serie Delta DVP. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Delta DVP herstellen</p>
<p><strong>1.  Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK53"></span><span id="OLE_LINK2"></span> (serielle Schnittstelle, Protokoll RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI der HM-Serie COM1/COM2</p></td>
<td colspan="2"><p>Serie Delta DVP</p></td>
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
<p><img src="../../drivers/delta.files/image008.gif" width="281" /><img src="../../drivers/delta.files/image009.gif" width="146" /><img src="../../drivers/delta.files/image010.gif" width="130" />  </p>
<p><span id="OLE_LINK54"></span>Der Anschluss des HMI der HM-Serie ist DB9F, der der Delta-DVP-SPS MD8M.</p>
<p>RS485 (serielle Schnittstelle, Protokoll RS485)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI der HM-Serie COM1/COM2</p></td>
<td><p>Serie Delta DVP</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/delta.files/image011.gif" width="130" /><img src="../../drivers/delta.files/image012.gif" width="156" /></p>
<p>Der Anschluss der HM-Serie ist DB9F, der der Delta-DVP-SPS eine Zweidrahtklemme.</p></td>
</tr>
</tbody>
</table>

**2. Softwareeinstellungen**

ü Wählen Sie unter „Geräteservice“ Delta Corporation.

ü Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

ü Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

ü Zu den Einstellungen der SPS siehe die technischen Unterlagen der Delta-SPS der Serie DVP.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Delta DVP Series            | Delta DVP Series                             |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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

|                   |                    |                 |                                               |
|-------------------|--------------------|-----------------|-----------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                   |
| **X**             | ooo                | 0~377           | Bit: Eingang, nur lesen        |
| **Y**             | ooo                | 0~377           | Bit: Ausgang                  |
| **M**             | dddd               | 0~4095          | Bit: Hilfsrelais (Merker)                          |
| **S**             | dddd               | 0~1023          | Bit: Schrittrelais                           |
| **T**             | ddd                | 0~255           | Bit: Timerstatus                             |
| **C**             | ddd                | 0~255           | Bit: Zählerstatus                           |
| **D**             | dddd               | 0~9999          | Wort: Datenspeicher                  |
| **TV**            | ddd                | 0~255           | Wort: Istwert des Timers                  |
| **CV**            | ddd                | 0~199           | Wort: Istwert des Zählers                |
| **CV32**          | ddd                | 200~255         | Doppelwort: Istwert des 32-Bit-Zählers |

<img src="../../drivers/delta.files/image013.gif" width="595" />

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Hinweis:</p>
<p>d: dezimal, Eingabebereich 0-9;</p>
<p>o: oktal, Eingabebereich 0-7;</p>
<p>Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;</p>
<p>Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;</p>
<p>Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;</p>
<p>Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;</p>
<p>Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.</p>
<p>Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.</p></td>
</tr>
</tbody>
</table>
