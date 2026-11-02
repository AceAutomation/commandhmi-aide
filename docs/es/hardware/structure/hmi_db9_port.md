# Asignación de pines

Esquema del puerto de comunicación de 9 pines, como en la figura siguiente:

<img src="../../../hardware/structure/hmi_db9_port.files/image002.jpg" width="473" alt="pin.jpg" />

Puerto de comunicación de 9 pines

Este puerto sirve para conectar un PLC u otro controlador con puerto de comunicación RS232 / RS422 / RS485

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
