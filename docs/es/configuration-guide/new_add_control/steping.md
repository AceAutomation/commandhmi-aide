# Botón de pasos

Este comando crea un botón de pasos en la pantalla actual, que hace pasar cíclicamente de un estado a otro. Haga clic en el icono<img src="../../../configuration-guide/new_add_control/steping.files/image002.jpg" width="31" /> para abrir el cuadro de diálogo de la figura 4-113:

<img src="../../../configuration-guide/new_add_control/steping.files/image004.jpg" width="675" />

Figura 4-113   Cuadro de diálogo Botón de pasos

Orden de los estados: orientación del texto en el objeto

Por ejemplo, con 3 estados en total, los textos de los estados 0, 1 y 2 son 0, 1 y 2.

• De izquierda a derecha: el objeto es horizontal y el texto va de izquierda a derecha: 0, 1, 2

• De derecha a izquierda: el objeto es horizontal y el texto va de derecha a izquierda: 2, 1, 0

• De arriba abajo: el objeto es vertical y el texto va de arriba abajo: 0, 1, 2

• De abajo arriba: el objeto es vertical y el texto va de abajo arriba: 2, 1, 0

Tipo de estado: véase la «Lámpara multiestado».

Estado actual: color de fondo y color del texto del estado actual.

Para las páginas «Texto» e «Imagen», véase la «Lámpara multiestado».

Para la página «Avanzado» y las teclas de acceso rápido, véase el Botón de bit.

Por ejemplo, con tipo de estado «Valor», dirección de escritura LW1, 3 estados y textos 0, 1 y 2 para los estados 0, 1 y 2: tras descargar el proyecto al HMI, cada clic en el objeto hace pasar cíclicamente el estado de 0 a 2 y el valor correspondiente se escribe en LW1.
