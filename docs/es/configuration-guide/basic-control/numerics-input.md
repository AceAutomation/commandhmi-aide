# Entrada numérica

La entrada numérica es el objeto más usado, prácticamente imprescindible en cualquier control de proceso. Permite introducir, mostrar y guardar valores en los registros de datos del PLC u otros equipos conectados, como velocidad, corriente, presión, etc.

La entrada numérica y la visualización numérica funcionan prácticamente igual; la única diferencia es que la entrada numérica permite escribir valores en los registros de datos del PLC u otros equipos, además de mostrarlos.

Para crear una entrada numérica:

Elija el icono de entrada numérica<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input596.png" width="31" /> en la barra de herramientas; se abre un cuadro de diálogo, como en la figura 4-95.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input665.png" width="662" />

Figura 4-95 Cuadro de diálogo Entrada numérica

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input705.png" width="130" />

Nota: para forma, color del borde, color de primer plano, color de fondo y trama, véase el objeto «Botón de bit».

Nota: para «Alineación», «Relleno», «Decimales» y «Número total de cifras», véase el objeto «Visualización numérica».

Nota: haga doble clic en el campo de visualización para modificar su contenido y sus propiedades. Cuando el objeto funciona en el HMI aparece un teclado en pantalla para que el usuario introduzca datos, como en la figura 4-96.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1192.png" width="693" />

Figura 4-96 Teclado numérico

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1228.png" width="130" />

Nota: con un tipo de dato de 32 bits, la dirección ocupa 2 palabras. Por ejemplo, si se escribe en el registro de datos V10 de un PLC SIEMENS, se ocupan V10 y V11; si otro objeto monitoriza también V11, se produce un error. Tenga cuidado con los tipos de 32 bits para evitar errores de datos y direcciones.

Nota: el número de decimales influye en la visualización. Con los tipos entero positivo o entero de 16/32 bits, el valor mostrado se obtiene desplazando la coma del valor devuelto el número de cifras indicado. Si se devuelve 212 con 2 decimales, se muestra 2.12. Con el tipo coma flotante de 32 bits, el valor no se desplaza; solo se muestran los decimales indicados. Si se devuelve 2.123 con 2 decimales, se muestra 2.12.

Nota: el número total de cifras es la suma de la parte entera y la decimal. Si la parte entera del valor es más larga que la definida, se muestra con su longitud real. Por ejemplo, para el valor 2123 con longitud 2 y 1 decimal, se muestra 212.3.

• Entrada de contraseña: los caracteres introducidos por el usuario se muestran como «\*» durante la entrada y la visualización.

• Usar script: marque «Usar script» para ver la lista de scripts. El usuario elige uno que se ejecuta al pulsar la entrada numérica. La lista solo muestra los scripts compilados.

• Número total de cifras: suma de las cifras enteras y decimales. Limita el tamaño de los valores mostrados e introducidos. Con 4 cifras en total y 1 decimal, el valor máximo es 999.9, máximo de entrada y de visualización del objeto. Una entrada mayor da error; una visualización mayor ignora las cifras sobrantes y solo muestra el número de cifras definido. Por ejemplo: 4 cifras, 1 decimal y valor real 12345: el objeto muestra 234.5.

Página «Avanzado»: sirve para ajustar la ganancia, el offset y la comprobación de rango de los datos introducidos (comprueba si el valor está fuera del rango definido). También ofrece las opciones «Disponibilidad táctil» y «Notificación», que funcionan igual que en el objeto «Botón de bit».

Haga clic en la pestaña «Avanzado», como en la figura 4-97:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input3958.png" width="675" />

Figura 4-97 Página «Avanzado» de la entrada numérica

• Controlado por bit: si se marca, el objeto solo está disponible en determinadas condiciones. Si «Estado válido» es 1, el objeto solo responde cuando el «Bit de control» vale 1. Si «Estado válido» es 0, solo responde cuando el «Bit de control» vale 0. En los demás casos no funciona.

• Controlado por nivel de usuario: el usuario puede marcar varias opciones. En la simulación o en el HMI se comprueba si el usuario actual tiene ese permiso.

• Usar teclas de acceso rápido: véase el Botón de bit.

• Mostrar valor: si se marca, el teclado de entrada muestra el valor actual del objeto. Por ejemplo, si el valor mostrado es 389, al hacer clic en la entrada numérica la zona de entrada muestra 389; si no, está vacía, como abajo:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4972.png" width="93" />

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4974.png" width="630" />

Por ejemplo, si en la página «Avanzado» del objeto se marcan las opciones 2 y 3 del control por nivel, y las contraseñas de usuario en los parámetros de la pantalla táctil son las de la figura 4-98:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input5185.png" width="605" />

Figura 4-98 Contraseñas de usuario en los parámetros de la pantalla táctil

Si el nivel de usuario por defecto es NULL, el objeto no responde; puede usar la función «Cambiar nivel de usuario» de un botón de función para cambiarlo. Por ejemplo, si el usuario introduce 6666 (nivel 6), que solo tiene la opción 1 y no la 2 ni la 3, el sistema indica que la contraseña es incorrecta; si introduce 2222 o 3333, ambos usuarios tienen la opción 2, que coincide con 2 o 3: la contraseña es válida y el objeto responde. Si el nivel por defecto es el usuario 2 o 3, ambos tienen la opción 2 y el objeto responde desde el inicio en la simulación o en la pantalla; si es el usuario 3 y no hay coincidencia, el objeto no responde. Los ajustes por defecto se muestran en la figura siguiente:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6241.png" width="266" />

Si se marca «Cambiar nivel de usuario si es insuficiente», cuando el nivel no coincide aparece una ventana de inicio de sesión para elegir un nivel adecuado y volver a conectarse, como abajo:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6435.png" width="268" />

• Notificación: si el objeto responde, en la simulación o en la pantalla, al hacer clic en él e introducir un valor con el teclado emergente, se escribe el estado definido (1 o 0) en la dirección del «Bit de notificación».

• Escalado: si se marca, el valor escrito en la dirección = (valor introducido por el usuario con el teclado - offset) / ganancia; el valor mostrado (valor de la dirección de monitorización) = valor de la dirección de monitorización × ganancia + offset

• Mostrar rango: si se marca, el usuario define los límites inferior y superior y los colores de fondo bajo y alto. El valor monitorizado (leído) se representa con colores distintos según esos límites.

• Rango variable: los valores «Límite inferior» y «Límite superior» cambian dinámicamente según la dirección indicada por el usuario

• Límite inferior: límite inferior de visualización. Si el valor es menor, el fondo toma el color definido en «Color de fondo nivel bajo».

• Límite superior: límite superior de visualización. Si el valor es mayor, el fondo toma el color definido en «Color de fondo nivel alto».

• Comprobación de rango: comprueba si el valor introducido supera el máximo o el mínimo definidos.

Tras los ajustes, haga clic en «Aceptar» para añadir el objeto a la zona de trabajo (la pantalla)

• Con la página «General» configurada como abajo, el número se muestra en binario y se introduce en decimal. Con otro tipo de visualización, el tipo de entrada es el mismo que el de visualización.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input8099.png" width="663" />

• Tras ajustar las propiedades, haga clic en «Aceptar»; el cursor se convierte en una cruz. Dibuje un rectángulo en la pantalla con el ratón para añadir el objeto.
