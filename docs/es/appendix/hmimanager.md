# Uso de HMIManager

Vaya a la página de herramientas de descarga

![](../../appendix/hmimanageer.files/002.png)

Página «Descarga»:

Ajustes de comunicación:
USB: el PC se conecta al HMI por USB
WAN: el PC se conecta al HMI por Ethernet

También puede hacer clic en el botón «Escanear» para buscar direcciones IP

![](../../appendix/hmimanageer.files/a1.png)

Puede marcar la dirección IP encontrada y modificarla en el campo de modificación inferior

![](../../appendix/hmimanageer.files/a2.png)

Haga clic en el botón de la derecha para modificar la información de la pantalla; al terminar aparece una ventana emergente.

![](../../appendix/hmimanageer.files/a3.png)

Si hace clic en «Volver a escanear», verá el resultado modificado en la lista.

![](../../appendix/hmimanageer.files/a4.png)

Marque la dirección IP que desea usar y haga clic en «Seleccionar» para elegir la IP de destino; la información IP se sincroniza con la ventana de descarga.

**¡Atención!**

Para usar la búsqueda de IP deben cumplirse estos tres requisitos:

1. Las pantallas táctiles fabricadas antes del 30 de diciembre de 2024 necesitan instalar manualmente el parche de búsqueda IP; si no encuentra el archivo «hmi.patch» en el directorio de instalación, pídalo al personal técnico.
     2. La versión del software de configuración no debe ser inferior a HMITOOLV7.1_022
     3. La versión del firmware no debe ser inferior a Simulator 8.1.0.10.

Selección de descarga:
Descargar la configuración: debe generar el archivo de proyecto u-disk-prj.bin; en el software de configuración elija Download-&gt;Extract Project Save As-&gt;generar el archivo u-disk-prj.bin, haga clic en «Examinar» para seleccionar el archivo y después en «Iniciar» para descargarlo y actualizar la configuración del HMI.
Descargar la receta: compile el proyecto HMI editado; en la carpeta compile del directorio de instalación se generan los archivos recipe60.bin y recipe62.bin; para la versión 6.0 o anterior elija recipe60.bin, para versiones superiores a la 6.0 elija recipe62.bin. Haga clic en «Examinar» para seleccionar el archivo y después en «Iniciar descarga».

![](../../appendix/hmimanageer.files/003.png)

Página «Carga»:

Ajustes de comunicación:
Igual que para la descarga.

Selección de carga:
Zona de selección: la configuración solo puede cargarse si los parámetros de la pantalla táctil lo permiten; recetas, datos históricos y alarmas históricas solo pueden cargarse si existen en el programa del HMI.
Cargar datos históricos: haga clic en «Examinar» para indicar la ubicación y el nombre del archivo, y en «Iniciar carga» para cargar el zip de datos históricos y el archivo .csv; véase «Cargar archivos de datos históricos».
Cargar la configuración: haga clic en «Examinar» para indicar la ubicación y el nombre del archivo, y en «Iniciar carga» para cargar el zip de la configuración; después descomprímalo para ver y editar el proyecto normalmente; véase «Cargar el programa de configuración».
Cargar la receta: haga clic en «Examinar» para indicar la ubicación y el nombre del archivo, y en «Iniciar carga» para cargar el archivo de recetas del HMI.
Cargar alarmas históricas: haga clic en «Examinar» para indicar la ubicación y el nombre del archivo, y en «Iniciar carga» para cargar el archivo de alarmas del HMI.

![](../../appendix/hmimanageer.files/004.png)

Página «Versión»:

Ajustes de comunicación:
Igual que para la descarga.

Información de versión: versión del HMI conectado.

![](../../appendix/hmimanageer.files/005.png)

Página «Firmware»:

Ajustes de comunicación:
Igual que para la descarga.

Información del firmware
Firmware: haga clic en «Examinar» para seleccionar el firmware a actualizar y después en «Actualizar»

![](../../appendix/hmimanageer.files/006.png)

Página «Simulación»:

Seleccione el archivo de proyecto .vpm para ejecutar la simulación en línea o sin conexión.

![](../../appendix/hmimanageer.files/007.png)

Página «Dirección»:

Servicio: elija el fabricante del equipo.
Modelo: elija el modelo de equipo
Muestra toda la información de direcciones del equipo seleccionado.
