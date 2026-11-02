# Ejemplo de visualización de trayectorias

En el capítulo «Visualización de trayectorias» hemos visto el significado y la configuración de sus parámetros; este capítulo detalla el uso del objeto para dibujar puntos, líneas, arcos y círculos.
Índice: [punto](#jump1), [línea](#jump2), [arco](#jump3), [círculo](#jump4)
**Crear la pantalla principal**
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image.png)**Crear una pantalla común**
Una pantalla común permite agrupar en una sola pantalla objetos fijos y repetitivos y usarlos cuando haga falta. Para las pantallas comunes, véase el capítulo «[Crear una pantalla](../screen/new-screen.md)».
Cree la pantalla común siguiente, con estos objetos:
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-1-.png)

- Visualización de trayectorias
  ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-2-.png)
- LB0 (dibujar)
- LB1 (borrar)
- LW50000 (número de puntos)
- LW50001 (color)
- Botón de pantalla (volver a la pantalla principal)

**Consejo**: en el proyecto, para mostrar muchos puntos es práctico asignar los valores de las direcciones mediante un script
**Punto**

1.  Crear el script

\#include "MacroInit.h"

/\*\*\* @file pointInit\* @brief Visualización de trayectorias: copia la información de los puntos\* @details A partir del punto inicial, coordenadas x, y en cada paso\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];           ///&lt; Número de elementos    unsigned short colour = LocalWord\[50001\];           ///&lt; color    unsigned short coordinateX = LocalWord\[50002\];      ///&lt; Coordenada X    unsigned short coordinateY = LocalWord\[50003\];      ///&lt; Coordenada Y

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 0;                   ///&lt; modo 0:punto 1:línea 2:arco 3:círculo        LocalWord\[i\*8+2\] = colour;              ///&lt;color        LocalWord\[i\*8+3\] = coordinateX+i;       ///&lt; Coordenada X        LocalWord\[i\*8+4\] = coordinateY+i;       ///&lt; Coordenada Y    }}

2.  Ajustes

<!-- -->

3.  - LW50002: coordenada X
    - LW50003: Y

4.  Resultado de la simulación

        Ejecute la simulación en línea y vaya a «punto» desde la «pantalla principal»
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-4-.png)Introduzca 50 puntos en total, negro, X、Y（10，10）; para los colores, véase la sección «[Visualización de trayectorias](path-display.md)». Haga clic en el botón «Dibujar»; el resultado es el siguiente
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-5-.png)Cambie el color a blanco (introduzca ffffffff) y vuelva a dibujar: hay que activar **LB1** para borrar el dibujo y redibujar con **LB0**
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-6-.png)Lo esencial de la visualización de trayectorias es rellenar la «zona de definición de la trayectoria», lo que puede hacerse en un script.

[volver](#jump)

**Línea**

1.  Crear el script

\#include "MacroInit.h"

/\*\*\* @file straightLineInit\* @brief Visualización de trayectorias: copia la información de las líneas\* @details La coordenada x aumenta en 10 cada vez a partir del punto inicial\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateEndX = LocalWord\[50004\];      unsigned short coordinateEndY = LocalWord\[50005\];       unsigned short mondel = LocalWord\[50006\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 1;                        ///&lt; modo 0:punto 1:línea 2:arco 3:círculo        LocalWord\[i\*8+2\] = colour;                        LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY;                        LocalWord\[i\*8+5\] = coordinateEndX+i\*10;               LocalWord\[i\*8+6\] = coordinateEndY;                   LocalWord\[i\*8+7\] = mondel;                       }}

2.  Ajustes

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateEndX
    - LW50005：coordinateEndY
    - LW50006：mondel

4.  Simulación

        Ejecute la simulación en línea y vaya a la pantalla «línea» desde la pantalla principal
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-8-.png)size 5, negro, punto inicial X、Y（10，10）, punto final X、Y（100，100）, mondel 1; para los colores y tipos de línea, véase la sección «[Visualización de trayectorias](path-display.md)». Haga clic en el botón «Dibujar»; el resultado es el siguiente
        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-9-.png)mondel 2: hay que activar LB1 para borrar el dibujo y redibujar con LB0        ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-10-.png)

