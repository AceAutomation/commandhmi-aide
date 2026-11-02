# Auswahlliste

Die Auswahlliste zeigt eine Liste von Einträgen an, die der Benutzer ansehen und auswählen kann. Nach der Auswahl wird der zugehörige Wert in die Steueradresse (Wortregister) geschrieben.

Das Symbol in der Werkzeugleiste ist <img src="../../../configuration-guide/new_add_control/combobox.files/combobox771.png" width="35" />; ein Klick darauf öffnet das Dialogfeld in Abbildung 4-115:

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1012.png" width="677" />

Abbildung 4-115   Seite „Allgemein“ der Auswahlliste

• Anzahl der Zustände: Anzahl der Zustände des Objekts. Jeder Eintrag steht für einen Zustand und erscheint in der Liste; sein Wert kann in die \[Steueradresse\] geschrieben werden.

• Hintergrundfarbe: Hintergrundfarbe des ausgewählten Eintrags

• Textfarbe: Textfarbe des ausgewählten Eintrags

• Steueradresse: Schreibadresse

• Skript verwenden: Führt das gewählte Skript aus, wenn das Objekt bedienbar ist.

Zustände: Klicken Sie auf die Seite „Status Set“; es erscheint Abbildung 4-116:

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1554.png" width="675" />

Abbildung 4-116   Seite „Zustände“ der Auswahlliste

• Sprache: Alle Zustände verwenden dieselbe Schriftart und Schriftgröße; je Sprache können Schriftart und Schriftgröße verschieden sein.

• Wert: Jedem Eintrag wird ein Wert zugeordnet; dabei gelten zwei Regeln:

a\. \[Lesen\]: Ändert sich der Inhalt der \[Steueradresse\], vergleicht das Objekt ihn mit den Werten und wählt den ersten passenden Eintrag. Passt keiner, wechselt es in den Fehlerzustand und setzt das Fehlerbenachrichtigungsbit (falls eingestellt).

b\. \[Schreiben\]: Bei Auswahl eines Eintrags schreibt das System dessen Wert in die \[Steueradresse\].

• Beschriftung: Für jeden Eintrag kann ein Text festgelegt werden. Die Liste zeigt die Texte aller Einträge zur Ansicht und Auswahl an.

• Fehlerbenachrichtigung

a\. Beispiel: Bei \[Anzahl der Zustände\] = 8 ist Zustand 8 der Fehlerzustand; bei 11 ist es Zustand 11.

b\. Bei einem Fehler zeigt die Auswahlliste den Text des Fehlerzustands an.

Bei einem Fehler setzt das System ein bestimmtes Bit auf ON/OFF (in die \[Fehlerbenachrichtigungsadresse\]). Über dieses Bit kann eine Aktion zur Fehlerbehebung ausgelöst werden.

Zu den Seiten „Erweitert“ und „Sichtbarkeit“ siehe „Bit-Taste“.
