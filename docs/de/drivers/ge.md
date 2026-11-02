# Gerätetreiber GE

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie GE Fanuc. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

**1. Hardwareanschluss**

Verbindungskabel:

RS232 (serielle Schnittstelle, Protokoll RS232)

|                             |     |                     |     |
|-----------------------------|-----|---------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Serie GE Fanuc** |     |
| 2                           | RX  | 4                   | TX  |
| 3                           | TX  | 3                   | RX  |
| 5                           | GND | 8                   | GND |

|     |                                                 |     |                                                 |     |                                                |
|-----|-------------------------------------------------|-----|-------------------------------------------------|-----|------------------------------------------------|
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     | <img src="../../drivers/ge.files/image002.gif" width="97" /> |
|     | <img src="../../drivers/ge.files/image003.gif" width="130" /> |     |                                                 |     |                                                |
|     |                                                 |     | <img src="../../drivers/ge.files/image004.gif" width="278" /> |     |                                                |
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     |                                                |

Der Anschluss des HMI der HM-Serie ist DB9F, der der SPS der Serie GE Fanuc RJ45.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ GE Corporation.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie GE Fanuc.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | GE Fanuc SNP-X              | GE Fanuc SNP-X/ GE Fanuc CCM                 |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
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
| **Erweiterter Modus**       | Nein                          |

**3. Verwendbare Register und Adressbereiche**

|                   |                    |                 |                            |
|-------------------|--------------------|-----------------|----------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                |
| **%I**            | ddddd              | 1~10000         | Bit: Digitaleingang        |
| **%Q**            | ddddd              | 1~10000         | Bit: Digitalausgang       |
| **%M**            | ddddd              | 1~10000         | Bit: Interne Verwendung          |
| **%S**            | ddd                | 1~128           | Bit: Systemverwendung, nur lesen |
| **%SA**           | ddd                | 1~128           | Bit: Systemverwendung, nur lesen |
| **%SB**           | ddd                | 1~128           | Bit: Systemverwendung, nur lesen |
| **%SC**           | ddd                | 1~128           | Bit: Systemverwendung, nur lesen |
| **%T**            | ddd                | 1~256           | Bit: Temporärer Status      |
| **%G**            | dddd               | 1~7680          | Bit: Genius-Global        |
| **%AI**           | ddddd              | 1~10000         | Wort: Analogeingang         |
| **%AQ**           | ddddd              | 1~10000         | Wort: Analogausgang        |
| **%R**            | ddddd              | 1~32640         | Wort: Registerspeicher      |

 <img src="../../drivers/ge.files/image005.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts.

<img src="../../drivers/ge.files/image005.gif" width="595" />
