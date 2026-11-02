# FAQ und Lösungen

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>       <strong>No.</strong></p></td>
<td colspan="2"><p><strong>Symptom</strong></p></td>
<td><p><strong>Ursache</strong></p></td>
<td><p><strong>Abhilfe</strong></p></td>
</tr>
<tr class="even">
<td rowspan="6"><p><strong>Anzeige</strong></p></td>
<td rowspan="5"><p>Schwarzer Bildschirm</p></td>
<td rowspan="3"><p>Schwarzer Bildschirm nach dem Einschalten</p></td>
<td><p>Probleme mit der Stromversorgung</p></td>
<td><p>1、Anschluss der Stromversorgung prüfen; 2、Art der Versorgung prüfen; ist sie keine eigene 24-V-DC-Versorgung (±20 %), austauschen.</p></td>
</tr>
<tr class="odd">
<td><p>Fehler im Projekt, z. B. falsch verwendete Skripte: Nullzeiger, ungültige Zeiger, Feldüberlauf oder Division durch 0.</p></td>
<td><p>DIP-Schalter 2 auf ON stellen und das Projekt zum Test erneut herunterladen; läuft ein Skript fehlerhaft, es debuggen und korrekt programmieren.</p></td>
</tr>
<tr class="even">
<td><p>Gerätedefekt: Korrosion am Flachbandkabel des LCD, Problem mit dem Quarzoszillator usw.</p></td>
<td><p>Wenden Sie sich zur Werksreparatur an den Kundendienst.</p></td>
</tr>
<tr class="odd">
<td rowspan="2"><p>Plötzlich schwarzer Bildschirm im Betrieb, gelegentlich schwarzer Bildschirm oder Absturz</p></td>
<td><p>Problem mit der Stromversorgung</p></td>
<td><p>Versorgungsleitung und Stromversorgung prüfen.</p></td>
</tr>
<tr class="even">
<td><p>Gerätedefekt</p></td>
<td><p>Wenden Sie sich zur Werksreparatur an den Kundendienst.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Linien auf dem Bildschirm, senkrecht oder waagerecht</p></td>
<td><p>LCD-Defekt</p></td>
<td><p>Treten die Linien in jedem Bild auf, wenden Sie sich zur Werksreparatur an den Kundendienst.</p></td>
</tr>
<tr class="even">
<td rowspan="4"><p><strong>Touch</strong></p></td>
<td colspan="2" rowspan="2"><p>Träge Touch-Reaktion, Objekte schwer bedienbar</p></td>
<td><p>Einbauproblem</p></td>
<td><p>1. Prüfen, ob der Einbauausschnitt zu klein ist und das HMI einklemmt; gegebenenfalls mit korrektem Ausschnitt einbauen; 2. Prüfen, ob die Befestigungsschrauben zu fest angezogen sind, und auf möglichst gleichmäßigen Druck an allen vier Ecken achten.</p></td>
</tr>
<tr class="odd">
<td><p>Ungeeignetes Projekt</p></td>
<td><p>Zu viele Projektdaten, Hintergrundskripte und zu viele Variablen und Objekte in den Bildern; Projekt überarbeiten und Objekte und Bilder sinnvoll verteilen bzw. reduzieren.</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Touch-Ausfall</p></td>
<td><p>Koordinatenkalibrierung oder beschädigtes Touchpanel</p></td>
<td><p>1. DIP-Schalter 1 auf ON stellen und die Koordinatenkalibrierung ausführen;</p>
<p>2. <span id="OLE_LINK4"></span><span id="OLE_LINK3"></span>Hilft das nicht, wenden Sie sich zur Werksreparatur an den Kundendienst.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Falsche Zuordnung (auf der Tastatur wird A gedrückt, aber X oder ein anderes Zeichen angezeigt)</p></td>
<td><p>Touchpanel-Defekt</p></td>
<td><p>Wenden Sie sich zur Werksreparatur an den Kundendienst.</p></td>
</tr>
<tr class="even">
<td rowspan="9"><p><strong>Kommunikationsfehler</strong></p></td>
<td rowspan="6"><p>Kommunikationsausfall zwischen HMI und Steuerung</p></td>
<td rowspan="3"><p>Kommunikation ist nie möglich</p></td>
<td><p>Defekt der Kommunikationsgeräte (SPS, Mikrocontroller usw.)</p></td>
<td><p>Zustand der Kommunikationsschnittstelle prüfen und Kommunikationsparameter erneut abgleichen.</p></td>
</tr>
<tr class="odd">
<td><p>Defekt der Kommunikationsschnittstelle des HMI</p></td>
<td><p>Wenden Sie sich zur Werksreparatur an den Kundendienst.</p></td>
</tr>
<tr class="even">
<td><p>Unterbrechung des Kommunikationskabels</p></td>
<td><p>Möglichst das Originalkabel von CommandHMI verwenden.</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>Kommunikationsabbruch nach einiger Zeit normalen Betriebs</p></td>
<td><p>Korrosion und Oxidation an den Anschlüssen der Kommunikationsleitung nach langem Betrieb.</p></td>
<td><p>Kommunikationsleitung austauschen oder neu löten.</p></td>
</tr>
<tr class="even">
<td><p>Störeinflüsse aus der Umgebung</p></td>
<td><p>Störquellen abschirmen; geschirmte Leitung verwenden; ordnungsgemäß erden</p></td>
</tr>
<tr class="odd">
<td><p>Defekt des HMI (durch starke Magnetfelder, Ströme oder Blitzeinschlag vor Ort)</p></td>
<td><p>Wenden Sie sich zur Werksreparatur an den Kundendienst.</p></td>
</tr>
<tr class="even">
<td colspan="2" rowspan="3"><p>HMI verbindet sich nicht mit dem PC, Download nicht möglich.</p></td>
<td><p>USB-Treiber des PC falsch installiert</p></td>
<td><p>Passenden Treiber für das Betriebssystem wählen und USB-Treiber neu installieren.</p></td>
</tr>
<tr class="odd">
<td><p>Größe und Modell des HMI stimmen nicht mit dem tatsächlichen Gerät überein.</p></td>
<td><p>In der Projektierungssoftware das richtige HMI-Modell einstellen.</p></td>
</tr>
<tr class="even">
<td><p>Download-Schnittstelle des HMI beschädigt</p></td>
<td><p>Wenden Sie sich zur Werksreparatur an den Kundendienst. (Prüfung: Ein anderes HMI mit demselben USB-Kabel und PC verbinden; funktioniert der Download, liegt der Fehler an der USB-Schnittstelle des HMI.)</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p><strong>Anwendung</strong></p></td>
<td colspan="2"><p>Projekt funktioniert nicht</p></td>
<td><p>Unzulässiges Objekt oder Skript im Projekt</p></td>
<td><p>Projekt korrigieren</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Skript lässt sich nicht kompilieren</p></td>
<td><p>Installationsverzeichnis von HM in den Umgebungsvariablen</p></td>
<td><p>Das Installationsverzeichnis von CommandHMI in den Umgebungsvariablen nach vorne stellen.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Offline- und Online-Simulation funktionieren nicht.</p></td>
<td><p>Ausführung ohne Administratorrechte</p></td>
<td><p>CommandHMI als Administrator ausführen</p></td>
</tr>
</tbody>
</table>
