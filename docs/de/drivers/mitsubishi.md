# Gerätetreiber Mitsubishi

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Melsec FXxn/Q00J/C24N. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Melsec FXxn/Q00J/Q00U/C24N herstellen</p>
<p><strong>1.  Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS422- Melsec-FXxn/FX3U/3G<span id="OLE_LINK1"></span><span id="OLE_LINK3"></span><span id="OLE_LINK2"></span> <span id="OLE_LINK24"></span><span id="OLE_LINK26"></span><span id="OLE_LINK25"></span>(serielle Schnittstelle, Protokoll RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Melsec-FXxn</strong></p></td>
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

<img src="../../drivers/mitsubishi.files/image002.gif" width="145" /><img src="../../drivers/mitsubishi.files/image003.gif" width="280" /><img src="../../drivers/mitsubishi.files/image004.gif" width="130" />

Der Anschluss des Touchscreens ist DB9F, der der SPS der Serie Melsec FXxn MD8M.

**RS232- Melsec-Q00J/Q00U**

|                                                                                       |     |              |     |
|---------------------------------------------------------------------------------------|-----|--------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Q00J CPU** |     |
| **2**                                                                                 | RX  | 2            | TX  |
| **3**                                                                                 | TX  | 1            | RX  |
| **5**                                                                                 | GND | 3            | GND |

<img src="../../drivers/mitsubishi.files/image005.gif" width="146" /><img src="../../drivers/mitsubishi.files/image006.gif" width="280" /><img src="../../drivers/mitsubishi.files/image007.gif" width="130" />

Der Anschluss des Touchscreens ist DB9F, der der SPS der Serie Melsec FXxn MD8M.

Hinweis: Anschluss der Q00U

Q00U: Pins 5 und 6 der 6-poligen Buchse brücken

MITSUBISHI-Programmiersoftware: Parameter &gt;SPS-Parameter -- &gt; Einstellungen der seriellen Kommunikation

Serielle Kommunikation aktivieren, Baudrate 115200 wählen, Prüfsumme aktivieren und „Schreiben im RUN“ aktivieren

Mit dem MITSUBISHI-Kommunikationskabel direkt mit dem HMI verbinden

**RS232 – Modul Melsec-QC24N**

|                             |     |              |     |
|-----------------------------|-----|--------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Q00J CPU** |     |
| **2**                       | RX  | 3            | TX  |
| **3**                       | TX  | 2            | RX  |
| **5**                       | GND | 5            | GND |

<img src="../../drivers/mitsubishi.files/image008.gif" width="130" /><img src="../../drivers/mitsubishi.files/image009.gif" width="290" /><img src="../../drivers/mitsubishi.files/image010.gif" width="130" />

Der Anschluss des Touchscreens ist DB9F, der des Moduls Melsec QC24N MB9M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ MITSUBISHI.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Melsec FXxn/Q00J/C24N.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Melsec-FX2N                 | Melsec-FX/ FX2N/ FX3U/3G /Q_C24N Q00J        |
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

Melsec-FXxn/FX3U/3G/ FX3U-Ethernet

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                  |
| **X**             | oooo               | 0~377           | Bit: Eingangsspule, nur lesen                   |
| **Y**             | oooo               | 0~377           | Bit: Ausgangsspule                             |
| **M**             | dddd               | 0~7999          | Bit: Zwischenrelais (Merker)                      |
| **SM**            | dddd               | 8000~8999       | Bit: Sonderzwischenrelais              |
| **S**             | dddd               | 0~999           | Bit: Statusbit                              |
| **T**             | dddd               | 0~256           | Bit: Timerstatus                         |
| **C**             | dddd               | 0~256           | Bit: Timerstatus                         |
| **D_Bit**         | dddd.dd            | 0.00~7999.15    | Bit: Bit eines 16-Bit-Registers                  |
| **D**             | dddd               | 0~7999          | Wort: Register                               |
| **SD**            | dddd               | 8000~8999       | Wort: Sonderregister                       |
| **TV**            | dddd               | 0~255           | Wort: Istwert des Timers                 |
| **CV**            | dddd               | 0~199           | Wort: Istwert des Zählers               |
| **CV32**          | dddd               | 200~255         | Doppelwort: Istwert des 32-Bit-Zählers |

FX5U/FX5U-Ethernet

|                   |                    |                               |                                         |
|-------------------|--------------------|-------------------------------|-----------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich**               | **Bemerkungen**                             |
| **X**             | oooo               | 0~1777                        | Bit: Eingangsspule, nur lesen              |
| **Y**             | oooo               | 0~1777                        | Bit: Ausgangsspule                        |
| **M**             | dddd               | 0~7679                        | Bit: Internes Relais (Merker)                     |
| **L**             | dddd               | 0~7679                        | Bit: Selbsthalterelais                     |
| **F**             | ddd                | 0~127                         | Bit: Alarmrelais                        |
| **TS**            | ddd                | 0~511                         | Bit: Timerkontakt                      |
| **CS**            | ddd                | 0~255                         | Bit: Zählerkontakt                    |
| **S**             | dddd               | 0~4095                        | Bit: Schrittrelais                     |
| **SM**            | dddd               | 0~9999                        | Bit: Sonderrelais                      |
| **B**             | hh                 | 0-ff (hexadezimal)  | Bit: Bit: Link-Relais                     |
| **D_Bit**         | dddd.dd            | 0.0~7999.15                   | Bit: Bit eines 16-Bit-Registers             |
| **D**             | dddd               | 0~7999                        | Wort: Register                          |
| **R**             | ddddd              | 0~32767                       | Wort: Kumulierter Istwert des Timers |
| **W**             | hhh                | 0-1ff (hexadezimal) | Wort: Link-Register                     |
| **CN**            | ddd                | 0~255                         | Wort: Istwert des Registers         |
| **TN**            | ddd                | 0~511                         | Wort: Istwert des Timers            |
| **SD**            | ddddd              | 0~11999                       | Wort: Sonderregister                  |

  Melsec-Q00J/QC24N

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                    |
| **X**             | hhh                | 0~7ff           | Bit: Eingangsrelais, nur lesen    |
| **Y**             | hhh                | 0~7ff           | Bit: Ausgangsrelais              |
| **M**             | dddd               | 0~8191          | Bit: Internes Relais (Merker)            |
| **L**             | dddd               | 0~2047          | Bit: Selbsthalterelais            |
| **F**             | dddd               | 0~2047          | Bit: Alarm                     |
| **V**             | dddd               | 0~2047          | Bit: Indexrelais            |
| **S**             | dddd               | 0~2047          | Bit: Schrittrelais            |
| **B**             | hhh                | 0~7ff           | Bit: Konvertierungsrelais          |
| **SB**            | hhh                | 0~3ff           | Bit: Sonder-Link-Relais        |
| **T**             | ddd                | 0~511           | Bit: Timerstatus           |
| **C**             | ddd                | 0~511           | Bit: Zählerstatus         |
| **D**             | ddddd              | 0~11135         | Wort: Datenregister            |
| **W**             | hhh                | 0~7ff           | Wort: Konvertierungsregister      |
| **SW**            | hhh                | 0~3ff           | Wort: Sonder-Link-Register    |
| Z                 | d                  | 0~9             | Wort: Indexregister           |
| TV                | ddd                | 0~511           | Wort: Istwert des Timers   |
| CV                | ddd                | 0~511           | Wort: Istwert des Zählers |

Q00U

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                    |
| **X**             | hhhh               | 0~1fff          | Bit: Eingangsrelais, nur lesen    |
| **Y**             | hhhh               | 0~1fff          | Bit: Ausgangsrelais              |
| **M**             | dddd               | 0~8191          | Bit: Internes Relais (Merker)            |
| **L**             | dddd               | 0~8191          | Bit: Selbsthalterelais            |
| **F**             | dddd               | 0~2047          | Bit: Alarmrelais               |
| **V**             | dddd               | 0~2047          | Bit: Indexrelais            |
| **B**             | ffff               | 0~1fff          | Bit: Konvertierungsrelais          |
| **T**             | ddd                | 0~2047          | Bit: Timerstatus           |
| **C**             | dddd               | 0~1023          | Bit: Zählerstatus         |
| **SB**            | hhh                | 0~7ff           | Bit: Sonder-Link-Relais        |
| **SM**            | ddd                | 0~2047          | Bit: Sonderrelais             |
| **D_Bit**         | Dddd.h             | 0.0~12287.f     | Bit: Bit eines 16-Bit-Registers    |
| **D**             | Dddd               | 0~12287         | Wort: Datenregister            |
| **W**             | Hhhh               | 0~1fff          | Wort: Konvertierungsregister      |
| **TV**            | Dddd               | 0~2047          | Wort: Istwert des Timers   |
| **CV**            | Dddd               | 0~1023          | Wort: Istwert des Zählers |
| **SW**            | Hhh                | 0~7ff           | Wort: Sonder-Link-Register    |
| **SD**            | Dddd               | 0~2047          | Wort: Sonderregister         |
| **Z**             | Dd                 | 0~19            | Wort: Indexregister           |

Melsec-E71

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                    |
| **X**             | hhhh               | 0~1fff          | Bit: Eingangsrelais, nur lesen    |
| **Y**             | hhhh               | 0~1fff          | Bit: Ausgangsrelais              |
| **M**             | dddd               | 0~8191          | Bit: Internes Relais (Merker)            |
| **L**             | dddd               | 0~8191          | Bit: Selbsthalterelais            |
| **F**             | dddd               | 0~2047          | Bit: Alarmrelais               |
| **V**             | dddd               | 0~2047          | Bit: Indexrelais            |
| **S**             | dddd               | 0~8191          | Bit: Schrittrelais            |
| **B**             | ffff               | 0~1fff          | Bit: Konvertierungsrelais          |
| **T**             | ddd                | 0~2047          | Bit: Timerstatus           |
| **C**             | dddd               | 0~1023          | Bit: Zählerstatus         |
| **SB**            | hhh                | 0~7ff           | Bit: Sonder-Link-Relais        |
| **SM**            | ddd                | 0~2047          | Bit: Sonderrelais             |
| **D_Bit**         | Dddd.h             | 0.0~12287.f     | Bit: Bit eines 16-Bit-Registers    |
| **D**             | Dddd               | 0~12287         | Wort: Datenregister            |
| **W**             | Hhhh               | 0~1fff          | Wort: Konvertierungsregister      |
| **TV**            | Dddd               | 0~2047          | Wort: Istwert des Timers   |
| **CV**            | Dddd               | 0~1023          | Wort: Istwert des Zählers |
| **SW**            | Hhh                | 0~7ff           | Wort: Sonder-Link-Register    |
| **SD**            | Dddd               | 0~2047          | Wort: Sonderregister         |
| **Z**             | Dd                 | 0~19            | Wort: Indexregister           |

Melsec-LCPU

|                |              |              |                                |
|----------------|--------------|--------------|--------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                       |
| **X**          | hhhh         | 0~1fff       | Bit: Eingangsrelais, nur lesen    |
| **Y**          | hhhh         | 0~1fff       | Bit: Ausgangsrelais              |
| **M**          | dddd         | 0~8191       | Bit: Internes Relais (Merker)            |
| **L**          | dddd         | 0~8191       | Bit: Selbsthalterelais            |
| **F**          | dddd         | 0~2047       | Bit: Alarmrelais               |
| **V**          | dddd         | 0~2047       | Bit: Indexrelais            |
| **S**          | dddd         | 0~8191       | Bit: Schrittrelais            |
| **B**          | hhhh         | 0~1fff       | Bit: Konvertierungsrelais          |
| **SB**         | hhh          | 0~7ff        | Bit: Sonder-Link-Relais        |
| **T**          | dddd         | 0~2047       | Bit: Timerstatus           |
| **C**          | dddd         | 0~1023       | Bit: Zählerstatus         |
| **D-bit**      | ddddd.dd     | 0~45055.15   | Bit: Bit eines 16-Bit-Registers    |
| **D**          | ddddd        | 0~45055      | Wort: Datenregister            |
| **TV**         | dddd         | 0~2047       | Wort: Istwert des Timers   |
| **CV**         | dddd         | 0~1023       | Wort: Istwert des Zählers |
| **W**          | hhhh         | 0~1fff       | Wort: Konvertierungsregister      |
| **SW**         | hhh          | 0~7ff        | Wort: Sonder-Link-Register    |
| **SD**         | hhhh         | 0~2047       | Wort: Sonderregister         |
| **Z**          | hh           | 0~19         | Wort: Indexregister           |

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

h: hexadezimal, Eingabebereich 0-9, a-f;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

**4. Anbindung der HMI der HM-Serie an die SPS FX5U von Mitsubishi**

GX Works3 öffnen – Neue Datei – Serie FX5CPU – Typ FX5U

<img src="../../drivers/mitsubishi.files/image012.gif" width="384" />

Navigation – Parameter – Modulparameter – Ethernet

<img src="../../drivers/mitsubishi.files/image013.gif" width="1092" />

Verbindungsziel – Detaileinstellungen

<img src="../../drivers/mitsubishi.files/image014.gif" width="1024" />

CommandHMI-Software: Allgemein

<img src="../../drivers/mitsubishi.files/image015.gif" width="532" />

Verbindung – Parameter

<img src="../../drivers/mitsubishi.files/image016.gif" width="532" />
