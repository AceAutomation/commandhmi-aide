# Voorbeeld padweergave

In het hoofdstuk “Padweergave” zagen we de betekenis en de instelling van de parameters van de padweergave; dit hoofdstuk beschrijft in detail de werking en het gebruik van het object voor de elementen “punt”, “lijn”, “boog” en “cirkel”.
Index: [punt](#jump1), [lijn](#jump2), [boog](#jump3), [cirkel](#jump4)
**Het hoofdscherm aanmaken**
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image.png)**Een gemeenschappelijk scherm aanmaken**
Met gemeenschappelijke schermen kan de gebruiker vaste, terugkerende objecten in één scherm plaatsen en ze gebruiken wanneer nodig. Zie voor gemeenschappelijke schermen het hoofdstuk “[Nieuw scherm aanmaken](../screen/new-screen.md)”.
Maak het volgende gemeenschappelijke scherm aan, met de objecten:
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-1-.png)

- Padweergave
  ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-2-.png)
- LB0 (trigger)
- LB1 (trigger wissen)
- LW50000 (aantal punten)
- LW50001 (kleur)
- Afbeeldingsknop (terug naar het hoofdscherm)

**Tip**: in het configuratieprogramma kunnen meerdere punten handig worden getoond door de adressen via een script te vullen
**Punt**

1.  Script aanmaken

\#include "MacroInit.h"

/\*\*\* @file pointInit\* @brief Padweergave: kopieert de puntgegevens\* @details Vanaf het beginpunt, x- en y-coördinaten bij elke stap\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];           ///&lt; Aantal elementen    unsigned short colour = LocalWord\[50001\];           ///&lt; kleur    unsigned short coordinateX = LocalWord\[50002\];      ///&lt; X-coördinaat    unsigned short coordinateY = LocalWord\[50003\];      ///&lt; Y-coördinaat

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 0;                   ///&lt; modus 0:punt 1:lijn 2:boog 3:cirkel        LocalWord\[i\*8+2\] = colour;              ///&lt;kleur        LocalWord\[i\*8+3\] = coordinateX+i;       ///&lt; X-coördinaat        LocalWord\[i\*8+4\] = coordinateY+i;       ///&lt; Y-coördinaat    }}

2.  Instellen

<!-- -->

3.  - LW50002: X-coördinaat
    - LW50003: Y

4.  Simulatieresultaat

        Start de onlinesimulatie en ga in het “hoofdscherm” naar “punt”
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-4-.png)Stel in: totaal 50 punten, zwart, X, Y (10, 10); zie voor de kleureigenschappen het hoofdstuk “[Padweergave](path-display.md)”. Klik op de knop “Tekenen”; het resultaat staat hieronder
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-5-.png)Stel de kleur wit in (voer ffffffff in) en teken opnieuw: trigger **LB1** om de tekening te wissen en **LB0** om opnieuw te tekenen
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-6-.png)De kern van de padweergave is het vullen van het “padgebied”, wat met een script kan gebeuren.

[Terug](#jump)

**Lijn**

1.  Script aanmaken

\#include "MacroInit.h"

/\*\*\* @file straightLineInit\* @brief Padweergave: kopieert de lijngegevens\* @details De x-coördinaat neemt vanaf het beginpunt telkens met 10 toe\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateEndX = LocalWord\[50004\];      unsigned short coordinateEndY = LocalWord\[50005\];       unsigned short mondel = LocalWord\[50006\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 1;                        ///&lt; modus 0:punt 1:lijn 2:boog 3:cirkel        LocalWord\[i\*8+2\] = colour;                        LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY;                        LocalWord\[i\*8+5\] = coordinateEndX+i\*10;               LocalWord\[i\*8+6\] = coordinateEndY;                   LocalWord\[i\*8+7\] = mondel;                       }}

2.  Instellen

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateEndX
    - LW50005：coordinateEndY
    - LW50006：mondel

4.  Simulatie

        Start de onlinesimulatie en ga in het hoofdscherm naar het scherm “lijn”
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-8-.png)size 5, zwart, beginpunt X, Y (10, 10), eindpunt X, Y (100, 100), mondel 1; zie voor de kleur- en lijntype-eigenschappen het hoofdstuk “[Padweergave](path-display.md)”. Klik op de knop “Tekenen”; het resultaat staat hieronder
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-9-.png)mondel 2: trigger LB1 om de tekening te wissen en LB0 om opnieuw te tekenen        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-10-.png)

[Terug](#jump)

**Boog**

1.  Script aanmaken

\#include "MacroInit.h"

/\*\*\* @file circularArcInit\* @brief Padweergave: kopieert de booggegevens\* @details x+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];         unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateBeginX = LocalWord\[50004\];     unsigned short coordinateBeginY = LocalWord\[50005\];     unsigned short coordinateEndX = LocalWord\[50006\];       unsigned short coordinateEndY = LocalWord\[50007\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 2;                        ///&lt; modus 0:punt 1:lijn 2:boog 3:cirkel        LocalWord\[i\*8+2\] = colour;                           LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY+i;                   LocalWord\[i\*8+5\] = coordinateBeginX+i\*10;          LocalWord\[i\*8+6\] = coordinateBeginY+i;               LocalWord\[i\*8+7\] = coordinateEndX+i\*10;               LocalWord\[i\*8+8\] = coordinateEndY+i;           }}

2.  Instellen

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateBeginX
    - LW50005：coordinateBeginY
    - LW50006：coordinateEndX
    - LW50007：coordinateEndY

4.  Simulatie

Start de onlinesimulatie en ga in het “hoofdscherm” naar het scherm “boog”
            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-12-.png)size 1, zwart, middelpunt X, Y (100, 100), beginpunt boog X, Y (120, 120), eindpunt boog X, Y (90, 120); zie voor de kleur het hoofdstuk “[Padweergave](path-display.md)”.            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-13-.png)size 5: trigger LB1 om de tekening te wissen en LB0 om opnieuw te tekenen![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-14-.png)

[Terug](#jump)

**Cirkel**

1.  Script aanmaken

\#include "MacroInit.h"

/\*\*\* @file roundInit\* @brief Padweergave: kopieert de cirkelgegevens\* @details x+10,y+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];              unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateRadius = LocalWord\[50004\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 3;                   ///&lt; modus 0:punt 1:lijn 2:boog 3:cirkel        LocalWord\[i\*8+2\] = colour;                      LocalWord\[i\*8+3\] = coordinateX+i\*10;           LocalWord\[i\*8+4\] = coordinateY+i;               LocalWord\[i\*8+5\] = coordinateRadius;      }}

2.  Instellen

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateRadius

4.  Simulatie

Start de onlinesimulatie en ga naar “cirkel”
![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-16-.png)
size 1, zwart, X, Y (100, 100), straal 10; zie het hoofdstuk “[Padweergave](path-display.md)”.![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-17-.png)
size 5, wit (FFFF), opnieuw tekenen: trigger LB1 om de tekening te wissen en LB0 om opnieuw te tekenen![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-18-.png)

[Terug](#jump)

Wat de padweergave tekent, hangt vooral af van de gegevens in het “padgebied” op het opgegeven adres: het eerste adres geeft het aantal elementen, daarna beschrijven telkens 8 adressen één element. Zie voor andere functies, zoals de melding bij het selecteren van een punt, het hoofdstuk “[Padweergave](path-display.md)”.