[volver](#jump)

**Arco**

1.  Crear el script

\#include "MacroInit.h"

/\*\*\* @file circularArcInit\* @brief Visualización de trayectorias: copia la información de los arcos\* @details x+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];               unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];         unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateBeginX = LocalWord\[50004\];     unsigned short coordinateBeginY = LocalWord\[50005\];     unsigned short coordinateEndX = LocalWord\[50006\];       unsigned short coordinateEndY = LocalWord\[50007\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 2;                        ///&lt; modo 0:punto 1:línea 2:arco 3:círculo        LocalWord\[i\*8+2\] = colour;                           LocalWord\[i\*8+3\] = coordinateX+i\*10;               LocalWord\[i\*8+4\] = coordinateY+i;                   LocalWord\[i\*8+5\] = coordinateBeginX+i\*10;          LocalWord\[i\*8+6\] = coordinateBeginY+i;               LocalWord\[i\*8+7\] = coordinateEndX+i\*10;               LocalWord\[i\*8+8\] = coordinateEndY+i;           }}

2.  Ajustes

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateBeginX
    - LW50005：coordinateBeginY
    - LW50006：coordinateEndX
    - LW50007：coordinateEndY

4.  Simulación

Ejecute la simulación en línea y vaya a la pantalla «arco» desde la «pantalla principal»
            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-12-.png)size 1, negro, centro X、Y（100，100）, inicio del arco X、Y（120，120）, fin del arco X、Y（90，120）; para los colores, véase la sección «[Visualización de trayectorias](path-display.md)».            ![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-13-.png)size 5: hay que activar LB1 para borrar el dibujo y redibujar con LB0![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-14-.png)

[volver](#jump)

**Círculo**

1.  Crear el script

\#include "MacroInit.h"

/\*\*\* @file roundInit\* @brief Visualización de trayectorias: copia la información de los círculos\* @details x+10,y+10\*/void Macro_main(IN \*p){MarcoInit//ToDo    unsigned int i = 0;

unsigned short size   = LocalWord\[50000\];              unsigned short colour = LocalWord\[50001\];               unsigned short coordinateX = LocalWord\[50002\];          unsigned short coordinateY = LocalWord\[50003\];          unsigned short coordinateRadius = LocalWord\[50004\];

LocalWord\[0\] = size;    for(i=0; i&lt;size; ++i){        LocalWord\[i\*8+1\] = 3;                   ///&lt; modo 0:punto 1:línea 2:arco 3:círculo        LocalWord\[i\*8+2\] = colour;                      LocalWord\[i\*8+3\] = coordinateX+i\*10;           LocalWord\[i\*8+4\] = coordinateY+i;               LocalWord\[i\*8+5\] = coordinateRadius;      }}

2.  Ajustes

<!-- -->

3.  - LW50002：coordinateX
    - LW50003：coordinateY
    - LW50004：coordinateRadius

4.  Simulación

Ejecute la simulación en línea y vaya a «círculo»
![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-16-.png)
size 1, negro, X,Y（100，100）, radio 10; véase la sección «[Visualización de trayectorias](path-display.md)».![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-17-.png)
size 5, blanco (FFFF), redibujar: hay que activar LB1 para borrar el dibujo y redibujar con LB0![](../../../configuration-guide/new_add_control/pathdisplaycase_files/image-18-.png)

[volver](#jump)

El dibujo del objeto de visualización de trayectorias depende de los datos de la «zona de definición de la trayectoria»: la primera dirección indica el número de elementos y cada grupo de 8 direcciones siguientes describe un elemento. Para las demás funciones, como la notificación del punto seleccionado, véase la sección «[Visualización de trayectorias](path-display.md)».
