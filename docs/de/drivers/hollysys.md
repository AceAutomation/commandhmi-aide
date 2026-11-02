# Gerätetreiber HollySys

Mit diesem Treiber lesen und schreiben die Touchscreens der Serie HMI-TOOLS Daten bzw. Zustände der Register von SPS der Serie HollySys LM. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

**Verbindung mit einer SPS der Serie HOLLYSYS herstellen**

**1.  Hardwareanschluss**

Verbindungskabel:

RS232 (serielle Schnittstelle, Protokoll RS232)

|                             |     |                        |     |
|-----------------------------|-----|------------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Serie HollySys LM** |     |
| 2                           | RX  | 3                      | TX  |
| 3                           | TX  | 2                      | RX  |
| 5                           | GND | 5                      | GND |

<img src="../../drivers/hollysys.files/image002.gif" width="130" /><img src="../../drivers/hollysys.files/image003.gif" width="290" /><img src="../../drivers/hollysys.files/image004.gif" width="130" />

Der Anschluss des HMI der HM-Serie ist DB9F, der der SPS der Serie HollySys LM DB9M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ HollySys Group.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie HollySys LM.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie HollySys LM          | Serie HollySys LM                           |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 38400                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**              | NONE                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 51                          | 0~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation** | Ja                         |
| **Online-Simulation**  | Ja                         |
| **Erweiterter Modus**       | Nein                          |

**3. Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                                                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                                           |
| **IX**            | ddd.o              | 0.0~511.7       | Bit: I-Speicherbereich, nur lesen                                                                        |
| **QX**            | ddd.o              | 0.0~511.7       | Bit: Q-Speicherbereich                                                                                   |
| **MX**            | dddd.o             | 0.0~7816.7      | Bit: M-Speicherbereich                                                                                   |
| **IW**            | ddd                | 0~510           | Wort: I-Speicherbereich, 8-Bit-Register, jedes Wort belegt zwei Adressen |
| **QW**            | ddd                | 0~510           | Wort: Q-Speicherbereich, 8-Bit-Register, jedes Wort belegt zwei Adressen |
| **MW**            | dddd               | 0~8190          | Wort: M-Speicherbereich, 8-Bit-Register, jedes Wort belegt zwei Adressen                               |

<img src="../../drivers/hollysys.files/image005.gif" width="600" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

8-Bit-Register in den Bemerkungen: Der Adressabstand zweier benachbarter Worte im Register beträgt 2;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/hollysys.files/image005.gif" width="600" />
