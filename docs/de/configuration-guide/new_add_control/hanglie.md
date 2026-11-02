# Datentabelle

Dieses Objekt zeigt benutzerdefinierte Daten in Tabellenform an und erleichtert Auswahl und Bearbeitung. Zu den Funktionen gehören automatisches Blättern, Einfügen, Löschen, Kopieren und Einfügen aus der Zwischenablage.

Seite „Allgemein“

![](../../../configuration-guide/new_add_control/hanglie.files/001.png)

Dateneinstellungen

Gesamtzahl der Felder: Anzahl der Tabellenspalten

Anfängliche Gesamtzahl der Einträge: anfängliche Anzahl der Tabellenzeilen

Einträge pro Seite: Anzahl der Zeilen pro Seite

Startadresse: Adresse des ersten Tabellenelements

Adress-Offset: Adress-Offset jeder Zeile der Spalte

Adressvorschau

Zeigt die Adressverteilung der Tabelle an

Feldeinstellungen

Aktuelles Feld: aktuelle Spalte

Feldtyp: Zustand, Zeichenkette, Zahl

Feldbreite: Spaltenbreite

Ausrichtung: Ausrichtung der Spaltenelemente

Gesamtzahl der Zustände: Anzahl der Zustände des Spaltenelements

Erweitert

![](../../../configuration-guide/new_add_control/hanglie.files/002.png)

Status

Ausgewählte Einträge: ausgewählte Elemente

Tatsächliche Gesamtzahl der Einträge: tatsächliche Anzahl der Elemente

Sichtbare Einträge: Anzahl der sichtbaren Elemente

Aktuelle Seite: aktuelle Seitennummer

Seitenanzahl: Gesamtzahl der Seiten

Daten der aktuellen Seite automatisch aktualisieren: Ja: automatisch; sonst über die eingestellte Adresse gesteuert

Daten aktualisieren: Aktualisierungsadresse

Bedienung

Unsichtbar-Bit: Blendet die Daten aus

Unsichtbar-Pegel: Bedingung, unter der das Unsichtbar-Bit wirkt

Triggeradresse vorherige Seite: zur vorherigen Seite blättern

Triggeradresse nächste Seite: zur nächsten Seite blättern

Triggeradresse vorheriger Eintrag: vorherigen Eintrag der Spalte auswählen

Triggeradresse nächster Eintrag: nächsten Eintrag der Spalte auswählen

Triggeradresse Kopieren: aktuellen Eintrag kopieren

Triggeradresse Einfügen: Daten einfügen

Triggeradresse Ersetzen: aktuellen Eintrag mit den eingefügten Daten überschreiben

Triggeradresse Einfügen an Position: Eintrag beim aktuellen Eintrag einfügen

Triggeradresse Ausschneiden: Daten ausschneiden

Berührungsschutz-Bit: Schutz gegen Berührung

Adresse für den ausgewählten Eintrag: legt den auszuwählenden Eintrag fest

Trigger für die Auswahl: Die Auswahl wird wirksam

Adresse für die Gesamtzahl der Einträge: legt die Gesamtzahl der Einträge fest

Trigger für die Gesamtzahl: Die Gesamtzahl wird wirksam

Erweitert 2

Der Zwischenspeicher ist ein Pufferbereich, in dem das Element Daten vorübergehend ablegen kann. Daten im Puffer können eingefügt, angehängt und in ausgewählte Einträge geschrieben werden; ebenso lassen sich die Daten des ausgewählten Eintrags in den Puffer lesen.

![](../../../configuration-guide/new_add_control/hanglie.files/003.png)

Zwischenspeicher

Startadresse: Startadresse des Zwischenspeichers

Bit „Ausgewählten Eintrag einfügen“: Bei ON werden die Daten im Puffer (Adresse: Startadresse des Puffers + Adress-Offset des Eintrags) beim ausgewählten Eintrag eingefügt; die tatsächliche Anzahl der Einträge steigt um 1. Ist die Höchstzahl erreicht, kann nicht eingefügt werden.

Bit „An ausgewählten Eintrag anhängen“: Bei ON werden die Daten im Puffer (Adresse: Startadresse des Puffers + Adress-Offset des Eintrags) beim ausgewählten Eintrag angefügt; die tatsächliche Anzahl der Einträge steigt um 1. Ist die Höchstzahl erreicht, kann nicht eingefügt werden.

Am Ende anhängen: Bei ON werden die Daten im Puffer (Adresse: Startadresse des Puffers + Adress-Offset des Eintrags) am Ende angefügt; die tatsächliche Anzahl der Einträge steigt um 1. Ist die Höchstzahl erreicht, kann nicht eingefügt werden.

Ausgewählten Eintrag lesen: Bei ON wird der Inhalt des ausgewählten Eintrags in den Puffer gelesen (Adresse: Startadresse des Puffers + Adress-Offset des Eintrags)

Ausgewählten Eintrag schreiben: Bei ON werden die Pufferdaten (Adresse: Startadresse des Puffers + Adress-Offset des Eintrags) in den ausgewählten Eintrag geschrieben

Aussehen

![](../../../configuration-guide/new_add_control/hanglie.files/004.png)

Feldeinstellungen

Tabellennummer usw.

Stil

Rasterlinien, Hintergrundfarbe, Hintergrundfarbe bei Auswahl usw.
