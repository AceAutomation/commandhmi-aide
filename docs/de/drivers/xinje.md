# Gerätetreiber Xinje

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Thinget XC/XCM/XD. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Thinget XC/XCM/XD herstellen</p>
<p><strong>1.  Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Touchscreen COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Thinget XC/XCM/XD</strong></p></td>
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
<p><img src="../../drivers/xinje.files/image006.gif" width="130" /><img src="../../drivers/xinje.files/image007.gif" width="280" /><img src="../../drivers/xinje.files/image008.gif" width="146" /></p></td>
</tr>
</tbody>
</table>

Der Anschluss des HMI ist DB9F, der der SPS der Serie Thinget XC/XCM/XD MD8M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Xinje Electronic.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Thinget XC/XCM/XD.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie Thinget XC           | Serie Thinget XC/XCM/XD                     |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Erweiterter Modus**       | Ja                         |

**3. Verwendbare Register und Adressbereiche**

Serie Thinget XC/XCM

|                   |                    |                 |                                    |
|-------------------|--------------------|-----------------|------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                        |
| **X**             | dddd               | 0 bis 1037       | Bit: Eingangsspule                    |
| **Y**             | dddd               | 0 bis 1037       | Bit: Ausgangsspule                   |
| **M**             | dddd               | 0 bis 8767       | Bit: Interne Spule                 |
| **S**             | dddd               | 0 bis 1023       | Bit: Ablaufschritt                       |
| **T**             | ddd                | 0 bis 639        | Bit: Timerstatus                   |
| **C**             | ddd                | 0 bis 639        | Bit: Zählerstatus                 |
| **D**             | dddd               | 0 bis 9023       | Wort: Datenregister                |
| **TD**            | ddd                | 0 bis 639        | Wort: Istwert des Timers   |
| **CD**            | ddd                | 0 bis 639        | Wort: Istwert des Zählers |
| **FD**            | dddd               | 0 bis 9023       | Wort: FlashROM-Register            |
| **ED**            | ddddd              | 0 bis 16383      | Wort: Erweitertes internes Register   |

Serie Thinget XD2

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
<td><p><strong>X</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Eingangsspule</p></td>
</tr>
<tr class="odd">
<td><p><strong>Y</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Ausgangsspule</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Internes Relais (Merker)</p></td>
</tr>
<tr class="odd">
<td><p><strong>HM</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~959</p></td>
<td><p>Internes Relais (Merker)</p></td>
</tr>
<tr class="even">
<td><p><strong>SM</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Internes Sonderrelais</p></td>
</tr>
<tr class="odd">
<td><p><strong>S</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Ablaufschritt</p></td>
</tr>
<tr class="even">
<td><p><strong>HS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~127</p></td>
<td><p>Ablaufschritt</p></td>
</tr>
<tr class="odd">
<td><p><strong>T</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Timer</p></td>
</tr>
<tr class="even">
<td><p><strong>TD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Istwert des Timers</p></td>
</tr>
<tr class="odd">
<td><p><strong>HT</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Timer</p></td>
</tr>
<tr class="even">
<td><p><strong>ET</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Präzisionstimer</p></td>
</tr>
<tr class="odd">
<td><p><strong>ETD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~31</p></td>
<td><p>Erweitertes internes Register</p></td>
</tr>
<tr class="even">
<td><p><strong>C</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Zähler</p></td>
</tr>
<tr class="odd">
<td><p><strong>CD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Istwert des Zählers</p></td>
</tr>
<tr class="even">
<td><p><strong>HC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Zähler</p></td>
</tr>
<tr class="odd">
<td><p><strong> HSC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Schneller Zähler</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Datenregister</p></td>
</tr>
<tr class="odd">
<td><p><strong>HD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~999</p></td>
<td><p>Datenregister</p></td>
</tr>
<tr class="even">
<td><p><strong>SD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Sonderdatenregister</p></td>
</tr>
<tr class="odd">
<td><p><strong>HSD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~499</p></td>
<td><p>Sonderdatenregister</p></td>
</tr>
<tr class="even">
<td><p><strong>FD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~4095</p></td>
<td><p>FlashROM-Register</p></td>
</tr>
<tr class="odd">
<td><p><strong>SFD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1999</p></td>
<td><p>FlashROM-Register</p></td>
</tr>
<tr class="even">
<td><p><strong>FS</strong></p></td>
<td><p>dd</p></td>
<td><p>0~47</p></td>
<td><p>Spezielles Sicherungsregister</p></td>
</tr>
<tr class="odd">
<td><p><strong>SEM</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Ablauffunktionsblock WAIT<br />
Befehlsspule</p></td>
</tr>
</tbody>
</table>

