# Datenübertragung

Überträgt Daten zwischen SPS und HMI oder zwischen zwei SPS. Ein Klick auf „Datenübertragung“ im Projektmanager zeigt die aktuelle Übertragungsliste.

<img src="../../../configuration-guide/extended-controls/transmission.files/image005.jpg" width="564" />

Abbildung 7-36

Die Übertragungsliste zeigt alle Übertragungen im Detail; der Benutzer kann sie anlegen, löschen und ändern. Die Projektierungssoftware CommandHMI unterstützt bis zu 512 Datenübertragungen.

Zum Anlegen oder Ändern einer Übertragung öffnen Sie die Eigenschaftsseite:

<img src="../../../configuration-guide/extended-controls/transmission.files/image006.jpg" width="339" />

Abbildung 7-37

**1. Eigenschaften**

Zyklisch / Trigger: Auslöseart der Datenübertragung.

Zyklisch: Übertragung im eingestellten Intervall.

Trigger: Die Übertragung wird über eine Adresse gesteuert und bei Wert 1 ausgeführt.

Automatisch zurücksetzen: Ist die Triggeradresse 1, wird sie automatisch auf 0 gesetzt.

Adresstyp: Adresstyp der übertragenen Daten: Bit / Wort / Doppelwort.

Wort / Bit: Länge der zu übertragenden Daten, 1 bis 64.

**2. Adresse**

Quelladresse: Quelladresse der übertragenen Daten; <span id="OLE_LINK497"></span><span id="OLE_LINK498"></span>sie muss dem unter „Eigenschaften“ eingestellten Adresstyp entsprechen.

Zieladresse: Zieladresse der übertragenen Daten; sie muss dem unter „Eigenschaften“ eingestellten Adresstyp entsprechen.

<img src="../../../configuration-guide/extended-controls/transmission.files/image004.jpg" width="130" />

Ziel- und Quelladresse dürfen nicht in derselben SPS liegen.
