# Indicadores de funcionamiento

La pantalla táctil tiene tres LED indicadores: alimentación (PWR), funcionamiento (RUN) y comunicación (COM), como en la figura siguiente.

<img src="../../../hardware/structure/lamp.files/image002.jpg" width="713" />

Indicadores de funcionamiento de la serie HM

PWR se enciende en verde cuando hay alimentación;

RUN se enciende en amarillo si la CPU funciona normalmente y se apaga si la CPU falla;

COM se enciende en amarillo cuando la pantalla táctil está conectada al PLC.

La tabla 1-1 muestra el estado de los 3 LED según el estado de funcionamiento.

|                                                    |                  |                   |                   |
|----------------------------------------------------|------------------|-------------------|-------------------|
| Estado del equipo                                       | LED verde (PWR) | LED amarillo (RUN) | LED amarillo (COM) |
| Sin alimentación                                    | ○                | ○                 | ○                 |
| Encendido                                           | ●                |                   |                   |
| CPU en marcha                                        | ●                | ●                 |                   |
| Comunicación con el equipo conectado                | ●                | ●                 | ※                 |
| ○: LED apagado;  ●: LED encendido;   ※: LED parpadeando |                  |                   |                   |

Tabla 1-1
