# Betriebsanzeigen

Der Touchscreen hat drei LED-Anzeigen: Stromversorgung (PWR), Betrieb (RUN) und Kommunikation (COM), wie in der folgenden Abbildung.

<img src="../../../hardware/structure/lamp.files/image002.jpg" width="713" />

Betriebsanzeigen der HM-Serie

PWR leuchtet grün bei eingeschalteter Versorgung;

RUN leuchtet gelb, wenn die CPU normal arbeitet, und erlischt bei einem CPU-Fehler;

COM leuchtet gelb, wenn der Touchscreen mit der SPS verbunden ist.

Tabelle 1-1 zeigt die Zustände der 3 LED-Anzeigen in den verschiedenen Betriebszuständen.

|                                                    |                  |                   |                   |
|----------------------------------------------------|------------------|-------------------|-------------------|
| Gerätezustand                                       | Grüne LED (PWR) | Gelbe LED (RUN) | Gelbe LED (COM) |
| Keine Stromversorgung                                    | ○                | ○                 | ○                 |
| Eingeschaltet                                           | ●                |                   |                   |
| CPU läuft                                        | ●                | ●                 |                   |
| Kommunikation mit dem angeschlossenen Gerät                | ●                | ●                 | ※                 |
| ○: LED aus;  ●: LED an;   ※: LED blinkt |                  |                   |                   |

Tabelle 1-1
