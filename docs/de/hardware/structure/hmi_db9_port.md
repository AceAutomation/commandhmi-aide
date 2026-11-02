# Anschlussbelegung

Belegung der 9-poligen Kommunikationsschnittstelle, siehe Abbildung:

<img src="../../../hardware/structure/hmi_db9_port.files/image002.jpg" width="473" alt="pin.jpg" />

9-polige Kommunikationsschnittstelle

An diese Schnittstelle werden SPS oder andere Steuerungen mit RS232-, RS422- oder RS485-Schnittstelle angeschlossen

|     |       |       |       |
|-----|-------|-------|-------|
| Pin | RS232 | RS422 | RS485 |
| 1   |       |       |       |
| 2   | RX    |       |       |
| 3   | TX    |       |       |
| 4   |       |       |       |
| 5   | GND   |       |       |
| 6   |       | RX-   |       |
| 7   |       | RX+   |       |
| 8   |       | TX-   | B     |
| 9   |       | TX+   | A     |
