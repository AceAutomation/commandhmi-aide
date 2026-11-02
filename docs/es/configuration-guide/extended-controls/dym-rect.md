# Rectángulo dinámico

El rectángulo dinámico funciona como el círculo dinámico: ambos reflejan en tiempo real el valor de la dirección de monitorización cambiando la posición o el tamaño del gráfico.

Elija el icono de rectángulo dinámico<img src="../../../configuration-guide/extended-controls/dym-rect.files/image002.jpg" width="34" /> en la barra de herramientas para abrir el cuadro de diálogo de la figura 4-57.

Figura 4-57    Cuadro de diálogo Rectángulo dinámico

El rectángulo dinámico lee cuatro grupos de direcciones, que representan la coordenada x, la coordenada y, la anchura y la altura del rectángulo. La forma de leerlas depende del tipo de dato elegido.

• Grosor de línea: cambia el grosor de la línea

• Tipo: esquina recta, achaflanada o redondeada.

• Nota: el tipo solo tiene efecto si el grosor de línea es mayor que 1.

Ejemplo:

Con el tipo de dato «entero de 16 bits» y la dirección de monitorización LW1, se leen LW1, LW2, LW3 y LW4, con este significado:

LW1 es la coordenada x <span id="OLE_LINK558"></span><span id="OLE_LINK559"></span>del rectángulo;

LW2 es la coordenada y del rectángulo;

LW3 es la anchura del rectángulo;

LW4 es la altura del rectángulo.

Con el tipo de dato «entero de 16 bits», se leen cuatro datos consecutivos según el formato de dirección de cada PLC, que representan la coordenada x, la coordenada y, la anchura y la altura del rectángulo.

Con el tipo de dato «entero de 32 bits» y la dirección de monitorización LW1, se leen LW1, LW3, LW5 y LW7.

LW1 es la coordenada x del rectángulo;

LW3 es la coordenada y del rectángulo;

LW5 es la anchura del rectángulo;

LW7 es la altura del rectángulo;

Con el tipo «entero de 32 bits», según el formato de dirección de cada PLC, la dirección de monitorización se incrementa de 2 en 2 para obtener los cuatro datos: coordenada x, coordenada y, anchura y altura del rectángulo.

**Control:**

• Posición: la altura y la anchura del rectángulo no cambian; su posición cambia con las direcciones que representan las coordenadas x e y.

• Tamaño: la altura y la anchura cambian en función de uno de los cuatro puntos fijos siguientes; la posición no cambia.

• Arriba a la izquierda: <span id="OLE_LINK562"></span><span id="OLE_LINK563"></span>el punto fijo es la esquina superior izquierda y el rectángulo crece hacia abajo a la derecha.

• Arriba a la derecha: el punto fijo es la esquina superior derecha y el rectángulo crece hacia abajo a la izquierda.

• Abajo a la izquierda: el punto fijo es la esquina inferior izquierda y el rectángulo crece hacia arriba a la derecha.

• Abajo a la derecha: el punto fijo es la esquina inferior derecha y el rectángulo crece hacia arriba a la izquierda.

**Relleno:**

Si no se marca «Relleno», el rectángulo está vacío (sin color de fondo). Si se marca, es macizo y su color de fondo puede cambiarse con la opción correspondiente.

**Borde:**

Si no se marca esta opción, el rectángulo no tiene línea de borde y su color no puede cambiarse. Si se marca, el rectángulo tiene borde y su color puede cambiarse con la opción «Color del borde».

Transparencia: cambia la transparencia del color de fondo del rectángulo dinámico.

<span id="OLE_LINK570"></span><span id="OLE_LINK571"></span><img src="../../../configuration-guide/extended-controls/dym-rect.files/image004.jpg" width="130" />

Para la página «Visibilidad», véase el objeto «Botón de bit».
