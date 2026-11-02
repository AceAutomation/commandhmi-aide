# Cámara

El objeto cámara permite grabar vídeo o capturar imágenes de una cámara externa; la página del objeto es la siguiente:

![](../../../configuration-guide/new_add_control/camera.files/001.png)

USB: una cámara conectada por USB requiere un sistema HMI Linux 4.9.84 (001) o superior;

Cámara de red: el formato del flujo de entrada es RTSP; por ejemplo, el formato de flujo de una cámara Hikvision es:

admin:xl123456@192.168.1.63:554/ch1/sub/av_stream;

Estructura del flujo: nombre de cuenta: contraseña@dirección IP: los cuatro primeros elementos los define el usuario según los parámetros de la cámara; el resto lo fija la marca de la cámara.

¡Consejo!

Tanto con cámara USB como de red, si la resolución es demasiado alta, la reproducción en la pantalla táctil sufre retardos o saltos; hay que reducir la resolución, la frecuencia de imagen, etc. Las cámaras USB admiten flujo de vídeo MJPEG y las de red deben admitir flujo H.264. Las cámaras Hikvision se han probado y verificado; para otras marcas, compruébelo con pruebas reales.

Captura de imagen: al activar la captura por dirección, se crea en la memoria USB una carpeta «video» donde se guardan los vídeos o imágenes capturados.

Formato de grabación: con formato de vídeo, la duración máxima de grabación es de 60 s. La cámara de red guarda el vídeo en MP4 y la cámara USB en AVI.

Imagen: con formato de imagen, el archivo se guarda en JPG.

\[Iniciar/detener importación\]: con 1 se activa la cámara conectada y se importa el flujo de vídeo; con 0 se apaga la cámara y se cierra el flujo. \[Control de pausa\]: pausa la visualización de la cámara; el vídeo sigue transmitiéndose. Al configurar la dirección de control solo hay que indicar la dirección de inicio/fin; la dirección de pausa es la de inicio más 1.

Por ejemplo, si la dirección de inicio/importación es LW N, la dirección de pausa es LW N+1.

Para la página de visualización, véase el botón «Interruptor de posición».
