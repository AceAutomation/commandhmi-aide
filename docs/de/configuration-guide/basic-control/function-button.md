# Funktionstaste

Die Funktionstaste ist ein zentrales Objekt des HMI; mit ihr lassen sich zahlreiche Funktionen schnell und einfach umsetzen. Klicken Sie auf <img src="../../../configuration-guide/basic-control/function-button.files/function-button143.png" width="28" />, um das Eigenschaftsdialogfeld der Funktionstaste zu öffnen, wie in Abbildung 4-82:

<img src="../../../configuration-guide/basic-control/function-button.files/function-button223.png" width="660" />

Abbildung 4-82 Dialogfeld Funktionstaste

<img src="../../../configuration-guide/basic-control/function-button.files/function-button264.png" width="130" />

Hinweis: Form, Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster siehe Objekt „Bit-Taste“.

**1. Hintergrundbeleuchtung ausschalten**

Funktion „Hintergrundbeleuchtung ausschalten“: Durch Antippen der Taste wird die Beleuchtung ausgeschaltet, das HMI arbeitet weiter normal. Zum Einschalten genügt eine Berührung an beliebiger Stelle des Touchscreens.

**2. Alarm quittieren**

Funktion „Alarm quittieren“: Durch Antippen der Taste wird der ausgewählte Alarm quittiert

**3. Neustart**

Ist die Funktionstaste auf „Systemneustart“ eingestellt, startet der Touchscreen beim Antippen neu.

**4. Bildschirmschoner-Zeit einstellen**

Ist die Funktionstaste auf „Bildschirmschoner-Zeit einstellen“ eingestellt, öffnet sich beim Antippen ein Fenster zur Einstellung der Bildschirmschoner-Zeit.

**5. Rezept in die SPS schreiben**

Mit dieser Funktion wird das Rezept an die SPS übertragen: Beim Antippen der Taste wird das im HMI gespeicherte aktuelle Rezept in die entsprechenden zusammenhängenden Datenregister der SPS oder eines anderen Geräts übertragen. (Die Adresse ist die bei der Rezepterstellung in der Software festgelegte Schreibadresse.)

**6. Rezept aus der SPS lesen**

Mit dieser Funktion wird das Rezept aus der SPS gelesen: Beim Antippen der Taste werden die Rezeptdaten aus den entsprechenden zusammenhängenden Datenregistern der SPS oder eines anderen Geräts gelesen. (Die Adresse ist die bei der Rezepterstellung in der Software festgelegte Schreibadresse.)

**7. Datum und Uhrzeit einstellen**

Mit dieser Funktion werden Datum und Uhrzeit eingestellt: Beim Antippen der Taste lassen sich die interne Uhrzeit und das Datum einstellen.

**8. Alarm löschen**

Mit dieser Funktion werden Alarme gelöscht: Beim Antippen der Taste wird der ausgewählte, quittierte Alarm gelöscht.

**9. Vorheriges Rezept**

Mit der Funktion „Vorheriges Rezept“ wird beim Antippen das Rezept vor dem aktuellen geöffnet. Ist das aktuelle Rezept das erste oder gibt es nur ein Rezept, ändern sich die Rezeptparameter nicht.

**10. Nächstes Rezept**

Mit der Funktion „Nächstes Rezept“ wird beim Antippen das Rezept nach dem aktuellen geöffnet. Ist das aktuelle Rezept das letzte oder gibt es nur ein Rezept, ändern sich die Rezeptparameter nicht.

**11. Aktuelles Rezept speichern**

Mit dieser Funktion wird das aktuelle Rezept gespeichert: Beim Antippen der Taste werden die Rezeptdaten aus den entsprechenden zusammenhängenden Datenregistern der SPS oder des Geräts gespeichert, die bei der Rezepterstellung in der Software festgelegt wurden.

**12. Screenshot**

Ist die Funktionstaste auf „Screenshot“ eingestellt, wird beim Antippen das aktuelle Bild als Grafik am vom Benutzer festgelegten Ort gespeichert. Der Grafikname kann über eine ASCII-Eingabe angegeben werden; er darf keine Zeichen wie ：#￥%&\*-+&lt;&gt; enthalten und höchstens 20 Zeichen lang sein.

**13. Systemparameter**

Funktion „Systemparameter“: Beim Antippen auf dem HMI öffnet sich das Bild der Systemparameter, in dem sich z. B. Systemzeit, Bildschirmschoner-Zeit und Kontrast der Hintergrundbeleuchtung ändern lassen.

**14. Anmelden**

