# Códigos de error de comunicación entre el HMI y el PLC

|                |                                                            |                |                                                               |
|----------------|------------------------------------------------------------|----------------|---------------------------------------------------------------|
| **Código de error** | **Información**                                            | **Código de error** | **Información**                                               |
| **0x11**       | Datos locales – Lectura en tiempo real – error ECC                        | **0x41**       | Datos locales – Lectura en tiempo real – sin datos devueltos                    |
| **0x12**       | Datos locales – Operación de escritura – error ECC                       | **0x42**       | Datos locales – Operación de escritura – sin datos devueltos                  |
| **0x13**       | Datos locales – Leer datos históricos – error ECC                  | **0x43**       | Datos locales – Leer datos históricos – sin datos devueltos             |
| **0x14**       | Datos locales – Leer alarmas – error ECC                            | **0x44**       | Datos locales – Leer alarmas – sin datos devueltos                       |
| **0x15**       | Datos locales – Leer receta – error ECC                          | **0x45**       | Datos locales – Leer receta – sin datos devueltos                     |
| **0x16**       | Datos locales – Escribir receta – error ECC                         | **0x46**       | Datos locales – Escribir receta – sin datos devueltos                    |
| **0x17**       | Datos locales – Leer transferencia de datos – error ECC                | **0x47**       | Datos locales – Leer transferencia de datos – sin datos devueltos            |
| **0x18**       | Datos locales – Escribir transferencia de datos – error ECC               | **0x48**       | Datos locales – Escribir transferencia de datos – sin datos devueltos          |
| **0x19**       | Datos locales – Leer reloj – error ECC                            | **0x49**       | Datos locales – Leer reloj – sin datos devueltos                       |
| **0x20**       | Datos locales – Escribir reloj – error ECC                           | **0x50**       | Datos locales – Escribir reloj – sin datos devueltos                      |
| **0x21**       | Datos locales – Leer script – error ECC                            | **0x51**       | Datos locales – Leer script – sin datos devueltos                       |
| **0x22**       | Datos locales – Escribir script – error ECC                           | **0x52**       | Datos locales – Escribir script – sin datos devueltos                      |
| **0x71**       | Datos locales – Lectura en tiempo real – longitud de respuesta incorrecta              | **0x111**      | Datos de paso – Lectura en tiempo real – error ECC                     |
| **0x72**       | Datos locales – Operación de escritura – longitud de respuesta incorrecta            | **0x112**      | Datos de paso – Operación de escritura – error ECC                   |
| **0x73**       | Datos locales – Leer datos históricos – longitud de respuesta incorrecta       | **0x113**      | Datos de paso – Leer datos históricos – error ECC               |
| **0x74**       | Datos locales – Leer alarmas – longitud de respuesta incorrecta                 | **0x114**      | Datos de paso – Leer alarmas – error ECC                         |
| **0x75**       | Datos locales – Leer receta – longitud de respuesta incorrecta               | **0x115**      | Datos de paso – Leer receta – error ECC                       |
| **0x76**       | Datos locales – Escribir receta – longitud de respuesta incorrecta              | **0x116**      | Datos de paso – Escribir receta – error ECC                      |
| **0x77**       | Datos locales – Leer transferencia de datos – longitud de respuesta incorrecta     | **0x117**      | Datos de paso – Leer transferencia de datos – error ECC             |
| **0x78**       | Datos locales – Escribir transferencia de datos – longitud de respuesta incorrecta    | **0x118**      | Datos de paso – Escribir transferencia de datos – error ECC            |
| **0x79**       | Datos locales – Leer reloj – longitud de respuesta incorrecta                 | **0x119**      | Datos de paso – Leer reloj – error ECC                         |
| **0x80**       | Datos locales – Escribir reloj – longitud de respuesta incorrecta                | **0x120**      | Datos de paso – Escribir reloj – error ECC                        |
| **0x81**       | Datos locales – Leer script – longitud de respuesta incorrecta                 | **0x121**      | Datos de paso – Leer script – error ECC                         |
| **0x82**       | Datos locales – Escribir script – longitud de respuesta incorrecta                | **0x122**      | Datos de paso – Escribir script – error ECC                        |
| **0x141**      | Datos de paso – Lectura en tiempo real – sin datos devueltos           | **0x171**      | Datos de paso – Lectura en tiempo real – longitud de respuesta incorrecta           |
| **0x142**      | Datos de paso – Operación de escritura – sin datos devueltos         | **0x172**      | Datos de paso – Operación de escritura – longitud de respuesta incorrecta         |
| **0x143**      | Datos de paso – Leer datos históricos – sin datos devueltos    | **0x173**      | Datos de paso – Leer datos históricos – longitud de respuesta incorrecta    |
| **0x144**      | Datos de paso – Leer alarmas – sin datos devueltos              | **0x174**      | Datos de paso – Leer alarmas – longitud de respuesta incorrecta              |
| **0x145**      | Datos de paso – Leer receta – sin datos devueltos            | **0x175**      | Datos de paso – Leer receta – longitud de respuesta incorrecta            |
| **0x146**      | Datos de paso – Escribir receta – sin datos devueltos           | **0x176**      | Datos de paso – Escribir receta – longitud de respuesta incorrecta           |
| **0x147**      | Datos de paso – Leer transferencia de datos – sin datos devueltos   | **0x177**      | Datos de paso – Leer transferencia de datos – longitud de respuesta incorrecta  |
| **0x148**      | Datos de paso – Escribir transferencia de datos – sin datos devueltos | **0x178**      | Datos de paso – Escribir transferencia de datos – longitud de respuesta incorrecta |
| **0x149**      | Datos de paso – Leer reloj – sin datos devueltos              | **0x179**      | Datos de paso – Leer reloj – longitud de respuesta incorrecta              |
| **0x150**      | Datos de paso – Escribir reloj – sin datos devueltos             | **0x180**      | Datos de paso – Escribir reloj – longitud de respuesta incorrecta             |
| **0x151**      | Datos de paso – Leer script – sin datos devueltos              | **0x181**      | Datos de paso – Leer script – longitud de respuesta incorrecta              |
| **0x152**      | Datos de paso – Escribir script – sin datos devueltos             | **0x182**      | Datos de paso – Escribir script – longitud de respuesta incorrecta             |
| **0x201**      | Fallo de handshake                                          |                |                                                               |
