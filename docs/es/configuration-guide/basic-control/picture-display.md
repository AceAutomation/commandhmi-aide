# Visualización de imagen

La visualización de imagen amplía la imagen estática: esta solo muestra una imagen, mientras que la visualización de imagen puede mostrar hasta 32. Su comportamiento depende del tipo de estado elegido por el usuario.

Procedimiento:

Haga clic en el icono de visualización de imagen<img src="../../../configuration-guide/basic-control/picture-display.files/image002.jpg" width="32" /> de la barra de herramientas. Se abre el cuadro de diálogo de la figura 4-110:

Figura 4-110   Cuadro de diálogo Visualización de imagen

• Bit: con «Bit» solo hay dos estados, 0 y 1. La dirección de monitorización solo puede ser una dirección de bit. El objeto muestra la imagen correspondiente al estado 0 o 1 de esa dirección.

• Valor: con «Valor» puede haber hasta 2048 estados, y se muestran distintas imágenes según el valor de la dirección de monitorización. Si vale 0, se muestra la imagen del estado 0, etc.

• Cambio automático: con esta opción puede haber hasta 2048 estados y el objeto no depende del valor de la dirección de monitorización: basta con definir el número total de estados y la frecuencia de cambio. En el HMI, el objeto cambia de imagen automáticamente dentro de ese rango.

<img src="../../../configuration-guide/basic-control/picture-display.files/image004.jpg" width="130" />

Nota: la página «Imagen» de la visualización de imagen es similar a la del objeto «Lámpara multiestado».

Nota: para la «Visibilidad», véase el objeto «Botón de bit».

Tras los ajustes, haga clic en «Aceptar» para añadir el objeto a la zona de trabajo (la pantalla).
