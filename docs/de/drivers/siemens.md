# Gerätetreiber Siemens

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie Siemens S7-200/300/1200. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p> Verbindung mit einer SPS der Serie Siemens S7-200/300/1200tcp herstellen</p>
<p><strong>1. 1 Hardwareanschluss</strong></p>
<p>Verbindungskabel:</p>
<p>RS485-Siemens S7-200<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI der HM-Serie COM1/COM2</strong></p></td>
<td colspan="2"><p>Serie Siemens S7-200</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>8</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>3</p></td>
<td><p>TX+</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/siemens.files/image002.gif" width="130" /><img src="../../drivers/siemens.files/image003.gif" width="290" /><img src="../../drivers/siemens.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

  RS232-Siemens S7-300

|                             |     |                           |     |
|-----------------------------|-----|---------------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     | **Serie Siemens S7-300** |     |
| **2**                       | RX  | 3                         | TX  |
| **3**                       | TX  | 2                         | RX  |
| **5**                       | GND | 5                         | GND |

|     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |
|     | <img src="../../drivers/siemens.files/image005.gif" width="408" /> |     | <img src="../../drivers/siemens.files/image006.gif" width="129" /> |

Der Anschluss des HMI ist DB9F, der MPI-Anschluss der SPS der Serie Siemens S7-300 DB9M.

Verbindung mit einer SPS der Serie Siemens S7-200/300/1200 herstellen

**1. 2 Hardwareanschluss**

Verbindungskabel:

  Kabel RJ45;

  Belegung RJ45:

**<img src="../../drivers/siemens.files/image014.jpg" width="343" />**

1、 IP-Adresse und Port einstellen

Wählen Sie auf der Seite „Allgemein“ der Eigenschaften der Kommunikationsschnittstelle als Schnittstelle „Ethernet Port“ und als Service „SIEMENS“, „Siemens S7-200(TCP/IP)/Siemens S7-300(TCP/IP)/Siemens S7-1200(TCP)“;

Stellen Sie auf der Seite „Parameter“ der Eigenschaften der Kommunikationsschnittstelle IP-Adresse und Port ein.

Hinweis:

SPS und HMI müssen sich im selben Subnetz befinden; die Subnetzmaske ist einfach auf 255.255.255.0 einzustellen.

2、 Bei der Siemens-SPS 1200 ist zu prüfen, ob der Verbindungsschutz aktiv ist; gegebenenfalls die entsprechende Option aktivieren, neu übersetzen und in die SPS laden.

Laden Sie in TIA Portal das SPS-Programm hoch oder legen Sie ein neues S7-1200-Projekt an; klicken Sie mit der rechten Maustaste auf die CPU und wählen Sie „Eigenschaften“; aktivieren Sie unter „Schutz“ die Option „Zugriff über PUT/GET-Kommunikation durch entfernten Partner (SPS, HMI, OPC...) erlauben“, wie in der folgenden Abbildung:

**<img src="../../drivers/siemens.files/image015.jpg" width="1152" />**

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ SIEMENS.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie Siemens S7-200/300

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                         |                                    |                                              |
|-----------------------------|-------------------------|------------------------------------|----------------------------------------------|
| **Einstellung**            | Standardwert |                                    | Einstellbereich                                |
| **SPS-Typ**                | S7-200(PPI)             |                                    | S7-200(PPI)/ S7-300(MPI)                     |
| **Schnittstellentyp** | RS485                   |                                    | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                   |                                    | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 8                       |                                    | 7/8                                          |
| **Parität**              | EVEN                    |                                    | EVEN/ODD/NONE                                |
| **Stoppbits**         | 1                       |                                    | 1/2                                          |
| **SPS-Stationsnummer**      | 2                       |                                    | 1 bis 255                                     |
| **HMI-Stationsnummer**      | 0                       |                                    | 0 bis 255                                     |
| **Funktion**     |                         | **Unterstützt**        |                                              |
| **Offline-Simulation**     |                         | Ja                                |                                              |
| **Online-Simulation**      |                         | Ja                                |                                              |
| **Erweiterter Modus**           |                         | Ja: S7-200(PPI)/ Nein: S7-300(MPI) |                                              |
|                             |                         |                                    |                                              |

