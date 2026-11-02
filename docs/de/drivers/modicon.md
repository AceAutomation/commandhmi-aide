# Gerätetreiber Modicon

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Modicon NEZA/TWIDO/M218. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Modicon NEZA/TWIDO/M218 herstellen</p>
<p><strong>1.  Hardwareanschluss</strong></p>
<p><span id="OLE_LINK19"></span><span id="OLE_LINK20"></span>Verbindungskabel:</p>
<p>RS<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>485</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><span id="OLE_LINK60"></span><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Modicon NEZA/TWIDO/M218</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modicon.files/image002.gif" width="281" /><img src="../../drivers/modicon.files/image003.gif" width="130" /><img src="../../drivers/modicon.files/image004.gif" width="145" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie Modicon NEZA/TWIDO/M218 MD8M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Modicon Corp.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Modicon NEZA/TWIDO/M218.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie NEZA                 | Serie NEZA/TWIDO/M218                       |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**              | ODD                         | EVEN/ODD/NONE                                |
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

Serie NEZA

|                   |                    |                 |                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                           |
| **%MW**           | ddddd              | 0~65535         | Wort: Wort-Datenregister |

Serie TWIDO

|                   |                    |                 |                                                                                    |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                        |
| **%M**            | ddddd              | 0~65535         | Bit: Bit-Datenregister   |
| **%MW**           | ddddd              | 0~65535         | Wort: Wort-Datenregister |

Serie M218

|                   |                    |                 |                          |
|-------------------|--------------------|-----------------|--------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**              |
| **%MX**           | ddddd.o            | 0~131071.7      | Bit: Bit-Datenregister   |
| **%MW**           | ddddd              | 0~65535         | Wort: Wort-Datenregister |

<img src="../../drivers/modicon.files/image005.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/modicon.files/image006.gif" width="595" />
