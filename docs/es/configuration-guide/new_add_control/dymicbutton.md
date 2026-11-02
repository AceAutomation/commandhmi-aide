# Animación

Animación: permite definir de antemano el movimiento de un elemento y controlar su posición en la trayectoria con los datos de dos registros: uno controla el estado y otro la posición.

El icono del objeto en la barra de herramientas es: <img src="../../../configuration-guide/new_add_control/dymicbutton.files/image002.jpg" width="28" />; dibuje los puntos de la trayectoria en la pantalla (como máximo 64 puntos) y haga clic derecho para terminar.

Haga doble clic en el objeto para abrir el cuadro de diálogo de la figura 4-118:

Figura 4-118   Página «General» de la animación

Total de estados: número de estados del elemento

Posición:

Registro: con «Registro», el estado y la posición del elemento los controlan los datos de un registro.

Dirección de lectura: si el estado y la posición dependen de un registro, hay que indicar correctamente la dirección de lectura. Su formato se indica en la tabla siguiente.

|           |                            |                              |
|-----------|----------------------------|------------------------------|
| Tipo de dato | Dirección de control del estado | Dirección de control de la posición |
| 16 bits    | Dirección                    | Dirección + 1                  |
| 32 bits    | Dirección                    | Dirección + 2                  |

Por ejemplo, si el registro es \[LW100\] y el formato es «entero positivo de 16 bits», \[LW100\] contiene el estado del elemento y \[LW101\] su posición. En la figura 4-119, por ejemplo, \[LW100\] = 2 y \[LW101\] = 1: el elemento muestra el estado 2 en la posición 1.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image004.gif" width="520" />

Figura 4-119

• Reloj: con «Reloj», el elemento cambia automáticamente de estado y de posición. El apartado «Control automático de posición» define el modo de cambio de estado y de posición.

• Velocidad: velocidad del cambio de posición, en unidades de 0,1 segundos. Por ejemplo, 10 significa que el elemento avanza una posición por segundo.

• Retorno: supongamos que el elemento tiene cuatro posiciones: 0, 1, 2 y 3. Si esta opción no está marcada, al llegar a la última posición (3) el elemento vuelve a la posición inicial (0) y repite el ciclo.

Posición 0-&gt; posición 1-&gt; posición 2-&gt; posición 3-&gt; posición 0-&gt; posición 1-&gt; posición 2...

Si está marcada, al llegar a la última posición el elemento recorre el camino en sentido inverso. La secuencia de posiciones es:

Posición 0-&gt; posición 1-&gt; posición 2-&gt; posición 3-&gt; posición 2-&gt; posición 1-&gt; posición 0...

Cambio de estado: modo de cambio de estado

Puede elegirse «Según la posición» o «Según el tiempo». «Según la posición» indica que el estado cambia con la posición.

Con «Según el tiempo», la posición y el estado cambian según los puntos de la pantalla.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image005.jpg" width="484" />

Figura 4-120   Control automático de posición

**Página «Perfil»:**

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image006.jpg" width="484" />

Tamaño del dibujo vectorial:

• Anchura: anchura del <span id="OLE_LINK520"></span><span id="OLE_LINK521"></span>objeto gráfico de la página «General».

• Altura: altura del objeto gráfico de la página «General».

• Trayectoria: ajusta la posición de cada punto de la trayectoria seleccionándolo.

Para las páginas «Texto» e «Imagen», véase la «Lámpara multiestado».

<span id="OLE_LINK676"></span><span id="OLE_LINK677"></span>Para la página «Visibilidad», véase el «Botón de bit».
