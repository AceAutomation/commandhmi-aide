# Server

• **Pagina “Algemeen”**

<img src="../../setting/mqtt.files/server-general.png" width="706" />

- IP (domeinnaam)

IP-adres van de MQTT-server

- Poort

Poortnummer van de MQTT-server

- Client-ID

Client-ID; bepaalde speciale tekens zijn toegestaan

- Gebruikersnaam

Gebruikersnaam (authenticatie moet zijn ingeschakeld)

- Wachtwoord

Wachtwoord van de gebruiker (authenticatie moet zijn ingeschakeld)

- Duur verbindingstest

Ontvangt de MQTT-server na deze tijd nog geen testbericht van de HMI, dan wordt de HMI als niet verbonden beschouwd.

• **Pagina “Adres”**

<img src="../../setting/mqtt.files/server-addr.png" width="706" />

- Statusadres

Een groep woordadressen om de verbindingsstatus te controleren.

**\[Statusadres\] (statusindicatie)**

Bij de waarde 0: de verbinding met de server is gestopt.

Bij de waarde 1: de verbinding met de server is verbroken.

Bij de waarde 2: de verbinding met de server is geslaagd.

**■   \[Statusadres + 1\] (foutindicatie)**

|                      |                                                                                                                                                                                                                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Waarde** | **Beschrijving**                                                                                                                                                                                                                                                                             |
| 0                    | Bewerking geslaagd                                                                                                                                                                                                                                                        |
| -1                   | MQTT-clientbewerking mislukt                                                                                                                                                                                                                                                                |
| -2                   | Persistentiefouten                                                                                                                                                                                                                                                                           |
| -3                   | Client losgekoppeld                                                                                                                                                                                                                                                                         |
| -4                   | Het maximale aantal gelijktijdige berichten is bereikt                                                                                                                                                                                                         |
| -5                   | Ongeldige UTF-8-tekenreeks gedetecteerd                                                                                                                                                                                                                                                               |
| -6                   | Er is een ongeldige lege parameter opgegeven                                                                                                                                                                                                                                                     |
| -7                   | Het onderwerp is afgekapt (het bevat NULL-tekens); gebruik de onderwerplengte om het volledige onderwerp te lezen                                                                                                                                              |
| -8                   | De structuurparameter heeft niet de juiste herkenning (eye catcher) en versie                                                                                                                                                                                                            |
| -9                   | De parameter qos is niet 0, 1 of 2                                                                                                                                                                                                                                                          |
| -10                  | Alle 65535 MQTT-msgids zijn in gebruik                                                                                                                                                                                                                                                            |
| -11                  | Het verzoek is onvolledig en wordt verworpen                                                                                                                                                                                                                                          |
| -12                  | Er kunnen geen berichten meer worden gebufferd                                                                                                                                                                                                                                                                 |
| -13                  | Poging de niet-SSL-versie van de bibliotheek te gebruiken voor een SSL-verbinding                                                                                                                                                                                                                         |
| -14                  | Het protocolvoorvoegsel in serverURI moet zijn: tcp:// of mqtt:// (onversleutelde TCP), ssl:// of mqtts:// (versleutelde SSL/TLS), ws:// (onveilige WebSockets) of wss:// (veilige WebSockets). De TLS-voorvoegsels (ssl, mqtts, wss) zijn alleen geldig als de TLS-versie van de bibliotheek is gekoppeld |
| -15                  | Gebruik geen andere versies van de MQTT-optie                                                                                                                                                                                                                                                |
| -16                  | De aanroep is niet van toepassing op de MQTT-versie van de client                                                                                                                                                                                                                                   |
| -17                  | Lengte van het Will-onderwerp is nul                                                                                                                                                                                                                                                                 |
| -18                  | Verbind- of verbreekopdracht genegeerd omdat er al zo een vooraan in de wachtrij staat. Gebruik de callbacks onSuccess/onFailure om te wachten tot de vorige opdracht is voltooid                                                    |
| -19                  | maxBufferedMessages in de verbindingsopties moet &gt;=0 zijn                                                                                                                                                                                                                                      |

- Besturingsadres

**Het gegevenstype van het register is 16-bits geheel getal.**

Bij een waarde kleiner dan of gelijk aan 0: verbinding met de MQTT-server verbreken.

Bij een waarde groter dan 0: verbinding met de MQTT-server behouden.
