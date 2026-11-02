# Beispiel Bahnanzeige

Im Kapitel „Bahnanzeige“ wurden Bedeutung und Einstellung der Parameter erläutert; dieses Kapitel zeigt die Funktion und Verwendung des Objekts an den Elementen „Punkt“, „Linie“, „Bogen“ und „Kreis“.
Index: [Punkt](#jump1), [Linie](#jump2), [Bogen](#jump3), [Kreis](#jump4)
**Hauptbild anlegen**
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image.png)**Gemeinsames Bild anlegen**
In einem gemeinsamen Bild können feste, wiederkehrende Objekte abgelegt und bei Bedarf verwendet werden. Zu gemeinsamen Bildern siehe das Kapitel „[Neues Bild anlegen](../screen/new-screen.md)“.
Legen Sie folgendes gemeinsames Bild mit diesen Objekten an:
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-1-.png)

- Bahnanzeige
  ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-2-.png)
- LB0 (Zeichnen auslösen)
- LB1 (Löschen auslösen)
- LW50000 (Anzahl der Punkte)
- LW50001 (Farbe)
- Bildwechsel-Taste (zurück zum Hauptbild)

**Tipp**: Um im Projekt bequem viele Punkte anzuzeigen, werden die Adressen per Skript beschrieben
**Punkt**

1.  Skript anlegen

\#include "MacroInit.h"

/\*\*\* @file pointInit\* @brief Path display copy point information\* @details On the starting point, the x, y coordinates each time\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];           ///&lt; Drawing number    unsigned short colour = LocalWord\[50001\];           ///&lt; color    unsigned short coordinateX = LocalWord\[50002\];      ///&lt; X coordinates    unsigned short coordinateY = LocalWord\[50003\];      ///&lt; Y coordinates

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 0;                   ///&lt; mode 0:point 1:line 2:circular arc 3:round        LocalWord\[i\*8+2\] = colour;              ///&lt;color        LocalWord\[i\*8+3\] = coordinateX+i;       ///&lt; X coordinates        LocalWord\[i\*8+4\] = coordinateY+i;       ///&lt; Y coordinates    }}

2.  Einstellungen

<!-- -->

3.  - LW50002: X-Koordinate
    - LW50003: Y

4.  Simulation

        Starten Sie die Online-Simulation und wechseln Sie im „Hauptbild“ zu „Punkt“
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-4-.png)Anzahl der Punkte 50, Schwarz, X, Y (10, 10); zu den Farben siehe Abschnitt „[Bahnanzeige](path-display.md)“. Klicken Sie auf „Zeichnen“; das Ergebnis sehen Sie unten
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-5-.png)Farbe Weiß (ffffffff eingeben) und neu zeichnen: Dazu muss **LB1** die Zeichnung löschen und **LB0** neu zeichnen
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-6-.png)Entscheidend für die Bahnanzeige ist das Füllen des „Bahndefinitionsbereichs“, das per Skript erfolgen kann.

[zurück](#jump)

**Linie**

1.  Skript anlegen

\#include "MacroInit.h"

/\*\*\* @file straightLineInit\* @brief The path display copies the line information\* @details The x-coordinate is every time on the starting point+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateEndX = LocalWord\[50004\];      unsigned short coordinateEndY = LocalWord\[50005\];       unsigned short mondel = LocalWord\[50006\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 1;                        ///&lt; mode 0:point 1:line 2:circular arc 3:round        LocalWord\[i\*8+2\] = colour;                        LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY;                        LocalWord\[i\*8+5\] = coordinateEndX+i\*10;               LocalWord\[i\*8+6\] = coordinateEndY;                   LocalWord\[i\*8+7\] = mondel;                       }}

2.  Einstellungen

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateEndX
    - LW50005：coordinateEndY
    - LW50006：mondel

4.  Simulation

        Starten Sie die Online-Simulation und wechseln Sie im Hauptbild zum Bild „Linie“
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-8-.png)Anzahl 5, Schwarz, Anfangspunkt X, Y (10, 10), Endpunkt X, Y (100, 100), mondel 1; zu Farben und Linienarten siehe Abschnitt „[Bahnanzeige](path-display.md)“. Klicken Sie auf „Zeichnen“; das Ergebnis sehen Sie unten
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-9-.png)mondel 2: Dazu muss LB1 die Zeichnung löschen und LB0 neu zeichnen        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-10-.png)

[zurück](#jump)

**Bogen**

1.  Skript anlegen

\#include "MacroInit.h"

/\*\*\* @file circularArcInit\* @brief The path display copies the circular information\* @details x+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];         unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateBeginX = LocalWord\[50004\];     unsigned short coordinateBeginY = LocalWord\[50005\];     unsigned short coordinateEndX = LocalWord\[50006\];       unsigned short coordinateEndY = LocalWord\[50007\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 2;                        ///&lt; mode 0:point 1:line 2:circular arc 3:round        LocalWord\[i\*8+2\] = colour;                           LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY+i;                   LocalWord\[i\*8+5\] = coordinateBeginX+i\*10;          LocalWord\[i\*8+6\] = coordinateBeginY+i;               LocalWord\[i\*8+7\] = coordinateEndX+i\*10;               LocalWord\[i\*8+8\] = coordinateEndY+i;           }}

2.  Einstellungen

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateBeginX
    - LW50005：coordinateBeginY
    - LW50006：coordinateEndX
    - LW50007：coordinateEndY

4.  Simulation

Starten Sie die Online-Simulation und wechseln Sie im „Hauptbild“ zum Bild „Bogen“
            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-12-.png)Anzahl 1, Schwarz, Mittelpunkt X, Y (100, 100), Anfangspunkt des Bogens X, Y (120, 120), Endpunkt X, Y (90, 120); zu den Farben siehe Abschnitt „[Bahnanzeige](path-display.md)“.            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-13-.png)Anzahl 5: Dazu muss LB1 die Zeichnung löschen und LB0 neu zeichnen![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-14-.png)

[zurück](#jump)

**Kreis**

1.  Skript anlegen

\#include "MacroInit.h"

/\*\*\* @file roundInit\* @brief The path display copies the round information\* @details x+10,y+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];              unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateRadius = LocalWord\[50004\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 3;                   ///&lt; mode 0:point 1:line 2:circular arc 3:round        LocalWord\[i\*8+2\] = colour;                      LocalWord\[i\*8+3\] = coordinateX+i\*10;           LocalWord\[i\*8+4\] = coordinateY+i;               LocalWord\[i\*8+5\] = coordinateRadius;      }}

2.  Einstellungen

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateRadius

4.  Simulation

Starten Sie die Online-Simulation und wechseln Sie zu „Kreis“
![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-16-.png)
Anzahl 1, Schwarz, X, Y (100, 100), Radius 10; siehe Abschnitt „[Bahnanzeige](path-display.md)“.![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-17-.png)
Anzahl 5, Weiß (FFFF), neu zeichnen: Dazu muss LB1 die Zeichnung löschen und LB0 neu zeichnen![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-18-.png)

[zurück](#jump)

Die Darstellung der Bahnanzeige beruht auf den Daten der Adressen im „Bahndefinitionsbereich“: Die erste Adresse gibt die Anzahl der Elemente an, danach beschreiben je 8 Adressen ein Element. Zu weiteren Funktionen wie der Benachrichtigung bei der Punktauswahl siehe Abschnitt „[Bahnanzeige](path-display.md)“.
