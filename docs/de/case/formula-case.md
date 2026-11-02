# Rezept-Beispiel

Das folgende Beispiel zeigt Einstellung und Anzeige von Rezepten.

1\. **Neues Rezept anlegen**

Klicken Sie im Projektmanager mit der rechten Maustaste auf „Rezept“, wie in Abbildung 1:

<img src="../../case/formula-case.files/formula-case168.png" width="284" />

Abbildung 11 Neues Rezept anlegen

Öffnen Sie das Rezept per Doppelklick, wie in Abbildung 2:

<img src="../../case/formula-case.files/formula-case254.png" width="514" />

Abbildung 12 Allgemeine Einstellungen des Rezepts

Stellen Sie die Rezeptlänge auf 4 ein, d. h. jedes Rezept enthält 4 Werte. Die Gesamtanzahl ist 10, also 10 Rezepte. Stellen Sie die Adresse zum Schreiben des Rezepts in die SPS auf D50 und wählen Sie „16-Bit positive Ganzzahl“; das Rezept wird in die Register D50, D51, D52 und D53 geschrieben. Die übrigen Einstellungen entsprechen denen der Schreibadresse.

2\. **Datenelemente des Rezepts:**

<img src="../../case/formula-case.files/formula-case637.png" width="511" />

Abbildung 13 Datenelemente des Rezepts

Nachdem Sie den Rezeptnamen festgelegt haben, klicken Sie auf „OK“. Mit dem Objekt „Numerische Ein-/Ausgabe“ werden die Rezeptdaten auf dem Touchscreen angezeigt. Wählen Sie für dieses Objekt die interne Speicheradresse RWI0; der ein- und ausgegebene Wert ist die Rezeptnummer. RWI0 enthält die Rezeptnummer; der Wert 2 bedeutet Rezept Nr. 2 usw. Zeigen Sie mit „Numerische Ein-/Ausgabe“-Objekten die Daten von D50 bis D53 an. Speichern oder Lesen eines Rezepts erfolgt über Funktionstasten; siehe „Funktionstaste“.

<img src="../../case/formula-case.files/formula-case1276.png" width="663" />

Abbildung 14 Objekt „Numerische Ein-/Ausgabe“ für die Rezeptdaten D50

Legen Sie die Objekte „Numerische Ein-/Ausgabe“ an und platzieren Sie sie im Bild:

<img src="../../case/formula-case.files/formula-case1422.png" width="746" />

Abbildung 15 Bildansicht der Rezeptanzeige

Rezeptparameter lassen sich über „Numerische Ein-/Ausgabe“ ändern; Prüfen, Lesen und Schreiben von Rezepten erfolgen über Funktionstasten.
