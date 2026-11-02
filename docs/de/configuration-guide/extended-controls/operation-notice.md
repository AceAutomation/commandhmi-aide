# Hinweise zu den CommandHMI-Objekten

Die Projektierungssoftware CommandHMI bietet umfassende Basisobjekte. Per Doppel- oder Rechtsklick auf ein Objekt im Ansichtsbereich legen Sie seine Eigenschaften fest. Position und Größe lassen sich in der Statusleiste unten eingeben oder direkt mit der Maus ändern.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/image002.jpg" width="829" alt="2018_11_20_08_51_35.jpg" />

Adresseingabe: Adressen der SPS können direkt über die Tastatur eingegeben werden. Groß- und Kleinschreibung des Adressnamens spielt keine Rolle.

Zustandsauswahl: In der Werkzeugleiste zeigt eine Auswahlliste den Zustand von Bit-Taste, Bit-Lampe, Mehrzustandstaste, Mehrzustandslampe, Grafikbewegung, Meldungsanzeige und Grafikanzeige an und ermöglicht dessen Änderung.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice675.png" width="92" />

Ist ein solches Objekt ausgewählt, erscheint sein aktueller Zustand in dieser Auswahlliste, über die er geändert werden kann.

Adresssuche: Ermittelt die Verwendung einer Adresse und listet die Objekte auf, die sie belegen; ein Doppelklick auf einen Eintrag wählt das Objekt aus.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice997.png" width="299" />

Geben Sie die Adresse ein und wählen Sie „Suchen“; das Ausgabefenster listet die Ergebnisse auf:

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1102.png" width="406" />

Ein Doppelklick auf ein Suchergebnis wählt das Objekt aus, das die Adresse belegt.

Adressanzeige: Ein Klick auf „Adressanzeige“ listet die im Projekt verwendeten Adressen auf; ein Doppelklick auf einen Eintrag öffnet die Eigenschaften des Objekts, das diese Adresse verwendet, zur schnellen Bearbeitung.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1461.png" width="719" />

Im Anzeigemodus wählen Sie die angezeigten Adressen oder alle Bilder.

Überlagerte Objekte: Durch Übereinanderlegen von Objekten lassen sich mehrere Objekte mit einer Berührung auslösen. CommandHMI unterstützt bis zu 32 übereinanderliegende Objekte. Beim Antippen werden die Aktionen in der Reihenfolge der Überlagerung ausgeführt, wie in der Abbildung:

Liegen die Objekte 1, 2 und 3 übereinander, werden beim Antippen nacheinander die Befehle 1, 2 und 3 ausgeführt.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1966.png" width="435" />

Befindet sich unter den überlagerten Objekten eine Bildwechsel-Taste, wird das Bild gewechselt, sobald dieser Befehl an der Reihe ist; die nachfolgenden Befehle werden nicht ausgeführt. Ebenso wird bei einer eingeblendeten Eingabetastatur die Tastatur angezeigt, ohne die nachfolgenden Befehle auszuführen.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice2303.png" width="494" />