Funktion „Anmelden“: Beim Antippen erscheint ein Anmeldefenster. Nach Auswahl des Benutzernamens erscheint eine Tastatur zur Eingabe des Passworts, mit dem die Zugriffsberechtigung erlangt wird.

**15. Benutzer abmelden**

Funktion „Benutzer abmelden“: Beim Antippen wird der aktuelle Benutzer abgemeldet und seine Berechtigung aufgehoben; die Benutzerebene fällt auf die niedrigste Stufe.

**16. Alarmton (EIN/AUS)**

Funktion „Alarmton EIN/AUS“: Bei einem Alarm ertönt ein Signal; mit der Taste wird diese Funktion ein- oder ausgeschaltet. Ist sie eingeschaltet, wird der Alarmton nach dem Antippen stummgeschaltet und umgekehrt

**17. Berührungston (EIN/AUS)**

Funktion „Berührungston EIN/AUS“: Durch Antippen der Taste wird der Berührungston ein- bzw. ausgeschaltet. Ist er gerade eingeschaltet, wird er nach dem Antippen ausgeschaltet und umgekehrt.

**18. Alle historischen Daten löschen**

Die im HMI gespeicherten historischen Daten werden gelöscht.

**19. Historische Alarme löschen**

Die im HMI gespeicherten historischen Alarme werden gelöscht.

**20. HMI-Schutz entsperren**

Passwort eingeben, um den HMI-Schutz aufzuheben.

**21. Rezept lesen und speichern**

Liest das Rezept und speichert es.

**22. Reservefunktion**

Nur als Reserve vorgesehen, führt keine Aktion aus.

**23. Rezept neu laden**

Lädt die Rezeptdaten aus dem Flash erneut in die entsprechenden RWI-Adressen.

**24. Sprache wechseln**

Schaltet die Texte aller Objekte auf eine andere, festgelegte Sprache um

**25. Bild über seriellen Drucker drucken**

Druckt das festgelegte Bild über einen seriellen Drucker. Die Verbindungseinstellungen des Druckertreibers befinden sich links in der Software unter „HMI-Parametereinstellungen“ -&gt; „Drucker- und Download-Einstellungen“.

**26.IP-Konfiguration der Slave-Geräte**

Diese Funktion erfordert den „Erweiterten Modus“, der in den „Eigenschaften der Kommunikationsschnittstelle“ eingestellt wird. Für Ethernet-Kommunikation mit mehreren Geräten müssen vor dem jeweiligen Objekt eine Stationsnummer und die Registeradresse angegeben werden, die diese Stationsnummer steuert. Wird im laufenden HMI-Projekt das Funktionsobjekt angetippt, erscheint die eingestellte Stationsnummer im Dialogfeld „IP config“; dort stellen Sie die IP-Parameter der Station ein, um die Ethernet-Kommunikation mit mehreren Geräten herzustellen.

**27. Funktionen der DIP-Schalter 1 und 3**

Funktionen, die bei eingeschalteten DIP-Schaltern 1 und 3 am Gerät verfügbar sind: im Wesentlichen IP-Einstellung, Systemzeit und Parameter der Hintergrundbeleuchtung. Nach der Einstellung mit OK bestätigen und neu starten.

Skript verwenden (Use Macro): Mit „Skript verwenden“ wird eine Skriptliste angezeigt; der Benutzer kann ein Skript wählen, das beim Ausführen der Funktion ausgeführt wird. Nur kompilierte Skripte erscheinen in der Liste.

<img src="../../../configuration-guide/basic-control/function-button.files/function-button6119.png" width="130" />

Hinweis: Beim Wechsel in das Systembild schließt das System das aktuelle Projekt; bei der Rückkehr aus dem Systembild wird das Projekt neu gestartet und das eingestellte Startbild angezeigt.

Hinweis: Die Seite „Beschriftung“ der Funktionstaste entspricht weitgehend der der „Bit-Taste“; da die Funktionstaste nur einen Zustand hat, fehlen „Text Zustand 1“ und „Grafik Zustand 1“.

Hinweis: Die Seiten „Erweitert“ und „Sichtbarkeit“ der Funktionstaste entsprechen denen der Bit-Taste; zur Verwendung von Tastenkürzeln siehe ebenfalls die Bit-Taste.

Hinweis: „Vorheriges Rezept“, „Nächstes Rezept“, „Rezept speichern“ und „Rezept lesen und speichern“ wirken nur auf die aktuelle Rezeptgruppe. Für eine andere Gruppe stellen Sie zuvor LW61141 ein.

Hinweis: „Historische Daten löschen“ löscht alle Gruppen historischer Daten.

Klicken Sie nach allen Einstellungen auf „OK“, um das Objekt in den Ansichtsbereich (das Bild) einzufügen
