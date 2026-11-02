# Crear un proyecto

Este paso es necesario para crear un proyecto nuevo. Elija «Nuevo proyecto» en el menú «Archivo» o el botón «Nuevo proyecto» <img src="../../start-new-project/new-project.files/new-project136.png" width="28" /> de la barra de herramientas; CommandHMI abre el cuadro de diálogo «Nuevo proyecto», donde se definen el nombre y la ruta del proyecto. Elija el modelo de HMI; «Aceptar» crea el proyecto y abre los ajustes del puerto de comunicación; «Cancelar» cierra el cuadro de diálogo.

**1. Cuadro de diálogo Nuevo proyecto**

Nombre del proyecto:

Ruta: ruta de guardado del nuevo archivo de proyecto; por defecto C: \\

Modelo: modelos disponibles para el proyecto:

HM-035AE(320\*240)        HM-035UE(320\*240)        HM-043AE()480\*272        HM-043D(480\*272)        HM-043AD(480-272)        HM-043BE(480\*272)        HM-043BS(480\*272)        HM-043QE(480\*272)        HM-043UE(480\*272)        HM-043TE(480\*272)        HM-050AS(480\*272)        HM-050AE(480\*272)        HM-050BS(800\*480)        HM-050BE(800\*480)        HM-057AE(640\*480)        HM-070AS(800\*480)        HM-070AE(800\*480)        HM-070BS(800\*480)        HM-070BE(800\*480)        HM-070GS(800\*480)        HM-070GE(800\*480)        HM-070QS(800\*480)        HM-070QE(800\*480)        HM-070GG(800\*480)        HM-070GW(800\*480)        HM-070MS(800\*480)        HM-070ME(800\*480)        HM-070MG(800\*480)        HM-070MW(800\*480)        HM-T070XS(1024\*600)        HM-102AS(800\*480)        HM-102AE(800\*480)        HM-102BS(1024\*600)        HM-102BE(1024\*600)        HM-102CW(1024\*600)        HM-102CG(1024\*600)        HM-102HE(1024\*600)        HM-102HS(1024\*600)        HM-121AS(800\*600)        HM-121AE(800\*600)        HM-H150AS(1024\*768)        HM-156QS(1920\*1080)

El modelo por defecto es HM-070AE(800\*480); la resolución (800 \* 480) entre paréntesis no se muestra en el cuadro de diálogo.

Modo de visualización: orientación de la pantalla táctil en el proyecto. Opciones:

Horizontal: configuración con la pantalla táctil en horizontal.

Vertical: configuración con la pantalla táctil en vertical.

Por defecto: horizontal.

<img src="../../start-new-project/new-project.files/image002.jpg" width="547" alt="ScreenShot00217.jpg" />

Figura 3-1      Cuadro de diálogo Nuevo proyecto

En el cuadro de diálogo «Nuevo proyecto» anterior se definen el nombre, la ruta, el modelo y el modo de visualización; haga clic en «Siguiente» para configurar el puerto de comunicación.

El modelo concreto depende del modelo de HMI del usuario.

<img src="../../start-new-project/new-project.files/new-project1533.png" width="130" />

El nombre del proyecto no puede contener estos caracteres: \\ /: \* "&lt;&gt; \|?.

La ubicación del proyecto no puede contener estos caracteres: \\ /: \* "&lt;&gt; \|?.

## 2. Cuadro de diálogo Ajustes de comunicación

En este cuadro de diálogo se definen los parámetros del puerto de comunicación del HMI. Solo con parámetros correctos se garantiza la comunicación normal entre el PLC y la pantalla táctil. Los parámetros dependen del modelo de PLC conectado.

Nombre de la conexión: nombre del puerto de comunicación.

Servicio de equipo: marca de PLC y tipo de CPU.

Interfaz de conexión: puerto COM o puerto Ethernet.

Intervalo de direcciones continuas del PLC: espacio de direcciones consecutivas del PLC; se recomienda el valor por defecto.

##

<img src="../../start-new-project/new-project.files/new-project2298.png" width="624" />

Figura 3-2      Cuadro de diálogo Ajustes de comunicación

En el cuadro de diálogo anterior se elige el servicio de equipo según el equipo conectado. Para una conexión Ethernet, elija «Conexión directa (Ethernet)» en «Tipo de conexión».

ID de conexión: parámetro interno, no modificable.

Las propiedades de comunicación también pueden ajustarse después en «Conexión» del gestor de proyecto; los demás parámetros se ajustan en las propiedades de comunicación.

**3.       Cuadro de diálogo Propiedades de la pantalla**

Haga clic en «Siguiente» en el cuadro de diálogo de ajustes de comunicación; se abre el cuadro «Nueva pantalla», donde se definen el nombre y el color de fondo de la pantalla. El nombre por defecto es un número de pantalla y el color de fondo por defecto es azul. Con cada pantalla nueva, CommandHMI asigna un número que indica el orden de las pantallas en el proyecto. La numeración empieza en 1: la primera pantalla es la n.º 1 y la n.º 5 es la quinta. Para cambiar el color de fondo, haga clic en el rectángulo junto a «Color de fondo»; se abre el selector de color. Con más de doscientos colores para elegir rápidamente, CommandHMI ofrece una gama de colores muy amplia. Si no basta, haga clic abajo a la derecha del selector para personalizar el color. En el cuadro «Colores personalizados», elija primero un color básico y después el tono en el cuadro central; ajuste el color arrastrando el ratón, también en la barra vertical de la derecha, y haga clic en «Aceptar». También puede introducir directamente los valores del color.

<img src="../../start-new-project/new-project.files/new-project4278.png" width="626" />

Figura 3-3      Cuadro de diálogo Nueva pantalla

<img src="../../start-new-project/new-project.files/new-project4313.png" width="506" />

Figura 3-4      Cuadro de diálogo Selección de color

También se pueden usar imágenes propias como fondo de pantalla. Haga clic en el icono de ruta para elegir la imagen.

<img src="../../start-new-project/new-project.files/new-project4463.png" width="331" />

Figura 3-5      Ruta de la imagen

Haga clic en «Aceptar»; el sistema abre inmediatamente la pantalla creada. Los preparativos han terminado; ya puede editar su proyecto.
