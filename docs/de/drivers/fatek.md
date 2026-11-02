# Gerätetreiber Fatek

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von <span id="OLE_LINK158"></span><span id="OLE_LINK159"></span>SPS der Serie Fatek FB. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

**Verbindung mit einem Fatek-Gerät herstellen**

**1.Hardwareanschluss**

Verbindungskabel:

RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (serielle Schnittstelle, Protokoll RS232)

|                         |     |                 |     |
|-------------------------|-----|-----------------|-----|
| HMI der HM-Serie COM1/COM2 |     | Serie Fatek FB |     |
| 2                       | RX  | 1               | TX  |
| 3                       | TX  | 2               | RX  |
| 5                       | GND | 4               | GND |

|     |                                                    |     |                                                    |     |                                                    |
|-----|----------------------------------------------------|-----|----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     | <img src="../../drivers/fatek.files/image006.gif" width="146" /> |
|     | <img src="../../drivers/fatek.files/image007.gif" width="129" /> |     |                                                    |     |                                                    |
|     |                                                    |     | <img src="../../drivers/fatek.files/image008.gif" width="280" /> |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |

Der Anschluss des HMI der HM-Serie ist DB9F, der der SPS der Serie Fatek FB MD4M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Fatek Automation Corp.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Fatek FB.

Standard-Verbindungsparameter des Touchscreens

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie Fatek FB             | Serie Fatek FB                              |
| **Schnittstellentyp** | RS232                       | RS232                                        |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 7                           | 7/8                                          |
| **Parität**              | EVEN                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 1                           | 0~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation** | Ja                         |
| **Online-Simulation**  | Ja                         |
| **Erweiterter Modus**       | Ja                         |

**3.Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                                   |
|-------------------|--------------------|-----------------|---------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                       |
| X                 | dddd               | 0~9999          | Bit: Eingang, nur lesen            |
| Y                 | dddd               | 0~9999          | Bit: Ausgangsrelais                                 |
| M                 | dddd               | 0~9999          | Bit: Internes Relais (Merker)                               |
| S                 | dddd               | 0~9999          | Bit: Schrittrelais                               |
| T                 | dddd               | 0~9999          | Bit: Timerstatus                                 |
| C                 | dddd               | 0~9999          | Bit: Zählerstatus                               |
| R                 | dddd               | 0~9999          | Wort: Datenregister |
| D                 | dddd               | 0~9999          | Wort: Datenregister                               |
| TR                | dddd               | 0~9999          | Wort: Istwert des Timers                      |
| CR                | dddd               | 0~9999          | Wort: Istwert des Zählers                    |
| F                 | dddd               | 0~9999          | Wort: Dateiregister                               |
| DRC               | ddd                | 200~255         | Doppelwort: Istwert des 32-Bit-Zählers      |

<img src="../../drivers/fatek.files/image009.gif" width="600" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/fatek.files/image009.gif" width="600" />
