# Descargar el proyecto

<img src="../../start-new-project/download-project.files/image012.jpg" width="368" />

Figura 3-11    Mensaje de error de compilación

Corrija el error según el mensaje de la ventana de salida; o haga doble clic en el error y CommandHMI localiza y selecciona automáticamente el objeto erróneo. Haciendo doble clic en el objeto se ven sus propiedades, se encuentra la causa del error y se corrige. Después haga clic en «Guardar» para volver a compilar. Si no hay errores, el sistema indica al cabo de un momento que la compilación es correcta. Haga clic en «Aceptar» para terminar, como en la figura 3-12:

<img src="../../start-new-project/download-project.files/image013.jpg" width="364" />

Figura 3-12    Ventana de salida

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Antes de descargar hay que compilar, y antes de compilar hay que guardar; si no, la compilación falla, como en la figura 3-11. Tras cualquier modificación hay que volver a compilar.

<img src="../../start-new-project/download-project.files/image014.jpg" width="425" />

Figura 3-13    Aviso de compilación

Por último, ejecute el comando USB del menú «Download» para descargar por cable USB; también puede elegir directamente «Compilar + Descargar» en el menú «Download». Se abre el cuadro de diálogo de la figura 3-14:

<img src="../../start-new-project/download-project.files/image015.jpg" width="716" />

Figura 3-14    Cuadro de diálogo de descarga

Haga clic en «Descargar»; la barra de progreso muestra el avance. Al terminar, una ventana indica que la descarga USB se ha completado. Haga clic en «Aceptar», como en la figura 3-15:

<img src="../../start-new-project/download-project.files/image005.jpg" width="720" alt="2018_11_20_09_02_42.jpg" />

Figura 3-15    Descarga completada

El paso siguiente es conectar el PLC para comprobar que el proyecto funciona correctamente en el HMI.

Las formas de conexión entre el HMI y el PLC o el PC se describen en «Conexión» del manual de hardware.

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Durante la transferencia no desconecte la alimentación del HMI ni del PC ni el cable USB, y no realice otras operaciones; si no, la transferencia se verá afectada.

Instale los controladores USB antes de descargar; si no, el PC no podrá conectarse al HMI y no podrá completar la descarga.

<img src="../../start-new-project/download-project.files/image017.jpg" width="716" />

Figura 3-16    Aviso del controlador USB

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

El cuadro de diálogo de la figura 3-16 indica que el PC no reconoce el HMI. Compruebe si el controlador USB está instalado: conecte el PC al HMI encendido y busque «CommandHMI HMI Tech Corp USB drive» en Windows «Mi PC» - «Propiedades» - «Hardware» - «Administrador de dispositivos» - «Controladoras de bus serie universal» (puede desconectar el cable USB para comprobar si el PC reconoce el HMI):

**Descarga del proyecto por Ethernet**

• Ajustar los parámetros de red del HMI

Ponga a la vez en ON los interruptores DIP 1 y 3; defina la IP (aquí 192.168.1.100), la pasarela, la subred y el puerto. El puerto es fijo: 12345.

• Compilar el proyecto

Para descargar por Ethernet hay que introducir la dirección IP y el puerto en el campo correspondiente. La IP es la del HMI de destino, aquí 192.168.1.100 como arriba; el puerto es fijo, 12345. Haga clic en «Reiniciar y descargar», como en la figura 3-18:

![](../../start-new-project/download-project.files/001.png)

Figura 3-18 Descarga del proyecto por Ethernet

También puede hacer clic en el botón «Escanear» para buscar direcciones IP

![](../../start-new-project/download-project.files/002.png)

Puede marcar la dirección IP encontrada y modificarla en el campo de modificación inferior

![](../../start-new-project/download-project.files/003.png)

Haga clic en el botón de la derecha para modificar la información de la pantalla; al terminar aparece una ventana emergente.

![](../../start-new-project/download-project.files/004.png)

Si hace clic en «Volver a escanear», verá el resultado modificado en la lista.

![](../../start-new-project/download-project.files/005.png)

Marque la dirección IP que desea usar y haga clic en «Seleccionar» para elegir la IP de destino; la información IP se sincroniza con la ventana de descarga.

**¡Atención!**

Para usar la búsqueda de IP deben cumplirse estos tres requisitos:

1. Las pantallas táctiles fabricadas antes del 30 de diciembre de 2024 necesitan instalar manualmente el parche de búsqueda IP; si no encuentra el archivo «hmi.patch» en el directorio de instalación, pídalo al personal técnico.
     2. La versión del software de configuración no debe ser inferior a HMITOOLV7.1_022
     3. La versión del firmware no debe ser inferior a Simulator 8.1.0.10.

![](../../start-new-project/download-project.files/006.png)
