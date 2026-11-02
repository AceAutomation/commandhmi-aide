# Gerätetreiber Koyo

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Koyo SN. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p> Verbindung mit einer SPS der Serie Koyo SN herstellen</p>
<p><strong>1.</strong> <strong>Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232 (serielle Schnittstelle, Protokoll RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HM-HMI COM1/COM2</p></td>
<td colspan="2"><p>Serie Koyo SN</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>4</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/koyo.files/image006.gif" width="278" /><img src="../../drivers/koyo.files/image007.gif" width="130" /><img src="../../drivers/koyo.files/image008.gif" width="90" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie Koyo SN eine 6-polige Modularbuchse.

**2.Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Koyo Electronics.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Koyo SN.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie Koyo SN              | Serie Koyo SN                               |
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

**3.Serie Koyo SN**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                    |
| **I**             | ooo                | 0~377           | Bit: Eingangsrelais, nur lesen    |
| **O**             | ooo                | 0~377           | Bit: Ausgangsrelais              |
| **M**             | oooo               | 0~1177          | Bit: Hilfsrelais (Merker)           |
| **SP**            | ooo                | 0~777           | Bit: Sonderhilfsrelais   |
| **S**             | ooo                | 0~177           | Bit: Schrittrelais            |
| **T**             | ooo                | 0~177           | Bit: Timer                     |
| **C**             | ooo                | 0~177           | Bit: Zähler                   |
| **R**             | ooooo              | 0~13777         | Wort: Datenregister            |
| **TR**            | ooooo              | 0~13777         | Wort: Istwert des Timers   |
| **CR**            | ooooo              | 0~13777         | Wort: Istwert des Zählers |
| **SR**            | ooooo              | 0~13777         | Wort: Sonderdatenregister    |

**4.Serie Koyo DIRECT**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                    |
| **X**             | ooo                | 0~3777          | Bit: Eingangsrelais, nur lesen    |
| **Y**             | ooo                | 0~3777          | Bit: Ausgangsrelais              |
| **GX**            | oooo               | 0~7777          | Bit: Eingangsrelais, nur lesen    |
| **GY**            | oooo               | 0~7777          | Bit: Ausgangsrelais              |
| **C**             | oooo               | 0~7777          | Bit: Zähler                   |
| **S**             | oooo               | 0~1777          | Bit: Schrittrelais            |
| **SP**            | oooo               | 0~1777          | Bit: Sonderhilfsrelais   |
| **CT**            | ooo                | 0~777           | Bit: Zähler                   |
| **T**             | ooo                | 0~777           | Bit: Timer                     |
| **V**             | oooo               | 0~77777         | Wort: Sonderdatenregister    |
| **TV**            | ooo                | 0~777           | Wort: Istwert des Timers   |
| **CV**            | ooo                | 0~777           | Wort: Istwert des Zählers |

KV-Nano

|                |              |              |                                            |
|----------------|--------------|--------------|--------------------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                                   |
| **R**          | ddddd        | 0~59915      | Bit: Relais                            |
| **B**          | DDDD         | 0~1FFF       | Bit: Link-Relais                       |
| **MR**         | ddddd        | 0~59915      | Bit：Interner Hilfsmerker         |
| **LR**         | ddddd        | 0~19915      | Bit: Selbsthalterelais                   |
| **CR**         | dddd         | 0~8915       | Bit: Steuerrelais                    |
| **VB**         | DDDD         | 0~1FFF       | Bit: Arbeitsrelais                       |
| **T**          | ddd          | 0~511        | Bit: Timer                            |
| **C**          | ddd          | 0~255        | Bit: Zähler                          |
| **DM**         | dddd         | 0~32767      | Wort：Datenspeicher                         |
| **W**          | DDDD         | 0~3FFF       | Wort：Link-Register                        |
| **TM**         | dddd         | 0~511        | Wort：Datenspeicher               |
| **Z**          | dddd         | 1~12         | Wort：Indexregister                       |
| **TC**         | dddd         | 0~511        | Doppelwort：Timer (Istwert)         |
| **TS**         | dddd         | 0~511        | Doppelwort：Timer (Sollwert)         |
| **CC**         | ddd          | 0~255        | Doppelwort：Zähler (Istwert)       |
| **CS**         | ddd          | 0~255        | Doppelwort：Zähler (Sollwert)       |
| **CTH**        | d            | 0~3          | Doppelwort：Schneller Zähler            |
| **CTC**        | d            | 0~7          | Doppelwort：Vergleicher des schnellen Zählers |
| **CM**         | dddd         | 0~8999       | Wort：Steuerspeicher                      |
| **VM**         | dddd         | 0~9999       | Wort：Arbeitsspeicher                       |

<img src="../../drivers/koyo.files/image009.gif" width="595" />

Hinweis:

o: oktal, Eingabebereich 0-7;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/koyo.files/image010.gif" width="595" />
