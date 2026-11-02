# Wort-Taste

Die Wort-Taste führt an einer Datenregisteradresse des verbundenen Geräts folgende Operationen aus: Konstante, Wert eingeben, Hochzählen, Herunterzählen, Passwort eingeben, Addieren und Subtrahieren.

Wort-Taste hinzufügen:

• Wählen Sie das Symbol Wort-Taste <img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton222.png" width="29" /> in der Werkzeugleiste; es erscheint das folgende Dialogfeld, wie in Abbildung 4-76:

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton308.png" width="664" />

Abbildung 4-76 Dialogfeld Wort-Taste

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton345.png" width="130" />

Form, Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster siehe Objekt „Bit-Taste“.

**Funktion:**

• Konstante setzen: CommandHMI bietet verschiedene Datentypen: 16/32-Bit positive Ganzzahl, 16/32-Bit Ganzzahl, 16/32-Bit BCD positive Ganzzahl und 32-Bit-Gleitkommazahl. Die eingestellte Konstante wird in die Schreibadresse geschrieben. Ist z. B. die Schreibadresse LW1 und die Konstante 10, wird LW1 bei jedem Antippen auf 10 gesetzt, unabhängig vom aktuellen Wert.

• Wert eingeben: Nach Wahl des Datentyps erscheint beim Antippen der Wort-Taste eine Tastatur zur Eingabe eines Werts zwischen Minimum und Maximum, wie in Abbildung 4-77:

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton1128.png" width="693" />

Abbildung 4-77

• Hochzählen: Ist der Verzögerungsparameter 0, entspricht die Funktion „Addieren“. Ist er nicht 0, wird der Wert der Schreibadresse um die Konstante erhöht und in das Register geschrieben.

• Herunterzählen: Ist der „Verzögerungsparameter“ 0, entspricht die Funktion „Subtrahieren“. Ist er nicht 0, wird nach einer bestimmten Zeit der Wert der Adresse um die Konstante verringert und in das Register geschrieben.

• Passwort eingeben: Wie „Wert eingeben“, jedoch ohne Nachkommastellen.

• Addieren: Nach Festlegung von Datentyp, Schreibadresse, Konstante und Höchstwert wird bei jedem Antippen der Wort-Taste die Konstante zum bisherigen Registerwert addiert; der geschriebene Wert kann den eingestellten Höchstwert jedoch nicht überschreiten. Beispiel: Schreibadresse LW1, Konstante 5, Höchstwert 65535. Bei jedem Antippen wird LW1 um 5 erhöht, überschreitet aber nie 65535.

• Subtrahieren: Nach Festlegung von Datentyp, Schreibadresse, Konstante und Mindestwert wird bei jedem Antippen der Wort-Taste die Konstante vom bisherigen Registerwert abgezogen; der geschriebene Wert kann den eingestellten Mindestwert jedoch nicht unterschreiten. Beispiel: Schreibadresse LW1, Konstante 5, Mindestwert 0. Bei jedem Antippen wird LW1 um 5 verringert, aber nie unter 0.

• Gesamtstellen: Anzahl der Stellen einschließlich Nachkommastellen.

• Nachkommastellen: Ist der Datentyp keine „32-Bit-Gleitkommazahl“ und gibt es Nachkommastellen, verringert sich der Höchstwert der Eingabe um den Faktor 10 hoch n. Beispiel: Bei Datentyp „32-Bit positive Ganzzahl“ und 3 Nachkommastellen kann der Benutzer nur Werte von 0 bis 99999.999 eingeben.

• Skript: Mit „Skript verwenden“ wird eine Skriptliste angezeigt. Der Benutzer kann ein Skript wählen, das beim Drücken der Wort-Taste ausgeführt wird. Nur kompilierte Skripte erscheinen in der Liste.

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton3632.png" width="130" />

Die Registerkarte „Beschriftung“ der Wort-Taste entspricht weitgehend der der „Bit-Taste“; da die Wort-Taste nur einen Zustand hat, fehlen „Text Zustand 1“ und „Grafik Zustand 1“.

Bei Datentyp 32 Bit belegt die Adresse der Wort-Taste zwei Worte. Wird z. B. V10 in ein Datenregister einer SIEMENS-SPS geschrieben, sind die Register V10 und V11 belegt. Überwacht der Benutzer V11 zusätzlich mit einem anderen Objekt, funktioniert dies nicht. Achten Sie bei 32-Bit-Datentypen auf Fehler.

Die Seiten „Erweitert“ und „Sichtbarkeit“ der Wort-Taste entsprechen denen der Bit-Taste; zur Verwendung von Tastenkürzeln siehe ebenfalls die Bit-Taste.
