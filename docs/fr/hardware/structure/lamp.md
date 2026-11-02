# Voyants de fonctionnement

L'écran tactile comporte trois LED : alimentation (PWR), fonctionnement (RUN) et communication (COM), comme sur la figure ci-dessous.

<img src="../../../hardware/structure/lamp.files/image002.jpg" width="713" />

Voyants de fonctionnement de la série HM

PWR s'allume en vert quand l'appareil est alimenté ;

RUN s'allume en jaune quand le processeur fonctionne normalement et s'éteint en cas de défaut ;

COM s'allume en jaune quand l'écran tactile est connecté à l'automate.

Le tableau 1-1 indique l'état des 3 LED selon l'état de fonctionnement.

|                                                    |                  |                   |                   |
|----------------------------------------------------|------------------|-------------------|-------------------|
| État de l'appareil                                 | LED verte（PWR） | LED jaune（RUN）  | LED jaune（COM）  |
| Pas d'alimentation                                 | ○                | ○                 | ○                 |
| Sous tension                                       | ●                |                   |                   |
| Processeur en marche                               | ●                | ●                 |                   |
| Communication avec l'équipement connecté           | ●                | ●                 | ※                 |
| ○ : LED éteinte ;  ● : LED allumée ;   ※ : LED clignotante |          |                   |                   |

Tableau 1-1
