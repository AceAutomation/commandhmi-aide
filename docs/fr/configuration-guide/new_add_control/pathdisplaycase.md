# Exemple d'affichage de tracé

Le chapitre « Affichage de tracé » a présenté la signification et le réglage des paramètres de l'affichage de tracé ; ce chapitre détaille l'utilisation de l'objet pour dessiner des points, des lignes, des arcs et des cercles.
Index : [point](#jump1), [ligne droite](#jump2), [arc](#jump3), [cercle](#jump4)
**Créer l'écran principal**
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image.png)**Créer un écran commun**
L'écran commun permet de placer dans un seul écran des objets fixes et répétitifs, réutilisés au besoin. Pour la présentation de l'écran commun, voir le chapitre « [Créer un écran](../screen/new-screen.md) ».
Créez l'écran commun suivant, avec les objets :
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-1-.png)

- Affichage de tracé
  ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-2-.png)
- LB0 (déclenchement)
- LB1 (effacement)
- LW50000 (nombre de points)
- LW50001 (couleur)
- Bouton d'écran (retour à l'écran principal)

**Astuce** : dans le programme de configuration, pour afficher facilement plusieurs points, on affecte les valeurs des adresses par une macro
**point**

1.  Créer la macro

\#include "MacroInit.h"

/\*\*\* @file pointInit\* @brief Path display copy point information\* @details On the starting point, the x, y coordinates each time\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];           ///&lt; Drawing number    unsigned short colour = LocalWord\[50001\];           ///&lt; color    unsigned short coordinateX = LocalWord\[50002\];      ///&lt; X coordinates    unsigned short coordinateY = LocalWord\[50003\];      ///&lt; Y coordinates

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 0;                   ///&lt; mode 0:point 1:line 2:circular arc 3:round        LocalWord\[i\*8+2\] = colour;              ///&lt;color        LocalWord\[i\*8+3\] = coordinateX+i;       ///&lt; X coordinates        LocalWord\[i\*8+4\] = coordinateY+i;       ///&lt; Y coordinates    }}

2.  Réglages

<!-- -->

3.  - LW50002：X coordinates
    - LW50003：Y

4.  Résultat en simulation

        Lancez la simulation en ligne et passez à « point » dans l'« écran principal »
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-4-.png)Réglez 50 points au total, noir, X, Y (10, 10) ; pour les valeurs de couleur, voir la section « [Affichage de tracé](path-display.md) ». Cliquez sur le bouton « dessiner » : le résultat est le suivant
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-5-.png)Réglez la couleur blanche (saisissez ffffffff) et redessinez : il faut déclencher **LB1** pour effacer le dessin et **LB0** pour redessiner
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-6-.png)L'essentiel de l'affichage de tracé est le remplissage de la « zone de définition du tracé », que l'on peut faire par affectation dans une macro.

[retour](#jump)

**Ligne droite**

1.  Créer la macro

\#include "MacroInit.h"

/\*\*\* @file straightLineInit\* @brief The path display copies the line information\* @details The x-coordinate is every time on the starting point+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateEndX = LocalWord\[50004\];      unsigned short coordinateEndY = LocalWord\[50005\];       unsigned short mondel = LocalWord\[50006\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 1;                        ///&lt; mode 0:point 1:line 2:circular arc 3:round        LocalWord\[i\*8+2\] = colour;                        LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY;                        LocalWord\[i\*8+5\] = coordinateEndX+i\*10;               LocalWord\[i\*8+6\] = coordinateEndY;                   LocalWord\[i\*8+7\] = mondel;                       }}

2.  Réglages

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateEndX
    - LW50005：coordinateEndY
    - LW50006：mondel

4.  Simulation

        Lancez la simulation en ligne et passez à l'écran « ligne » depuis l'écran principal
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-8-.png)size 5, noir, point de départ X, Y (10, 10), point d'arrivée X, Y (100, 100), mondel 1 ; pour les couleurs et types de trait, voir la section « [Affichage de tracé](path-display.md) ». Cliquez sur le bouton « dessiner » : le résultat est le suivant
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-9-.png)mondel 2 ; il faut déclencher LB1 pour effacer le dessin et LB0 pour redessiner        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-10-.png)

[retour](#jump)

**Arc**

1.  Créer la macro

\#include "MacroInit.h"

/\*\*\* @file circularArcInit\* @brief The path display copies the circular information\* @details x+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];         unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateBeginX = LocalWord\[50004\];     unsigned short coordinateBeginY = LocalWord\[50005\];     unsigned short coordinateEndX = LocalWord\[50006\];       unsigned short coordinateEndY = LocalWord\[50007\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 2;                        ///&lt; mode 0:point 1:line 2:circular arc 3:round        LocalWord\[i\*8+2\] = colour;                           LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY+i;                   LocalWord\[i\*8+5\] = coordinateBeginX+i\*10;          LocalWord\[i\*8+6\] = coordinateBeginY+i;               LocalWord\[i\*8+7\] = coordinateEndX+i\*10;               LocalWord\[i\*8+8\] = coordinateEndY+i;           }}

2.  Réglages

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateBeginX
    - LW50005：coordinateBeginY
    - LW50006：coordinateEndX
    - LW50007：coordinateEndY

4.  Simulation

Lancez la simulation en ligne et passez à l'écran « arc » depuis l'« écran principal »
            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-12-.png)size 1, noir, centre X, Y (100, 100), début de l'arc X, Y (120, 120), fin de l'arc X, Y (90, 120) ; pour la couleur, voir la section « [Affichage de tracé](path-display.md) ».            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-13-.png)size 5 ; il faut déclencher LB1 pour effacer le dessin et LB0 pour redessiner![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-14-.png)

[retour](#jump)

**cercle**

1.  Créer la macro

\#include "MacroInit.h"

/\*\*\* @file roundInit\* @brief The path display copies the round information\* @details x+10,y+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];              unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateRadius = LocalWord\[50004\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 3;                   ///&lt; mode 0:point 1:line 2:circular arc 3:round        LocalWord\[i\*8+2\] = colour;                      LocalWord\[i\*8+3\] = coordinateX+i\*10;           LocalWord\[i\*8+4\] = coordinateY+i;               LocalWord\[i\*8+5\] = coordinateRadius;      }}

2.  Réglages

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateRadius

4.  Simulation

Lancez la simulation en ligne et passez à « cercle »
![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-16-.png)
size 1, noir, X, Y (100, 100), rayon 10 ; voir la section « [Affichage de tracé](path-display.md) ».![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-17-.png)
size 5, blanc (FFFF), redessin ; il faut déclencher LB1 pour effacer le dessin et LB0 pour redessiner![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-18-.png)

[retour](#jump)

Le dessin de l'affichage de tracé repose sur les données de la « zone de définition du tracé » : la première adresse indique le nombre d'éléments, puis chaque groupe de 8 adresses décrit un élément. Pour les autres fonctions, comme la notification de point sélectionné, voir la section « [Affichage de tracé](path-display.md) ».
