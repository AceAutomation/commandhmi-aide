# Ajustar parámetros y añadir objetos gráficos

**Parámetros:**

1\. Los parámetros pueden modificarse con «Preferencias» del menú «Ajustes» o haciendo doble clic en [Parámetros del HMI](../setting/paramater.md) en «Ajustes» del gestor de proyecto. Se abre el cuadro de diálogo de la figura 3-6:

<img src="../../start-new-project/setting-parameter.files/image001.jpg" width="643" alt="ScreenShot00218.jpg" />

Figura 3-6     Cuadro de diálogo de parámetros generales

• Modelo de HMI: cambia el modelo de HMI.

• Modo de visualización: pantalla horizontal o vertical.

• Ajustes de arranque del HMI

• Pantalla de inicio: pantalla mostrada al encender el HMI

• Tiempo del salvapantallas: tiempo hasta el salvapantallas

• Frecuencia de parpadeo: frecuencia de parpadeo de los objetos que parpadean; se cambia introduciendo directamente un valor o con las flechas.

• Sonido de alarma: al producirse una alarma, la pantalla táctil puede avisar con un sonido; la lista de la derecha ofrece con o sin sonido.

• Sonido táctil: la lista de la derecha ofrece «Con sonido» o «Sin sonido».

• Pantalla de salvapantallas: se elige una pantalla existente como salvapantallas; al tocar la pantalla se vuelve a la anterior.

• Pantalla de carga: si se marca, tras el encendido el HMI muestra durante un tiempo la pantalla de carga elegida y después pasa a la pantalla de inicio; permite mostrar indicaciones o notas.

• Otros ajustes

• Ocultar el cursor del ratón: indica si se muestra el cursor

• Ajustes de coma flotante:

\[Estándar\]: byte alto primero, byte bajo después;

\[Personalizado\]: el usuario define el orden.

• Toque no válido: con «Usar marca personalizada», los objetos bloqueados no responden y se marcan con la imagen elegida por el usuario.

• Mostrar el efecto de pulsación de los objetos: novedad de CommandHMI. Con el efecto activado, al tocar un objeto aparece un marco rectangular, del color elegido por el usuario. Actualmente lo admiten el botón de bit, el botón de palabra, el botón de pantalla, el botón de función, la entrada numérica y la entrada ASCII. Por defecto: sin efecto.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2109.png" width="130" />

En los objetos elípticos, el efecto de pulsación sigue siendo rectangular.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2172.png" width="230" />

Figura 3-7

2、Contraseñas de usuario

<img src="../../start-new-project/setting-parameter.files/setting-parameter2206.png" width="692" />

Figura 3-8     Contraseñas de usuario en los parámetros del HMI

Esta función ofrece 8 contraseñas de usuario, cada una con ocho niveles.

• Nivel de usuario por defecto: el nivel por defecto actual es NULL.

• Permitir la carga del proyecto: si se marca, el proyecto puede cargarse del HMI al PC; si no, no.

• Contraseña para la carga: indica si cargar el proyecto requiere contraseña.

• Contraseña para actualizar el proyecto por memoria USB: si se define, hay que introducirla al actualizar el proyecto del HMI con una memoria USB.

• Contraseña de máxima autoridad: permite manejar todos los objetos restringidos por nivel.

• Carga: indica si esta contraseña permite cargar proyectos del HMI al PC.

• Permisos: indica si esta contraseña permite todas las operaciones restringidas.

**3. Ajustes de impresora <span id="OLE_LINK247"></span><span id="OLE_LINK246"></span>y descarga**

Haga clic en «Ajustes de conexión entre el HMI y la impresora», como en la figura 3-9:

<img src="../../start-new-project/setting-parameter.files/setting-parameter3209.png" width="693" />

Figura 3-9      Ajustes de conexión entre el HMI y la impresora

<span id="OLE_LINK245"></span><span id="OLE_LINK244"></span>Esta página contiene los parámetros de conexión entre la impresora y el HMI; elija los adecuados según el modelo de impresora.

**Ajustes de descarga:**

• Modo de descarga: elija USB o Ethernet. Con Ethernet hay que definir la dirección IP y el puerto (los del HMI).

• Borrar las alarmas históricas: indica si se borran las alarmas históricas antes de la descarga.

• Borrar los datos históricos: indica si se borran los datos históricos antes de la descarga.

• Descargar recetas: indica si se descargan al HMI las recetas del proyecto actual.

**Opciones de descarga de imágenes:**

• Conservar el formato original: el formato de las imágenes no cambia en la descarga.

• Convertir a JPG: todas las imágenes se convierten a JPG antes de descargarlas al HMI.

(Nota: como las imágenes BMP ocupan mucho espacio, se recomienda esta opción.)

4. Ubicación de almacenamiento y sistema de alarmas, como abajo

<img src="../../start-new-project/setting-parameter.files/setting-parameter4305.png" width="692" />

Figura 3-10   Cuadro de diálogo Ubicación de almacenamiento y alarma del sistema

• Ubicación de almacenamiento: ubicación de los datos históricos, las alarmas históricas y las capturas de pantalla. Opciones: «Local (FLASH)» y «Memoria USB». Por defecto: Local (FLASH).

• IP del HMI: parámetros de red de la pantalla táctil

• Sistema de alarmas

Usar el sistema de alarmas: indica si se usa la alarma del sistema. Al producirse una alarma, el sistema muestra el mensaje actual arriba o abajo de cada pantalla, según lo definido.

Color de fondo de la alarma, color del texto, fuente y tamaño de fuente: propiedades de visualización del sistema de alarmas, ajustables según las necesidades.

Modo de visualización: «Mostrar siempre» muestra la alarma de forma continua; «Mostrar cíclicamente» la muestra y oculta periódicamente, con efecto de parpadeo.

Posición de la barra de alarmas: posición donde aparece la barra de alarmas.

5. Otros ajustes, como abajo

<img src="../../start-new-project/setting-parameter.files/setting-parameter5287.png" width="690" />

Figura 3-11   Contraseña de desbloqueo del salvapantallas

• Si se marca esta opción, el usuario debe introducir esta contraseña para salir del salvapantallas.

<img src="../../start-new-project/setting-parameter.files/setting-parameter5429.png" width="130" />

El tiempo del salvapantallas solo tiene efecto si se ha elegido una «Pantalla de salvapantallas»; al tocar el salvapantallas se vuelve a la pantalla anterior.
