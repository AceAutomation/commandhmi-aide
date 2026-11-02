# Círculo dinámico

El círculo dinámico es un gráfico colocado en la pantalla que se desplaza y cambia de tamaño siguiendo una trayectoria. El movimiento y el tamaño dependen del valor de la dirección de monitorización. Para añadir el objeto y modificar sus propiedades:

Elija el icono de círculo dinámico<img src="../../../configuration-guide/extended-controls/circle.files/image002.jpg" width="32" /> en la barra de herramientas, como en la figura 4-56:

Figura 4-56    Cuadro de diálogo Círculo dinámico

El círculo dinámico lee tres grupos de direcciones, que representan la coordenada x y la coordenada y del centro y el radio del círculo. La forma de leerlas depende del tipo de dato elegido.

• Control:

• Centro: el círculo se desplaza según la posición del centro; el radio no cambia.

• Radio: solo cambia el radio; la posición no cambia.

• Centro y radio: el radio cambia con la dirección que representa el radio, y el centro con las direcciones que representan sus coordenadas x e y.

• Transparencia: cambia la transparencia del color de fondo del círculo dinámico.

<span id="OLE_LINK564"></span><span id="OLE_LINK565"></span>• Relleno:

Si no se marca «Relleno», el círculo está vacío (sin color de fondo). Si se marca, el círculo es macizo y su color de fondo puede cambiarse con la opción correspondiente.

• Borde

Si no se marca esta opción, el círculo no tiene línea de borde y su color no puede cambiarse. Si se marca, el círculo tiene borde y su color puede cambiarse con la opción «Color del borde».

Ejemplo:

Con el tipo de dato «entero de 16 bits», se leen tres datos consecutivos que representan la coordenada x, la coordenada y del centro y el radio, según el formato de dirección de cada PLC. Con la dirección de monitorización LW1, <span id="OLE_LINK548"></span><span id="OLE_LINK549"></span>se leen LW1, LW2 y LW3, con este significado:

LW1 es la coordenada x del centro.

<span id="OLE_LINK552"></span><span id="OLE_LINK553"></span>         LW2 es la coordenada y del centro.

LW3 es el radio del círculo.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Tanto si se elige «Centro» como «Radio» en la opción de control, el HMI lee siempre los tres grupos de direcciones, con el mismo significado. Por ejemplo, si elige «Radio» y la dirección de monitorización es LW1, solo LW3 controla el radio.

Con el tipo de dato «entero de 32 bits» y la dirección de monitorización LW1, se leen las direcciones con este significado:

<span id="OLE_LINK550"></span><span id="OLE_LINK551"></span>LW1 es la coordenada x del centro.

LW3 es la coordenada y del centro.

LW5 es el radio del círculo.

Con el tipo «entero de 32 bits», según el formato de dirección de cada PLC, la dirección de monitorización se incrementa de 2 en 2 para obtener los tres datos: coordenada x, coordenada y del centro y radio.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Para la página «Visibilidad», véase el objeto «Botón de bit».
