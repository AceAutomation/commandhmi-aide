# Movimiento de gráfico

Con el objeto de movimiento de gráfico, un gráfico de la galería o un archivo de imagen se desplaza en una dirección concreta de la pantalla, según el valor de las variables asociadas. Este objeto permite crear animaciones en la pantalla.

Añadir el objeto de movimiento de gráfico y modificar sus propiedades:

Elija el botón Movimiento de gráfico<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move351.png" width="35" /> de la barra de herramientas, ajuste las propiedades en el cuadro de diálogo y haga clic en «Aceptar», como en la figura 4-61:

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move459.png" width="662" />

Figura 4-61 Cuadro de diálogo Movimiento de gráfico

• Elección de imagen:

En la página «Imágenes», elija la imagen que se moverá; también puede ser personalizada.

• Dirección de monitorización:

La dirección de monitorización del movimiento ocupa tres direcciones, que corresponden al número total de estados, al valor del eje X y al valor del eje Y. Por ejemplo, con la dirección interna LW1 y tipo de dato de 16 bits, los valores de LW1, LW2 y LW3 controlan directamente el número total de estados, el movimiento en X y el movimiento en Y; con tipo de 32 bits, el número total de estados está en LW1, la coordenada X en LW3 y la coordenada Y en LW5.

• Método: en los ejemplos siguientes la dirección de monitorización es la dirección interna LW1, con tipo de dato de 16 bits. Cada tipo de movimiento:

• Movimiento horizontal en el eje X: el gráfico solo se mueve en horizontal, no en vertical, y no puede salir de los límites inferior y superior del eje X. El número total de estados es el valor de LW1 y LW2 representa la coordenada X.

• Movimiento vertical en el eje Y: el gráfico solo se mueve en vertical, no en horizontal, y no puede salir de los límites inferior y superior del eje Y. El número total de estados es el valor de LW1 y LW2 representa la coordenada Y.

• Movimiento horizontal y vertical simultáneo: el gráfico se mueve a la vez en horizontal y en vertical, sin salir de los límites de los ejes X e Y. El número total de estados es el valor de LW1, LW2 representa la coordenada X y LW3 la coordenada Y.

• Movimiento horizontal proporcional en el eje X: el gráfico solo se mueve en horizontal, no en vertical, y no puede salir de los límites inferior y superior del eje X. El número total de estados es el valor de LW1 y LW2 representa la coordenada X.

• Movimiento vertical proporcional en el eje Y: el gráfico solo se mueve en vertical, no en horizontal, y no puede salir de los límites inferior y superior del eje Y. El número total de estados es el valor de LW1 y LW2 representa la coordenada.

• Movimiento horizontal proporcional inverso en el eje X: el gráfico solo se mueve en horizontal, no en vertical, y no puede salir de los límites inferior y superior del eje X. El número total de estados es el valor de LW1 y LW2 representa la coordenada X.

• Movimiento vertical proporcional inverso en el eje Y: el gráfico solo se mueve en vertical, no en horizontal, y no puede salir de los límites inferior y superior del eje Y. El número total de estados es el valor de LW1 y LW2 representa la coordenada.

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move3614.png" width="130" />

• Para las páginas «Texto» e «Imagen», véase el objeto «Lámpara multiestado».

• Para la página «Visibilidad», véase el objeto «Botón de bit».

• Los valores de las dos últimas direcciones de monitorización controlan la posición del gráfico.

• La coordenada máxima de los ejes X / Y es el tamaño máximo de la pantalla.
