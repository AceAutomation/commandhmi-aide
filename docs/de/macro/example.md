# Ein einfacher Skriptbaustein

Legen Sie ein Projekt an und wählen Sie das HMI-Modell. Das Skript führt eine einfache Berechnung aus: Das Initialisierungsskript Init füllt die Objekte „Numerische Anzeige“ mit den Elementen des Arrays char source \[4\] = {2, 3, 4, 5}; der Benutzer gibt Daten in diese Objekte ein; ein Druck auf die Taste „=“ führt das Skript ADDSUM aus, dessen Ergebnis im vorgesehenen Objekt angezeigt wird.

Vorgehen im Einzelnen:

**Schritt 1: &lt;Skript anlegen&gt;**

Klicken Sie links in der Werkzeugleiste auf die Schaltfläche „Skripteditor“; es öffnet sich ein Dialogfeld.

**Schritt 2: &lt;Skript Init anlegen&gt;**

Klicken Sie im Skripteditor auf die Schaltfläche <img src="../../macro/example.files/example866.png" width="25" />; in der Liste „Nicht gespeichert“ erscheint ein neues Skript, wie in Abbildung 5-7. Ändern Sie den Skriptnamen im Feld „Script“ und geben Sie den Quellcode im Bearbeitungsfenster ein, wie in Abbildung 5-8

<img src="../../macro/example.files/example1100.png" width="886" />

Abbildung 5-7      Neues Skript

<img src="../../macro/example.files/example1126.png" width="1087" />

Abbildung 5-8 Skript Init bearbeiten

<img src="../../macro/example.files/example1156.png" width="130" />

Skriptnamen dürfen nur Ziffern (0-9), Buchstaben (a-z, A-Z) und den Unterstrich (\_) enthalten. Geben Sie den Inhalt aus Abbildung 5-9 ein:

**Schritt 3: &lt;Variablen einstellen&gt;**

Name, Typ usw. der Variablen werden im Fenster in Abbildung 5-9 festgelegt. Doppelklicken Sie in das Fenster „Variablen“ oder wählen Sie im Kontextmenü „Neue Variable“, um das Dialogfeld in Abbildung 5-10 zu öffnen, in dem die externen Variablen eingestellt werden.

<img src="../../macro/example.files/example1677.png" width="499" />

Abbildung 5-9 Skriptcode

Name: LW0, LW1, LW2, LW3 als Variablennamen eingeben;

Datentyp: 16-Bit Ganzzahl;

Lesen/Schreiben: Lesen und Schreiben wählen;

Adressen: LW0 = 0, LW1 = 1, LW2 = 2, LW3 = 3;

Das Ergebnis zeigt Abbildung 5-10.

<img src="../../macro/example.files/example1981.png" width="843" />

Abbildung 5-10     Variablen einstellen

**Schritt 4: &lt;Quelldatei kompilieren&gt;**

Danach wird kompiliert: Klicken Sie auf die Schaltfläche „Kompilieren“, wie in Abbildung 5-11; die Software speichert, kompiliert, bindet und prüft automatisch auf Fehler.

<img src="../../macro/example.files/example2223.png" width="800" />

Abbildung 5-11    Ausgabefenster

Zeigt das Ausgabefenster „0 errors! Compile successfully“, ist das Skript erfolgreich angelegt und wird automatisch in die Liste der kompilierten Skripte aufgenommen; andernfalls erscheint eine Fehlermeldung, und das Skript kommt in die Liste der fehlgeschlagenen Kompilierungen. Korrigieren Sie das Skript, bis die Kompilierung gelingt.

**Schritt 5: &lt;Skript ADDSUM anlegen&gt;**

Legen Sie mit den Schritten 2 bis 4 das Skript ADDSUM an, wie in Abbildung 5-13

&lt;1&gt;: Geben Sie „ADDSUM“ als Skriptnamen ein.

&lt;2&gt;: Geben Sie den eingekreisten Inhalt im Code-Fenster ein.

&lt;3&gt;: Legen Sie die Eigenschaften der Variablen im Variablenfenster fest.

&lt;4&gt;: Klicken Sie auf „Kompilieren“.

<img src="../../macro/example.files/example2991.png" width="1168" />

Abbildung 5-13    Skript ADDSUM anlegen

**Schritt 6: &lt;Objekte bearbeiten&gt;**

&lt;1&gt;. Platzieren Sie die Objekte im Projektbild und passen Sie ihre Größe an, wie in Abbildung 5-14.

<img src="../../macro/example.files/example3164.png" width="558" />

Abbildung 5-14    Anordnung der Objekte

&lt;2&gt;. Eigenschaften der Objekte einstellen

Klicken Sie mit der rechten Maustaste auf das Objekt „Numerische Eingabe“ und stellen Sie Adresse und Eigenschaften jedes Objekts ein, wie in Abbildung 5-15.

<img src="../../macro/example.files/example3375.png" width="660" />

Abbildung 5-15    Eigenschaften der numerischen Eingabe

Die Adressen der Variablen LW0, LW1, LW2, LW3 und SumLW müssen der „Schreibadresse“ (Abbildung 5-15) des jeweiligen Objekts entsprechen. Klicken Sie auf „OK“, um zu speichern.

&lt;3&gt;. Eigenschaften der Bit-Taste einstellen

<img src="../../macro/example.files/example3658.png" width="661" />

Abbildung 5-16 (Eigenschaften der Bit-Taste)

&lt;4&gt;. Eigenschaften des Timers

Wählen Sie das Skript Init und klicken Sie auf „OK“, um zu speichern.

<img src="../../macro/example.files/example3792.png" width="661" />

Abbildung 5-17    Eigenschaften des Timers

&lt;5&gt;. Geben Sie auf der Seite „Beschriftung“ -&gt; „Text“ der Funktionstaste das Zeichen „+“ in das Textfeld ein, wie in Abbildung 5-18.

<img src="../../macro/example.files/example3963.png" width="662" />

Abbildung 5-18    Eigenschaften der Funktionstaste

**Schritt 7: Kompilieren und in das HMI laden**

&lt;1&gt;: Klicken Sie auf das Symbol „Kompilieren“.

<img src="../../macro/example.files/example4101.png" width="64" />

Abbildung 5-19    Projekt kompilieren

&lt;2&gt;: Wählen Sie „Download (D) -&gt; USB-Download (D)“ und klicken Sie im Dialogfeld auf „Download“. Starten Sie das HMI neu.

Alternativ verwenden Sie die Schaltfläche „Kompilieren und herunterladen“.

**Schritt 8: &lt;Ergebnis testen&gt;**

Nach dem Neustart des HMI erscheint das Bild in Abbildung 5-20.

Denn beim Start führt der Timer zuerst das Skript Init aus.

<img src="../../macro/example.files/example4642.png" width="484" />

Abbildung 5-20    Anzeige der Anfangswerte

Geben Sie z. B. „31,42,53,64“ in die Objekte „Numerische Anzeige“ ein und drücken Sie „=“: Das Skript ADDSUM wird ausgeführt und zeigt 190 an, wie in Abbildung 5-21:

<img src="../../macro/example.files/example5009.png" width="481" />

Abbildung 5-21     Anzeige des Ergebnisses

Damit sind Bearbeitung, Kompilierung, Download und Test des Skripts erfolgreich abgeschlossen.
