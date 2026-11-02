# HTTP

<img src="../../setting/lisanbaojing.files/image007.jpg" width="133" alt="lisanbaojing2414" /> Nur das entfernte Bild unterstützt diese Funktion

![](../../setting/http.files/open.png)

Mit dieser Funktion lassen sich die Parameter des HTTP-Servers einfach einstellen

Ø  Seite „Allgemein“

<img src="../../setting/http.files/general.png" width="606" />

- Name

Verbindungsname

- URL

Ziel-URL der HTTP-Anfrage

- Methode

Methode der HTTP-Anfrage: GET oder POST

- Kodierung

Kodierungsformat

- Request-Header

Header der HTTP-Anfrage

- Timeout

Antwortzeit von HTTP

- Formate

umfasst: JSON (allgemein) oder JSON (erweitert), [wie bei 【MQTT】](mqtttheme.md#anchor-name)

- Übertragungsmodi

umfasst: automatisch und durch Bit ausgelöst

Ø  Seite „Adresse“ (JSON allgemein)

Einstellbar, wenn auf der Seite \[Allgemein\] das Format \[JSON allgemein\] gewählt ist.

Fügt einen Wert hinzu. Typ Bit oder Wort; fester Wert oder aus einer angegebenen Adresse gelesene Daten. [Siehe 【MQTT】](mqtttheme.md#anchor-name1)

Ø  Seite „JSON senden“ (JSON erweitert)

Einstellbar, wenn auf der Seite \[Allgemein\] das Format \[JSON erweitert\] gewählt ist.
<img src="../../setting/http.files/sendjson.png" width="606" />

Legt die gesendeten Daten fest. Die Adresseinstellung unterstützt eine Baumstruktur mit Elementen, Arrays usw.; Zeitstempel und Datennamen sind frei definierbar. [Siehe 【MQTT】](mqtttheme.md#anchor-name1)

Ø  Seite „JSON empfangen“

<img src="../../setting/http.files/receivejson.png" width="606" />

Legt die empfangenen Daten fest. Die Adresseinstellung unterstützt eine Baumstruktur mit Elementen, Arrays usw.; Zeitstempel und Datennamen sind frei definierbar. Siehe [【JSON senden】](#anchor-name)

Ø  Seite „Sicherheit“

Siehe Seite \[Sicherheit\] unter [\[MQTT\].](mqtttheme.md#anchor-name2)
