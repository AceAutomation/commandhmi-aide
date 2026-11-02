# Rezept

In der Fertigung beschreibt ein Rezept die Mengenverhältnisse der Materialien für ein Produkt: eine Gruppe von Parameterwerten für die Produktion. Für Brot etwa braucht man ein Grundrezept mit Gewicht oder Anteil aller Zutaten wie Wasser, Mehl, Zucker, Eier, Öl usw. Es kann auch optionale Zutaten wie Früchte, Nüsse oder Schokolade enthalten, die dem Grundrezept für unterschiedliche Brotsorten hinzugefügt werden. Ein anderes Beispiel: In einem Stahlwerk kann ein Rezept ein Satz Maschinenparameter sein. Bei Chargenmaschinen kann ein Rezept die Schritte der Chargenverarbeitung beschreiben.

Eine Maschine kann Brot und Kuchen herstellen, Brot verschiedener Sorten und Kuchen verschiedener Formen. Hier heißen die Zutatenverhältnisse eines Brots „Rezept“ und die Verhältnisse der verschiedenen Brotsorten zusammen „Datei“. Rezeptdatensätze sind also in Rezeptdateien enthalten.

CommandHMI bietet eine Rezeptprojektierung über das Menü „Rezept“ oder den Projektmanager: Im Dialogfeld der Rezeptkonfiguration wird eine neue Rezeptgruppe angelegt, wie in Abbildung 7-32:

<img src="../../setting/formula.files/formula1334.png" width="515" />

Abbildung 7-32 Eigenschaften eines fortlaufenden Rezepts

• Name: Name der aktuellen Rezeptdatei.

• Beschreibung: Beschreibung der aktuellen Rezeptdatei;

• Rezeptlänge: Länge und Anzahl der vom aktuellen Rezept gelesenen Adressen. Die Adressen der Rezepttabelle werden vom System automatisch fortlaufend vergeben und sind nicht änderbar. Maximale Rezeptlänge: 4096.

• Anzahl: Anzahl der Rezepte, höchstens 512;

• Rezeptgruppe im HMI bearbeitbar: erlaubt die Bearbeitung des Rezepts im HMI.

<img src="../../setting/formula.files/formula1872.png" width="794" />

Abbildung 7-33 Eigenschaften eines diskreten Rezepts

• Gruppenname: Name der aktuellen Rezeptdatei.

• Rezeptbeschreibung: Beschreibung der aktuellen Rezeptdatei;

• Kennung „Rezept geschrieben“: Nachdem das aktuelle Rezept in die SPS geschrieben wurde, wird die angegebene Bitadresse auf 1 gesetzt;

• Rezeptgruppe im HMI bearbeitbar: erlaubt die Bearbeitung des Rezepts im HMI.

<img src="../../setting/formula.files/formula2225.png" width="130" />

Hinweis: Rezeptlänge \* Bytes des Datentyps \* Anzahl &lt;= 512 KB

• Datentyp: Datentyp des Datenregisters;

• Rezept in SPS schreiben: zugehörige Datenregisteradresse der SPS;

• Rezept aus SPS lesen: zugehörige Datenregisteradresse der SPS;

• Rezeptspeicher: Adressbereich des Rezepts im HMI, automatisch erzeugt und nicht änderbar;

• Aktuelles Rezept: Speicheradressen des Rezepts im HMI und Datenregister der SPS, automatisch der Reihe nach erzeugt und nicht änderbar;

• Rezeptnummernregister: Die Rezepte werden automatisch fortlaufend nummeriert, nicht änderbar; die Nummer entspricht der Reihenfolge der Rezeptnamen in den Daten.

Daten eines fortlaufenden Rezepts, siehe Abbildung 7-33:

<img src="../../setting/formula.files/formula2990.png" width="514" />

Abbildung 7-34 Seite „Daten“ eines fortlaufenden Rezepts

• Name: Name des aktuellen Rezepts;

• Daten: Eingabe und Anzeige der Adresswerte des aktuellen Rezepts;

• Rezeptdaten kopieren: kopiert die Daten des Quellrezepts in das Zielrezept. „OK“ speichert, „Abbrechen“ schließt das Dialogfeld. Nach der Rezeptprojektierung können die Bilder zur Bedienung der Rezepte im HMI gestaltet werden.

Anwendungsbeispiel für Rezepte:

1\. Legen Sie eine Rezeptkonfiguration wie oben beschrieben an. Das Ergebnis zeigt Abbildung 7-34:

<img src="../../setting/formula.files/formula3531.png" width="515" />

