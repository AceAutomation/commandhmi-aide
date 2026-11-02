# Esempio di visualizzazione percorso

Il capitolo "Visualizzazione percorso" ha descritto il significato e l'impostazione dei parametri della visualizzazione percorso; questo capitolo illustra in dettaglio l'uso dell'oggetto per disegnare punti, linee, archi e cerchi.
Indice: [punto](#jump1), [linea](#jump2), [arco](#jump3), [cerchio](#jump4)
**Creare la pagina principale**
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image.png)**Creare una pagina comune**
Le pagine comuni permettono di raccogliere in un'unica pagina oggetti fissi e ripetitivi, da usare quando servono. Per la presentazione delle pagine comuni, vedere il capitolo "[Creare una nuova pagina](../screen/new-screen.md)".
Creare la seguente pagina comune, con gli oggetti:
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-1-.png)

- Visualizzazione percorso
  ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-2-.png)
- LB0 (trigger)
- LB1 (trigger di cancellazione)
- LW50000 (numero di punti)
- LW50001 (colore)
- Pulsante immagine (ritorno alla pagina principale)

**Suggerimento**: nel programma di configurazione, per visualizzare comodamente più punti, si assegnano i valori agli indirizzi tramite una macro
**Punto**

1.  Creare la macro

\#include "MacroInit.h"

/\*\*\* @file pointInit\* @brief Copia delle informazioni dei punti per la visualizzazione percorso\* @details A partire dal punto iniziale, coordinate x, y incrementate a ogni punto\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];           ///&lt; Numero di elementi    unsigned short colour = LocalWord\[50001\];           ///&lt; colore    unsigned short coordinateX = LocalWord\[50002\];      ///&lt; coordinata X    unsigned short coordinateY = LocalWord\[50003\];      ///&lt; coordinata Y

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 0;                   ///&lt; modo 0:punto 1:linea 2:arco 3:cerchio        LocalWord\[i\*8+2\] = colour;              ///&lt;colore        LocalWord\[i\*8+3\] = coordinateX+i;       ///&lt; coordinata X        LocalWord\[i\*8+4\] = coordinateY+i;       ///&lt; coordinata Y    }}

2.  Impostazione

<!-- -->

3.  - LW50002: coordinata X
    - LW50003: coordinata Y

4.  Risultato della simulazione

        Avviare la simulazione online e passare alla pagina "punto" dalla "pagina principale"
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-4-.png)Impostare 50 punti in totale, colore nero, X, Y (10, 10); per le proprietà del colore, vedere la sezione "[Visualizzazione percorso](path-display.md)". Fare clic sul pulsante "draw": il risultato è il seguente
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-5-.png)Impostare il colore bianco (inserire ffffffff) e ridisegnare la figura: occorre attivare **LB1** per cancellare il disegno e ridisegnare con **LB0**
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-6-.png)La visualizzazione percorso si basa sulla compilazione dell'"area di definizione del percorso", che può essere valorizzata in una macro.

[ritorno](#jump)

**Linea**

1.  Creare la macro

\#include "MacroInit.h"

/\*\*\* @file straightLineInit\* @brief Copia delle informazioni delle linee per la visualizzazione percorso\* @details Coordinata x del punto iniziale incrementata di 10 a ogni linea\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateEndX = LocalWord\[50004\];      unsigned short coordinateEndY = LocalWord\[50005\];       unsigned short mondel = LocalWord\[50006\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 1;                        ///&lt; modo 0:punto 1:linea 2:arco 3:cerchio        LocalWord\[i\*8+2\] = colour;                        LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY;                        LocalWord\[i\*8+5\] = coordinateEndX+i\*10;               LocalWord\[i\*8+6\] = coordinateEndY;                   LocalWord\[i\*8+7\] = mondel;                       }}

2.  Impostazione

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateEndX
    - LW50005：coordinateEndY
    - LW50006：mondel

4.  Simulazione

        Avviare la simulazione online e passare alla pagina "linea" dalla pagina principale
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-8-.png)size 5, nero, punto iniziale X, Y (10, 10), punto finale X, Y (100, 100), mondel 1; per le proprietà di colore e tipo di linea, vedere la sezione "[Visualizzazione percorso](path-display.md)". Fare clic sul pulsante "draw": il risultato è il seguente
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-9-.png)mondel 2: occorre attivare LB1 per cancellare il disegno e ridisegnare con LB0        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-10-.png)

[ritorno](#jump)

**Arco**

1.  Creare la macro

\#include "MacroInit.h"

/\*\*\* @file circularArcInit\* @brief Copia delle informazioni degli archi per la visualizzazione percorso\* @details x+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];         unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateBeginX = LocalWord\[50004\];     unsigned short coordinateBeginY = LocalWord\[50005\];     unsigned short coordinateEndX = LocalWord\[50006\];       unsigned short coordinateEndY = LocalWord\[50007\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 2;                        ///&lt; modo 0:punto 1:linea 2:arco 3:cerchio        LocalWord\[i\*8+2\] = colour;                           LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY+i;                   LocalWord\[i\*8+5\] = coordinateBeginX+i\*10;          LocalWord\[i\*8+6\] = coordinateBeginY+i;               LocalWord\[i\*8+7\] = coordinateEndX+i\*10;               LocalWord\[i\*8+8\] = coordinateEndY+i;           }}

2.  Impostazione

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateBeginX
    - LW50005：coordinateBeginY
    - LW50006：coordinateEndX
    - LW50007：coordinateEndY

4.  Simulazione

Avviare la simulazione online e passare alla pagina "arco" dalla "pagina principale"
            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-12-.png)size 1, nero, centro X, Y (100, 100), punto iniziale dell'arco X, Y (120, 120), punto finale dell'arco X, Y (90, 120); per il colore, vedere la sezione "[Visualizzazione percorso](path-display.md)".            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-13-.png)size 5: occorre attivare LB1 per cancellare il disegno e ridisegnare con LB0![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-14-.png)

[ritorno](#jump)

**Cerchio**

1.  Creare la macro

\#include "MacroInit.h"

/\*\*\* @file roundInit\* @brief Copia delle informazioni dei cerchi per la visualizzazione percorso\* @details x+10,y+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];              unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateRadius = LocalWord\[50004\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 3;                   ///&lt; modo 0:punto 1:linea 2:arco 3:cerchio        LocalWord\[i\*8+2\] = colour;                      LocalWord\[i\*8+3\] = coordinateX+i\*10;           LocalWord\[i\*8+4\] = coordinateY+i;               LocalWord\[i\*8+5\] = coordinateRadius;      }}

2.  Impostazione

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateRadius

4.  Simulazione

Avviare la simulazione online e passare alla pagina "cerchio"
![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-16-.png)
size 1, nero, X, Y (100, 100), raggio 10; vedere la sezione "[Visualizzazione percorso](path-display.md)".![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-17-.png)
size 5, ridisegno in bianco (FFFF): occorre attivare LB1 per cancellare il disegno e ridisegnare con LB0![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-18-.png)

[ritorno](#jump)

Il disegno dell'oggetto Visualizzazione percorso dipende principalmente dai dati dell'"area di definizione del percorso" all'indirizzo specificato: il primo indirizzo indica il numero di elementi, poi ogni gruppo di 8 indirizzi descrive un elemento. Per le altre funzioni, come la notifica di selezione dei punti, vedere la sezione "[Visualizzazione percorso](path-display.md)".
