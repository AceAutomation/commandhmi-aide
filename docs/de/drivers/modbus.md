# Gerätetreiber Modbus

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der <span id="OLE_LINK37"></span><span id="OLE_LINK38"></span>MODBUS-Geräte. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der des MODBUS-Geräts hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen des MODBUS-Geräts sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einem MODBUS-Gerät herstellen</p>
<p><strong>1.</strong> <strong>Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS232<span id="OLE_LINK24"></span><span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK62"></span><span id="OLE_LINK63"></span><span id="OLE_LINK64"></span><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Modbus-Gerät</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>Benutzerdefinierter Pin</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modbus.files/image002.gif" width="157" /><img src="../../drivers/modbus.files/image003.gif" width="130" />

Der Anschluss des HMI ist DB9F. Die Anschlussbelegung des Modbus-Geräts hängt vom jeweiligen Gerät ab.

**RS422**

|                                                                                                                    |     |                   |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Modbus device** |     |
| 6                                                                                                                  | RX- | Benutzerdefinierter Pin | TX- |
| 7                                                                                                                  | RX+ | Benutzerdefinierter Pin | TX+ |
| 8                                                                                                                  | TX- | Benutzerdefinierter Pin | RX- |
| 9                                                                                                                  | TX+ | Benutzerdefinierter Pin | RX+ |

<img src="../../drivers/modbus.files/image004.gif" width="157" /><img src="../../drivers/modbus.files/image005.gif" width="130" />

Der Anschluss des HMI ist DB9F. Die Anschlussbelegung des Modbus-Geräts hängt vom jeweiligen Gerät ab.

**RS485**

|                                                                                       |     |                   |     |
|---------------------------------------------------------------------------------------|-----|-------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Modbus device** |     |
| 8                                                                                     | D-  | Benutzerdefinierter Pin | B   |
| 9                                                                                     | D+  | Benutzerdefinierter Pin | A   |

<img src="../../drivers/modbus.files/image006.gif" width="157" /><img src="../../drivers/modbus.files/image007.gif" width="130" />

Der Anschluss des HMI ist eine 9-polige Sub-D-Buchse. Die Anschlussbelegung des Modbus-Geräts hängt vom jeweiligen Gerät ab.

**TCP/IP (RJ45-Direktverbindung)**

|                                                                                                                    |      |                   |      |
|--------------------------------------------------------------------------------------------------------------------|------|-------------------|------|
| **HMI der HM-Serie COM1/COM2** |      | **Modbus device** |      |
| 1                                                                                                                  | TX+  | 3                 | RX+  |
| 2                                                                                                                  | TX-  | 6                 | RX-  |
| 3                                                                                                                  | RX+  | 1                 | TX+  |
| 4                                                                                                                  | BD4+ | 4                 | BD4+ |
| 5                                                                                                                  | BD4- | 5                 | BD4- |
| 6                                                                                                                  | RX-  | 2                 | TX-  |
| 7                                                                                                                  | BD3+ | 7                 | BD3+ |
| 8                                                                                                                  | BD3- | 8                 | BD3- |

|     |                                                    |     |                                                     |     |                                                    |
|-----|----------------------------------------------------|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                     |     |                                                    |
|     | <img src="../../drivers/modbus.files/image008.gif" width="95" /> |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     | <img src="../../drivers/modbus.files/image009.gif" width="95" /> |
|     |                                                    |     | <img src="../../drivers/modbus.files/image010.gif" width="267" /> |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |

<span id="OLE_LINK68"></span><span id="OLE_LINK69"></span><span id="OLE_LINK70"></span>

Der Anschluss des HMI ist RJ45, der des Modbus-Geräts RJ45.

**TCP/IP (RJ45-Verbindung über Router)**

|                       |      |               |      |
|-----------------------|------|---------------|------|
| **HM-HMI COM1/COM2** |      | Modbus device |      |
| 1                     | TX+  | 3             | RX+  |
| 2                     | TX-  | 6             | RX-  |
| 3                     | RX+  | 1             | TX+  |
| 4                     | BD4+ | 4             | BD4+ |
| 5                     | BD4- | 5             | BD4- |
| 6                     | RX-  | 2             | TX-  |
| 7                     | BD3+ | 7             | BD3+ |
| 8                     | BD3- | 8             | BD3- |

<img src="../../drivers/modbus.files/image011.gif" width="95" />

|     |                                                     |     |                                                    |
|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                     |     |                                                    |
|     |                                                     |     | <img src="../../drivers/modbus.files/image012.gif" width="95" /> |
|     | <img src="../../drivers/modbus.files/image013.gif" width="267" /> |     |                                                    |
|     |                                                     |     |                                                    |

Der Anschluss des HMI ist RJ45, der des Modbus-Geräts RJ45.

**2.Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Modbus.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen siehe die technischen Unterlagen des Modbus-Geräts.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | RTU Master                  | RTU/RTU_S/ASCII/ASCII_S Master               |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
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

<img src="../../drivers/modbus.files/image014.gif" width="595" />

Hinweis: RTU_S und ASCII_S verwenden zum Schreiben den Funktionscode 0x10 (unabhängig von der Datenlänge);

·Ist die SPS-Stationsnummer 0, arbeitet das System im Broadcast-Modus.

**3.Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                                                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                                      |
| 0x                | ddddd              | 0~65535         | Bit: Eingangsspule                                                                                  |
| 1x                | ddddd              | 0~65536         | Bit: Eingangsspule, nur lesen                                                                       |
| 3x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit: Bit eines 16-Bit-Eingangsregisters, nur lesen                       |
| 4x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit: Bit eines 16-Bit-Ausgangsregisters                                                               |
| 3x                | ddddd              | 0~65535         | Wort: 16-Bit-Eingangsregister, nur lesen                                                           |
| 4x                | ddddd              | 0~65535         | Wort: 16-Bit-Ausgangsregister                                                                     |
| 3x_D              | ddddd              | 0~65535         | Doppelwort: Eingangsregister, höher- und niederwertige 16 Bit des 3x-Doppelworts vertauscht, nur lesen |
| 4x_D              | ddddd              | 0~65535         | Doppelwort: Ausgangsregister, höher- und niederwertige 16 Bit des 4x-Doppelworts vertauscht           |

Modbus Slave

|                       |                             |                 |                                                                |
|-----------------------|-----------------------------|-----------------|----------------------------------------------------------------|
| **Internes Register** | **Unterstützter Funktionscode** | **Eingabebereich** | **Bemerkung**                                                     |
| LB                    | 01/02/05/15                 | 0~59999         | Bit：Interne Adresse des Touchscreens lesen und schreiben (LB) |
| LW                    | 03/04/06/16                 | 0~59999         | Wort：Interne Adresse des Touchscreens lesen und schreiben  |

<img src="../../drivers/modbus.files/image015.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

DD: 16 Bit, Eingabebereich 0-15;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/modbus.files/image016.gif" width="595" />
