# Lista desplegable

La lista desplegable muestra una lista de elementos que el usuario puede consultar y seleccionar. Al seleccionar un elemento, su valor se escribe en la dirección de control del registro.

El icono del objeto en la barra de herramientas es<img src="../../../configuration-guide/new_add_control/combobox.files/combobox771.png" width="35" />; haga clic en él para abrir el cuadro de diálogo de la figura 4-115:

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1012.png" width="677" />

Figura 4-115   Página «General» de la lista desplegable

• Número total de estados: número de estados del objeto. Cada elemento representa un estado y aparece en la lista. Su valor puede escribirse en la \[Dirección de control\].

• Color de fondo: color de fondo del elemento seleccionado

• Color del texto: color del texto del elemento seleccionado

• Dirección de control: dirección de escritura

• Usar script: ejecuta el script elegido si el objeto responde al tacto.

Ajuste de estados: haga clic en la página «Ajuste de estados»; se muestra la figura siguiente (figura 4-116):

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1554.png" width="675" />

Figura 4-116   Página «Ajuste de estados» de la lista desplegable

• Idioma: la «fuente» y el «tamaño de fuente» son comunes a todos los estados, pero pueden variar según el idioma.

• Valor: valor de cada elemento, sujeto a estas dos reglas:

a\. \[Lectura\]: si el sistema detecta un cambio en el contenido de la \[Dirección de control\], el objeto compara ese contenido con sus valores y selecciona el primer elemento que coincide. Si ninguno coincide, pasa al estado de error y activa el bit de notificación de error (si está definido).

b\. \[Escritura\]: al seleccionar un elemento, el sistema escribe su valor en la \[Dirección de control\].

• Etiqueta: texto de cada elemento. El menú muestra los textos de todos los elementos de la lista para que el usuario los consulte y elija.

• Notificación de error

a\. Por ejemplo, si el \[Número de estados\] es 8, el estado 8 es el estado de error. Del mismo modo, si es 11, el estado 11 es el de error.

b\. En caso de error, la lista muestra el texto del estado de error.

En caso de error, el sistema pone un bit concreto a ON / OFF (escrito en la \[Dirección de notificación de error\]). Este bit puede usarse para lanzar una operación que corrija el error.

Para las páginas «Avanzado» y «Visibilidad», véase el «Botón de bit».
