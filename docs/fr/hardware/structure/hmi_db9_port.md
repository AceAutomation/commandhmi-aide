# Brochage

Schéma du port de communication 9 broches, comme sur la figure ci-dessous :

<img src="../../../hardware/structure/hmi_db9_port.files/image002.jpg" width="473" alt="pin.jpg" />

Port de communication 9 broches

Ce port sert à relier un automate ou un autre contrôleur doté d'un port RS232 / RS422 / RS485

|     |       |       |       |
|-----|-------|-------|-------|
| Broche | RS232 | RS422 | RS485 |
| 1   |       |       |       |
| 2   | RX    |       |       |
| 3   | TX    |       |       |
| 4   |       |       |       |
| 5   | GND   |       |       |
| 6   |       | RX-   |       |
| 7   |       | RX+   |       |
| 8   |       | TX-   | B     |
| 9   |       | TX+   | A     |
