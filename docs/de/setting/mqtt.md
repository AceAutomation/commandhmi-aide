# Server

• **Seite „Allgemein“**

<img src="../../setting/mqtt.files/server-general.png" width="706" />

- IP (Domänenname)

IP des MQTT-Servers

- Port

Portnummer des MQTT-Servers

- Client-ID

Client-ID; bestimmte Sonderzeichen sind zulässig

- Benutzername

Benutzername (Authentifizierung muss aktiviert sein)

- Passwort

Benutzerpasswort (Authentifizierung muss aktiviert sein)

- Dauer der Verbindungsprüfung

Erhält der MQTT-Server nach Ablauf dieser Zeit keine Prüfnachricht vom HMI, gilt das HMI als getrennt.

• **Seite „Adresse“**

<img src="../../setting/mqtt.files/server-addr.png" width="706" />

- Statusadresse

Legt eine Gruppe von Wortadressen zur Prüfung des Verbindungsstatus fest.

**\[Statusadresse\] (Statusanzeige)**

Wert 0: Verbindung zum Server gestoppt.

Wert 1: vom Server getrennt.

Wert 2: Verbindung zum Server hergestellt.

**■   \[Statusadresse + 1\] (Fehleranzeige)**

|                      |                                                                                                                                                                                                                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Wert** | **Beschreibung**                                                                                                                                                                                                                                                                             |
| 0                    | Vorgang erfolgreich abgeschlossen                                                                                                                                                                                                                                                        |
| -1                   | MQTT-Client-Operation fehlgeschlagen                                                                                                                                                                                                                                                                |
| -2                   | Persistenzfehler                                                                                                                                                                                                                                                                           |
| -3                   | Client getrennt                                                                                                                                                                                                                                                                         |
| -4                   | Die Höchstzahl gleichzeitiger Nachrichten ist erreicht                                                                                                                                                                                                         |
| -5                   | Ungültige UTF-8-Zeichenkette erkannt                                                                                                                                                                                                                                                               |
| -6                   | Ein ungültiger leerer Parameter wurde übergeben                                                                                                                                                                                                                                                     |
| -7                   | Der Betreff wurde gekürzt (er enthält NULL-Zeichen); über die Betrefflänge auf den vollständigen Betreff zugreifen                                                                                                                                              |
| -8                   | Der Strukturparameter hat nicht die richtige Kennung (eye catcher) und Versionsnummer                                                                                                                                                                                                            |
| -9                   | Der Parameter qos ist nicht 0, 1 oder 2                                                                                                                                                                                                                                                          |
| -10                  | Alle 65535 MQTT-msgids sind belegt                                                                                                                                                                                                                                                            |
| -11                  | Die Anfrage ist unvollständig und wird verworfen                                                                                                                                                                                                                                          |
| -12                  | Keine weiteren Nachrichten puffern möglich                                                                                                                                                                                                                                                                 |
| -13                  | Versuch, die Nicht-SSL-Version der Bibliothek für eine SSL-Verbindung zu verwenden                                                                                                                                                                                                                         |
| -14                  | Das Protokollpräfix im serverURI muss lauten: tcp:// oder mqtt:// (unverschlüsseltes TCP), ssl:// oder mqtts:// (verschlüsseltes SSL/TLS), ws:// (unsichere WebSockets) oder wss:// (sichere WebSockets). Die TLS-Präfixe (ssl, mqtts, wss) gelten nur, wenn die TLS-Version der Bibliothek eingebunden ist |
| -15                  | Keine anderen Versionen der MQTT-Option verwenden                                                                                                                                                                                                                                                |
| -16                  | Der Aufruf gilt nicht für die MQTT-Version des Clients                                                                                                                                                                                                                                   |
| -17                  | Länge des Will-Betreffs ist null                                                                                                                                                                                                                                                                 |
| -18                  | Verbindungs- oder Trennbefehl ignoriert, da bereits ein solcher Befehl am Anfang der Warteschlange steht. Mit den Callbacks onSuccess/onFailure auf den Abschluss des vorherigen Befehls warten                                                    |
| -19                  | maxBufferedMessages in den Verbindungsoptionen muss &gt;=0 sein                                                                                                                                                                                                                                      |

- Steueradresse

**Datentyp des Registers: 16-Bit Ganzzahl.**

Ist der Wert kleiner oder gleich 0, wird die Verbindung zum MQTT-Server getrennt.

Ist der Wert größer als 0, bleibt die Verbindung zum MQTT-Server bestehen.
