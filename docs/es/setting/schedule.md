# Programación horaria

La programación horaria permite planificar eventos. Por ejemplo, una fábrica arranca las máquinas los días laborables a las 8:00 y las para a las 18:00.

Haga clic en «Programación horaria» en la lista estándar; se abre el cuadro de diálogo de programación, como abajo.

<img src="../../setting/schedule.files/schedule706.png" width="728" />

 Figura 7-49 Cuadro de diálogo Programación horaria

Haga clic en «Nuevo»; se abre un nuevo cuadro de diálogo, como abajo. Primero se muestra la página «General».

<img src="../../setting/schedule.files/schedule984.png" width="694" />

  Figura 7-50 Cuadro de diálogo Nueva programación

• Descripción:

Introduzca aquí un texto que explique la función de esta programación.

• Ejecutar la acción de inicio/fin al encender:

Si el HMI se enciende después de la hora de inicio, se ejecuta la acción de inicio/fin.

• Dirección de destino:

Introduzca el tipo y la dirección de destino; el valor se escribe en esta dirección a la hora de inicio/fin.

• Operación de escritura:

Tipos: «Constante» y «Dirección». Con «Constante» se escribe el valor indicado en la dirección de destino. Con «Dirección», a la hora de inicio/fin se escribe en la dirección de destino el valor de la dirección indicada.

• Usar la acción de fin:

Si se marca, el valor de la operación de escritura se escribe en la dirección de destino a la hora de fin.

 Tras la página «General», haga clic en la página «Periodo», como abajo.

<img src="../../setting/schedule.files/schedule2016.png" width="694" />

  Figura 7-51 Página «Periodo»

• Constante: marque las horas de inicio/fin; a esas horas se ejecuta la escritura correspondiente.

• Dirección: las horas de inicio y fin se controlan mediante un rango de direcciones, como abajo.

 <img src="../../setting/schedule.files/schedule2396.png" width="693" />

 Figura 7-52 Control por direcciones

Por ejemplo, si la dirección es LW0, LW0~LW10 son las direcciones de la programación.

LW0: dirección de control. Con LW0 == 1 se cargan las horas en el HMI y la programación empieza a funcionar. Tras la carga, LW0 vuelve a 0;

LW1: estado de la programación. Tras cargar las horas (LW0 == 0), LW1 pasa a 1.

LW2: modo de acción. Si LW2 = 1 y la hora actual es posterior a la de inicio, se ejecuta la escritura. Si LW2 = 0, la acción de inicio/fin se ejecuta cuando la hora actual coincide con la hora de inicio/fin.

LW3: día de la semana de la hora de inicio; valor = 2^(número del día), LW3 = (0,1,4,8,16,32,64)

LW4~LW6: horas, minutos y segundos de la hora de inicio.

LW7: día de la semana de la hora de fin; valor = 2^(número del día), LW3 = (0,1,4,8,16,32,64)

LW8~LW10: horas, minutos y segundos de la hora de fin.

Del mismo modo, si la dirección de control es LWn, LWn~LWn+10 son las direcciones de la programación.

**Consejo:** con «Dirección» marcada, no olvide poner a 1 la dirección de control tras definir las horas de inicio/fin para cargar la programación. Si no, la programación no funciona.

Página «Bloqueo», como abajo:

<img src="../../setting/schedule.files/schedule3691.png" width="694" />

 Figura 7-53 Página «Bloqueo»

Si se marca «Usar bloqueo», la programación solo funciona cuando la dirección de bit cumple la condición (0 o 1).

Tras ajustar los parámetros, haga clic en «Aceptar»; se crea un elemento de programación, como abajo.

<img src="../../setting/schedule.files/schedule4054.png" width="732" />

  Figura 7-50 Programación creada
