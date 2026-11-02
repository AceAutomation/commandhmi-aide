# Gerätetreiber Omron

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mit diesem Treiber lesen und schreiben die HMI der HM-Serie Daten bzw. Zustände der Register von SPS der Serie SYSMAC C/CPM/CS/CJ. Die serielle Verbindung wird zwischen der seriellen Schnittstelle des Touchscreens und der der SPS hergestellt. Lesen Sie vor der Verwendung dieses Treibers dieses Kapitel und die technischen Unterlagen der SPS sorgfältig.</p></td>
</tr>
<tr class="even">
<td><p>Verbindung mit einer SPS der Serie SYSMAC C/CPM/CS/CJ herstellen</p>
<p>1.  Hardwareanschluss</p>
<p>Verbindungskabel:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>Touchscreen COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>SYSMAC CS/CJ</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>2</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>9</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/omron.files/image002.gif" width="130" /><img src="../../drivers/omron.files/image003.gif" width="290" /><img src="../../drivers/omron.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Der Anschluss des HMI ist DB9F, der der SPS der Serie SYSMAC C/CPM/CS/CJ DB9M.

**2. Softwareeinstellungen**

Wählen Sie unter „Geräteservice“ OMRON.

Wählen Sie unter „Geräteservice“ den Eintrag, der zum angeschlossenen SPS-Modell bzw. zum unterstützten Protokoll passt.

Die Kommunikationsparameter des Touchscreens und die SPS-Stationsnummer müssen mit der angeschlossenen SPS übereinstimmen.

Zu den Einstellungen der SPS siehe die technischen Unterlagen der SPS der Serie SYSMAC C/CPM/CS/CJ.

Standard-Verbindungsparameter der HMI der HM-Serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Einstellung**            | **Standardwert** | **Einstellbereich**                            |
| **SPS-Typ**                | Serie SYSMAC C/CPM         | Serie SYSMAC C/CPM/CS/CJ                    |
| **Schnittstellentyp** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Datenbits**         | 7                           | 7/8                                          |
| **Parität**              | EVEN                        | EVEN/ODD/NONE                                |
| **Stoppbits**         | 2                           | 1/2                                          |
| **SPS-Stationsnummer**      | 0                           | 0~255                                        |
| **HMI-Stationsnummer**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Funktion** | **Unterstützt** |
| **Offline-Simulation** | Ja                         |
| **Online-Simulation**  | Ja                         |
| **Erweiterter Modus**       | Nein                          |

**3. Verwendbare Register und Adressbereiche**

Serie SYSMAC C/CPM

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                                                      |
| **IR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Ein-/Ausgangsrelais                                                                                          |
| **HR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Halterelais                                                                                                  |
| **LR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Link-Relais                                                                                                  |
| **AR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Hilfsmerker                                                                                      |
| **T**             | ddd                | 0~255           | Bit: Timerstatus                                                                                             |
| **C**             | ddd                | 0~255           | Bit: Zählerstatus                                                                                           |
| **IR**            | dddd               | 0~4095          | Wort: Ein-/Ausgangsrelais                                                                                         |
| **HR**            | dddd               | 0~4095          | Wort: Halterelais                                                                                                 |
| **LR**            | dddd               | 0~4095          | Wort: Link-Relais                                                                                                 |
| **AR**            | dddd               | 0~4095          | Wort: Hilfsmerker                                                                                     |
| **TC**            | ddd                | 0~255           | Wort: Wert des Timers                                                               |
| **DM**            | dddd               | 0~9999          | Wort: Gemeinsamer Datenbereich |

Serie SYSMAC CS/CJ

