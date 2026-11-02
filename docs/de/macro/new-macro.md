# Skript anlegen

Klicken Sie auf die Schaltfläche <img src="../../macro/new-macro.files/new-macro12.png" width="25" />, um in der Liste „Nicht gespeichert“ ein Skript anzulegen, wie in Abbildung 5-4 (Skriptcompiler)

<img src="../../macro/new-macro.files/new-macro112.png" width="1086" />

Abbildung 5-4 (Skriptcompiler)

**Hinweise:**

**Hinweis 1: Konventionen für das Kompilieren**

Geben Sie im Bearbeitungsfenster ein C-Quellprogramm nach ANSI-C-Standard ein.

**Hinweis 2: Ausgabefenster**

Dieses Fenster zeigt Kompilier- und Binderinformationen des Programms an. Anhand dieser Meldungen kann der Benutzer Fehler suchen und korrigieren.

**Hinweis 3: Variablen einstellen**

Variablenname: im Programm verwendeter Variablenname.

Datentyp: Typ der Variablen, der die Speichergröße bestimmt.

Bytes: Speichergröße der Variablen, automatisch nach dem Datentyp festgelegt.

Lesen/Schreiben: Lese-/Schreibrechte der Variablen im Speicher des Touchscreens.

Adresse: physische Speicheradresse der Variablen im Touchscreen.

Zweck der Variableneinstellung: Wenn von außen mit dem Touchscreen interagiert werden muss (Datenaustausch, Datenerfassung), bietet sie die Schnittstelle, um das Verhalten des Touchscreens dynamisch zu ändern.

Tipp: Die im Programm verwendeten Variablen gehören in den Deklarationsteil (am Anfang des Codes).