**3. Verwendbare Register und Adressbereiche**

Siemens S7-200

|                   |                    |                 |                                                                                                    |
|-------------------|--------------------|-----------------|----------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                                        |
| **I**             | dd.o               | 0.0 bis 4095.7   | Bit: Eingangsabbild, nur lesen                                                              |
| **Q**             | dd.o               | 0.0 bis 4095.7   | Bit: Ausgangsabbild                                                                        |
| **M**             | dd.o               | 0.0 bis 4095.7   | Bit: Bitspeicher (Merker)                                                                                    |
| **S**             | dd.o               | 0.0 bis 4095.7   | Bit: Ablaufsteuerungsrelais                                                                        |
| **SM**            | ddd.o              | 0.0 bis 4095.7   | Bit: Sonder-Bitspeicher, SM0.0-SM29.7 nur lesen                                                    |
| **T**             | ddd                | 0 bis 255        | Bit: Timerstatus: nur lesen                                                                        |
| **C**             | ddd                | 0 bis 255        | Bit: Zählerstatus: nur lesen                                                                      |
| **VB_Bit**        | ddddd.o            | 0.0 bis 10239.7  | Bit: Bit des Variablenspeichers                                                                           |
| **IW**            | dd                 | 0 bis 4095       | Wort: Eingangsabbild, nur lesen, 8-Bit-Register, jedes Wort belegt zwei Adressen         |
| **QW**            | dd                 | 0 bis 4095       | Wort: Ausgangsabbild, 8-Bit-Register, jedes Wort belegt zwei Adressen                   |
| **MW**            | dd                 | 0 bis 4095       | Wort: Bitspeicher (Merker), 8-Bit-Register, jedes Wort belegt zwei Adressen                               |
| **SW**            | dd                 | 0 bis 4095       | Wort: Ablaufsteuerungsrelais, 8-Bit-Register, jedes Wort belegt zwei Adressen                   |
| **SMW**           | ddd                | 0 bis 4095       | Wort: Sonder-Bitspeicher, SMW0-SMW29 nur lesen, 8-Bit-Register, jedes Wort belegt zwei Adressen |
| **VB**            | ddddd              | 0 bis 10239      | Wort: Variablenspeicher, 8-Bit-Register                                                            |
| **VW**            | ddddd              | 0 bis 10238      | Wort: Variablenspeicher, 8-Bit-Register, jedes Wort belegt zwei Adressen                          |
| **VD**            | ddddd              | 0 bis 10236      | Doppelwort: Variablenspeicher, 8-Bit-Register, jedes Doppelwort belegt vier Adressen           |
| **TV**            | ddd                | 0 bis 255        | Wort: Istwert des Timers                                                                   |
| **CV**            | ddd                | 0 bis 255        | Wort: Istwert des Zählers                                                                 |
| **AIW**           | dd                 | 0 bis 62         | Wort: Analogeingang, nur lesen, 8-Bit-Register, jedes Wort belegt zwei Adressen                  |
| **AQW**           | dd                 | 0 bis 62         | Wort: Analogausgang, nur schreiben, 8-Bit-Register, jedes Wort belegt zwei Adressen                |

Siemens S7-300 / Siemens S7-300(MPI) / Siemens S7-300tcp

