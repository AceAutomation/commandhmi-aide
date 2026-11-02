# Foutcodes van de communicatie tussen HMI en PLC

|                |                                                            |                |                                                               |
|----------------|------------------------------------------------------------|----------------|---------------------------------------------------------------|
| **Foutcode** | **Informatie**                                            | **Foutcode** | **Informatie**                                               |
| **0x11**       | Lokale gegevens – Realtime lezen – ECC-fout                        | **0x41**       | Lokale gegevens – Realtime lezen – geen gegevens teruggestuurd                    |
| **0x12**       | Lokale gegevens – Schrijfbewerking – ECC-fout                       | **0x42**       | Lokale gegevens – Schrijfbewerking – geen gegevens teruggestuurd                  |
| **0x13**       | Lokale gegevens – Historische gegevens lezen – ECC-fout                  | **0x43**       | Lokale gegevens – Historische gegevens lezen – geen gegevens teruggestuurd             |
| **0x14**       | Lokale gegevens – Alarmen lezen – ECC-fout                            | **0x44**       | Lokale gegevens – Alarmen lezen – geen gegevens teruggestuurd                       |
| **0x15**       | Lokale gegevens – Recept lezen – ECC-fout                          | **0x45**       | Lokale gegevens – Recept lezen – geen gegevens teruggestuurd                     |
| **0x16**       | Lokale gegevens – Recept schrijven – ECC-fout                         | **0x46**       | Lokale gegevens – Recept schrijven – geen gegevens teruggestuurd                    |
| **0x17**       | Lokale gegevens – Gegevensoverdracht lezen – ECC-fout                | **0x47**       | Lokale gegevens – Gegevensoverdracht lezen – geen gegevens teruggestuurd            |
| **0x18**       | Lokale gegevens – Gegevensoverdracht schrijven – ECC-fout               | **0x48**       | Lokale gegevens – Gegevensoverdracht schrijven – geen gegevens teruggestuurd          |
| **0x19**       | Lokale gegevens – Klok lezen – ECC-fout                            | **0x49**       | Lokale gegevens – Klok lezen – geen gegevens teruggestuurd                       |
| **0x20**       | Lokale gegevens – Klok schrijven – ECC-fout                           | **0x50**       | Lokale gegevens – Klok schrijven – geen gegevens teruggestuurd                      |
| **0x21**       | Lokale gegevens – Script lezen – ECC-fout                            | **0x51**       | Lokale gegevens – Script lezen – geen gegevens teruggestuurd                       |
| **0x22**       | Lokale gegevens – Script schrijven – ECC-fout                           | **0x52**       | Lokale gegevens – Script schrijven – geen gegevens teruggestuurd                      |
| **0x71**       | Lokale gegevens – Realtime lezen – verkeerde antwoordlengte              | **0x111**      | Doorgestuurde gegevens – Realtime lezen – ECC-fout                     |
| **0x72**       | Lokale gegevens – Schrijfbewerking – verkeerde antwoordlengte            | **0x112**      | Doorgestuurde gegevens – Schrijfbewerking – ECC-fout                   |
| **0x73**       | Lokale gegevens – Historische gegevens lezen – verkeerde antwoordlengte       | **0x113**      | Doorgestuurde gegevens – Historische gegevens lezen – ECC-fout               |
| **0x74**       | Lokale gegevens – Alarmen lezen – verkeerde antwoordlengte                 | **0x114**      | Doorgestuurde gegevens – Alarmen lezen – ECC-fout                         |
| **0x75**       | Lokale gegevens – Recept lezen – verkeerde antwoordlengte               | **0x115**      | Doorgestuurde gegevens – Recept lezen – ECC-fout                       |
| **0x76**       | Lokale gegevens – Recept schrijven – verkeerde antwoordlengte              | **0x116**      | Doorgestuurde gegevens – Recept schrijven – ECC-fout                      |
| **0x77**       | Lokale gegevens – Gegevensoverdracht lezen – verkeerde antwoordlengte     | **0x117**      | Doorgestuurde gegevens – Gegevensoverdracht lezen – ECC-fout             |
| **0x78**       | Lokale gegevens – Gegevensoverdracht schrijven – verkeerde antwoordlengte    | **0x118**      | Doorgestuurde gegevens – Gegevensoverdracht schrijven – ECC-fout            |
| **0x79**       | Lokale gegevens – Klok lezen – verkeerde antwoordlengte                 | **0x119**      | Doorgestuurde gegevens – Klok lezen – ECC-fout                         |
| **0x80**       | Lokale gegevens – Klok schrijven – verkeerde antwoordlengte                | **0x120**      | Doorgestuurde gegevens – Klok schrijven – ECC-fout                        |
| **0x81**       | Lokale gegevens – Script lezen – verkeerde antwoordlengte                 | **0x121**      | Doorgestuurde gegevens – Script lezen – ECC-fout                         |
| **0x82**       | Lokale gegevens – Script schrijven – verkeerde antwoordlengte                | **0x122**      | Doorgestuurde gegevens – Script schrijven – ECC-fout                        |
| **0x141**      | Doorgestuurde gegevens – Realtime lezen – geen gegevens teruggestuurd           | **0x171**      | Doorgestuurde gegevens – Realtime lezen – verkeerde antwoordlengte           |
| **0x142**      | Doorgestuurde gegevens – Schrijfbewerking – geen gegevens teruggestuurd         | **0x172**      | Doorgestuurde gegevens – Schrijfbewerking – verkeerde antwoordlengte         |
| **0x143**      | Doorgestuurde gegevens – Historische gegevens lezen – geen gegevens teruggestuurd    | **0x173**      | Doorgestuurde gegevens – Historische gegevens lezen – verkeerde antwoordlengte    |
| **0x144**      | Doorgestuurde gegevens – Alarmen lezen – geen gegevens teruggestuurd              | **0x174**      | Doorgestuurde gegevens – Alarmen lezen – verkeerde antwoordlengte              |
| **0x145**      | Doorgestuurde gegevens – Recept lezen – geen gegevens teruggestuurd            | **0x175**      | Doorgestuurde gegevens – Recept lezen – verkeerde antwoordlengte            |
| **0x146**      | Doorgestuurde gegevens – Recept schrijven – geen gegevens teruggestuurd           | **0x176**      | Doorgestuurde gegevens – Recept schrijven – verkeerde antwoordlengte           |
| **0x147**      | Doorgestuurde gegevens – Gegevensoverdracht lezen – geen gegevens teruggestuurd   | **0x177**      | Doorgestuurde gegevens – Gegevensoverdracht lezen – verkeerde antwoordlengte  |
| **0x148**      | Doorgestuurde gegevens – Gegevensoverdracht schrijven – geen gegevens teruggestuurd | **0x178**      | Doorgestuurde gegevens – Gegevensoverdracht schrijven – verkeerde antwoordlengte |
| **0x149**      | Doorgestuurde gegevens – Klok lezen – geen gegevens teruggestuurd              | **0x179**      | Doorgestuurde gegevens – Klok lezen – verkeerde antwoordlengte              |
| **0x150**      | Doorgestuurde gegevens – Klok schrijven – geen gegevens teruggestuurd             | **0x180**      | Doorgestuurde gegevens – Klok schrijven – verkeerde antwoordlengte             |
| **0x151**      | Doorgestuurde gegevens – Script lezen – geen gegevens teruggestuurd              | **0x181**      | Doorgestuurde gegevens – Script lezen – verkeerde antwoordlengte              |
| **0x152**      | Doorgestuurde gegevens – Script schrijven – geen gegevens teruggestuurd             | **0x182**      | Doorgestuurde gegevens – Script schrijven – verkeerde antwoordlengte             |
| **0x201**      | Handshakefout                                          |                |                                                               |
