# Gráfico de tendencia

**Presentación del gráfico de tendencia:**

<span id="OLE_LINK525"></span><span id="OLE_LINK526"></span>Muestra de forma dinámica y continua los valores de las variables.

Dibuja curvas de referencia de varios datos, con el tiempo en el eje horizontal y el valor en el eje vertical, para apreciar de forma precisa e intuitiva la evolución de un valor durante un periodo.

Se pueden mostrar hasta 8 polilíneas (curvas).

Propiedades del gráfico de tendencia:

1. Elija el icono de gráfico de tendencia<img src="../../../configuration-guide/extended-controls/trend.files/image002.jpg" width="35" /> en la barra de herramientas; se abre el cuadro de propiedades, como en la figura 4-50

Figura 4-50    Cuadro de diálogo general del gráfico de tendencia

• Color de fondo: cambia el color de fondo del gráfico. El efecto solo se ve al hacer clic en «Aceptar».

• Tipo de dato: hay 7 tipos de dato disponibles.

• Bit de disparo de lectura: la curva solo avanza cuando la «dirección del bit de disparo de lectura» vale 1.

• Número de curvas: número de curvas, hasta 8.

• Reinicio automático del bit de disparo de lectura: cuando la dirección de lectura vale 1, se pone a 0.

• Puntos por grupo: <span id="OLE_LINK492"></span><span id="OLE_LINK493"></span>número de datos mostrados en el <span id="OLE_LINK494"></span><span id="OLE_LINK495"></span>eje X.

• Tiempo de muestreo: frecuencia de muestreo.

• Dirección de lectura: su valor es el valor de cada curva en el eje Y. Según el número de grupos y el tipo de dato, las direcciones se leen de forma continua (datos de 16 bits) o a intervalos (datos de 32 bits).

• Número de puntos variable: los «puntos por grupo» se definen dinámicamente según el valor de una dirección. Con esta opción, el valor por defecto de la dirección es el valor inicial de los puntos por grupo.

**Línea de detección**

• Activar: indica si la línea de detección (línea de referencia) está activada.

• Color: color de la línea de detección (línea de referencia).

<span id="OLE_LINK527"></span><span id="OLE_LINK528"></span><span id="OLE_LINK543"></span>• Dirección de detección: el valor de la línea de detección (línea de referencia) actual se escribe en esta dirección.

• Usar dirección de control: define dinámicamente el mínimo y el máximo del eje Y según el valor de la dirección de control. Esta dirección ocupa cinco offsets consecutivos: cambia el mínimo y el máximo de la escala del eje Y y si se vuelve al estado inicial.

|                |                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Offset de dirección | Elemento controlado por el registro de control                                                                                                                            |
| 0              | 16 bits bajos del valor mínimo                                                                                                                                |
| 1              | 16 bits altos del valor mínimo                                                                                                                                |
| 2              | 16 bits bajos del valor máximo                                                                                                                                |
| 3              | 16 bits altos del valor máximo                                                                                                                                |
| 4              | Restablecer los valores máximo y mínimo iniciales. 1 indica cambio dinámico; en caso contrario se restablece el valor inicial |

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

La dirección de control solo puede ser una dirección interna; el mínimo y el máximo ocupan cada uno dos palabras consecutivas.

E.g.:

Con el tipo de dato de 16 bits y 8 grupos de datos, si la dirección introducida es LW3, se leen 8 direcciones consecutivas:

LW3: valor de la curva 1

LW4: <span id="OLE_LINK513"></span><span id="OLE_LINK514"></span>valor de la curva 2

LW5: <span id="OLE_LINK515"></span><span id="OLE_LINK516"></span>valor de la curva 3

LW6: valor de la curva 4

LW7: valor de la curva 5

LW8: valor de la curva 6

LW9: valor de la curva 7

LW10: valor de la curva 8

Así, con datos de 16 bits y N grupos, se leen N direcciones consecutivas según las reglas de direccionamiento de cada PLC.

Con el tipo de dato de 32 bits y 5 grupos de datos, si la dirección introducida es LW3, se leen 5 valores consecutivos.

LW3: <span id="OLE_LINK517"></span><span id="OLE_LINK518"></span>valor de la curva 1

LW5: valor de la curva 2

LW7: valor de la curva 3

LW9: valor de la curva 4

LW11: valor de la curva 5

Así, con datos de 32 bits y N grupos, se leen N valores incrementando la dirección de 2 en 2 según las reglas de direccionamiento de cada PLC.

• Dirección:

• De izquierda a derecha: la curva avanza desde la izquierda.

• De derecha a izquierda: la curva avanza desde la derecha.

• Color: color de la curva

• Bit de borrado: borra el estado actual de todas las curvas cuando la dirección pasa de 0 a 1 (flanco ascendente). Las curvas no cambian cuando pasa de 1 a 0 (flanco descendente) o no cambia.

La página «Curvas» del gráfico de tendencia se muestra en la figura 4-51: en ella se definen el máximo, el mínimo, el estilo y el color de cada curva.

<img src="../../../configuration-guide/extended-controls/trend.files/image005.jpg" width="774" />

Figura 4-51    Cuadro de diálogo de curvas del gráfico de tendencia

El tipo de dato de la página «General» determina el de los valores máximo y mínimo.

Por ejemplo, si el máximo o el mínimo es un número de coma flotante, hay que elegir antes «coma flotante de 32 bits» como tipo de dato en la página «General». Si no, se produce un error al hacer clic en «Aceptar».

3\. La página «Ejes XY» del gráfico de tendencia se muestra en la figura 4-52:

<img src="../../../configuration-guide/extended-controls/trend.files/image006.jpg" width="774" />

Figura 4-52    Cuadro de diálogo de ejes XY del gráfico de tendencia

• Eje X

• Mostrar escala: si se muestra la escala del eje X.

• Mostrar cuadrícula Y: si se muestra la cuadrícula del eje Y.

• Color de eje / escala: cambia el color del eje X / escala.

• Color de cuadrícula: cambia el color de la cuadrícula del eje X.

• Divisiones principales: divisiones principales del eje X.

• Divisiones secundarias: divisiones secundarias del eje X.

Mostrar escala: si se muestra la escala del eje X.

• Eje Y

• Mostrar escala: si se muestra la escala del eje Y.

• Mostrar cuadrícula X: si se muestra la cuadrícula del eje X.

• Color de eje / escala: cambia el color del eje Y / escala.

• Color de cuadrícula: cambia el color de la cuadrícula del eje Y.

• Divisiones principales: número de divisiones principales del eje Y.

• Divisiones secundarias: número de divisiones secundarias del eje Y.

• Mostrar marcas: si se muestran las marcas de la escala del eje Y.

• Tamaño de fuente: cambia el tamaño de fuente de la escala del eje Y.

• Mínimo: valor mínimo de la escala del eje Y.

• Máximo: valor máximo de la escala del eje Y.

• Total: número máximo de cifras de los datos.

• Decimales: número máximo de cifras tras la coma.

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

Para la página «Visibilidad», véase el objeto «Botón de bit».
