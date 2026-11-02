# Mehrzustandstaste

Mehrzustandstaste und Mehrzustandslampe funktionieren im Wesentlichen gleich; der einzige Unterschied ist, dass die Mehrzustandstaste auch Werte schreiben kann, statt nur anzuzeigen. Vorgehen:

Klicken Sie auf das Symbol <img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button271.png" width="31" /> in der Werkzeugleiste, um das Dialogfeld in Abbildung 4-87 zu öffnen.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button336.png" width="663" />

Abbildung 4-87 Dialogfeld Mehrzustandstaste

• Zustand: Der Benutzer kann den Zustand wählen und für jeden Zustand Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster des Objekts ändern

• Zustandstyp: (angenommen, der eingegebene Wert ist n)

• Wert: Der geschriebene Wert liegt zwischen null und der Gesamtzahl der Zustände.

• Registerbit: Der geschriebene Wert ist 2 hoch n.

E.g:

Wählen Sie „Wert“ als Zustandstyp, „Tastatureingabe“ als Modus, LW3 als Schreibadresse, aktivieren Sie „Überwachungsadresse gleich Schreibadresse“ und stellen Sie 8 Zustände ein. Klicken Sie auf OK, fügen Sie das Objekt in das Bild ein und speichern Sie das Projekt.

In der Simulation oder auf dem Bild erscheint beim Antippen des Objekts eine Tastatur zur Eingabe eines Zustandswerts. Bei Eingabe von 3 wird 2 hoch 3 in das Register LW3 geschrieben, und das Objekt zeigt den Text des Zustands 3 (den Text des Zustands 3 auf der Seite „Text“). Umgekehrt zeigt das Objekt bei LW3 = 8 den Text des Zustands 3. Bei LW3 = 5 zeigt das Objekt keinen Zustand an.

• Benutzerdefinierte Zustandswerte: Bei Aktivierung dieser Option erscheint die Schaltfläche „Define Status Value...“, wie in Abbildung 4-88:

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1611.png" width="662" />

Abbildung 4-88 Mehrzustandstaste mit benutzerdefinierten Zustandswerten

Ein Klick auf „Define status value...“ öffnet das Dialogfeld „Benutzerdefinierte Zustandswerte“, wie in Abbildung 4-89:

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1799.png" width="333" />

Abbildung 4-89 Dialogfeld Zustandswerte definieren

In diesem Dialogfeld enthält die Spalte „S #“ den Zustand. Nach Auswahl einer Zeile gibt der zugehörige Wert den Wert dieses Zustands an; per Doppelklick geben Sie den Wert für den aktuellen Zustand ein.

Beispiel: Wählen Sie „Benutzerdefinierte Zustandswerte“ als Zustandstyp, „Tastatureingabe“ als Modus, LW3 als Schreibadresse, aktivieren Sie „Überwachungsadresse gleich Schreibadresse“ und stellen Sie 8 Zustände ein. Klicken Sie auf OK, fügen Sie das Objekt in das Bild ein und speichern Sie das Projekt. In der Simulation oder auf dem Bild erscheint beim Antippen eine Tastatur zur Eingabe eines Zustandswerts. Bei Eingabe von 1 wird 22 in das Register LW3 geschrieben, und das Objekt zeigt den Text des Zustands 1 (den Text des Zustands 1 auf der Seite „Text“). Umgekehrt zeigt das Objekt bei LW3 = 33 den Text des Zustands 2. Bei LW3 = 2 zeigt das Objekt keinen Zustand an.

• Modus: Sechs Funktionen stehen zur Auswahl: „Tastatureingabe“, „Konstante ausgeben“, „Erhöhen“, „Verringern“, „Zyklisch erhöhen“ und „Zyklisch verringern“.

• Tastatureingabe: Alle drei „Zustandstypen“ sind wählbar. In der Simulation oder auf dem Bild erscheint beim Antippen des Objekts eine Tastatur zur Eingabe des Werts, wie in Abbildung 4-90:

![](../../../configuration-guide/basic-control/multiple-button.files/001.png)

Abbildung 4-90 Tastatur

• Konstante ausgeben: Von den drei „Zustandstypen“ ist nur „Wert“ wählbar. Nach Auswahl dieser Option erscheint ein Feld „Konstante“ zur Eingabe der Konstanten. In der Simulation oder auf dem Bild wird beim Antippen des Objekts die eingestellte Konstante geschrieben

• Erhöhen: Von den drei „Zustandstypen“ ist nur „Wert“ wählbar. In der Simulation oder auf dem Bild erhöht jedes Antippen den Zustand um 1; bei Erreichen der Gesamtzahl der Zustände wird nicht weiter erhöht.

• Verringern: Von den drei „Zustandstypen“ ist nur „Wert“ wählbar. In der Simulation oder auf dem Bild verringert jedes Antippen den Zustand um 1; bei Erreichen der Bereichsgrenze wird nicht weiter verringert.

• Zyklisch erhöhen: Von den drei „Zustandstypen“ ist nur „Wert“ wählbar. In der Simulation oder auf dem Bild erhöht jedes Antippen den Zustand um 1; nach dem letzten Zustand geht es zurück zu Zustand 0.

• Zyklisch verringern: Von den drei „Zustandstypen“ ist nur „Wert“ wählbar. In der Simulation oder auf dem Bild verringert jedes Antippen den Zustand um 1; unter Zustand 0 geht es zurück zum höchsten Zustand.

• Datentyp: Datentyp der Schreib- und Überwachungs-(Lese-)adresse

• Überwachungsadresse: Leseadresse, deren Wert den Zustand liefert und den aktuellen Zustand des Objekts bestimmt.

• Gesamtzahl der Zustände: maximale Anzahl der Zustände

• Skript verwenden: Ist diese Option aktiviert, wird beim Antippen des Objekts in der Simulation oder auf dem Bild das vom Benutzer gewählte Skript ausgeführt.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button5026.png" width="130" />

Hinweis: Form, Rahmenfarbe, Vordergrundfarbe, Hintergrundfarbe und Muster siehe Objekt „Bit-Taste“.

Hinweis: Zu den Seiten „Text“ und „Grafik“ siehe Objekt „Mehrzustandslampe“.

Hinweis: Zu den Seiten „Erweitert“ und „Sichtbarkeit“ siehe Objekt „Bit-Taste“, dort auch zu Tastenkürzeln.

Klicken Sie nach den Einstellungen auf „OK“, um das Objekt in den Ansichtsbereich (das Bild) einzufügen
