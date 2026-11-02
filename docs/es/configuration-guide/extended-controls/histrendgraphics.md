# Gráfico de tendencia histórica

• Presentación: este gráfico de tendencia se usa junto con el «[Recopilador de datos históricos](../../setting/history-data.md)» del gestor de proyecto; muestra los valores de los datos del recopilador.

• Presentación del gráfico de tendencia XY:

Muestra de forma dinámica y continua los valores de las variables.

Muestra varias curvas de referencia, con el tiempo en el eje X y el valor de la dirección en el eje Y, para apreciar de forma precisa e intuitiva la evolución de un valor durante un periodo.

Se pueden mostrar hasta 8 polilíneas (curvas).

• Añadir el gráfico de tendencia y modificar sus propiedades:

1. Elija el icono de tendencia<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image002.jpg" width="34" /> de la barra de herramientas; se abre el cuadro de propiedades de la tendencia histórica, como en la figura 4-53:

Figura 4-53    Página «General» de la tendencia histórica

• Color de fondo: cambia el color de fondo del gráfico. El cambio no se ve directamente; haga clic en «Aceptar» para aplicarlo.

• Transparencia: cambia la transparencia del color de fondo.

• Recopilación de datos: por defecto, el «Recopilador de datos históricos» del gestor de proyecto. CommandHMI admite varios grupos de datos históricos; con esta opción el diseñador elige qué grupo usar. Como abajo:

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image004.jpg" width="774" />

• Número de curvas: número de curvas mostradas; máximo 8.

• Color: color del trazo de la curva.

• Usar dirección de control: indica si se usa una dirección de control. Ocupa 28 offsets y controla la visualización de cada curva, los valores máximo y mínimo, la hora de fin, el periodo (minutos), el máximo y el mínimo cuando solo se muestra el eje Y, si se muestra el eje Y y el retorno al estado inicial.

|                |                                                                                                         |
|----------------|---------------------------------------------------------------------------------------------------------|
| Offset de dirección | Elemento controlado por el registro de control                                                           |
| 0              | Número total de curvas mostradas                                                                 |
| 1              | <span id="OLE_LINK534"></span><span id="OLE_LINK533"></span>Mostrar la curva 1                        |
| 2              | Mostrar la curva 2                                                                                    |
| 3              | Mostrar la curva 3                                                                                    |
| 4              | Mostrar la curva 4                                                                                    |
| 5              | Mostrar la curva 5                                                                                    |
| 6              | Mostrar la curva 6                                                                                    |
| 7              | Mostrar la curva 7                                                                                    |
| 8              | Mostrar la curva 8                                                                                    |
| 9              | Valor máximo del eje Y                                                                                 |
| 10             |                                                                                                         |
| 11             | Valor mínimo del eje Y                                                                              |
| 12             |                                                                                                         |
| 13             | 0: usar los valores máximo y mínimo por defecto; 1: usar los límites superior e inferior definidos |
| 14             | Hora de inicio de la consulta                                                                                        |
| 15             |                                                                                                         |
| 16             |                                                                                                         |
| 17             |                                                                                                         |
| 18             |                                                                                                         |
| 19             |                                                                                                         |
| 20             | Hora de fin de la consulta                                                                                          |
| 21             |                                                                                                         |
| 22             |                                                                                                         |
| 23             |                                                                                                         |
| 24             |                                                                                                         |
| 25             |                                                                                                         |
| 26             | Con 1 se lanza la consulta; vuelve automáticamente a 0                                 |
| 27             | Con 1 se vuelve al estado actual; vuelve automáticamente a 0                             |

Mostrar la dirección de control:

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/2020-03-23_091355.jpg" width="774" />

**Línea de detección**

• Activar: indica si la línea de detección (línea de referencia) está activada.

• Color: color de la línea de detección (línea de referencia).

• Dirección de detección: el valor correspondiente a la línea de detección actual se escribe en este registro.

• Mostrar la hora de detección: la hora de la posición actual de la línea de detección se escribe en este registro; se muestra con un objeto de visualización ASCII de 19 palabras en total.

• Diferencia de tiempo del punto de detección: la diferencia entre la hora de la posición actual de la línea de detección y la hora de inicio se escribe en esta dirección; se muestra con un objeto de visualización numérica, entero de 16 bits, en segundos.

2\. La página «Curvas» del gráfico de tendencia histórica se muestra en la figura 4-54.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image005.jpg" width="774" />

Figura 4-54    Pestaña «Curvas» de la tendencia histórica

En esta página se definen el máximo, el mínimo, el estilo y el color de cada curva. El origen de los datos es el «[Recopilador de datos históricos](../../setting/history-data.md)» del gestor de proyecto. Cada curva puede tener un origen distinto.

3\. La página «Ejes XY» del gráfico de tendencia histórica se muestra en la figura 4-55.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image006.jpg" width="774" />

Figura 4-55    Pestaña «Ejes XY» de la tendencia histórica

**Eje X**

• Mostrar escala: si se muestra la escala del eje X.

• Mostrar cuadrícula Y: si se muestra la cuadrícula del eje Y.

• Color de eje / escala: cambia el color del eje X / escala.

• Color de cuadrícula: cambia el color de la cuadrícula del eje X.

• Divisiones principales: divisiones principales del eje X.

• Divisiones secundarias: divisiones secundarias del eje X.

• Mostrar hora: formato y tamaño de fuente de la hora.

• Rango de tiempo: intervalo de tiempo mostrado en el gráfico.

**Eje Y**

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

• Mostrar varios ejes: si se muestran varios ejes.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image007.jpg" width="130" />

Para la página «Visibilidad», véase el objeto «Botón de bit».
