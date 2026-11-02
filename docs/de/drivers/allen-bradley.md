# Gerätetreiber Allen-Bradley

Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände von AIBUS-Geräten über das AIBUS-Protokoll. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des HMI und der des AIBUS-Geräts hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen des AIBUS-Geräts sorgfältig.

**Verbindung mit einem AIBUS-Gerät herstellen**

**1. Hardwareanschluss**

Verbindungskabel:

RS232 (serielle Schnittstelle, Protokoll RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **AIBUS-Gerät**  |     |
| 2                           | RX  | Benutzerdefinierter Pin | TX  |
| 3                           | TX  | Benutzerdefinierter Pin | RX  |
| 5                           | GND | Benutzerdefinierter Pin | GND |

<img src="../../drivers/allen-bradley.files/image002.gif" width="130" /><img src="../../drivers/allen-bradley.files/image003.gif" width="280" /><img src="../../drivers/allen-bradley.files/image004.gif" width="145" />

ControlLogix/CompactLogix:

|                             |     |                         |     |
|-----------------------------|-----|-------------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Allen-Bradley (AB)** |     |
| 2                           | RX  | 3                       | TX  |
| 3                           | TX  | 2                       | RX  |
| 5                           | GND | 5                       | GND |

<img src="../../drivers/allen-bradley.files/image005.gif" width="129" /><img src="../../drivers/allen-bradley.files/image006.gif" width="290" /><img src="../../drivers/allen-bradley.files/image007.gif" width="130" />

Der Anschluss des HMI der HM-Serie ist DB9F, der des AB-Geräts MD8M.

**2. Softwareeinstellungen**

ü Wählen Sie unter „Geräteservice“ Allen-Bradley.

ü Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

ü Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

ü Zu den Einstellungen der SPS siehe die technischen Unterlagen der Allen-Bradley-SPS.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | MicroLogix DF1_CRC          | MicroLogix DF1_CRC/MicroLogix DF1_BCC        |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                           | 7/8                                          |
| **Parität**              | NONE                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                           | 1/2                                          |
| **SPS-Stationsnummer**      | 1                           | 1~31                                         |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |
| **Prüfung**                   | CRC                         | BCC                                          |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation** | Ja                         |
| **Online-Simulation**  | Ja                         |
| **Erweiterter Modus**       | Nein                          |

**3. Verwendbare Register und Adressbereiche**

Serie SLC / MicroLogix:

|                   |                    |                        |                                |
|-------------------|--------------------|------------------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich**        | **Bemerkungen**                    |
| **I**             | 1:ddd/o            | 1:0/0~1:255/15         | Bit: Eingangsabbild     |
| **O**             | 0:ddd/o            | 0:0/0~0:255/15         | Bit: Ausgangsabbild    |
| **B**             | ddd:ddd/o          | 3:0/0~255:255/15       | Bit: Bitspeicher                |
| **S_Bit**         | 2:ddd/o            | 2:0/0~2:255/15         | Bit: Systemstatusbit          |
| **N_Bit**         | ddd:ddd/o          | 7:0、10:0/0~255:255/15 | Bit: Bit eines Datenregisterworts |
| **S**             | 2:ddd              | 2:0~2:255              | Wort: Systemstatuswort        |
| **ST**            | ddd:ddd.dd         | 0:0.0~255:255.40       | Wort: Systemstatuswort        |
| **N**             | ddd:ddd            | 7:0、10:0~255:255      | Wort: Datenregister            |
| **F**             | ddd:ddd            | 8:0~255:255            | Wort: Gleitkommaregister |
| **T_ACC**         | ddd:ddd            | 4:0~255:255            | Wort: Timer, ACC-Wert          |
| **T_PRE**         | ddd:ddd            | 4:0~255:255            | Wort: Timer, PRE-Wert          |
| **C_ACC**         | ddd:ddd            | 5:0~255:255            | Wort: Zähler, ACC-Wert        |
| **C_PRE**         | ddd:ddd            | 5:0~255:255            | Wort: Zähler, PRE-Wert        |

ControlLogix/CompactLogix:

|                   |                    |                  |                                |
|-------------------|--------------------|------------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich**  | **Bemerkungen**                    |
| **B-Bit**         | ddd:ddd/dd         | 3~225:0~255/0~15 | Bit: Bit eines Datenregisterworts |
| **N_Bit**         | ddd:ddd/dd         | 7~225:0~255/0~15 | Bit: Bit eines Datenregisterworts |
| **N_Bit**         | ddd:ddd/o          | 7:0/0~255:255/7  | Bit: Bit eines Datenregisterworts |
| **S**             | 2:ddd              | 2:0~2:255        | Wort: Systemstatuswort        |
| **N**             | ddd:ddd            | 7:0~255:255      | Wort: Datenregister            |
| **F**             | ddd:ddd            | 8:0~255:255      | Wort: Gleitkommaregister |

CompactLogix_L16ER_TCP (Port: 44818)

|               |                    |                 |                                        |
|---------------|--------------------|-----------------|----------------------------------------|
| Registername | **Adressformat** | **Eingabebereich** | **Bemerkungen**                            |
| **B**         | ddd.ddd            | 0.0~255.255     | Bit: Adresse vom Typ bool                 |
| **I**         | Ddd.ddd            | 0.0~255.255     | Wort: 16-Bit-int-Register              |
| **F**         | ddd.ddd            | 0.0~255.99      | Doppelwort: 32-Bit-float-Register |

MicroLogix DF1_TCP            (Port: 44818)

|               |                    |                  |                                                    |
|---------------|--------------------|------------------|----------------------------------------------------|
| Registername | **Adressformat** | **Eingabebereich**  | **Bemerkungen**                                        |
| **I**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: Eingangsabbild, nur lesen             |
| **O**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: Ausgangsabbild                         |
| **B**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: Bitspeicher                                   |
| **T**         | ddd.ddd            | 0.0~255.255      | Bit: Timerstatus                                   |
| **C**         | ddd.ddd            | 0.0~255.255      | Bit: Zählerstatus                                 |
| **S_Bit**     | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: Bit des Systemregisters                |
| **N_Bit**     | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: Bit eines Datenregisters                      |
| **S**         | ddd.ddd            | 0.0~255.255      | Wort: Systemregister                              |
| **N**         | ddd.ddd            | 0.0~255.255      | Wort: 16-Bit-Ganzzahlregister                      |
| **F**         | ddd.ddd            | 0.0~255.255      | Doppelwort: 32-Bit-Gleitkommaregister |
| **TV**        | ddd.ddd            | 0.0~255.255      | Wort: Istwert des Timers                       |
| **CV**        | ddd.ddd            | 0.0~255.255      | Wort: Istwert des Zählers                     |
| **TS**        | ddd.ddd            | 0.0~255.255      | Wort: Sollwert des Timers                          |
| **CS**        | ddd.ddd            | 0.0~255.255      | Wort: Sollwert des Zählers                            |

**4. Anbindung der HMI der HM-Serie an SPS der Serien ControlLogix und CompactLogix von Allen-Bradley**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Öffnen Sie RSLinx und richten Sie den Kommunikationstreiber der SPS ein</p>
<p><img src="../../drivers/allen-bradley.files/image008.gif" width="349" /></p>
<p>Legen Sie einen Treiber an; wählen Sie serielle Verbindung und RS-232-DF1-Geräte</p>
<p><img src="../../drivers/allen-bradley.files/image009.gif" width="425" /></p>
<p>Ist ein Kabel zwischen PC und SPS angeschlossen, erscheint die SPS nach der Einstellung in RSLinx</p>
<p><img src="../../drivers/allen-bradley.files/image010.gif" width="430" /></p>
<p>Öffnen Sie die SPS-Programmiersoftware RSLogix 5000 und legen Sie Ihr Projekt und neue Tags an</p>
<p><img src="../../drivers/allen-bradley.files/image011.gif" width="282" /></p>
<p>Legen Sie die Tags B003, N007 und F008 an</p>
<p><img src="../../drivers/allen-bradley.files/image012.gif" width="390" /></p>
<p>Tag-Liste nach dem Anlegen:</p>
<p><img src="../../drivers/allen-bradley.files/image013.gif" width="633" /></p>
<p>Legen Sie die <a href="javascript:;">Adresszuordnung</a> an</p>
<p><img src="../../drivers/allen-bradley.files/image014.gif" width="428" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image015.gif" width="410" /><strong></strong></p>
<p><strong>SPS-Parameter einstellen</strong></p>
<p><img src="../../drivers/allen-bradley.files/image016.gif" width="807" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image017.gif" width="552" /><strong></strong></p>
<p>·d: dezimal, Eingabebereich 0-9;</p>
<p>·o: oktal, Eingabebereich 0-7;</p>
<p>·Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;</p>
<p>·Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;</p>
<p>·Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;</p>
<p>·Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.</p>
<p>Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts </p></td>
</tr>
</tbody>
</table>

SPS CompactLogix der Serie 1769 anschließen

Neue Adresslabels in der SPS

Zuordnung der Adresslabels

Register        Labeltyp     Array-Größe

B                          bool             255

I                           int                 255

F                          real               100

Das Label muss 3 Zeichen lang sein, z. B. B003, I004 und F005

<img src="../../drivers/allen-bradley.files/image018.jpg" width="314" alt="ab_guanli.jpg" />

<img src="../../drivers/allen-bradley.files/image019.jpg" width="390" alt="ab_guanli2.jpg" />

MicroLogix DF1_TCP der Serie 1766 anschließen

Außer bei den E/A-Registern, deren Größe nicht einstellbar ist, wird die Array-Größe der Register auf 256 gesetzt. Die erste Zahl im Adressformat ist die Dateinummer: Bei F8 ist sie 8, bei I1 ist sie 1 usw.
