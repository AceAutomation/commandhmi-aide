# Gerätetreiber ZhengHang

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie ZhengHang A5. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.

Verbindung mit einer SPS der Serie ZhengHang A5 herstellen

**1.Hardwareanschluss**

Verbindungskabel:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

|                           |     |                    |     |
|---------------------------|-----|--------------------|-----|
| **HM-HMI COM1/COM2** |     | **ZhengHang A5　** |     |
| 2                         | RX  | 2                  | TX  |
| 3                         | TX  | 3                  | RX  |
| 5                         | GND | 5                  | GND |

<img src="../../drivers/zhenghang.files/image002.gif" width="130" /><img src="../../drivers/zhenghang.files/image003.gif" width="290" /><img src="../../drivers/zhenghang.files/image004.gif" width="130" />

Der Anschluss des HMI ist DB9F, der der SPS der Serie ZhengHang A5 DB9M.

**2.Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ ZhengHang Electronics.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie ZhengHang A5.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie A5                   | Serie A5                                    |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**                  | NONE                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 1                           | 0~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation**  | Ja                         |
| **Online-Simulation**   | Ja                         |
| **Erweiterter Modus**       | Ja                         |

**3.Verwendbare Register und Adressbereiche**

|                   |                    |                 |                                                                           |
|-------------------|--------------------|-----------------|---------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                               |
| **I**             | dd.o               | 0.0 bis 15.7     | Bit: Eingangsabbild, nur lesen                                      |
| **Q**             | dd.o               | 0.0 bis 15.7     | Bit: Ausgangsabbild                                                |
| **M**             | dddd.o             | 0.0 bis 4095.7   | Bit: Bitspeicher (Merker)                                                           |
| **VW**            | dddd               | 0 bis 1998       | Wort: Variablenspeicher, 8-Bit-Register, jedes Wort belegt zwei Adressen |
| **AIW**           | d                  | 0 bis 9          | Wort: Analogeingang, nur lesen                                             |
| **AQW**           | d                  | 0 bis 9          | Wort: Analogausgang, nur schreiben                                           |

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />
