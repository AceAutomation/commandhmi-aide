# Gerätetreiber LG

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie LG Master-K. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

Verbindung mit einer SPS der Serie LG Master-K herstellen

**1.Hardwareanschluss**

Verbindungskabel:

RS232 mit CNet-Protokoll<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> (serielle Schnittstelle, Protokoll RS232)

|                                                                                                                    |     |                 |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-----------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                                                  | RX  | 7               | TX  |
| 3                                                                                                                  | TX  | 4               | RX  |
| 5                                                                                                                  | GND | 5               | GND |

<img src="../../drivers/lg.files/image002.gif" width="130" /><img src="../../drivers/lg.files/image003.gif" width="291" /><img src="../../drivers/lg.files/image004.gif" width="130" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie LG Master-K DB9M.

RS232 mit KLoader-Protokoll

|                                                                                       |     |                 |     |
|---------------------------------------------------------------------------------------|-----|-----------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                     | RX  | 3               | TX  |
| 3                                                                                     | TX  | 2               | RX  |
| 5                                                                                     | GND | 5               | GND |

<img src="../../drivers/lg.files/image005.gif" width="291" /><img src="../../drivers/lg.files/image006.gif" width="130" /><img src="../../drivers/lg.files/image007.gif" width="130" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie LG Master-K DB9M.

RS<span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>485

|                                                          |     |                 |
|----------------------------------------------------------|-----|-----------------|
| **HMI der HM-Serie COM1/COM2** |     | **LG Master-K** |
| 8                                                        | D-  | B               |
| 9                                                        | D+  | A               |

 <img src="../../drivers/lg.files/image008.gif" width="157" /><img src="../../drivers/lg.files/image009.gif" width="130" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie LG Master-K eine Zweidrahtklemme.

RS232-K10S1

|                             |     |                 |     |
|-----------------------------|-----|-----------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **LG Master-K** |     |
| 2                           | RX  | 4               | TX  |
| 3                           | TX  | 1               | RX  |
| 5                           | GND | 6               | GND |

Der Anschluss des HMI ist DB9F, der der SPS der Serie LG Master-K MD6M.

|     |                                                 |     |                                                 |
|-----|-------------------------------------------------|-----|-------------------------------------------------|
|     |                                                 |     |                                                 |
|     |                                                 |     | <img src="../../drivers/lg.files/image010.gif" width="146" /> |
|     | <img src="../../drivers/lg.files/image011.gif" width="401" /> |     |                                                 |
|     |                                                 |     |                                                 |

**2.Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ LG Industrial Systems.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie LG Master-K.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | LG Master-K Cnet            | LG Master-K Cnet/K Loader/K10s1              |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**              | NONE                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 0                           | 0~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation** | Ja                         |
| **Online-Simulation**  | Ja                         |
| **Erweiterter Modus**       | Ja                         |

**3.Verwendbare Register und Adressbereiche**

Verwendbare Adressbereiche der SPS der Serie Kxxx:

|               |                |             |                                |
|---------------|----------------|-------------|--------------------------------|
| Registername | Adressformat | Eingabebereich | Bemerkungen                        |
| P_Bit         | dddh           | 0~255f      | Bit: Ein-/Ausgangsbereich         |
| M_Bit         | dddh           | 0~255f      | Bit: Hilfsrelais (Merker)           |
| K_Bit         | dddh           | 0~255f      | Bit: Schutzrelais (remanent)          |
| L_Bit         | dddh           | 0~255f      | Bit: Link-Relais                |
| F_Bit         | dddh           | 0~255f      | Bit: Sonderrelais             |
| P             | dddh           | 0~255f      | Wort: Ein-/Ausgangsbereich        |
| M             | dddh           | 0~255f      | Wort: Hilfsrelais (Merker)          |
| K             | dddh           | 0~255f      | Wort: Schutzrelais (remanent)         |
| L             | dddh           | 0~255f      | Wort: Link-Relais               |
| F             | dddh           | 0~255f      | Wort: Sonderrelais            |
| T             | ddd            | 0~255       | Bit: Timerrelais               |
| C             | ddd            | 0~255       | Bit: Zählerrelais             |
| S             | dddd           | 0~9999      | Wort: Schrittregister        |
| D             | dddd           | 0~9999      | Wort: Datenregister            |
| TV            | ddd            | 0~255       | Wort: Istwert des Timers   |
| CV            | ddd            | 0~255       | Wort: Istwert des Zählers |

