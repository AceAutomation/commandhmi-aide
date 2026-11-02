# Gerätetreiber HaiWell

|                                                                                                                                                                                                                                                                                                                                                                                                                                                     |     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Haiwell E/S/H. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig. |     |

<span id="OLE_LINK217"></span><span id="OLE_LINK218"></span><span id="OLE_LINK219"></span>Verbindung mit einem HAIWELL-Gerät herstellen<span id="OLE_LINK221"></span>

<span id="OLE_LINK222"></span><span id="OLE_LINK223"></span><span id="OLE_LINK224"></span>**1. Hardwareanschluss**

<span id="OLE_LINK225"></span><span id="OLE_LINK226"></span><span id="OLE_LINK227"></span>Verbindungskabel:

RS232 (serielle Schnittstelle, Protokoll RS232)

|                                                                                                                       |     |                          |     |
|-----------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Serie HaiWell E/S/H** |     |
| 2                                                                                                                     | RX  | 2                        | TX  |
| 3                                                                                                                     | TX  | 1                        | RX  |
| 5                                                                                                                     | GND | 3                        | GND |

|     |                                                      |     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                      |
|     | <img src="../../drivers/haiwell.files/image002.gif" width="129" /> |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     | <img src="../../drivers/haiwell.files/image003.gif" width="140" /> |
|     |                                                      |     | <img src="../../drivers/haiwell.files/image004.gif" width="280" /> |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |

<span id="OLE_LINK231"></span>Der Anschluss des HMI der HM-Serie ist DB9F, der der SPS der Serie Haiwell E/S/H MD4M.

<span id="OLE_LINK237"></span>**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Haiwell Technology Corp.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Haiwell E/S/H.

<span id="OLE_LINK242"></span>Standard-Verbindungsparameter des Touchscreens

|                             |                             |                             |                                              |     |
|-----------------------------|-----------------------------|-----------------------------|----------------------------------------------|-----|
| **Einstellung**            | **Standardwert** |                             | **Einstellbereich**                            |     |
| **Schnittstellentyp** | RS232                       |                             | RS232/RS422/RS485                            |     |
| **Baudrate**               | 19200                       |                             | 1200/2400/4800/9600/19200/38400/57600/115200 |     |
| **Datenbits**         | 8                           |                             | 7/8                                          |     |
| **Parität**              | NONE                        |                             | EVEN/ODD/NONE                                |     |
| **Stoppbits**         | 2                           |                             | 1/2                                          |     |
| **SPS-Stationsnummer**      | 1                           |                             | 1~31                                         |     |
| **HMI-Stationsnummer**      | 0                           |                             | 0~255                                        |     |
| **Funktion**     |                             | **Unterstützt** |                                              |     |
| **Offline-Simulation**     |                             | Ja                         |                                              |     |
| **Online-Simulation**      |                             | Ja                         |                                              |     |
| **Erweiterter Modus**           |                             | Ja                         |                                              |     |
|                             |                             |                             |                                              |     |

3\. **Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                |
| X                 | ddd                | 0~1023          | Bit: Externer Schalteingang                                 |
| Y                 | ddd                | 0~1023          | Bit: Externer Schaltausgang                                |
| M                 | ddd                | 0~12287         | Bit: Internes Relais (Merker)                                        |
| SM                | ddd                | 0~215           | Bit: Systemstatus           |
| S                 | ddd                | 0~2047          | Bit: Schrittstatus                                           |
| T                 | ddd                | 0~1023          | Bit: Timerstatus                                          |
| C                 | ddd                | 0~255           | Bit: Zählerstatus                                        |
| AI                | ddd                | 0~255           | Wort: Analoges Eingangsregister                                |
| AQ                | ddd                | 0~255           | Wort: Analoges Ausgangsregister                               |
| V                 | ddd                | 0~14847         | Wort: Internes Register                                    |
| TCV               | ddd                | 0~1023          | Wort: Istwert des Timers |
| CCV               | ddd                | 0~47, 80~255    | Wort: Istwert des Zählers                             |
| SV                | ddd                | 0~154           | Wort: Systemregister                                      |
| CCV32             | ddd                | 0~31            | Doppelwort: Istwert des Zählers                      |

<img src="../../drivers/haiwell.files/image010.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/haiwell.files/image011.gif" width="595" />
