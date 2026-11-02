# Kamera

Das Objekt Kamera nimmt Videos auf oder erfasst Bilder einer externen Kamera; die Einstellungsseite des Objekts sieht so aus:

![](../../../configuration-guide/new_add_control/camera.files/001.png)

USB: Für eine per USB angeschlossene Kamera ist eine HMI-Systemversion Linux 4.9.84 (001) oder höher erforderlich;

Netzwerkkamera: Das Eingangsformat ist RTSP; bei einer Hikvision-Kamera z. B. lautet der Stream:

admin:xl123456@192.168.1.63:554/ch1/sub/av_stream;

Aufbau des Streams: Kontoname:Passwort@IP-Adresse: Die ersten vier Angaben legt der Benutzer anhand der Kameraparameter fest, der Rest ist durch die Kameramarke vorgegeben.

Tipp!

Ist die Auflösung einer USB- oder Netzwerkkamera zu hoch, ruckelt oder verzögert die Wiedergabe auf dem Touchscreen; Auflösung, Bildrate usw. des Streams müssen dann verringert werden. USB-Kameras unterstützen MJPEG-Videostreams, Netzwerkkameras müssen H.264-Streams liefern. Hikvision-Kameras wurden getestet; bei anderen Marken ist ein eigener Test nötig.

Aufnahmefunktion: Nach Aktivierung der adressgesteuerten Aufnahme wird auf dem USB-Stick ein Ordner „video“ angelegt, in dem die Videos oder Bilder gespeichert werden.

Aufnahmeformat: Bei Format „Bild“ können höchstens 60 s an Bildern aufgezeichnet werden. Netzwerkkameras speichern Videos als MP4, USB-Kameras als AVI.

Bild: Bei Aufnahmeformat „Bild“ wird die Datei im JPG-Format gespeichert.

\[Import starten/stoppen\]: Bei Eingabe 1 wird die Kamera eingeschaltet und der Videostream importiert; bei 0 wird die verbundene Kamera ausgeschaltet und der Stream geschlossen. \[Pausensteuerung\]: Hält die Anzeige des Kamerabilds an, das Video wird weiter übertragen. Bei der Steueradresse muss nur die Start-/Endadresse eingestellt werden; die Pausenadresse ist die Startadresse plus 1.

Beispiel: Ist die Start-/Importadresse LW N, ist die Pausenadresse LW N+1.

Zur Seite „Anzeige“ siehe die Bit-Taste.
