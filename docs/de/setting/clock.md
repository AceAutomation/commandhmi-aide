# Uhr

Die Uhreinstellung umfasst drei Funktionen: Systemzeit in das HMI laden, Zeit in die SPS schreiben und mit der SPS synchronisieren.

Doppelklicken Sie im Projektmanager auf „Uhr“, um das Eigenschaftsfenster der Uhr zu öffnen.

<img src="../../setting/clock.files/image004.jpg" width="388" />

<img src="../../setting/clock.files/image005.jpg" width="388" />

Abbildung 7-11 Dialogfeld Uhr

Systemuhr in das HMI laden: legt fest, ob die Systemzeit in das HMI geladen wird.

• Zeit/Datum in die SPS schreiben:

• Datentyp und Länge sind Standardwerte.

• Zeit: Jahr-Monat-Tag-Stunde-Minute-Sekunde-Wochentag. Einzelheiten siehe LW 60000~LW 60006 unter den Registeradressen. Der Wochentag der Systemzeit ist nicht änderbar.

Schreibadresse: Die Systemzeit wird in diese SPS-Adresse geschrieben.

• Auslösung:

Zyklisch: schreibt die Systemzeit im eingestellten Intervall in die angegebene SPS-Adresse.

Trigger: schreibt die Systemzeit in die angegebene SPS-Adresse, wenn die Triggeradresse 1 ist.

Automatisch zurücksetzen: setzt die Triggeradresse automatisch auf 0, wenn sie 1 ist.

**Synchronisation mit der SPS-Zeit:**

Datentyp und Länge sind Standardwerte.

 Zeit: Jahr-Monat-Tag-Stunde-Minute-Sekunde-Wochentag. Einzelheiten siehe LW 60000~LW 60006 unter den Registeradressen. Der Wochentag der Systemzeit ist nicht änderbar.

• Leseadresse: Die Informationen werden aus dieser SPS-Adresse gelesen.

• Auslösung:

Zyklisch: schreibt die Systemzeit im eingestellten Intervall in die angegebene SPS-Adresse.

Trigger: Die Systemzeit wird mit der SPS synchronisiert, wenn die Triggeradresse 1 ist.

Automatisch zurücksetzen: setzt die Triggeradresse automatisch auf 0, wenn sie 1 ist.
