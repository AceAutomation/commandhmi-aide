# Botón de bit

El botón de bit acciona y muestra el estado ON/OFF (1/0) de una dirección de bit del equipo conectado a la pantalla táctil. Es el objeto más básico y más utilizado.

Pasos para configurar un botón de bit:

1\. Haga clic en el icono de botón de bit<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton263.png" width="30" /> en la barra de herramientas para abrir el cuadro de diálogo de propiedades, como en la figura 4-68:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton381.png" width="664" />

Figura 4-68 Cuadro de diálogo Botón de bit

2\. El cuadro de diálogo tiene cuatro páginas: General, Etiqueta, Avanzado y Visibilidad.

Forma: haga clic en «Forma» para elegir la forma gráfica del objeto, como en la figura 4-69

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton600.png" width="472" />

Figura 4-69 Ventana de selección de forma

• Color del borde: con una forma con borde, este botón permite elegir otro color de borde.

• Color de primer plano: para cambiar el color de primer plano, elíjalo en la lista de colores desplegable (solo tiene efecto con un estilo de degradado).

• Color de fondo: para cambiar el color de fondo, elíjalo en la lista de colores desplegable.

• Trama: la lista desplegable ofrece 21 tramas, como en la figura 4-70:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton1213.png" width="662" />

Figura 4-70 Cambio de forma y trama

• Activar (Set): con esta función, tras la descarga al HMI, al pulsar el botón de bit la dirección de escritura pasa a 1. Es decir, la dirección de escritura del equipo conectado pasa a ON y se muestra el estado 1/ON.

• Desactivar (Reset): con esta función, tras la descarga al HMI, al pulsar el botón de bit la dirección de escritura pasa a 0. Es decir, la dirección de escritura del equipo conectado pasa a OFF y se muestra el estado 0/OFF.

• Pulsador momentáneo (Inching): se puede elegir «pulsado = 1» o «pulsado = 0». Con «pulsado = 1», tras la descarga al HMI, la dirección de escritura del equipo conectado pasa a 1/ON mientras el botón está pulsado y se muestra 1/ON; al soltar el botón pasa a 0/OFF y se muestra 0/OFF. Con «pulsado = 0», la dirección pasa a 0/OFF mientras el botón está pulsado y se muestra 0/OFF; al soltarlo pasa a 1/ON y se muestra 1/ON.

• Alternar: tras la descarga al HMI, si el estado actual del botón es 0/OFF, al tocarlo la dirección de escritura pasa a 1/ON y se muestra 1/ON; si el estado actual es 1/ON, pasa a 0/OFF y se muestra 0/OFF. El estado cambia con cada toque.

• Dirección de escritura: haga clic en el icono de teclado junto a «Dirección de escritura» para introducir la dirección. CommandHMI propone los símbolos de dirección según el equipo conectado. Por ejemplo, en la serie FX-2N de MITSUBISHI, X es la dirección de bobina de entrada, Y la de bobina de salida, M la de relé intermedio (marca), C la de contador (estado), T la de temporizador (estado), D la de registro de datos, C \* la de contador (valor de cuenta) y T \* la de temporizador (valor de cuenta). En la serie SIEMENS S7-200: I es la dirección de entrada, Q la de salida, M la de marca y V la de registro de datos. Como en la figura 4-71:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton3963.png" width="251" />

Figura 4-71 Introducción de dirección

Así, el estado actual del botón de bit se escribe en la dirección con el símbolo correspondiente del PLC u otro equipo. La dirección de escritura o de visualización vale 0/OFF cuando el botón está en 0/OFF y 1/ON cuando el objeto está en 1/ON.

• Monitorizar: marque «Monitorizar» para mostrar la «Dirección de monitorización»; el botón de bit muestra entonces los cambios de esa dirección. La dirección de monitorización vale 0/OFF cuando el botón está en 0/OFF y 1/ON cuando está en 1/ON. La dirección de monitorización puede ser distinta de la de escritura. Por ejemplo, con la función «Activar», tocar el objeto pone la dirección de escritura a 1/ON; pero si la dirección de monitorización está en 0/OFF, el botón sigue mostrando 0/OFF. En general se elige «Dirección de monitorización igual a la de escritura» para ver directamente el valor escrito.

• Script: marque «Usar script» para ver la lista de scripts. El usuario elige uno que se ejecuta al pulsar el botón de bit. La lista solo muestra los scripts compilados.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5308.png" width="130" />

Si «Monitorizar» no está marcado, el estado del botón no cambia aunque se toque el objeto.

**Etiqueta**

En la pestaña «Etiqueta» se muestran las propiedades del texto del estado 0, como en la figura 4-72:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5512.png" width="664" />

Figura 4-72 Página «Etiqueta» del botón de bit

La página tiene cuatro apartados: «Texto estado 0», «Texto estado 1», «Imagen estado 0» e «Imagen estado 1».

• Texto estado 0, Texto estado 1: cambian la fuente, el tamaño, el margen, el color y la posición del texto del estado 0 o 1. CommandHMI permite copiar las propiedades de un estado a otro, lo que es práctico y ahorra tiempo.

• Todos los textos en el primer idioma: opción para proyectos multilingües («Idioma» en el gestor de proyecto). Si hay más de un idioma, esta opción impide que el contenido del objeto cambie con el idioma.

• Idioma: opción para proyectos multilingües: introduzca el contenido en cada idioma. (En el botón de función, elija «Cambiar idioma» y el idioma de destino; en la simulación o en el HMI, todos los objetos con texto se muestran en ese idioma). El texto, la fuente y el tamaño pueden variar según el idioma; el color, el espaciado y la posición son comunes

