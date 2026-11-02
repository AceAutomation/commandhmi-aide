# Lámpara multiestado

La lámpara multiestado muestra distintos estados según el valor de la dirección de monitorización. Puede mostrar hasta 32 estados.

Haga clic en el icono de lámpara multiestado<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image002.jpg" width="28" /> de la barra de herramientas para abrir el cuadro de diálogo de la figura 4-83.

Figura 4-83    Cuadro de diálogo Lámpara multiestado

1\. General:

• Estado: el usuario puede cambiar el valor de estado para modificar el color del borde, de primer plano y de fondo y la trama del objeto en cada estado

• Tipo de estado: (suponiendo que el valor introducido es n)

• Valor: el valor escrito va de cero al número total de estados menos 1.

• Bit de registro: el valor escrito es 2 elevado a n.

E.g.:

<span id="OLE_LINK657"></span><span id="OLE_LINK511"></span><span id="OLE_LINK510"></span>La dirección de monitorización (lectura) es LW3 y el número total de estados es 8. Haga clic en «Aceptar» para añadir el objeto a la pantalla, añada después una entrada numérica con LW3 como dirección de escritura y de monitorización y guarde el proyecto.

En la simulación o en la pantalla, el usuario hace clic en la entrada numérica e introduce un valor de estado con el teclado. Si introduce 2, el valor de la dirección de monitorización (lectura) es 1 y el objeto muestra el texto del estado 1 (definido en la página «Texto»); si LW3 vale 8, el objeto muestra el texto del estado 3. Si se introduce 3 en LW3, la lámpara multiestado no pasa a ningún estado.

• Valores de estado personalizados: con esta opción aparece un botón «Definir valores de estado». Haga clic en él para abrir el cuadro de diálogo «Valores de estado personalizados», como en la figura 4-84:

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image004.jpg" width="333" />

Figura 4-84    Cuadro de diálogo de valores de estado definidos por el usuario

En este cuadro, la columna «S \#» es la columna de estado: el valor seleccionado indica el estado actual; haga doble clic en un valor para introducir el valor de ese estado.

Por ejemplo: la dirección de monitorización (lectura) es LW3 y el número total de estados es 8. Haga clic en «Aceptar» para añadir el objeto a la pantalla, añada después una entrada numérica con LW3 como dirección de escritura y de monitorización y guarde el proyecto.

En la simulación o en la pantalla, el usuario hace clic en la entrada numérica e introduce un valor de estado con el teclado. Si introduce 1, el valor de la dirección de monitorización (lectura) es 1 y el objeto muestra el texto del estado 1 (definido en la página «Texto»); si LW3 vale 33, el objeto muestra el texto del estado 2. Si se introduce 2 en LW3, la lámpara multiestado no pasa a ningún estado.

• Tipo de dato: tipo de dato de las direcciones de escritura y de monitorización (lectura)

• Dirección de monitorización: dirección de lectura cuyo valor de estado determina el estado mostrado por el objeto.

• Número total de estados: el usuario define el número total de estados según sus necesidades, hasta 32 estados (del 0 al 31).

Por ejemplo, con tipo de dato entero positivo de 16 bits y 32 estados en total: si la dirección de monitorización vale 0, la lámpara multiestado muestra el texto y la imagen del estado 0; si vale 5, los del estado 5. Si vale 60, sigue mostrando el estado 31, porque el máximo es 32 estados.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Nota: para forma, color del borde, color de primer plano, color de fondo y trama, véase el objeto «Botón de bit».

Nota: si la lámpara multiestado usa un tipo de dato de 32 bits, la dirección ocupa 2 palabras. <span id="OLE_LINK673"></span><span id="OLE_LINK672"></span>Por ejemplo, si se escribe en el registro de datos V10 de un PLC SIEMENS, se ocupan V10 y V11; si otro objeto monitoriza también V11, se produce un error. Tenga cuidado con los tipos de 32 bits para evitar errores de datos y direcciones.

Nota: el tipo de dato debe corresponder a los datos que se quieren indicar.

2\. Texto:

Haga clic en la pestaña «Texto» de las propiedades de la lámpara multiestado para ver los ajustes de texto, como en la figura 4-85:

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image006.jpg" width="675" />

Figura 4-85 Página «Texto» de la lámpara multiestado

Todos los idiomas usan el texto del primer idioma: opción para proyectos multilingües, es decir, cuando en «Idioma» del gestor de proyecto hay más de un idioma; el texto del objeto no cambia al cambiar de idioma.

<span id="OLE_LINK737"></span><span id="OLE_LINK736"></span>• Idioma: opción para proyectos multilingües. Elija un idioma para introducir textos distintos en cada estado y obtener así el multilingüismo. (En el botón de función, elija la opción «Cambiar idioma» y el idioma de destino; en la simulación o en la pantalla, al pulsar el botón todos los objetos con texto pasan a ese idioma). El texto, la fuente y el tamaño pueden variar según el idioma; el color, el espaciado y la posición son comunes.

• Fuente: tipo de letra del texto; puede variar según el estado y según el idioma.

• Tamaño de fuente: tamaño del texto; puede variar según el estado y según el idioma.

• Color, espaciado, posición: color, espaciado y alineación del texto seleccionado. Si en la página «Texto» elige un idioma distinto del idioma 1 y el proyecto tiene más de un idioma, estas tres opciones no tienen efecto, porque son las del idioma 1.

3\. Imagen:

Haga clic en la pestaña «Imagen» de las propiedades de la lámpara multiestado para ver los ajustes, como en la figura 4-86.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image007.jpg" width="675" />

Figura 4-86 Página «Imagen» de la lámpara multiestado

Esta página sirve para cargar imágenes para cada estado. Por defecto la imagen de cada estado está vacía y puede cambiarse según las necesidades.

• Procedimiento: seleccione en la lista el elemento cuya imagen quiere cambiar y elija la imagen en la biblioteca del sistema o en una ruta de Windows. Al hacer clic en cada estado, se carga debajo la imagen correspondiente. El usuario también decide si la imagen se ajusta al objeto: si no, puede modificar el margen y la posición para mejorar el aspecto.

• Ajustar al objeto: si se marca, la imagen toma el tamaño del objeto de la página «General» y se ocultan las opciones de margen y posición; si no, aparecen.

Si importa una imagen desde un archivo externo, aparece la opción «Transparente», que permite hacer transparente un color concreto

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Nota: para la página «Visibilidad», véase el objeto «Botón de bit».

Tras ajustar todas las propiedades, haga clic en «Aceptar» y añada el objeto a la pantalla