Verwendbare Adressbereiche der SPS der Serie XGB CPU (Kommunikation über die RS232-Programmierschnittstelle der SPS):

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                          |
| P_Bit          | ddddh        | 0-1023f      | Bit: Ein-/Ausgangsbereich            |
| M_Bit          | ddddh        | 0-1023f      | Bit: Hilfsrelais (Merker)              |
| F_Bit          | ddddh        | 0-1023f      | Bit: Sonderrelais                |
| L_Bit          | ddddh        | 0-2047f      | Bit: Link-Relais                   |
| K_Bit          | ddddh        | 0-4095f      | Bit: Schutzrelais (remanent)             |
| D_Bit          | ddddh        | 0-10239f     |                                   |
| T              | dddd         | 0-1023       | Bit: Timerrelais                  |
| C              | dddd         | 0-1023       | Bit: Zählerrelais                |
| TV             | dddd         | 0-1023       | Wort: Istwert des Timers      |
| CV             | dddd         | 0-1023       | Wort: Istwert des Zählers    |
| P              | dddd         | 0-1023       | Wort: Ein-/Ausgangsbereich           |
| M              | dddd         | 0-1023       | Wort: Hilfsrelais (Merker)             |
| F              | dddd         | 0-1023       | Wort: Sonderrelais (nur lesen) |
| L              | dddd         | 0-2047       | Wort: Link-Relais                  |
| K              | dddd         | 0-4095       | Wort: Schutzrelais (remanent)            |
| D              | dddd         | 0-10239      | Wort: Datenregister               |
| R              | dddd         | 0-10239      | Wort: Schrittregister           |
| ZR             | dddd         | 0-10239      | Wort:                             |
| S              | ddd          | 0-127        | Wort: Schrittregister           |
| Z              | ddd          | 0-127        | Wort:                             |
| U              | dd.dd        | 0.0-10.31    | Wort：(nur lesen)               |

Verwendbare Adressbereiche der SPS der Serie XGB CNET:

|               |                |             |                         |
|---------------|----------------|-------------|-------------------------|
| Registername | Adressformat | Eingabebereich | Bemerkungen                 |
| P             | dddh           | 0~127f      | Wort: Ein-/Ausgangsbereich |
| M             | dddh           | 0~255f      | Wort: Hilfsrelais (Merker)   |
| K             | dddh           | 0~2559f     | Wort: Schutzrelais (remanent)  |
| L             | dddh           | 0~1279f     | Wort: Link-Relais        |
| F             | dddh           | 0~255f      | Wort: Sonderrelais     |
| T             | ddd            | 0~255       | Bit: Timerrelais        |
| C             | ddd            | 0~255       | Bit: Zählerrelais      |
| S             | ddd            | 0~127.99    | Wort: Schrittregister |
| D             | dddd           | 0~5119      | Wort: Datenregister     |
| N             | dddd           | 0~3935      |                         |
| Z             | ddd            | 0~127       |                         |
| ZR            | dddd           | 0~1023      |                         |
| U             | d              | 0~7.31      |                         |

XGB TCP/IP

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                          |
| P_Bit          | ddddh        | 0-2047f      | Bit: Ein-/Ausgangsbereich            |
| M_Bit          | ddddh        | 0-2047f      | Bit: Hilfsrelais (Merker)              |
| F_Bit          | ddddh        | 0-2047f      | Bit: Sonderrelais                |
| L_Bit          | ddddh        | 0-4095f      | Bit: Link-Relais                   |
| K_Bit          | ddddh        | 0-8191f      | Bit: Schutzrelais (remanent)             |
| T              | dddd         | 0-2047       | Bit: Timerrelais                  |
| C              | dddd         | 0-2047       | Bit: Zählerrelais                |
| TV             | dddd         | 0-2047       | Wort: Istwert des Timers      |
| CV             | dddd         | 0-2047       | Wort: Istwert des Zählers    |
| P              | dddd         | 0-2047       | Wort: Ein-/Ausgangsbereich           |
| M              | dddd         | 0-2047       | Wort: Hilfsrelais (Merker)             |
| F              | dddd         | 0-2047       | Wort: Sonderrelais (nur lesen) |
| L              | dddd         | 0-4095       | Wort: Link-Relais                  |
| K              | dddd         | 0-8191       | Wort: Schutzrelais (remanent)            |
| D              | ddddd        | 0-19999      | Wort: Datenregister               |
| R              | ddddd        | 0-16383      |                                   |
| S              | ddd          | 0-127        | Wort: Schrittregister           |
| Z              | ddd          | 0-127        |                                   |
| U              | dd.dd        | 0.0-11.31    |                                   |
| N              | ddddd        | 0-10239      | Wort：(nur lesen)               |

<img src="../../drivers/lg.files/image012.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

h: hexadezimal, Eingabebereich 0-9, a-f;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/lg.files/image013.gif" width="595" />