• Fuente: tipo de letra del texto; cada idioma puede tener su propia fuente.

• Tamaño de fuente: tamaño del texto; cada idioma puede tener su propio tamaño.

• Color, margen, posición: color, margen y alineación del texto seleccionado. Con varios idiomas, estas opciones son las del idioma 1 y no tienen efecto en los demás idiomas.

• Imagen estado 0, Imagen estado 1: permiten añadir imágenes de distintos formatos para cada estado según el «Origen de imagen». La imagen elegida se añade automáticamente a la página «General». Con «Ajustar al tamaño del objeto», la imagen toma el tamaño del objeto.

• Ajustar al tamaño del objeto: si se marca, la imagen toma el tamaño del objeto y se ocultan las opciones de margen y posición.

• Si importa una imagen desde un archivo externo, aparece la opción «Transparencia» para hacer transparente un color concreto

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton7699.png" width="130" />

Con «Parpadeo», la visualización parpadea entre los estados ON/OFF. La frecuencia por defecto es 1 s. Para cambiarla, haga doble clic en «Parámetros del HMI» en el gestor de proyecto y modifique la «Frecuencia de parpadeo».

Elija la página «Avanzado» para ver sus propiedades, como en la figura 4-73

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8062.png" width="660" />

Figura 4-73  Página «Avanzado» del botón de bit

• Controlado por bit: si «Estado válido» es 1, el botón de bit solo responde al tacto cuando el «Bit de control» vale 1. Si «Estado válido» es 0, solo responde cuando el «Bit de control» vale 0. En los demás casos el botón no funciona.

• Controlado por nivel de usuario: el usuario puede marcar varias opciones. En la simulación o en el HMI se comprueba si el usuario actual tiene ese permiso.

Por ejemplo, si en la página «Avanzado» del objeto se marcan las opciones 2 y 3 del control por nivel, y las contraseñas de usuario en los parámetros de la pantalla táctil son las de la figura 4-74:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8900.png" width="692" />

Figura 4-74 Contraseñas de usuario en los parámetros de la pantalla táctil

Si el nivel de usuario por defecto es NULL, el objeto no responde; puede usar la función «Cambiar nivel de usuario» de un botón de función para cambiarlo. Por ejemplo, si el usuario introduce 6666 (nivel 6), que solo tiene la opción 1 y no la 2 ni la 3, el sistema indica que la contraseña es incorrecta; si introduce 2222 o 3333, ambos usuarios tienen la opción 2, que coincide con 2 o 3: la contraseña es válida y el objeto responde. Si el nivel por defecto es el usuario 2 o 3, ambos tienen la opción 2 y el objeto responde desde el inicio en la simulación o en la pantalla; si es el usuario 6, no hay coincidencia y el objeto no responde. Los ajustes por defecto se muestran en la figura siguiente:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton9956.png" width="459" />

Si se marca «Cambiar nivel de usuario si es insuficiente», cuando el nivel no coincide aparece una ventana de inicio de sesión para elegir un nivel adecuado y volver a conectarse, como abajo:

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton10150.png" width="466" />

En CommandHMI solo tienen esta función los objetos botón de bit, lista desplegable, entrada ASCII, botón de función, entrada por teclado ASCII, botón multifunción, botón multiestado, selección de receta, botón de pantalla, botón de opción, botón de pasos, botón de palabra, deslizador y entrada numérica; su uso es igual al del botón de bit.

• Tiempo mínimo de pulsación: segundos que debe durar la pulsación para que el objeto reaccione en la simulación o en el HMI.

• Notificación: si el objeto responde en la simulación o en el HMI, al hacer clic en él e introducir un valor con el teclado emergente, se escribe el estado (1 o 0) en la dirección del «Bit de notificación».

• Registro de notificación: si el objeto responde en la simulación o en el HMI, al hacer clic en él e introducir un valor con el teclado emergente, ese valor se escribe en la dirección del «Registro de notificación».

• Tecla de acceso rápido: con esta función, una cifra o carácter produce el mismo efecto que pulsar el objeto. Por ejemplo, con 1, pulsar 1 en el teclado numérico de la simulación o del HMI, o en un teclado externo, tiene el mismo efecto.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11418.png" width="161" />

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11420.png" width="130" />

El nivel de usuario por defecto es NULL, el más bajo. El diseñador puede cambiarlo con la función «Cambiar nivel de usuario» de un botón de función introduciendo la contraseña correspondiente.

Un toque efectivo es aquel que produce una acción real al tocar el objeto: activar, desactivar, pulsador momentáneo, alternar, etc. Otro ejemplo es la entrada numérica: al tocarla se abre el teclado, pero no se genera notificación porque no se escribe nada en la dirección. Salir del teclado con ESC tampoco genera notificación. Solo hay notificación si se introduce un valor entre el mínimo y el máximo y se pulsa ENTER.

Elija la página «Visibilidad» para ver sus propiedades, que determinan si el objeto se muestra u oculta. Como en la figura 4-75

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12372.png" width="675" />

Figura 4-75 Página «Visibilidad» del botón de bit

• Controlado por bit: si se marca y el estado válido es 1, el botón de bit solo se muestra en la pantalla táctil cuando el bit de control vale 1; si el estado válido es 0, solo se muestra cuando el bit de control vale 0.

• Controlado por nivel de usuario: las condiciones son las mismas que en la opción equivalente de la página «Avanzado»; el botón solo se muestra si se cumplen.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12995.png" width="130" />

Si no se marca ninguna de las dos opciones, el objeto se muestra siempre.
