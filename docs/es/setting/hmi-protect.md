# Protección del HMI

La protección del HMI define un periodo durante el que el HMI funciona normalmente. Transcurrido ese periodo, el HMI pasa a una pantalla concreta en la que hay que introducir una contraseña para seguir usándolo.

Haga doble clic en «Protección del HMI» en el gestor de proyecto para abrir el cuadro de diálogo de la figura 7-14:

<img src="../../setting/hmi-protect.files/hmi-protect343.png" width="622" />

Figura 7-14    Cuadro de diálogo Protección del HMI

Ejemplo de uso de esta función:

➢Marque «Contraseña de apertura»: la próxima vez hará falta una contraseña para abrir la protección del HMI.

➢Marque «Desbloquear todos los niveles»: si se introduce esta contraseña al desbloquear, se eliminan todos los niveles de protección del HMI.

➢Marque «Protección del HMI»: se abre automáticamente la página «Ajustes de protección», como abajo:

<img src="../../setting/hmi-protect.files/hmi-protect743.png" width="623" />

Figura 7-15    Ajustes de la protección del HMI

Ajuste el «Número total de niveles de contraseña» a 3; elija el botón 1 y después 2009-04-01 y 12-00-00 en la columna «Plazo» de «Parámetros»; elija la pantalla 1 como «Pantalla de aviso»; ajuste la «Contraseña de desbloqueo» a 1111. La protección de nivel 1 queda configurada.

Del mismo modo, defina los plazos y contraseñas de los niveles 2 y 3.

• Eliminar todos los niveles

Si esta función está activada y la contraseña definida, esa contraseña elimina todos los niveles de la protección del HMI

•  Contraseña de apertura

Si esta función está activada y la contraseña definida, habrá que introducirla la próxima vez para abrir la protección del HMI y ver su información

•  Activar la protección por contraseña

Activa la protección del HMI. Los detalles se definen en «Ajustes de protección».

• Ajustes de protección

Número total de niveles de contraseña: hasta 15 niveles de protección del HMI para distintos periodos

Nivel de contraseña actual: los parámetros siguientes se aplican al nivel actual

Parámetros:

Plazo de uso: fecha de caducidad de la protección del HMI

Pantalla de aviso de caducidad: pantalla mostrada al caducar la protección del HMI

Contraseña de desbloqueo: contraseña que elimina la protección del HMI tras su caducidad

Ajustes avanzados:

Ver los días restantes: muestra los días que quedan hasta el final del plazo de protección

Aviso previo:

Número de días antes del final del plazo de protección a partir del cual se avisa

Retardo:

Tras el final del plazo de protección, durante el número de días indicado, se muestra la pantalla indicada con el intervalo definido

Prioridad entre aviso previo y retardo

Aviso previo marcado, retardo marcado: se aplica el aviso previo

Aviso previo no marcado, retardo marcado: se aplica el retardo

Aviso previo marcado, retardo marcado, función «Desbloqueo diferido de la protección del HMI» del botón de función no usada: se aplica el aviso previo

Aviso previo marcado, retardo marcado, función «Desbloqueo diferido de la protección del HMI» del botón de función usada: se aplica el retardo

•  Ejemplo de uso:

Supongamos que el número total de niveles de contraseña es 3. Elija 0 en «Nivel de contraseña actual». En «Parámetros», elija la fecha de caducidad en la columna «Plazo de uso», por ejemplo 2009/04/01. Introduzca la hora en la columna siguiente, por ejemplo 12:00:00. En «Pantalla de aviso de caducidad», elija la pantalla, por ejemplo la pantalla 1. En «Contraseña de desbloqueo», introduzca la contraseña, por ejemplo 1111. La protección del HMI de nivel 1 queda configurada.

Después elija 1 en «Nivel de contraseña actual». En «Parámetros», elija la fecha en la columna «Plazo de uso», por ejemplo 2009-04-05. Introduzca la hora en la columna siguiente, por ejemplo 12-00-00. En «Pantalla de aviso de caducidad», elija la pantalla, por ejemplo la pantalla 2. En «Contraseña de desbloqueo», introduzca la contraseña, por ejemplo 2222. La protección del HMI de nivel 2 queda configurada.

Después elija 2 en «Nivel de contraseña actual». En «Parámetros», elija la fecha en la columna «Plazo de uso», por ejemplo 2009-04-10. Introduzca la hora en la columna siguiente, por ejemplo 12-00-00. En «Pantalla de aviso de caducidad», elija la pantalla, por ejemplo la pantalla 3. En «Contraseña de desbloqueo», introduzca la contraseña, por ejemplo 3333. La protección del HMI de nivel 3 queda configurada.

Ajustes de la protección del HMI tras hacer clic en «Aceptar».

Supongamos que hoy es 2009-04-01 a las 08-00-00. El plazo de la protección de nivel 1 termina el 2009-04-01 a las 12-00-00; como aún no ha llegado, el HMI funciona normalmente. Cuatro horas después, el 2009-04-01 a las 12-00-00, el HMI pasa automáticamente a la pantalla definida para ese periodo. Para seguir usando el HMI y manejar las demás pantallas, añada en esa pantalla (pantalla 1) un botón de función con la función «Desbloquear la protección del HMI». Al caducar el nivel 1, pulse ese botón e introduzca en la ventana la contraseña de desbloqueo del nivel 1, aquí 1111; la protección queda eliminada.

Tras desbloquear el nivel 1, el HMI funciona normalmente. Más tarde, el 2009-04-05 a las 12-00-00, llega el plazo del nivel 2: el HMI pasa automáticamente a la pantalla de protección definida (pantalla 2). Igualmente, el usuario debe usar el botón de función «Desbloquear la protección del HMI» e introducir la contraseña del nivel 2 (2222); después el HMI funciona normalmente.

Como también se ha definido el nivel 3, el 2009-04-10 a las 12-00-00 el usuario debe usar igualmente el botón de función «Desbloquear la protección del HMI» e introducir la contraseña del nivel 3 (3333); después el HMI funciona normalmente.

Una vez desbloqueados los 3 niveles, la protección del HMI queda eliminada y el HMI funciona normalmente.

Los ejemplos anteriores muestran el uso de la protección del HMI. Para otros niveles de contraseña el procedimiento es el mismo.
