# Fehlercodes der Kommunikation zwischen HMI und SPS

|                |                                                            |                |                                                               |
|----------------|------------------------------------------------------------|----------------|---------------------------------------------------------------|
| **Fehlercode** | **Information**                                            | **Fehlercode** | **Information**                                               |
| **0x11**       | Lokale Daten – Echtzeit lesen – ECC-Fehler                        | **0x41**       | Lokale Daten – Echtzeit lesen – keine Daten zurückgegeben                    |
| **0x12**       | Lokale Daten – Schreibvorgang – ECC-Fehler                       | **0x42**       | Lokale Daten – Schreibvorgang – keine Daten zurückgegeben                  |
| **0x13**       | Lokale Daten – Historische Daten lesen – ECC-Fehler                  | **0x43**       | Lokale Daten – Historische Daten lesen – keine Daten zurückgegeben             |
| **0x14**       | Lokale Daten – Alarme lesen – ECC-Fehler                            | **0x44**       | Lokale Daten – Alarme lesen – keine Daten zurückgegeben                       |
| **0x15**       | Lokale Daten – Rezept lesen – ECC-Fehler                          | **0x45**       | Lokale Daten – Rezept lesen – keine Daten zurückgegeben                     |
| **0x16**       | Lokale Daten – Rezept schreiben – ECC-Fehler                         | **0x46**       | Lokale Daten – Rezept schreiben – keine Daten zurückgegeben                    |
| **0x17**       | Lokale Daten – Datenübertragung lesen – ECC-Fehler                | **0x47**       | Lokale Daten – Datenübertragung lesen – keine Daten zurückgegeben            |
| **0x18**       | Lokale Daten – Datenübertragung schreiben – ECC-Fehler               | **0x48**       | Lokale Daten – Datenübertragung schreiben – keine Daten zurückgegeben          |
| **0x19**       | Lokale Daten – Uhr lesen – ECC-Fehler                            | **0x49**       | Lokale Daten – Uhr lesen – keine Daten zurückgegeben                       |
| **0x20**       | Lokale Daten – Uhr schreiben – ECC-Fehler                           | **0x50**       | Lokale Daten – Uhr schreiben – keine Daten zurückgegeben                      |
| **0x21**       | Lokale Daten – Skript lesen – ECC-Fehler                            | **0x51**       | Lokale Daten – Skript lesen – keine Daten zurückgegeben                       |
| **0x22**       | Lokale Daten – Skript schreiben – ECC-Fehler                           | **0x52**       | Lokale Daten – Skript schreiben – keine Daten zurückgegeben                      |
| **0x71**       | Lokale Daten – Echtzeit lesen – falsche Rücklänge              | **0x111**      | Durchgereichte Daten – Echtzeit lesen – ECC-Fehler                     |
| **0x72**       | Lokale Daten – Schreibvorgang – falsche Rücklänge            | **0x112**      | Durchgereichte Daten – Schreibvorgang – ECC-Fehler                   |
| **0x73**       | Lokale Daten – Historische Daten lesen – falsche Rücklänge       | **0x113**      | Durchgereichte Daten – Historische Daten lesen – ECC-Fehler               |
| **0x74**       | Lokale Daten – Alarme lesen – falsche Rücklänge                 | **0x114**      | Durchgereichte Daten – Alarme lesen – ECC-Fehler                         |
| **0x75**       | Lokale Daten – Rezept lesen – falsche Rücklänge               | **0x115**      | Durchgereichte Daten – Rezept lesen – ECC-Fehler                       |
| **0x76**       | Lokale Daten – Rezept schreiben – falsche Rücklänge              | **0x116**      | Durchgereichte Daten – Rezept schreiben – ECC-Fehler                      |
| **0x77**       | Lokale Daten – Datenübertragung lesen – falsche Rücklänge     | **0x117**      | Durchgereichte Daten – Datenübertragung lesen – ECC-Fehler             |
| **0x78**       | Lokale Daten – Datenübertragung schreiben – falsche Rücklänge    | **0x118**      | Durchgereichte Daten – Datenübertragung schreiben – ECC-Fehler            |
| **0x79**       | Lokale Daten – Uhr lesen – falsche Rücklänge                 | **0x119**      | Durchgereichte Daten – Uhr lesen – ECC-Fehler                         |
| **0x80**       | Lokale Daten – Uhr schreiben – falsche Rücklänge                | **0x120**      | Durchgereichte Daten – Uhr schreiben – ECC-Fehler                        |
| **0x81**       | Lokale Daten – Skript lesen – falsche Rücklänge                 | **0x121**      | Durchgereichte Daten – Skript lesen – ECC-Fehler                         |
| **0x82**       | Lokale Daten – Skript schreiben – falsche Rücklänge                | **0x122**      | Durchgereichte Daten – Skript schreiben – ECC-Fehler                        |
| **0x141**      | Durchgereichte Daten – Echtzeit lesen – keine Daten zurückgegeben           | **0x171**      | Durchgereichte Daten – Echtzeit lesen – falsche Rücklänge           |
| **0x142**      | Durchgereichte Daten – Schreibvorgang – keine Daten zurückgegeben         | **0x172**      | Durchgereichte Daten – Schreibvorgang – falsche Rücklänge         |
| **0x143**      | Durchgereichte Daten – Historische Daten lesen – keine Daten zurückgegeben    | **0x173**      | Durchgereichte Daten – Historische Daten lesen – falsche Rücklänge    |
| **0x144**      | Durchgereichte Daten – Alarme lesen – keine Daten zurückgegeben              | **0x174**      | Durchgereichte Daten – Alarme lesen – falsche Rücklänge              |
| **0x145**      | Durchgereichte Daten – Rezept lesen – keine Daten zurückgegeben            | **0x175**      | Durchgereichte Daten – Rezept lesen – falsche Rücklänge            |
| **0x146**      | Durchgereichte Daten – Rezept schreiben – keine Daten zurückgegeben           | **0x176**      | Durchgereichte Daten – Rezept schreiben – falsche Rücklänge           |
| **0x147**      | Durchgereichte Daten – Datenübertragung lesen – keine Daten zurückgegeben   | **0x177**      | Durchgereichte Daten – Datenübertragung lesen – falsche Rücklänge  |
| **0x148**      | Durchgereichte Daten – Datenübertragung schreiben – keine Daten zurückgegeben | **0x178**      | Durchgereichte Daten – Datenübertragung schreiben – falsche Rücklänge |
| **0x149**      | Durchgereichte Daten – Uhr lesen – keine Daten zurückgegeben              | **0x179**      | Durchgereichte Daten – Uhr lesen – falsche Rücklänge              |
| **0x150**      | Durchgereichte Daten – Uhr schreiben – keine Daten zurückgegeben             | **0x180**      | Durchgereichte Daten – Uhr schreiben – falsche Rücklänge             |
| **0x151**      | Durchgereichte Daten – Skript lesen – keine Daten zurückgegeben              | **0x181**      | Durchgereichte Daten – Skript lesen – falsche Rücklänge              |
| **0x152**      | Durchgereichte Daten – Skript schreiben – keine Daten zurückgegeben             | **0x182**      | Durchgereichte Daten – Skript schreiben – falsche Rücklänge             |
| **0x201**      | Handshake-Fehler                                          |                |                                                               |
