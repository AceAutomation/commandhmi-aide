# Digitale Alarme

Die Alarmeinstellungen dienen zur Anzeige von Alarmen; ohne sie funktionieren Alarmanzeige und Alarmlaufband nicht (sie zeigen die Meldungen der digitalen und analogen Alarme an).

Klicken Sie im Projektmanager mit der rechten Maustaste auf „Alarme“ und wählen Sie „Neuer digitaler Alarm“, wie in Abbildung 7-22:

<img src="../../setting/dig-alarm.files/image001.jpg" width="274" alt="ScreenShot00094.jpg" />

Abbildung 7-22    Alarmprotokoll wählen

Doppelklicken Sie auf „Digitale Alarme“, um das Dialogfeld zu öffnen, wie in Abbildung 7-23:

<img src="../../setting/dig-alarm.files/dig-alarm508.png" width="558" />

Abbildung 7-23    Fortlaufende Bits wählen

So legen Sie digitale Alarme an:

• Geben Sie zuerst die Leseadresse ein; hier wird die interne Adresse LB1 angenommen.

• Wählen Sie in der Spalte „Größe“ (Size) die Gesamtzahl der Alarme, d. h. die Anzahl fortlaufender Bitadressen. Hier wird 6 angenommen.

• Stellen Sie die „Abtastzeit“ (Scanning time) der Bitalarme ein, also die Abtastfrequenz.

• Klicken Sie auf einen Eintrag der Liste und gehen Sie rechts zum Bereich „Meldung“; geben Sie den Alarmtext im Feld „Text“ ein. Hier werden die Meldungen aus Abbildung 7-23 angenommen.

• Ist „Verwenden“ aktiviert, wird der Alarm in der Alarmanzeige oder im Alarmlaufband angezeigt. Andernfalls erscheint die Meldung nicht, auch wenn die Adresse 1 ist. Ist die Adresse 0, wird der Alarm nicht angezeigt.

• OFF-Alarm: Ist diese Option aktiviert, wird der Alarm ausgelöst, wenn die Adresse 0 (OFF) ist, sonst wenn sie 1 (ON) ist. Standard: Alarm bei 1 (ON).

• U-Export: exportiert die Alarmeinstellungen

• U-Import: importiert die Alarmeinstellungen

Beispiel mit dem Typ „Fortlaufende Bits“:

• Ist LB1 gleich 0, wird der Alarm weder in der Alarmanzeige noch im Alarmlaufband angezeigt, unabhängig von „Verwenden“.

• Ist LB1 gleich 1 und „Verwenden“ nicht aktiviert, wird der Alarm weder in der Alarmanzeige noch im Alarmlaufband angezeigt.

• Ist LB1 gleich 1 und „Verwenden“ aktiviert, wird der Alarm in Alarmanzeige und Alarmlaufband angezeigt.

Klicken Sie auf „OK“, um die Einstellung abzuschließen. Fügen Sie 6 Bit-Tasten mit der Funktion „Umschalten“ und den Adressen LB1-LB6 hinzu, platzieren Sie eine Alarmanzeige und ein Alarmlaufband im Bild und prüfen Sie die Anzeige mit der Offline-Simulation.

Beispiel einer Offline-Simulation, Abbildung 7-24:

<img src="../../setting/dig-alarm.files/dig-alarm2644.png" width="1182" />

Abbildung 7-24    Offline-Simulation digitaler Alarme

Ist als Typ „Fortlaufende Bits eines Worts“ gewählt, wie in Abbildung 7-25:

<img src="../../setting/dig-alarm.files/dig-alarm2789.png" width="559" />

Abbildung 7-25    Fortlaufende Bits eines Worts wählen

Ist „Verwenden“ für eine Bitnummer aktiviert, wird ein Alarm ausgelöst, wenn dieses Bit 1 ist.

<img src="../../setting/dig-alarm.files/dig-alarm2952.png" width="130" />

Hinweis: Wenn Sie Alarmtexte aus anderen Dokumenten kopieren, achten Sie darauf, dass sie keinen (unsichtbaren) Zeilenumbruch enthalten. Geben Sie die Texte besser von Hand ein, um Anzeigefehler zu vermeiden.

Ist als Typ „Wortwert“ gewählt, wie in Abbildung 7-26:

<img src="../../setting/dig-alarm.files/dig-alarm3352.png" width="556" />

Abbildung 7-26    Dialogfeld digitaler Alarm „Wortwert“

Der Alarm wird ausgelöst, wenn der Wert der Adresse dem in der Liste gewählten Wert entspricht.

Platzieren Sie eine Alarmanzeige mit 7 Zeilen wie in Abbildung 7-24 und ein dynamisches Alarmlaufband mit den Eigenschaften aus Abbildung 7-27:

<img src="../../setting/dig-alarm.files/dig-alarm3691.png" width="675" />

Abbildung 7-27    Eigenschaften des dynamischen Alarmlaufbands

Fügen Sie zum Schluss sechs Bit-Tasten mit den Schreibadressen LB1-LB6 und den Funktionen „Umschalten“, „Überwachen“ und „Überwachungsadresse gleich Schreibadresse“ hinzu. Speichern Sie das Projekt mit „Speichern“ in der Werkzeugleiste, wählen Sie im Menü „Download“ den Befehl „Offline“ und klicken Sie auf die Bit-Tasten LB1, LB2, LB4 und LB6: Alarmanzeige und dynamisches Alarmlaufband zeigen die digitalen Alarme von LB1, LB2, LB4 und LB6 an. Ein erneuter Klick setzt die Werte wegen der Umschaltfunktion auf 0, und Alarmanzeige und Laufband zeigen nichts mehr an.

<img src="../../setting/dig-alarm.files/dig-alarm4400.png" width="130" />

Hinweis: Mit dem Sprachwechsel kann jede Sprache eigene Alarmtexte haben.

Hinweis: Die HMI der HM-Serie unterstützen höchstens 10 digitale Alarme.
