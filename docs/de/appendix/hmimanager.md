# Verwendung von HMIManager

Öffnen Sie die Seite der Download-Tools

![](../../appendix/hmimanageer.files/002.png)

Seite „Download“:

Kommunikationseinstellung:
USB: PC über USB mit dem HMI verbunden
WAN: PC über Ethernet mit dem HMI verbunden

Mit der Schaltfläche „Scan“ können Sie auch nach IP-Adressen suchen

![](../../appendix/hmimanageer.files/a1.png)

Die gefundene IP-Adresse können Sie prüfen und im Änderungsfeld darunter ändern

![](../../appendix/hmimanageer.files/a2.png)

Klicken Sie auf die Schaltfläche rechts, um die Angaben zu ändern; nach Abschluss erscheint ein Popup-Fenster.

![](../../appendix/hmimanageer.files/a3.png)

Klicken Sie dann auf „Rescan“: Die geänderten Werte werden in der Liste angezeigt.

![](../../appendix/hmimanageer.files/a4.png)

Markieren Sie die gewünschte IP-Adresse und klicken Sie auf „Select“, um das Ziel auszuwählen; die IP-Angaben werden in das Download-Fenster übernommen.

**Achtung!**

Für die IP-Suche müssen die folgenden drei Voraussetzungen erfüllt sein:

1. Bei Touchpanels, die vor dem 30. Dezember 2024 hergestellt wurden, muss das entsprechende IP-Scan-Patch manuell eingespielt werden; wenn die Datei „hmi.patch“ im Installationsverzeichnis fehlt, wenden Sie sich an den technischen Support.
     2. Die Version der Projektierungssoftware muss mindestens HMITOOLV7.1_022 sein
     3. Die Firmware-Version muss mindestens Simulator 8.1.0.10 sein.

Download-Auswahl:
Projekt herunterladen: Erzeugen Sie zunächst die Projektdatei u-disk-prj.bin; in der Projektierungssoftware wählen Sie dazu Download-&gt;Projekt extrahieren und speichern unter-&gt;u-disk-prj.bin erzeugen. Klicken Sie auf „Browse“, um die Datei auszuwählen, dann auf „Start“, um das Projekt im HMI zu aktualisieren.
Rezepte herunterladen: Kompilieren Sie das bearbeitete HMI-Projekt; im Unterverzeichnis „compile“ des Installationsverzeichnisses werden die Dateien recipe60.bin und recipe62.bin erzeugt. Bis einschließlich Version 6.0 wählen Sie recipe60.bin, ab einer höheren Version als 6.0 recipe62.bin. Klicken Sie auf „Browse“, um die Datei auszuwählen, und dann auf „Start Download“.

![](../../appendix/hmimanageer.files/003.png)

Seite „Upload“:

Kommunikationseinstellung:
Wie beim Download.

Upload-Auswahl:
Upload-Bereich: Ein Projekt kann nur hochgeladen werden, wenn dies in den Touchscreen-Parametern erlaubt ist; Rezepte, historische Daten und historische Alarme lassen sich nur hochladen, wenn sie im laufenden HMI-Programm vorhanden sind.
Historische Daten hochladen: Legen Sie mit „Browse“ Speicherort und Dateiname fest und klicken Sie auf „Start Upload“, um die ZIP-Datei und die .csv-Datei der historischen Daten hochzuladen; siehe „Historische Daten hochladen“.
Projekt hochladen: Legen Sie mit „Browse“ Speicherort und Dateiname fest und klicken Sie auf „Start Upload“, um die ZIP-Datei des Projekts hochzuladen; nach dem Entpacken lässt sich die Projektdatei normal ansehen und bearbeiten, siehe „Projekt hochladen“.
Rezepte hochladen: Legen Sie mit „Browse“ Speicherort und Dateiname fest und klicken Sie auf „Start Upload“, um die Rezeptdatei aus dem HMI hochzuladen.
Historische Alarme hochladen: Legen Sie mit „Browse“ Speicherort und Dateiname fest und klicken Sie auf „Start Upload“, um die Alarmdatei aus dem HMI hochzuladen.

![](../../appendix/hmimanageer.files/004.png)

Seite „Version“:

Kommunikationseinstellung:
Wie beim Download.

Versionsinformationen: Version des aktuell verbundenen HMI.

![](../../appendix/hmimanageer.files/005.png)

Seite „Firmware“:

Kommunikationseinstellung:
Wie beim Download.

Firmware-Info
Firmware-Informationen: Wählen Sie mit „Browse“ die Firmware aus, die aktualisiert werden soll, und klicken Sie auf „Upgrade“

![](../../appendix/hmimanageer.files/006.png)

Seite „Simulation“:

Wählen Sie die Projektdatei .vpm aus, um eine Online- oder Offline-Simulation auszuführen.

![](../../appendix/hmimanageer.files/007.png)

Seite „Adresse“:

Service: Auswahl des Geräteherstellers.
Model: Auswahl des passenden Gerätemodells
Zeigt alle Adressangaben des ausgewählten Geräts an.
