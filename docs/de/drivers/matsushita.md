# Gerätetreiber Matsushita

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Matsushita FP. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

Verbindung mit einer SPS der Serie Matsushita FP herstellen

**1.  Hardwareanschluss**

Verbindungskabel:

RS232-FP0/FP2/FP2SH/FPM

|                                                                                                                                                 |     |                          |     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Serie Matsushita FP** |     |
| 2                                                                                                                                               | RX  | 3                        | TX  |
| 3                                                                                                                                               | TX  | 2                        | RX  |
| 5                                                                                                                                               | GND | 1                        | GND |

<img src="../../drivers/matsushita.files/image002.gif" width="280" /><img src="../../drivers/matsushita.files/image003.gif" width="129" /><img src="../../drivers/matsushita.files/image004.gif" width="145" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie Matsushita FP MD5M.

RS422-FP1

|                             |     |                      |     |
|-----------------------------|-----|----------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | Serie Matsushita FP |     |
| 6                           | RX- | 2                    | TX- |
| 7                           | RX+ | 5                    | TX+ |
| 8                           | TX- | 3                    | RX- |
| 9                           | TX+ | 6                    | RX+ |

<img src="../../drivers/matsushita.files/image005.gif" width="140" /><img src="../../drivers/matsushita.files/image006.gif" width="129" /><img src="../../drivers/matsushita.files/image007.gif" width="280" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie Matsushita FP MD8M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ MATSUSHITA.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Matsushita FP.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie FP                   | Serie FP                                    |
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
| **Erweiterter Modus**       | Nein                          |

**3. Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                            |
| **X**             | ddddh              | 0~9999f         | Bit: externer Eingang, nur lesen         |
| **Y**             | ddddh              | 0~9999f         | Bit: externer Ausgang                   |
| **R**             | ddddh              | 0~9999f         | Bit: Internes Relais (Merker)                    |
| **L**             | ddddh              | 0~9999f         | Bit: Link-Relais                        |
| **T**             | dddd               | 0~9999          | Bit: Timerstatus, nur lesen        |
| **C**             | dddd               | 0~9999          | Bit: Zählerstatus, nur lesen      |
| **WX**            | dddd               | 0~9999          | Wort: externer Eingang, nur lesen        |
| **WY**            | dddd               | 0~9999          | Wort: externer Ausgang                  |
| **WR**            | dddd               | 0~9999          | Wort: Internes Relais (Merker)                   |
| **WL**            | dddd               | 0~9999          | Wort: Link-Relais                       |
| **DT**            | ddddd              | 0~99999         | Wort: Datenregister                    |
| **LD**            | ddddd              | 0~99999         | Wort: Link-Register                    |
| **FL**            | ddddd              | 0~99999         | Wort: Dateiregister                    |
| **SV**            | dddd               | 0~9999          | Wort: Sollwertbereich Timer/Zähler     |
| **EV**            | dddd               | 0~9999          | Wort: Istwertbereich Timer/Zähler |

<img src="../../drivers/matsushita.files/image008.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

h: hexadezimal, Eingabebereich 0-9, a-f;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/matsushita.files/image009.gif" width="595" />