Abbildung 7-35  Kopieren von Daten eines fortlaufenden Rezepts

Dieses Rezept umfasst 4 Unterrezepte mit je 16 Einträgen, gespeichert von RWI: 1 bis RWI: 16 im Speicher des HMI.

2. Nach der Rezeptprojektierung können die Rezepte im Bild angezeigt, geändert oder direkt in die SPS geladen werden. Dazu dienen folgende Objekte.

• Rezeptanzeige: Klicken Sie auf „Numerische Ein-/Ausgabe“ <img src="../../setting/formula.files/formula3946.png" width="23" /> (siehe „Numerische Ein-/Ausgabe“)

Wählen Sie die interne Speicheradresse RWI: 0, um im Bild eine numerische Ein-/Ausgabe anzulegen. Der ein- und ausgegebene Wert ist die Rezeptnummer: RWI0 = 0 entspricht Rezept Nr. 1, RWI0 = 1 Rezept Nr. 2 usw.

• Klicken Sie auf die Funktionstaste <img src="../../setting/formula.files/formula4264.png" width="21" />: zur Bedienung siehe „Funktionstaste“.

Mit den entsprechenden Funktionen lassen sich Tasten zum Schreiben in die SPS, Lesen aus der SPS, Speichern sowie zur Wahl des vorherigen oder nächsten Rezepts anlegen.

Mehrere Rezeptgruppen: CommandHMI unterstützt mehrere Rezeptgruppen, jedoch höchstens zehn; darüber hinaus erscheint eine Meldung, wie in 7-34-2

<img src="../../setting/formula.files/formula4682.png" width="248" />

Abbildung 7-35-1

<img src="../../setting/formula.files/formula4698.png" width="321" />

Abbildung 7-35-2

In LW61141 wird die Rezeptgruppe eingegeben, RWI0 dient weiterhin für die Rezeptnummer. Zur Auswahl müssen also LW61141 und RWI0 gemeinsam eingestellt werden. Beispiel: Gruppe 0 in LW61141 und Nummer 2 in RWI0 wählt die Daten von Rezept 2 der Gruppe 0.

3. So lässt sich ein Bild wie in Abbildung 7-35 erstellen:

Angenommen, die Schreib- und Überwachungsadresse ist D0, die Rezeptlänge 16 und die Anzahl 4.

<img src="../../setting/formula.files/formula5250.png" width="746" />

Abbildung 7-36 Ergebnis des Rezepts

Mit Funktionstasten und numerischen Ein-/Ausgaben lassen sich Rezepte einfach ändern, speichern, lesen und schreiben. Dabei ist Folgendes zu beachten:

• Die Rezeptliste muss vor der Verwendung der Rezeptfunktionen angelegt werden.

• Achten Sie beim Eintragen der Rezeptparameter auf den Datentyp: 16-Bit-Daten belegen ein Wort, 32-Bit-Daten zwei Worte. Wählen Sie einen passenden Datentyp. Achten Sie besonders auf 32-Bit-Adressen: Da sie zwei Worte belegen, dürfen sich Schreib- und Überwachungsadressen nicht überschneiden.

• Die Adresse RWI0 ist reserviert und dient nur zum Wechseln der Rezeptnummer. RWI0 = 0 bedeutet das erste Rezept usw.

• Die Adressen der Rezeptparameter sind fortlaufend.

Daten eines diskreten Rezepts, siehe Abbildung 7-33:

<img src="../../setting/formula.files/formula6181.png" width="795" />

Abbildung7-41  Seite „Daten“ eines diskreten Rezepts

• Anzahl der Rezepte: höchstens 128;

• Sprache: Element- und Rezeptnamen können je Sprache festgelegt werden.

• Rezeptname: ändert den Namen des aktuellen Rezepts, z. B. „Rezept1“, „Rezept2“.

• Neu: öffnet das Dialogfeld „Rezeptelement“ zum Anlegen eines Elements, wie unten.

  <img src="../../setting/formula.files/formula6495.png" width="517" />

Abbildung7-42  Neues Element eines diskreten Rezepts

• Löschen: löscht das aktuelle Rezeptelement.

• Alle löschen: löscht alle Elemente dieses Rezepts.

• Ändern: öffnet das Dialogfeld „Rezeptelement“ des aktuellen Elements zur Bearbeitung.

• Exportieren: öffnet einen Speicherdialog, um das Rezept unter gewähltem Pfad und Namen als \*.csv-Datei zu speichern.

• Importieren: öffnet einen Öffnen-Dialog, um eine \*.csv-Datei als aktuelles Rezept zu laden.
