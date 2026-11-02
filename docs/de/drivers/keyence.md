# Gerätetreiber Keyence

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Keyence KV/VisualKV. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie Keyence KV/VisualKV herstellen</p>
<p><strong>1. Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232 (serielle Schnittstelle, Protokoll RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Keyence KV/VisualKV</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>2</p></td>
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
<td><p>3</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/keyence.files/image002.gif" width="130" /><img src="../../drivers/keyence.files/image003.gif" width="90" /><img src="../../drivers/keyence.files/image004.gif" width="278" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie Keyence KV/VisualKV eine 6-polige Modularbuchse.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Keyence Corporation.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Keyence KV/VisualKV.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | KV-1000/700 KV-L20(R)       | KV-1000/700 KV-L20(R)/ KV-/40 KV-P16         |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
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

l  KV-1000/700 KV-L20(R)

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                    |
| **R**             | dddDD              | 0~99915         | Bit: Ein-/Ausgangsrelais        |
| **MR**            | dddDD              | 0~3915          | Bit: Interner Hilfsmerker  |
| **LR**            | dddDD              | 0~3999          | Bit: Selbsthalterelais            |
| **CR**            | ddDD               | 0~3999          | Bit: Steuerrelais             |
| **T**             | dddd               | 0~65534         | Bit: Timer                     |
| **C**             | dddd               | 0~65534         | Bit: Zähler                   |
| **DM**            | ddddd              | 0~32766         | Wort: Datenspeicher             |
| **EM**            | ddddd              | 0~511           | Wort: Erweiterter Datenspeicher    |
| **FM**            | ddddd              | 0~11998         | Wort: Dateiregister            |
| **TM**            | ddd                | 0~3999          | Wort: Datenspeicher   |
| **CM**            | ddddd              | 0~3999          | Wort: Steuerspeicher          |
| **TV**            | dddd               | 0~99915         | Wort: Istwert des Timers   |
| **CV**            | dddd               | 0~3915          | Wort: Istwert des Zählers |

l  KV-10/16/24/40 KV-P16

|                   |                    |                 |                                           |
|-------------------|--------------------|-----------------|-------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                               |
| RLY               | dddDD              | 0~99915         | Bit: Relais                                |
| T                 | dddd               | 0~999           | Bit: Timer                                |
| C                 | dddd               | 0~999           | Bit: Zähler                              |
| DM                | ddddd              | 0~9999          | Wort: Datenspeicher                        |
| TM                | ddd                | 0~99            | Wort: Datenspeicher              |
| TV_c              | dddd               | 0~999           | Wort: Istwert des Timers              |
| TV_p              | dddd               | 0~999           | Wort: Vorgabewert des Timers               |
| CV_c              | dddd               | 0~999           | Wort: Istwert des Zählers            |
| CV_p              | dddd               | 0~999           | Wort: Vorgabewert des Zählers             |
| CTH               | dddd               | 0~9             | Wort: Istwert des schnellen Zählers |

l  KV-Nano

|                   |                    |                 |                                      |
|-------------------|--------------------|-----------------|--------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                          |
| **R**             | ddddd              | 0~59915         | Bit: Relais                      |
| **B**             | DDDD               | 0~1FFF          | Link-Relais                           |
| **MR**            | ddddd              | 0~59915         | Interner Hilfsmerker             |
| **LR**            | ddddd              | 0~19915         | Selbsthalterelais                       |
| **CR**            | dddd               | 0~8915          | Steuerrelais                        |
| **VB**            | DDDD               | 0~1FFF          | Arbeitsrelais                        |
| **T**             | ddd                | 0~511           | Bit: Timer                            |
| **C**             | ddd                | 0~255           | Bit: Zähler                         |
| **DM**            | dddd               | 0~32767         | Datenspeicher                          |
| **W**             | DDDD               | 0~3FFF          | Link-Register                        |
| **TM**            | dddd               | 0~511           | Datenspeicher               |
| **Z**             | dddd               | 1~12            | Indexregister                       |
| **TC**            | dddd               | 0~511           | Doppelwort: Timer (Istwert)   |
| **TS**            | dddd               | 0~511           | Doppelwort: Timer (Sollwert)       |
| **CC**            | ddd                | 0~255           | Doppelwort: Zähler (Istwert) |
| **CS**            | ddd                | 0~255           | Doppelwort: Zähler (Sollwert)     |
| **CTH**           | d                  | 0~3             | Schneller Zähler                   |
| **CTC**           | d                  | 0~7             | Doppelwort: schneller Vergleicher   |
| **CM**            | dddd               | 0~8999          | Steuerspeicher                       |
| **VM**            | dddd               | 0~9999          | Arbeitsspeicher                       |

<img src="../../drivers/keyence.files/image005.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

DD: 16 Bit, Eingabebereich 0-15;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/keyence.files/image005.gif" width="595" />
