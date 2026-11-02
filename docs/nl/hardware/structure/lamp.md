# Bedrijfsindicatielampjes

Het touchscreen heeft drie indicatie-LED's: voeding (PWR), bedrijf (RUN) en communicatie (COM), zoals in de afbeelding hieronder.

<img src="../../../hardware/structure/lamp.files/image002.jpg" width="713" />

Bedrijfsindicatielampjes HM-serie

PWR brandt groen als er voeding is;

RUN brandt geel als de CPU normaal werkt en dooft bij een CPU-fout;

COM brandt geel als het touchscreen met de PLC is verbonden.

Tabel 1-1 toont de status van de 3 LED's in de verschillende bedrijfstoestanden.

|                                                    |                  |                   |                   |
|----------------------------------------------------|------------------|-------------------|-------------------|
| Apparaatstatus                                       | Groene LED (PWR) | Gele LED (RUN) | Gele LED (COM) |
| Geen voeding                                    | ○                | ○                 | ○                 |
| Ingeschakeld                                           | ●                |                   |                   |
| CPU draait                                        | ●                | ●                 |                   |
| Communicatie met het aangesloten apparaat                | ●                | ●                 | ※                 |
| ○: LED uit;  ●: LED aan;   ※: LED knippert |                  |                   |                   |

Tabel 1-1
