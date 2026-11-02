# Parameter einstellen und Grafikobjekte hinzufügen

**Parameter:**

1\. Die Parameter lassen sich über „Voreinstellungen“ im Menü „Einstellungen“ ändern oder durch Doppelklick auf [HMI-Parametereinstellungen](../setting/paramater.md) unter „Einstellungen“ im Projektmanager. Es öffnet sich das Dialogfeld in Abbildung 3-6:

<img src="../../start-new-project/setting-parameter.files/image001.jpg" width="643" alt="ScreenShot00218.jpg" />

Abbildung 3-6     Dialogfeld Allgemeine Parametereinstellungen

• HMI-Modell: ändert das HMI-Modell.

• Anzeigemodus: Bildschirm horizontal oder vertikal.

• HMI-Starteinstellungen

• Startbild: Bild, das beim Einschalten des HMI angezeigt wird

• Bildschirmschonerzeit: Wartezeit bis zum Bildschirmschoner

• Blinkfrequenz: Blinkfrequenz blinkfähiger Objekte; die Geschwindigkeit wird durch direkte Eingabe eines Werts oder mit den Pfeiltasten geändert.

• Alarmton: Bei einem Alarm kann der Touchscreen den Benutzer akustisch warnen; die Auswahlliste rechts bietet mit oder ohne Ton.

• Berührungston: Die Auswahlliste rechts bietet „Mit Ton“ oder „Ohne Ton“.

• Bildschirmschoner-Bild: Ein vorhandenes Bild wird als Bildschirmschoner gewählt; eine Berührung kehrt zum vorherigen Bild zurück.

• Ladebild: Ist diese Option aktiviert, zeigt das HMI nach dem Einschalten eine Zeit lang das gewählte Ladebild und wechselt dann zum Startbild; so können Hinweise angezeigt werden.

• Weitere Einstellungen

• Mauszeiger ausblenden: legt fest, ob der Mauszeiger angezeigt wird

• Gleitkomma-Einstellungen:

\[Standard\]: höherwertiges Byte zuerst, niederwertiges danach;

\[Benutzerdefiniert\]: Der Benutzer legt die Reihenfolge fest.

• Ungültige Berührung: Ist „Benutzerdefinierte Markierung verwenden“ gewählt, sind sperrbare Objekte nicht bedienbar und werden mit der vom Benutzer gewählten Grafik gekennzeichnet.

• Druckeffekt der Objekte anzeigen: In CommandHMI neu hinzugefügt. Ist der Druckeffekt aktiviert, erscheint beim Berühren eines Objekts ein rechteckiger Rahmen in frei wählbarer Farbe. Derzeit unterstützen Bit-Taste, Wort-Taste, Bildwechsel-Taste, Funktionstaste, numerische Eingabe und ASCII-Eingabe diesen Effekt. Standard: kein Effekt.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2109.png" width="130" />

Auch bei elliptischen Objekten ist der Druckeffekt rechteckig.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2172.png" width="230" />

Abbildung 3-7

2、Benutzerpasswort einstellen

<img src="../../start-new-project/setting-parameter.files/setting-parameter2206.png" width="692" />

Abbildung 3-8     Benutzerpasswort in den HMI-Parametereinstellungen

Diese Funktion bietet 8 Benutzerpasswörter mit je acht Passwortebenen.

• Standard-Benutzerebene: Die aktuelle Standard-Benutzerebene ist NULL.

• Hochladen des Projekts erlauben: Ist diese Option aktiviert, kann das Projekt vom HMI auf den PC hochgeladen werden, sonst nicht.

• Passwort beim Hochladen: legt fest, ob zum Hochladen ein Passwort nötig ist.

• Passwort für Projektaktualisierung per USB-Stick: Ist es festgelegt, muss es beim Aktualisieren des HMI-Projekts über einen USB-Stick eingegeben werden.

• Höchstes Berechtigungspasswort: Mit diesem Passwort lassen sich alle durch Ebenen eingeschränkten Objekte bedienen.

• Hochladen: legt fest, ob dieses Passwort das Hochladen von Projekten vom HMI auf den PC erlaubt.

• Berechtigungen: legt fest, ob dieses Passwort alle eingeschränkten Bedienungen erlaubt.

**3. Einstellungen für Druckerverbindung <span id="OLE_LINK247"></span><span id="OLE_LINK246"></span>und Download**

Klicken Sie auf „Einstellungen der Verbindung zwischen HMI und Drucker“, wie in Abbildung 3-9:

<img src="../../start-new-project/setting-parameter.files/setting-parameter3209.png" width="693" />

Abbildung 3-9      Einstellungen der Verbindung zwischen HMI und Drucker

<span id="OLE_LINK245"></span><span id="OLE_LINK244"></span>Diese Seite enthält die Parameter der Verbindung zwischen Drucker und HMI; wählen Sie die passenden Parameter für das Druckermodell.

**Download-Einstellungen:**

• Download-Modus: Wählen Sie USB oder Ethernet für den Download. Bei Ethernet müssen IP-Adresse und Portnummer (die des HMI) eingestellt werden.

• Historische Alarme löschen: legt fest, ob die historischen Alarme vor dem Download gelöscht werden.

• Historische Daten löschen: legt fest, ob die historischen Daten vor dem Download gelöscht werden.

• Rezepte laden: legt fest, ob die Rezepte des aktuellen Projekts in das HMI geladen werden.

**Optionen für den Grafik-Download:**

• Originalformat beibehalten: Das Grafikformat bleibt beim Download unverändert.

• In JPG umwandeln: Alle Grafiken werden vor dem Download in das HMI in JPG umgewandelt.

(Hinweis: Da BMP-Grafiken viel Speicher belegen, wird diese Option empfohlen.)

4. Speicherort und Alarmsystem, wie unten

<img src="../../start-new-project/setting-parameter.files/setting-parameter4305.png" width="692" />

Abbildung 3-10   Dialogfeld Speicherort und Systemalarm

• Speicherort: Ort für historische Daten, historische Alarme und Bildschirmfotos. Zur Wahl stehen „Lokal (FLASH)“ und „USB-Stick“. Standard: Lokal (FLASH).

• HMI-IP: Netzwerkparameter des Touchscreens

• Alarmsystem

Alarmsystem verwenden: legt fest, ob der Systemalarm verwendet wird. Bei einem Alarm zeigt das Alarmsystem die aktuelle Alarmmeldung je nach Einstellung oben oder unten in jedem Bild an.

Alarm-Hintergrundfarbe, Textfarbe, Schriftart und Schriftgröße: Anzeigeeigenschaften des Alarmsystems, nach Bedarf einstellbar.

Anzeigeart: „Immer anzeigen“ zeigt den Alarm dauernd an; „Zyklisch anzeigen“ blendet ihn periodisch ein und aus und erzeugt so einen Blinkeffekt.

Position der Alarmleiste: Position, an der die Alarmleiste erscheint.

5. Sonstige Einstellungen, wie unten

<img src="../../start-new-project/setting-parameter.files/setting-parameter5287.png" width="690" />

Abbildung 3-11   Passwort zum Entsperren des Bildschirmschoners

• Ist diese Option aktiviert, muss der Benutzer beim Entsperren des Bildschirmschoners dieses Passwort eingeben.

<img src="../../start-new-project/setting-parameter.files/setting-parameter5429.png" width="130" />

Die Bildschirmschonerzeit wirkt erst, wenn ein „Bildschirmschoner-Bild“ gewählt ist; eine Berührung des Bildschirmschoners kehrt zum vorherigen Bild zurück.