Serie Thinget XD3

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                                                      |
| **X**             | ooooo              | 0~20077         | Eingangsspule (X10000~X11177 gehören zum Erweiterungsmodul) (X20000~X20277 zum BD-Erweiterungsmodul)              |
| **Y**             | ooooo              | 0~20077         | Ausgangsspule (Y10000~Y11177 gehören zum Erweiterungsmodul) (Y20000~Y20277 zum BD-Erweiterungsmodul) |
| **M**             | dddd               | 0~7999          | Internes Relais (Merker)                                                                                                   |
| **HM**            | ddd                | 0~959           | Internes Relais (Merker)                                                                                                   |
| **SM**            | dddd               | 0~2047          | Internes Sonderrelais                                                                                           |
| **S**             | dddd               | 0~1023          | Ablaufschritt                                                                                            |
| **HS**            | ddd                | 0~127           | Ablaufschritt                                                                                            |
| **T**             | ddd                | 0~575           | Timer                                                                                                            |
| **TD**            | ddd                | 0~575           | Istwert des Timers                                                                                              |
| **HT**            | dd                 | 0~95            | Timer                                                                                                            |
| **ET**            | dd                 | 0~31            | Präzisionstimer                                                                                                  |
| **ETD**           | ddd                | 0~31            | Erweitertes internes Register                                                                                       |
| **C**             | ddd                | 0~575           | Zähler                                                                                                          |
| **CD**            | ddd                | 0~575           | Istwert des Zählers                                                                                            |
| **HC**            | dd                 | 0~95            | Zähler                                                                                                          |
| **HSC**          | dd                 | 0~31            | Schneller Zähler                                                                                               |
| **D**             | dddd               | 0~7999          | Datenregister                                                                                                    |
| **HD**            | ddd                | 0~999           | Datenregister                                                                                                    |
| **SD**            | dddd               | 0~2047          | Sonderdatenregister                                                                                            |
| **HSD**           | ddd                | 0~499           | Sonderdatenregister                                                                                            |
| **FD**            | dddd               | 0~4095          | FlashROM-Register                                                                                                |
| **SFD**           | dddd               | 0~1999          | FlashROM-Register                                                                                                |
| **FS**            | dd                 | 0~47            | Spezielles Sicherungsregister                                                                                        |
| **ID**            | ddddd              | 0~20099         | Grundgerät (ID10000~ID10999 gehören zum Erweiterungsmodul) (ID20000~20099 zum BD-Erweiterungsmodul)              |
| **QD**            | ddddd              | 0~20099         | Grundgerät (QD10000~QD10999 gehören zum Erweiterungsmodul) (QD20000~QD20099 zum BD-Erweiterungsmodul)            |
| **SEM**           | dd                 | 0~31            | Ablauffunktionsblock WAIT, Befehlsspule                                                                      |

Serie Thinget XD5/XDM

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                                                      |
| **X**             | ooooo              | 0~20077         | Eingangsspule (X10000~X11177 gehören zum Erweiterungsmodul) (X20000~X20277 zum BD-Erweiterungsmodul)              |
| **Y**             | ooooo              | 0~20077         | Ausgangsspule (Y10000~Y11177 gehören zum Erweiterungsmodul) (Y20000~Y20277 zum BD-Erweiterungsmodul) |
| **M**             | ddddd              | 0~20479         | Internes Relais (Merker)                                                                                                   |
| **HM**            | ddddd              | 0~11999         | Internes Relais (Merker)                                                                                                   |
| **SM**            | dddd               | 0~4095          | Internes Sonderrelais                                                                                           |
| **S**             | dddd               | 0~7999          | Ablaufschritt                                                                                            |
| **HS**            | ddd                | 0~999           | Ablaufschritt                                                                                            |
| **T**             | dddd               | 0~4095          | Timer                                                                                                            |
| **TD**            | ddd                | 0~575           | Istwert des Timers                                                                                              |
| **HT**            | dddd               | 0~1023          | Timer                                                                                                            |
| **ET**            | dd                 | 0~39            | Präzisionstimer                                                                                                  |
| **ETD**           | ddd                | 0~39            | Erweitertes internes Register                                                                                       |
| **C**             | dddd               | 0~4095          | Zähler                                                                                                          |
| **CD**            | ddd                | 0~4095          | Istwert des Zählers                                                                                            |
| **HC**            | dddd               | 0~1023          | Zähler                                                                                                          |
| **HSC**          | dd                 | 0~36            | Schneller Zähler                                                                                               |
| **D**             | ddddd              | 0~20479         | Datenregister                                                                                                    |
| **HD**            | ddddd              | 0~6143          | Datenregister                                                                                                    |
| **SD**            | dddd               | 0~4095          | Sonderdatenregister                                                                                            |
| **HSD**           | dddd               | 0~1023          | Sonderdatenregister                                                                                            |
| **FD**            | dddd               | 0~4095          | FlashROM-Register                                                                                                |
| **SFD**           | dddd               | 0~5999          | FlashROM-Register                                                                                                |
| **FS**            | dd                 | 0~47            | Spezielles Sicherungsregister                                                                                        |
| **ID**            | ddddd              | 0~20099         | Grundgerät (ID10000~ID10999 gehören zum Erweiterungsmodul) (ID20000~20099 zum BD-Erweiterungsmodul)              |
| **QD**            | ddddd              | 0~20099         | Grundgerät (QD10000~QD10999 gehören zum Erweiterungsmodul) (QD20000~QD20099 zum BD-Erweiterungsmodul)            |
| **SEM**           | ddd                | 0~127           | Ablauffunktionsblock WAIT, Befehlsspule                                                                      |

<img src="../../drivers/xinje.files/image009.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/xinje.files/image011.gif" width="595" />