|                   |                    |                     |                                                                                                                                                            |
|-------------------|--------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich**     | **Bemerkungen**                                                                                                                                                |
| **I**             | dddd.o             | 0.0 bis 4095.7       | Bit: Eingangsabbild                                                                                                                                 |
| **Q**             | dddd.o             | 0.0 bis 4095.7       | Bit: Ausgangsabbild                                                                                                                                |
| **M**             | dddd.o             | 0.0 bis 4095.7       | Bit: Bitspeicher (Merker)                                                                                                                                            |
| **DB_Bit**        | DDD:dddd.o         | 0:0.0 bis 255:8192.7 | Bit: Bit eines Worts im DB-Bausteinbereich, Bausteinnummer DD 0 bis 255, Wort je Baustein dddd 0 bis 8192, Bit je Wort o 0 bis 7                          |
| **IW**            | dddd               | 0 bis 4095           | Wort: Eingangsabbild, 8-Bit-Register, jedes Wort belegt zwei Adressen                                                                            |
| **QW**            | dddd               | 0 bis 4095           | Wort: Ausgangsabbild, 8-Bit-Register, jedes Wort belegt zwei Adressen                                                                           |
| **MW**            | dddd               | 0 bis 4095           | Wort: Bitspeicher (Merker), 8-Bit-Register, jedes Wort belegt zwei Adressen                                                                                       |
| **DBW**           | DDD:dddd           | 0:0 bis 255:8192     | Wort: DB-Bausteinbereich, Bausteinnummer DD 0 bis 255, Wort dddd 0 bis 8192, 8-Bit-Register, jedes Wort belegt zwei Adressen                |
| **DBD**           | DDD:dddd           | 0:0 bis 255:8192     | Doppelwort: DB-Bausteinbereich, Bausteinnummer DD 0 bis 255, Wort dddd 0 bis 8192, 8-Bit-Register, jedes Doppelwort belegt vier Adressen |

Siemens S7-1200tcp

|                   |                    |                  |                                                                                                                                                            |
|-------------------|--------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich**  | **Bemerkungen**                                                                                                                             |
| **I**             | dddd.o             | 0.0~1024.7       | Bit: Eingangsabbild                                                                                                                                 |
| **Q**             | dddd.o             | 0.0~1024.7       | Bit: Ausgangsabbild                                                                                                                                |
| **M**             | dddd.o             | 0.0~8191.7       | Bit: Bitspeicher (Merker)                                                                                                                                            |
| **DB_Bit**        | DDD:dddd.o         | 0:0.0~255:8192.7 | Bit: Bit eines Worts im DB-Bausteinbereich, Bausteinnummer DD 0 bis 255, Wort je Baustein dddd 0 bis 8192, Bit je Wort o 0 bis 7                          |
| **IW**            | dddd               | 0~1024           | Wort: Eingangsabbild, 8-Bit-Register, jedes Wort belegt zwei Adressen                                                                            |
| **QW**            | dddd               | 0~1024           | Wort: Ausgangsabbild, 8-Bit-Register, jedes Wort belegt zwei Adressen                                                                           |
| **MW**            | dddd               | 0~8191           | Wort: Bitspeicher (Merker), 8-Bit-Register, jedes Wort belegt zwei Adressen                                                                                       |
| **DBW**           | DDD:dddd           | 0:0~255:8192     | Wort: DB-Bausteinbereich, Bausteinnummer DD 0 bis 255, Wort dddd 0 bis 8192, 8-Bit-Register, jedes Wort belegt zwei Adressen                |
| **DBD**           | DDD:dddd           | 0:0~255:8192     | Doppelwort: DB-Bausteinbereich, Bausteinnummer DD 0 bis 255, Wort dddd 0 bis 8192, 8-Bit-Register, jedes Doppelwort belegt vier Adressen |

LOGO_TCP

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen** |
| **I**             | dd                 | 1~64            | Bit: Eingangsabbild     |
| **Q**             | dd                 | 1~64            | Bit: Ausgangsabbild    |
| **M**             | ddd                | 1~112           | Bit: Bitspeicher (Merker)                |
| **VB**            | dddd.o             | 0.0~1023.7      | Bit                            |
| **AI**            | dd                 | 1~16            | Wort: Eingangsabbild    |
| **AQ**            | dd                 | 1~16            | Wort: Ausgangsabbild   |
| **AM**            | dd                 | 1~64            | Wort: Bitspeicher (Merker)               |
| **VW**            | dddd               | 0~511           | Word                           |

<img src="../../drivers/siemens.files/image007.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

o: oktal, Eingabebereich 0-7;

DDD: Bausteinnummer; Eingabebereich 0-255;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Doppelwort in den Bemerkungen: Der Datentyp des Registers muss in der Projektierung 32 Bit sein;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/siemens.files/image008.gif" width="595" />
