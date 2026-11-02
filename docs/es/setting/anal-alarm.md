# Alarmas analógicas

Abra el cuadro de diálogo de alarmas analógicas, como en la figura 7-28:

Hay dos tipos: valor numérico y comparación numérica.

<img src="../../setting/anal-alarm.files/image002.jpg" width="145" />

Alarma por comparación numérica:

<img src="../../setting/anal-alarm.files/image007.jpg" width="599" />

Figura 7-28    Cuadro de diálogo Alarmas analógicas

Para usar las alarmas analógicas:

• Introduzca primero la dirección a vigilar en la columna «Dirección de lectura» (Read Address). Aquí se supone la dirección interna LW1.

• En «Tamaño» (Size), elija el número total de alarmas, es decir, de direcciones; el tipo de dato determina cómo se leen. Por defecto cada dirección es de 16 bits y son consecutivas, pero el tipo de dato puede cambiarse. En la figura 7-28, LW1 es un entero positivo de 32 bits y LW3 y LW4 enteros positivos de 16 bits. Así, con datos de 32 bits la dirección siguiente es la anterior más 2, y con datos de 16 bits, la anterior más 1.

• Se puede ajustar el «Tiempo de exploración» (Scanning time) de la alarma, es decir, su frecuencia de lectura.

• Haga clic en cada elemento para introducir un valor en el campo «Límite» de la derecha y después el texto de la alarma en el campo «Texto». Aquí se suponen los mensajes de la figura 7-28: cada valor entra en uno de cuatro rangos: Bajo, Muy bajo, Alto, Muy alto.

Como en la figura 7-29:

<img src="../../setting/anal-alarm.files/image004.jpg" width="566" />

Figura 7-29    Los cuatro rangos de valores de la dirección LW1

• Muy bajo: si el valor es menor que el límite definido y «Usar» está marcado, la alarma se muestra en la visualización de alarmas o en la barra de alarmas dinámica;

• Bajo: si el valor es mayor o igual que el límite «Muy bajo» y menor que el límite «Bajo», y «Usar» está marcado, la alarma se muestra en la visualización de alarmas o en la barra de alarmas dinámica;

• Alto: si el valor es mayor que el límite «Alto» y menor o igual que el límite «Muy alto», y «Usar» está marcado, la alarma se muestra en la visualización de alarmas o en la barra de alarmas dinámica.

• Muy alto: si el valor es mayor que el límite definido y «Usar» está marcado, la alarma se muestra en la visualización de alarmas o en la barra de alarmas dinámica.

• Exportar U: exporta los ajustes de alarmas

• Importar U: importa los ajustes de alarmas

Para la opción «Usar», véase «Alarmas digitales».

En la alarma por valor numérico, la alarma se dispara cuando el valor alcanza el límite definido.

Ajustes siguientes: la alarma se dispara cuando el valor llega a 1, 12, 30 y 40.

<img src="../../setting/anal-alarm.files/image006.jpg" width="130" />

Nota: los HMI de la serie HM admiten como máximo 10 alarmas analógicas.
