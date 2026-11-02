# Spie di funzionamento

Le spie del touch screen sono tre LED: alimentazione (PWR), funzionamento (RUN) e comunicazione (COM), come mostrato nella figura seguente.

<img src="../../../hardware/structure/lamp.files/image002.jpg" width="713" />

Spie di funzionamento della serie HM

PWR è verde quando l'apparecchio è alimentato;

RUN è gialla se la CPU funziona normalmente e spenta in caso di guasto della CPU;

COM è gialla quando il touch screen è collegato al PLC.

La tabella 1-1 riporta lo stato dei 3 LED nelle diverse condizioni di funzionamento.

|                                                    |                  |                   |                   |
|----------------------------------------------------|------------------|-------------------|-------------------|
| Stato dell'apparecchio | LED verde (PWR) | LED giallo (RUN) | LED giallo (COM) |
| Non alimentato | ○ | ○ | ○ |
| Alimentato | ● |                   |                   |
| CPU in funzione | ● | ● |                   |
| Comunicazione con il dispositivo collegato | ● | ● | ※ |
| ○: LED spento;  ●: LED acceso;   ※: LED lampeggiante |                  |                   |                   |

Tabella 1-1
