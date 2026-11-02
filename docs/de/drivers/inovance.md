# Gerätetreiber Inovance

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Inovance H1u/H2u. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Inovance H1u/H2u herstellen</p>
<p><strong>1.  Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232 (serielle Schnittstelle, Protokoll RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HM-HMI COM1/COM2</p></td>
<td colspan="2"><p>Serie Inovance H1u/H2u</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>7</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>1</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>2</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/inovance.files/image002.gif" width="281" /><img src="../../drivers/inovance.files/image003.gif" width="130" /><img src="../../drivers/inovance.files/image004.gif" width="145" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie Inovance H1u/H2u DB9M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Inovance Technology Corp.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Inovance H1u/H2u.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | H1u/H2u                     | H1u/H2u                                      |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 7                           | 7/8                                          |
| **Parität**              | EVEN                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 0                           | 0~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation** | Ja                         |
| **Online-Simulation**  | Ja                         |
| **Erweiterter Modus**       | Nein                          |

**3. Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                  |
| **X**             | oooo               | 0~377           | Bit: Eingangsspule, nur lesen                   |
| **Y**             | oooo               | 0~377           | Bit: Ausgangsspule                             |
| **M**             | dddd               | 0~7999          | Bit: Zwischenrelais (Merker)                      |
| **SM**            | dddd               | 8000~8999       | Bit: Sonderzwischenrelais              |
| **S**             | dddd               | 0~999           | Bit: Statusbit                              |
| **T**             | dddd               | 0~256           | Bit: Timerstatus                         |
| **C**             | dddd               | 0~256           | Bit: Zählerstatus                       |
| **D**             | dddd               | 0~7999          | Wort: Register                               |
| **SD**            | dddd               | 8000~8999       | Wort: Sonderregister                       |
| **TV**            | dddd               | 0~255           | Wort: Istwert des Timers                 |
| **CV**            | dddd               | 0~199           | Wort: Istwert des Zählers               |
| **CV32**          | dddd               | 200~255         | Doppelwort: Istwert des 32-Bit-Zählers |

<img src="../../drivers/inovance.files/image005.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/inovance.files/image006.gif" width="595" />
