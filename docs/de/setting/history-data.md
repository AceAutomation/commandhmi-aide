# Historischer Datensammler

Der historische Datensammler arbeitet mit der [Historischen Datenanzeige](../configuration-guide/extended-controls/history-record.md) der Werkzeugleiste zusammen: Ersterer dient zur Parametereinstellung, Letztere zur Anzeige der historischen Daten.

Legen Sie einen Datensammler per Rechtsklick auf „Historischer Datensammler“ und „Neuer historischer Datensammler“ an.

Hinweis: CommandHMI unterstützt mehrere Gruppen historischer Daten; bis zu vier Datensammler können angelegt werden.

Mehr als vier Gruppen sind nicht möglich; sonst erscheint folgende Fehlermeldung:

<img src="../../setting/history-data.files/image008.jpg" width="456" />

Doppelklicken Sie im Projektmanager auf „Historischer Datensammler 0“, um das Dialogfeld in Abbildung 7-19 zu öffnen:

<img src="../../setting/history-data.files/image009.jpg" width="627" />

Abbildung 7-19     Dialogfeld Historischer Datensammler

• Name: im Projektmanager angezeigter Name.

• Abtastlänge: Anzahl der je Abtastung aus dem Speicher gelesenen Daten.

• Gesamtzahl der Abtastungen: Anzahl der Lesevorgänge.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Hinweis: benötigter Speicher = (20 + Bytes aller Datenelemente nach Datentyp) \* Gesamtzahl der Abtastungen.

„20“ sind die Bytes für Uhrzeit und Datum;

„Bytes aller Datenelemente“ ist die Summe der Größen der für jedes Element auf der Seite „Datenelemente“ gewählten Datentypen.

Beispiel, Abbildung 7-20:

a, Ist jedes Element vom Typ „16-Bit positive Ganzzahl“, sind die Bytes aller Elemente = 2 +2 +2 +2 +2; der benötigte Speicher ist (20 + 10) \* 2, also 60; 16-Bit-Daten belegen 2 Byte, 32-Bit-Daten 4 Byte.

b\. Sind „LH1“ und „LH3“ vom Typ „32-Bit positive Ganzzahl“ (die Adressen der „Datenelemente“ lauten dann LH0, LH1, LH3, LH5, LH6), sind die Bytes aller Elemente = 2 + 4 + 4 + 2 + 2 = 14; der benötigte Speicher = (20 + 14) \* 2 = 68.

Leseadresse: Startadresse der zu lesenden Daten (Einzelheiten siehe „Datenelemente“)

Abtastart:

• Zyklisch: liest die Daten im eingestellten Intervall.

• Trigger: liest die Daten, wenn die Triggeradresse 1 ist.

• Uhr: liest die Daten ab der vom Benutzer festgelegten Zeit im eingestellten Intervall.

Verhalten bei vollem Speicher: was geschieht, wenn die maximale Zahl der Abtastungen erreicht ist.

Abtastung stoppen: beendet die Abtastung bei vollem Speicher; ohne diese Option ersetzen neue Daten die ältesten.

Benachrichtigung: setzt eine Adresse auf 1, wenn die maximale Zahl der Abtastungen erreicht ist.

Klicken Sie auf die Registerkarte „Datenelemente“ und stellen Sie die Eigenschaften ein, wie in Abbildung 7-20:

<img src="../../setting/history-data.files/image002.jpg" width="627" />

Abbildung 7-20 Datenelemente des historischen Datensammlers

Bei Mehrsprachigkeit muss jedes neue Datenelement in jeder Sprache einen Namen erhalten; sonst kann es nicht hinzugefügt werden.

In CommandHMI können die Adressen einer Gruppe historischer Daten je nach LW-Registern nicht fortlaufend sein, z. B. S1 = LW1, S2 = LW89, S3 = LW8905.

Klicken Sie auf einen Eintrag der Liste, um seine Eigenschaften einzustellen.

Ausführliches Beispiel:

Stellen Sie auf der Seite „Allgemein“ die Leseadresse LW1 mit fortlaufenden Registern und Abtastlänge 5 ein; fügen Sie auf der Seite „Datenelemente“ 5 Spalten (LH0-LH4) hinzu. Legen Sie für jede Name, Adresse, Datentyp, Gesamtstellen, Nachkommastellen und Skalierung fest.

