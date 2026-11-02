# Gerätetreiber Fuji

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Fuji NB. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

**Verbindung mit einem Fuji-Gerät herstellen**

**1. Hardwareanschluss**

Verbindungskabel:

RS422<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (serielle Schnittstelle, Protokoll RS422)

|                         |     |                |     |
|-------------------------|-----|----------------|-----|
| HMI der HM-Serie COM1/COM2 |     | Serie Fuji NB |     |
| 6                       | RX- | 4              | TX- |
| 7                       | RX+ | 3              | TX+ |
| 8                       | TX- | 6              | RX- |
| 9                       | TX+ | 5              | RX+ |

|     |                                                   |     |                                                   |     |                                                  |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|--------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     | <img src="../../drivers/fuji.files/image002.gif" width="95" /> |
|     | <img src="../../drivers/fuji.files/image003.gif" width="130" /> |     |                                                   |     |                                                  |
|     |                                                   |     | <img src="../../drivers/fuji.files/image004.gif" width="278" /> |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |

Der Anschluss des HMI der HM-Serie ist DB9F, der der SPS der Serie Fuji NB RJ45.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ Fuji Electric Corporation.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Fuji NB.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie Fuji NB              | Serie Fuji NB                               |
| **Schnittstellentyp** | RS422                       | RS422                                        |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**              | ODD                         | EVEN/ODD/NONE                                |
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

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                            |
| **X**             | hhh                | 0~7ff           | Bit: Eingang, nur lesen |
| **Y**             | hhh                | 0~7ff           | Bit: Ausgang           |
| **M**             | hhhh               | 0~7fff          | Bit: Internes Relais (Merker)                    |
| **SM**            | hhhh               | 8000~81ff       | Bit: Internes Relais (Merker)                    |
| **L**             | hhh                | 0~5ff           | Bit: Verriegelungsrelais                     |
| **S**             | hh                 | 0~ff            | Bit: Schrittrelais                    |
| **T**             | hhh                | 0~1ff           | Bit: Timerstatus                   |
| **C**             | hh                 | 0~ff            | Bit: Zählerstatus                 |
| **D**             | hhhh               | 0~7fff          | Wort: Datenspeicher           |
| **SD**            | hhhh               | 8000~80ff       | Wort: Datenspeicher           |
| **TV**            | hhh                | 0~1ff           | Wort: Istwert des Timers           |
| **CV**            | hh                 | 0~ff            | Wort: Istwert des Zählers         |

<img src="../../drivers/fuji.files/image005.gif" width="595" />

Hinweis:

h: hexadezimal, Eingabebereich 0-9, a-f;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/fuji.files/image005.gif" width="595" />
