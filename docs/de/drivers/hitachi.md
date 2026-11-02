# Gerätetreiber Hitachi

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Hitachi E/EH. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

**1. Hardwareanschluss**

Verbindungskabel:

RS232 (serielle Schnittstelle, Protokoll RS232)

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
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="3"><p><strong>Serie Hitachi E/EH</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td colspan="2"><p>SD</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>6</p></td>
<td colspan="2"><p>RD</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>1</p></td>
<td colspan="2"><p>SG</p></td>
</tr>
<tr class="odd">
<td colspan="2" rowspan="2"></td>
<td><p>4</p></td>
<td><p>PHL</p></td>
<td rowspan="2"><p>4-7</p>
<p>Kurzschluss</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>DR</p></td>
</tr>
</tbody>
</table>

|     |                                                      |     |                                                      |     |                                                     |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|-----------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     | <img src="../../drivers/hitachi.files/image002.gif" width="91" /> |
|     | <img src="../../drivers/hitachi.files/image003.gif" width="130" /> |     |                                                      |     |                                                     |
|     |                                                      |     | <img src="../../drivers/hitachi.files/image004.gif" width="278" /> |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |

Der Anschluss des HMI der HM-Serie ist DB9F, der des AB-Geräts RJ45.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Hitachi Industrial.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Hitachi E/EH.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie Hitachi E/EH         | Serie Hitachi E/EH                          |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Erweiterter Modus**       | Ja                         |

**3. Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                                                    |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                        |
| **X**             | hhhh               | 0~ffff          | Bit: externer Schalteingang, nur lesen                     |
| **Y**             | hhhh               | 0~ffff          | Bit: externer Schaltausgang |
| **M**             | hhhh               | 0~ffff          | Bit: Internes Relais (Merker)                                                |
| **R**             | hhhh               | 0~ffff          | Bit: Internes Register                                             |
| **T**             | hhhh               | 0~ffff          | Bit: Timerstatus                                               |
| **L**             | hhhh               | 0~ffff          | Bit: Link-Relais                                                    |
| **WX**            | hhhh               | 0~ffff          | Wort: externer Schalteingang                               |
| **WY**            | hhhh               | 0~ffff          | Wort: externer Schaltausgang                              |
| **WM**            | hhhh               | 0~ffff          | Wort: Internes Relais (Merker)                                               |
| **WR**            | hhhh               | 0~ffff          | Wort: Internes Register                                            |
| **WL**            | hhhh               | 0~ffff          | Wort: Link-Relais                                                   |
| **TC**            | hhhh               | 0~ffff          | Wort: Istwert von Timer/Zähler                               |

<img src="../../drivers/hitachi.files/image005.gif" width="595" />

Hinweis:

h: hexadezimal, Eingabebereich 0-9, a-f;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/hitachi.files/image006.gif" width="595" />
