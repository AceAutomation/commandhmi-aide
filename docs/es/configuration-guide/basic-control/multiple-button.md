# Botón multiestado

El botón multiestado y la lámpara multiestado funcionan prácticamente igual; la única diferencia es que el botón multiestado admite la introducción de valores, además de la simple indicación. Procedimiento:

Haga clic en el icono<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button271.png" width="31" /> de la barra de herramientas para abrir el cuadro de diálogo de la figura 4-87.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button336.png" width="663" />

Figura 4-87 Cuadro de diálogo Botón multiestado

• Estado: el usuario puede cambiar el valor de estado y el color del borde, de primer plano y de fondo y la trama del objeto en cada estado

• Tipo de estado: (suponiendo que el valor introducido es n)

• Valor: el valor escrito es un número entre cero y el número total de estados.

• Bit de registro: el valor escrito es 2 elevado a n.

E.g:

Elija «Valor» como tipo de estado, «Entrada por teclado» como modo y LW3 como dirección de escritura, marque «Dirección de monitorización igual a la de escritura» y ponga 8 estados en total. Haga clic en «Aceptar» para añadir el objeto a la pantalla y guarde el proyecto.

En la simulación o en la pantalla, al hacer clic en el objeto aparece un teclado para introducir un valor de estado. Si se introduce 3, se escribe en LW3 el valor 2 elevado a 3 y se muestra el texto del estado 3 (definido en la página «Texto» del objeto). A la inversa, si LW3 vale 8, el objeto muestra el texto del estado 3. Si LW3 vale 5, el objeto no muestra ningún estado.

• Valores de estado personalizados: con esta opción aparece un botón «Definir valores de estado...», como en la figura 4-88:

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1611.png" width="662" />

Figura 4-88 Botón multiestado con valores de estado personalizados

Haga clic en «Definir valores de estado...»; se abre el cuadro de diálogo «Valores de estado personalizados», como en la figura 4-89:

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1799.png" width="333" />

Figura 4-89 Cuadro de diálogo Definir valores de estado

En este cuadro, la columna «S #» es la columna de estado. Al seleccionar una fila, el valor correspondiente a «S#» es el valor de ese estado; haga doble clic para introducir el valor del estado.

Por ejemplo, elija «Valores de estado personalizados» como tipo de estado, «Entrada por teclado» como modo y LW3 como dirección de escritura, marque «Dirección de monitorización igual a la de escritura» y ponga 8 estados en total. Haga clic en «Aceptar» para añadir el objeto a la pantalla y guarde el proyecto. En la simulación o en la pantalla, al hacer clic en el objeto aparece un teclado para introducir un valor de estado. Si se introduce 1, se escribe 22 en LW3 y se muestra el texto del estado 1 (definido en la página «Texto»). A la inversa, si LW3 vale 33, el objeto muestra el texto del estado 2. Si LW3 vale 2, el objeto no muestra ningún estado.

• Modo: seis opciones: «Entrada por teclado», «Constante», «Incrementar», «Decrementar», «Incremento cíclico» y «Decremento cíclico».

• Entrada por teclado: admite las tres opciones de «Tipo de estado». En la simulación o en la pantalla, al hacer clic en el objeto aparece un teclado para introducir el valor, como en la figura 4-90:

![](../../../configuration-guide/basic-control/multiple-button.files/001.png)

Figura 4-90 Teclado

• Constante: de las tres opciones de «Tipo de estado» solo admite «Valor». Aparece un campo «Constante» para definir el valor. En la simulación o en la pantalla, al hacer clic en el objeto se escribe esa constante

• Incrementar: de las tres opciones de «Tipo de estado» solo admite «Valor». En la simulación o en la pantalla, cada clic aumenta el estado en 1; deja de aumentar al alcanzar el número total de estados.

• Decrementar: de las tres opciones de «Tipo de estado» solo admite «Valor». En la simulación o en la pantalla, cada clic reduce el estado en 1; deja de disminuir al llegar al límite.

• Incremento cíclico: de las tres opciones de «Tipo de estado» solo admite «Valor». En la simulación o en la pantalla, cada clic aumenta el estado en 1; al superar el número total de estados vuelve al estado 0.

• Decremento cíclico: de las tres opciones de «Tipo de estado» solo admite «Valor». En la simulación o en la pantalla, cada clic reduce el estado en 1; al pasar del límite vuelve al estado máximo.

• Tipo de dato: tipo de dato de las direcciones de escritura y de monitorización (lectura)

• Dirección de monitorización: dirección de lectura cuyo valor determina el estado mostrado por el objeto.

• Número total de estados: número máximo de estados

• Usar script: si se marca, al hacer clic en el objeto en la simulación o en la pantalla se ejecuta el script elegido.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button5026.png" width="130" />

Nota: para forma, color del borde, color de primer plano, color de fondo y trama, véase el objeto «Botón de bit».

Nota: para las páginas «Texto» e «Imagen», véase el objeto «Lámpara multiestado».

Nota: para las páginas «Avanzado» y «Visibilidad», véase el objeto «Botón de bit»; para las teclas de acceso rápido, véase el botón de bit.

Tras los ajustes, haga clic en «Aceptar» para añadir el objeto a la zona de trabajo (la pantalla)
