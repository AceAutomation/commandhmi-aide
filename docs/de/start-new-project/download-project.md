# Projekt laden (Download)

<img src="../../start-new-project/download-project.files/image012.jpg" width="368" />

Abbildung 3-11    Meldung über Kompilierfehler

Korrigieren Sie den Fehler anhand der Meldung im Ausgabefenster; oder doppelklicken Sie auf den Fehler, dann findet und markiert CommandHMI das fehlerhafte Objekt automatisch. Per Doppelklick auf das Objekt lassen sich seine Eigenschaften anzeigen, die Fehlerursache finden und korrigieren. Klicken Sie dann auf „Speichern“, um erneut zu kompilieren. Ohne Fehler meldet das System nach kurzer Zeit die erfolgreiche Kompilierung. Klicken Sie zum Abschluss auf „OK“, wie in Abbildung 3-12:

<img src="../../start-new-project/download-project.files/image013.jpg" width="364" />

Abbildung 3-12    Ausgabefenster

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Vor dem Download muss kompiliert und vor dem Kompilieren gespeichert werden; sonst schlägt die Kompilierung fehl, wie in Abbildung 3-11. Nach jeder weiteren Änderung muss erneut kompiliert werden.

<img src="../../start-new-project/download-project.files/image014.jpg" width="425" />

Abbildung 3-13    Hinweis zur Kompilierung

Führen Sie schließlich den Befehl USB im Menü „Download“ aus, um über ein USB-Kabel zu laden; alternativ wählen Sie direkt „Kompilieren + Download“ im Menü „Download“. Es öffnet sich das Dialogfeld in Abbildung 3-14:

<img src="../../start-new-project/download-project.files/image015.jpg" width="716" />

Abbildung 3-14    Dialogfeld Download

Klicken Sie auf „Download“; der Fortschrittsbalken zeigt den Fortschritt. Danach meldet ein Fenster den Abschluss des USB-Downloads. Klicken Sie auf „OK“, wie in Abbildung 3-15:

<img src="../../start-new-project/download-project.files/image005.jpg" width="720" alt="2018_11_20_09_02_42.jpg" />

Abbildung 3-15    Download abgeschlossen

Im nächsten Schritt wird die SPS angeschlossen, um zu prüfen, ob das Projekt im HMI korrekt läuft.

Die Verbindungsarten zwischen HMI und SPS oder PC beschreibt das Kapitel „Verbindung“ im Hardware-Handbuch.

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Trennen Sie während der Übertragung weder die Stromversorgung von HMI oder PC noch das USB-Kabel und führen Sie keine anderen Bedienungen aus; sonst wird die Übertragung gestört.

Installieren Sie vor dem Download die USB-Treiber; sonst kann der PC keine Verbindung zum HMI herstellen und der Download nicht durchgeführt werden.

<img src="../../start-new-project/download-project.files/image017.jpg" width="716" />

Abbildung 3-16    Hinweis zum USB-Treiber

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Das Dialogfeld in Abbildung 3-16 bedeutet, dass der PC das HMI nicht erkennt. Prüfen Sie dann, ob der USB-Treiber installiert ist: Verbinden Sie den PC mit dem eingeschalteten HMI und suchen Sie „CommandHMI HMI Tech Corp USB drive“ unter Windows „Arbeitsplatz“ – „Eigenschaften“ – „Hardware“ – „Geräte-Manager“ – „USB-Controller“ (ziehen Sie ggf. das USB-Kabel ab, um zu prüfen, ob der PC das HMI erkennt):

**Projekt-Download über Ethernet**

• Netzwerkparameter des HMI einstellen

Schalten Sie DIP-Schalter 1 und 3 gemeinsam ein; stellen Sie IP (hier 192.168.1.100), Gateway, Subnetz und Port ein. Der Port ist fest 12345.

• Projekt kompilieren

Beim Download über Ethernet müssen IP-Adresse und Portnummer im Eingabefeld angegeben werden. Die IP ist die des Ziel-HMI, hier wie oben 192.168.1.100; der Port ist fest 12345. Klicken Sie dann auf „Neustart und Download“, wie in Abbildung 3-18:

![](../../start-new-project/download-project.files/001.png)

Abbildung 3-18 Projekt-Download über Ethernet

Mit der Schaltfläche „Scan“ können Sie auch nach IP-Adressen suchen

![](../../start-new-project/download-project.files/002.png)

Die gefundene IP-Adresse können Sie prüfen und im Änderungsfeld darunter ändern

![](../../start-new-project/download-project.files/003.png)

Klicken Sie auf die Schaltfläche rechts, um die Angaben zu ändern; nach Abschluss erscheint ein Popup-Fenster.

![](../../start-new-project/download-project.files/004.png)

Klicken Sie dann auf „Rescan“: Die geänderten Werte werden in der Liste angezeigt.

![](../../start-new-project/download-project.files/005.png)

Markieren Sie die gewünschte IP-Adresse und klicken Sie auf „Select“, um das Ziel auszuwählen; die IP-Angaben werden in das Download-Fenster übernommen.

**Achtung!**

Für die IP-Suche müssen die folgenden drei Voraussetzungen erfüllt sein:

1. Bei Touchpanels, die vor dem 30. Dezember 2024 hergestellt wurden, muss das entsprechende IP-Scan-Patch manuell eingespielt werden; wenn die Datei „hmi.patch“ im Installationsverzeichnis fehlt, wenden Sie sich an den technischen Support.
     2. Die Version der Projektierungssoftware muss mindestens HMITOOLV7.1_022 sein
     3. Die Firmware-Version muss mindestens Simulator 8.1.0.10 sein.

![](../../start-new-project/download-project.files/006.png)
