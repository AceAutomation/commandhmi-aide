# Visualización de grupos de datos

Visualización de grupos de datos: un grupo (o bloque) de datos son los datos de un conjunto de direcciones consecutivas, como LW12, LW13, LW14, LW15, etc. Este objeto muestra a la vez varios grupos de datos. Por ejemplo, puede mostrar a la vez los grupos LW12 a LW15 y RWI12 a RWI15 para observar y comparar los datos de cada registro. También dibuja curvas de referencia de varios grupos, con el número de punto en el eje horizontal y el valor de cada dato en el eje vertical, para apreciar de forma precisa e intuitiva la evolución de un valor durante un periodo. Se pueden mostrar hasta 8 polilíneas (curvas).

El icono del objeto en la barra de herramientas es: <img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay756.png" width="31" />; haga clic en él; se abre el cuadro de diálogo de la figura 4-122:

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay838.png" width="741" />

Figura 4-122 Cuadro de diálogo general de visualización de grupos de datos

• Color de fondo: color de fondo del gráfico.

• Tipo de dato: hay 7 tipos de dato disponibles.

• Bit de disparo de lectura: la curva solo avanza cuando la «dirección del bit de disparo de lectura» vale 1.

• Reinicio automático: cuando la «dirección del bit de disparo de lectura» vale 1, se pone automáticamente a 0 al soltar el botón del ratón.

• Número de canales: número de grupos de datos, es decir, de curvas.

• Canal actual: elija un canal para definir su \[Dirección de control\].

• Dirección de control: dirección de lectura. Cada canal tiene su propia dirección de control.

Cada canal puede tener una dirección inicial distinta; la longitud de la dirección = Len \* puntos mostrados (Len = 1 con datos de 16 bits; Len = 2 con datos de 32 bits).

Por ejemplo, si la dirección inicial del canal 1 es LW1, el tipo de dato es entero de 32 bits y hay 4 puntos, el canal 1 ocupa LW1 LW3 LW5 LW7;

• Puntos mostrados: número de direcciones de control leídas por canal.

• Detección

• Activar: indica si la línea de detección (línea de referencia) está activada.

• Color: color de la línea de detección (línea de referencia).

• Dirección de detección: el valor correspondiente a la línea de detección actual se escribe en este registro.

• Ejemplo

16 bits, 4 canales, 10 puntos, LW1 como \[Dirección de control\] del canal 1, LW100 del canal 2, LW200 del canal 3 y RWI1 del canal 4. Entonces:

Curva 1: LW1 a LW10

Curva 2: LW100 a LW109

Curva 3: LW200 a LW209

Curva 4: RWI1 a RWI10

Con datos de 32 bits y los demás ajustes iguales:

Curva 1: LW1 a LW20

Curva 2: LW100 a LW119

Curva 3: LW200 a LW219

Curva 4: RWI1 a RWI20

Así, con datos de 32 bits y N grupos, se leen N valores incrementando la dirección de 2 en 2 según las reglas de direccionamiento de cada PLC.

• Color de fondo: color de la zona por la que se mueven las curvas.

• Bit de borrado: borra el estado actual de todas las curvas cuando la dirección del bit de borrado pasa de 0 a 1 (flanco ascendente); no cambia nada cuando pasa de 1 a 0 (flanco descendente) o no cambia.

• Marcar puntos de datos: cada curva está formada por puntos

• Dibujar líneas: cada curva está formada por líneas.

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay3263.png" width="130" />

Para la página «Visibilidad», véase el «Botón de bit».
