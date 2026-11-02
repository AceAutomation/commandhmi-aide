# Topic

Ø  Veröffentlichungs-Topic hinzufügen

• Seite „Allgemein“

![](../../setting/mqtttheme.files/addpublish.png)

- Name

Projektname des MQTT-Topics

- Topic

Topic, unter dem der MQTT-Server die gesendete Nachricht empfängt

- Format

\[JSON (allgemein)\]: Daten im JSON-Format mit Listenstruktur.

\[JSON (erweitert)\]: JSON-Format mit frei definierbarer Baumstruktur.

- Sendemodus

**■  automatisch**

Bei Wertänderung: Ändert sich der Inhalt der Überwachungsadresse, wird er automatisch übertragen.

Zyklisch: Der Inhalt der Überwachungsadresse wird periodisch übertragen.

**■  Bit-Trigger**

Der Inhalt wird übertragen, wenn eine angegebene Bitadresse auslöst.

• Adresse (JSON allgemein)

Einstellbar, wenn auf der Seite \[Allgemein\] das Format \[JSON allgemein\] gewählt ist.
<img src="../../setting/mqtttheme.files/addgeneraladdr.png" width="606" />

Fügt einen Wert hinzu. Typ Bit oder Wort; fester Wert oder aus einer angegebenen Adresse gelesene Daten.

• Adresse (JSON erweitert)

Einstellbar, wenn auf der Seite \[Allgemein\] das Format \[JSON erweitert\] gewählt ist.
<img src="../../setting/mqtttheme.files/addextendaddr.png" width="606" />

Die Adresseinstellung unterstützt eine Baumstruktur mit Elementen, Arrays usw.; Zeitstempel und Datennamen sind frei definierbar.

- Element

Fügt ein Datenelement hinzu. Ein Element kann mehrere Datenformate enthalten, jedes mit eigenem Namen und Wert.

Die Daten des Elements stehen in geschweiften Klammern { }.

- Array

Fügt ein Datenarray hinzu. Ein Array kann mehrere Datenformate enthalten, hat aber nur einen Namen.

Die Daten stehen in eckigen Klammern \[ \].

- Wert

Fügt einen Wert, eine Zeichenkette oder einen Zeitstempel hinzu. Wert oder Zeichenkette können fest sein oder aus einer angegebenen Adresse gelesen werden.

- Vorlage

Wandelt einen vom Benutzer bearbeiteten JSON-Text in eine Baumstruktur um

- Vorschau

Wandelt die aktuelle Baumstruktur in JSON-Text um

• Seite „Sicherheit“

Wenn aktiviert, wirkt sie, sobald die eingestellte Bitadresse die Triggerbedingung erfüllt.
<img src="../../setting/mqtttheme.files/publishsecurity.png" width="606" />

Ø  Abonnement-Topic hinzufügen

• Seite „Allgemein“

<img src="../../setting/mqtttheme.files/addsubscribe.png" width="606" />

- Name

Projektname des MQTT-Topics

- Topic

Vom MQTT-Server abonniertes Topic

- Format

[wie bei【Veröffentlichen】](#anchor-name)

- Betriebsart

■  automatisch

automatisch.

■  Manuell

Die Ausführung erfolgt durch Setzen der angegebenen Adresse.

• Seite „Adresse“

[Wie bei【Veröffentlichen】](#anchor-name)

• Seite „Sicherheit“

[Wie bei【Veröffentlichen】](#anchor-name)