|                   |                    |                 |                                                                                         |
|-------------------|--------------------|-----------------|-----------------------------------------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                                                             |
| **CIO_Bit**       | dddd.DD            | 0.0~3189.15     | Bit: E/A-Kernbereich                                        |
| **W_Bit**         | dddd.DD            | 0.0~6143.15     | Bit: Arbeitsbereich                                            |
| **H_Bit**         | dddd.DD            | 0.0~511.15      | Bit: Haltebereich                                         |
| **A_Bit**         | dddd.DD            | 0.0~959.15      | Bit: Hilfsbereich, nur lesen: 7.168 Bit: A00000～A447.15 |
| **D_Bit**         | dddd.DD            | 0.0~32767.15    | Bit: Gemeinsamer Datenbereich                                     |
| **T**             | dddd               | 0~4095          | Bit: Timerstatus                                                                    |
| **C**             | dddd               | 0~4095          | Bit: Zählerstatus                                                                  |
| **CIO**           | dddd               | 0~3189          | Wort: E/A-Kernbereich                                                                     |
| **W**             | dddd               | 0~6143          | Wort: Arbeitsbereich                                                                         |
| **H**             | dddd               | 0~511           | Wort: Haltebereich                                                                      |
| **A**             | dddd               | 0~959           | Wort: Hilfsbereich, nur lesen: 448 Worte: A000～A447                                    |
| **D**             | dddd               | 0~32767         | Wort: Gemeinsamer Datenbereich                                                                  |
| **TV**            | dddd               | 0~4095          | Wort: Istwert des Timers                                                            |
| **CV**            | dddd               | 0~4095          | Wort: Istwert des Zählers                                                          |

CP1L Tcp/Ip       / Fins-udp

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Registername** | **Adressformat** | **Eingabebereich** | **Bemerkungen**                                               |
| **CIO_Bit**       | dddd.DD            | 0.0~3189.15     | Bit: E/A-Kernbereich                                        |
| **W_Bit**         | dddd.DD            | 0.0~6143.15     | Bit: Arbeitsbereich                                            |
| **H_Bit**         | dddd.DD            | 0.0~511.15      | Bit: Haltebereich                                         |
| **A_Bit**         | dddd.DD            | 0.0~959.15      | Bit: Hilfsbereich, nur lesen: 7.168 Bit: A00000～A447.15 |
| **D_Bit**         | dddd.DD            | 0.0~32767.15    | Bit: Gemeinsamer Datenbereich                                     |
| **T**             | dddd               | 0~4095          | Bit: Timerstatus                                      |
| **C**             | dddd               | 0~4095          | Bit: Zählerstatus                                    |
| **CIO**           | dddd               | 0~3189          | Wort: E/A-Kernbereich                                       |
| **W**             | dddd               | 0~6143          | Wort: Arbeitsbereich                                           |
| **H**             | dddd               | 0~511           | Wort: Haltebereich                                        |
| **A**             | dddd               | 0~959           | Wort: Hilfsbereich, nur lesen: 448 Worte: A000～A447      |
| **D**             | dddd               | 0~32767         | Wort: Gemeinsamer Datenbereich                                    |
| **TV**            | dddd               | 0~4095          | Wort: Istwert des Timers                              |
| **CV**            | dddd               | 0~4095          | Wort: Istwert des Zählers                            |

<img src="../../drivers/omron.files/image010.gif" width="595" />

Hinweis:

d: dezimal, Eingabebereich 0-9;

DD: 16 Bit; Eingabebereich 0-15;

Wort in den Bemerkungen: Das Register ist nur als Wort verwendbar;

Bit in den Bemerkungen: Das Register ist nur als Bit verwendbar;

Nur lesen in den Bemerkungen: Das Register kann gelesen, aber nicht beschrieben werden;

Namen und Bereiche der Register können je nach Gerätemodell verschieden sein.

Genaue Namen und Bereiche entnehmen Sie der technischen Dokumentation des angeschlossenen Geräts

<img src="../../drivers/omron.files/image011.gif" width="595" />

 Hinweise zur Verbindung CP1L TCP/IP: Einstellung

-&gt; integriertes Ethernet -&gt; IP-Adresse und Port einstellen. Hinweis:

Empfohlen wird die Kommunikation über FINS-UDP: Damit können mehrere Touchscreens mit derselben SPS verbunden werden; vor der normalen Kommunikation ist ein Verbindungsaufbau (Handshake) nötig, der etwas Zeit braucht

Hinweise zur Verbindung FINS-UDP:

Einstellung -&gt; integriertes Ethernet -&gt; IP-Adresse und Port einstellen

Die Knotennummer in der FINS-UDP-Konfiguration muss mit der Knotennummer in den Ethernet-Einstellungen der Omron-SPS übereinstimmen

<img src="../../drivers/omron.files/image008.jpg" width="500" alt="image009.jpg" />
