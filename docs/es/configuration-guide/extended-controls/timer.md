# Timer

El temporizador es un objeto cuya función se activa por tiempo. En el software CommandHMI, el temporizador sirve para disparar scripts. Haga clic en <img src="../../../configuration-guide/extended-controls/timer.files/timer152.png" width="35" /> en la barra de herramientas o haga doble clic en un temporizador existente para abrir su configuración:

<img src="../../../configuration-guide/extended-controls/timer.files/timer240.png" width="662" />

**Control**

• Modo de ejecución: «Ejecutar siempre» o «Disparo por dirección».

1\. «Ejecutar siempre»: el script se ejecuta siempre con la frecuencia definida por el usuario.

2\. «Disparo por dirección»: el script se ejecuta con la frecuencia definida cuando el bit indicado vale 1, y no se ejecuta cuando vale 0.

• Dirección: en modo «Disparo por dirección» aparece el campo para la dirección de bit que controla la ejecución del script. Con el valor 1, el script se ejecuta.

• Frecuencia: frecuencia de ejecución del script, de 0.1 a 60 s.

• Número de ejecuciones: número de veces que se ejecuta el script. Con 0 se ejecuta indefinidamente.

**Función**

• Tipo de función: tipo de función a ejecutar. En el software CommandHMI la función del temporizador es un script.

• Nombre: nombre del script a ejecutar. El temporizador no puede configurarse si no existe ningún script.

<img src="../../../configuration-guide/extended-controls/timer.files/timer1240.png" width="130" />

El tamaño del temporizador no puede cambiarse, pero su posición sí. Con el proyecto en marcha, el temporizador no se muestra en el HMI.