Angenommen, Namen, Datentypen und Skalierung von LH0-LH4 sind wie in Abbildung 7-20 eingestellt, die übrigen Eigenschaften auf Standard:

LH0 - 16-Bit positive Ganzzahl, Skalierung mit Verstärkung 3 und Offset 2

LH1 - 32-Bit positive Ganzzahl, Skalierung mit Verstärkung 2 und Offset 1

LH2 - 16-Bit Ganzzahl, ohne Skalierung

LH3 - 32-Bit Ganzzahl, ohne Skalierung

LH4 - Gleitkommazahl, Skalierung mit Verstärkung 4 und Offset 5

Da die Abtastlänge 5 ist (Seite „Allgemein“), werden ab der „Leseadresse“ 5 Werte fortlaufend gelesen, jeweils gemäß dem Datentyp des Elements.

Bei 16-Bit-Daten sind die gelesenen Adressen fortlaufend, bei 32-Bit-Daten im Abstand. Mit Skalierung ist der Endwert gleich dem gelesenen Wert mal Verstärkung plus Offset.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Hinweis: Die Verstärkung der Skalierung muss größer als 1 sein!

Je nach Datentyp und Skalierung werden folgende Adressen gelesen:

LH0-LW1 (16-Bit-Daten, Leseadresse + 1) Endwert von LH0 = Wert von LW1 × 3 + 2

LH1-LW2 (32-Bit-Daten, Leseadresse + 2) Endwert von LH1 = Wert von LW2 × 2 + 1

LH2-LW4 (16-Bit-Daten, Leseadresse + 1) Endwert von LH2 = Wert von LW4

LH3-LW5 (32-Bit-Daten, Leseadresse + 2) Endwert von LH3 = Wert von LW5

LH4-LW7 (32-Bit-Daten, Leseadresse + 2) Endwert von LH4 = Wert von LW7 × 4 + 5

Klicken Sie danach auf „OK“. Klicken Sie in der Werkzeugleiste auf „Historische Datenanzeige“ und stellen Sie im Dialogfeld 5 Zeilen ein; die übrigen Eigenschaften bleiben auf Standard.

Klicken Sie auf „OK“; im Bild wird automatisch eine Tabelle erzeugt, wie in Abbildung 7-21:

Abbildung 7-21 Tabelle der historischen Datenanzeige

Bedeutung der Tabelle:

• Datum: Datum, an dem der Wert gelesen wurde

• Zeit: Uhrzeit, zu der der Wert gelesen wurde

• „LH0“: Wert von LW1 zu einem bestimmten Zeitpunkt.

• „LH1“: Wert von LW2 zu einem bestimmten Zeitpunkt.

• „LH2“: Wert von LW4 zu einem bestimmten Zeitpunkt.

• „LH3“: Wert der Adresse LW5 zu einem bestimmten Zeitpunkt.

• „LH4“: Wert der Adresse LW7 zu einem bestimmten Zeitpunkt.

Beispiel: Leseadresse LW1, Abtastlänge 3, Gesamtzahl der Abtastungen 10, Abtastart Trigger, Intervall 1 Sekunde, Datentyp jeweils Standard;

1). Option „Abtastung stoppen“ nicht aktiviert:

Die Werte von LW1, LW2 und LW3 werden jede Sekunde gelesen. Da die Gesamtzahl 10 ist, sind nach 10 Sekunden 10 Datengruppen gelesen. Da „Abtastung stoppen“ nicht aktiviert ist, läuft die Abtastung weiter. Ein fester Speicherbereich, abhängig von Abtastlänge, Gesamtzahl und Datentyp, nimmt die Daten auf; ist die „Gesamtzahl der Abtastungen“ erreicht, ersetzt der neueste Datensatz den ältesten.

2). Option „Abtastung stoppen“ aktiviert:

Einziger Unterschied: Die Abtastung endet, sobald die Gesamtzahl erreicht ist.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Mit „[Historischen Trends](../configuration-guide/extended-controls/histrendgraphics.md)“ oder der „[Historischen Datenanzeige](../configuration-guide/extended-controls/history-record.md)“ lassen sich die Werte anschaulicher ablesen.
