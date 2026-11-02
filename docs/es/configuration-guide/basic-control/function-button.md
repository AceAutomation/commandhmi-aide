# Botón de función

El botón de función es un objeto esencial del HMI: permite realizar fácil y rápidamente muchas funciones. Haga clic en <img src="../../../configuration-guide/basic-control/function-button.files/function-button143.png" width="28" /> para abrir el cuadro de diálogo de propiedades, como en la figura 4-82:

<img src="../../../configuration-guide/basic-control/function-button.files/function-button223.png" width="660" />

Figura 4-82 Cuadro de diálogo Botón de función

<img src="../../../configuration-guide/basic-control/function-button.files/function-button264.png" width="130" />

Nota: para forma, color del borde, color de primer plano, color de fondo y trama, véase el objeto Botón de bit.

**1. Apagar la retroiluminación**

Elija la función «Apagar la retroiluminación». Al pulsar el botón en la pantalla, la retroiluminación se apaga y el HMI sigue funcionando normalmente. Para volver a encenderla, basta con tocar cualquier punto de la pantalla.

**2. Confirmar alarma**

Elija la función «Confirmar alarma». Al pulsar el botón se confirma la alarma seleccionada

**3. Reiniciar**

Con la función «Reinicio del sistema», al tocar este botón se reinicia la pantalla táctil.

**4. Tiempo del salvapantallas**

Con la función «Ajustar tiempo del salvapantallas», al tocar este botón se abre una ventana para ajustar el tiempo del salvapantallas.

**5. Escribir receta en el PLC**

Esta función transmite la receta al PLC. Al pulsar el botón en la pantalla táctil, la receta guardada en el HMI se envía a los registros de datos continuos del PLC u otro equipo conectado. (La dirección es la dirección de escritura definida al crear la receta en el software.)

**6. Leer receta del PLC**

Esta función lee la receta del PLC. Al pulsar el botón en la pantalla táctil, los datos de la receta se leen de los registros de datos continuos del PLC u otro equipo conectado. (La dirección es la dirección de escritura definida al crear la receta en el software.)

**7. Ajustar fecha y hora**

Esta función ajusta la fecha y la hora: al pulsar el botón en la pantalla táctil se ajustan la fecha y hora internas.

**8. Borrar alarma**

Esta función borra la alarma: al pulsar el botón en la pantalla táctil se borra la alarma seleccionada y confirmada.

**9. Receta anterior**

Con la función «Receta anterior», al pulsar el botón se abre la receta anterior a la actual. Si la receta actual es la primera o solo hay una receta, los parámetros no cambian.

**10. Receta siguiente**

Con la función «Receta siguiente», al pulsar el botón se abre la receta siguiente a la actual. Si la receta actual es la última o solo hay una receta, los parámetros no cambian.

**11. Guardar la receta actual**

Esta función guarda la receta actual: al pulsar el botón en la pantalla táctil se guardan los datos de la receta procedentes de los registros de datos continuos del PLC u otro equipo, definidos al crear la receta en el software.

**12. Captura de pantalla**

Con la función «Captura de pantalla», al pulsar el botón la pantalla actual se guarda como imagen en la ubicación indicada por el usuario. El nombre de la imagen puede introducirse con una entrada ASCII; no puede contener ：#￥%&\*-+&lt;&gt; etc. y debe tener como máximo 20 caracteres.

**13. Parámetros del sistema**

Con la función «Parámetros del sistema», al pulsar el botón en el HMI se abre la pantalla de parámetros del sistema, donde se pueden cambiar la hora, el tiempo del salvapantallas, el contraste de la retroiluminación, etc.

**14. Iniciar sesión**

Con la función «Iniciar sesión», al pulsar el botón aparece una ventana de inicio de sesión. Tras elegir el nombre de usuario aparece un teclado para introducir la contraseña y obtener el permiso de acceso.

**15. Cerrar sesión**

Con la función «Cerrar sesión», al pulsar el botón en la pantalla táctil se cierra la sesión y se retiran los permisos del usuario actual, cuyo nivel pasa a ser el más bajo.

**16. Sonido de alarma (ON / OFF)**

La función «Sonido de alarma ON / OFF» emite un sonido cuando se produce una alarma; el botón de función activa o desactiva esta función. Si está activada, al pulsar el botón se silencia el sonido de alarma, y viceversa

**17. Sonido táctil (ON / OFF)**

Con la función «Sonido táctil», al tocar el botón se activa o desactiva el sonido táctil. Si está activado, al tocar el botón se desactiva, y viceversa.

**18. Borrar todos los datos históricos**

Se borran los datos históricos guardados en el HMI.

**19. Borrar las alarmas históricas**

Se borran las alarmas históricas guardadas en el HMI.

**20. Desbloquear la protección del HMI**

Introduzca la contraseña para desactivar la protección del HMI.

**21. Leer y guardar receta**

Lee y guarda la receta.

**22. Función de reserva**

Solo como función de reserva; no realiza ninguna operación.

**23. Recargar la receta**

Recarga los datos de receta de la flash en la dirección RWI correspondiente.

**24. Cambiar idioma**

Cambia el texto de todos los objetos al idioma indicado

**25. Imprimir la pantalla en una impresora serie**

Imprime la pantalla indicada en una impresora serie. La conexión del controlador de impresora se configura en «Parámetros del HMI» -&gt; «Ajustes de impresora y descarga», en el panel izquierdo del software.

**26. Configuración IP de los equipos esclavos**

Esta función requiere el «Modo extendido», que se configura en las «Propiedades del puerto de comunicación». Para la comunicación Ethernet con varios equipos hay que añadir delante del objeto correspondiente un número de estación y la dirección del registro que controla ese número de estación. Con el proyecto en marcha en el HMI, al hacer clic en el objeto de función, el número de estación definido por el usuario aparece en el cuadro «IP config»; ajuste entonces los parámetros IP de ese número de estación para establecer la comunicación Ethernet con varios equipos.

**27. Funciones de los interruptores DIP 1 y 3**

Funciones disponibles cuando los interruptores DIP 1 y 3 del hardware están en ON: principalmente ajuste de IP, de la hora del sistema y de la retroiluminación. Tras el ajuste, haga clic en «Aceptar» para reiniciar.

Usar script: marque «Usar script» para ver la lista de scripts; el usuario elige uno que se ejecuta al ejecutarse la función. La lista solo muestra los scripts compilados.

<img src="../../../configuration-guide/basic-control/function-button.files/function-button6119.png" width="130" />

Nota: al pasar a la pantalla del sistema, se cierra el proyecto actual; al volver, el proyecto se reinicia y se abre su pantalla de inicio.

Nota: la página «Etiqueta» del botón de función es similar a la del objeto «Botón de bit», salvo que no tiene Texto estado 1 ni Imagen estado 1, porque solo tiene un estado.

Nota: las páginas «Avanzado» y «Visibilidad» del botón de función son iguales a las del objeto Botón de bit; para las teclas de acceso rápido, véase el Botón de bit.

Nota: las funciones Receta anterior, Receta siguiente, Guardar receta y Leer y guardar receta solo actúan sobre el grupo de recetas actual. Para otro grupo, ajuste antes LW61141.

Nota: borrar los datos históricos borra todos los grupos de datos históricos.

Tras ajustar todas las propiedades, haga clic en «Aceptar» para añadir el botón a la zona de trabajo (la pantalla)
