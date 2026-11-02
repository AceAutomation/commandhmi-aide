# Notas sobre los objetos de CommandHMI

El software de configuración CommandHMI ofrece objetos básicos completos. Para configurar sus propiedades, haga doble clic o clic derecho en el objeto en la zona de trabajo. La posición y el tamaño pueden modificarse en la barra de estado inferior o arrastrando con el ratón.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/image002.jpg" width="829" alt="2018_11_20_08_51_35.jpg" />

Introducción de direcciones: cuando hay que acceder a una dirección del PLC, puede escribirse directamente con el teclado. El nombre de la dirección no distingue mayúsculas y minúsculas.

Lista de estados: la barra de herramientas tiene una lista que muestra y cambia el estado del botón de bit, la lámpara de bit, el botón multiestado, la lámpara multiestado, el movimiento de gráfico, la visualización de mensajes y la visualización de imagen.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice675.png" width="92" />

Al seleccionar uno de estos objetos, su estado actual aparece en la lista, que puede desplegarse para cambiarlo.

Búsqueda de dirección: busca dónde se usa una dirección y lista los objetos que la ocupan; haga doble clic en una línea para seleccionar el objeto.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice997.png" width="299" />

Introduzca la dirección y elija «Buscar»; la ventana de salida muestra los resultados:

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1102.png" width="406" />

Haga doble clic en un resultado para seleccionar el objeto que usa la dirección.

Visualización de direcciones: haga clic en «Visualización de direcciones» para ver la lista de direcciones usadas por el proyecto; haga doble clic en una línea para abrir la página de propiedades del objeto que usa esa dirección y configurarlo rápidamente.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1461.png" width="719" />

En el modo de visualización se puede limitar a la dirección seleccionada o mostrar todas las pantallas.

Superposición de objetos: apilando objetos se ejecutan varios con una sola operación. CommandHMI admite hasta 32 objetos apilados. Al tocar objetos superpuestos, sus operaciones se ejecutan en el orden de superposición, como en la figura siguiente:

Con los objetos 1, 2 y 3 superpuestos, al tocar se ejecutan sucesivamente los comandos 1, 2 y 3.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1966.png" width="435" />

Si uno de los objetos superpuestos es un botón de cambio de pantalla, la pantalla cambia al llegar su turno y los comandos posteriores no se ejecutan. Igualmente, si aparece un teclado de entrada, se muestra el teclado y los comandos posteriores no se ejecutan.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice2303.png" width="494" />
