# Recopilador de datos históricos

El recopilador de datos históricos funciona junto con la [Visualización de datos históricos](../configuration-guide/extended-controls/history-record.md) de la barra de herramientas: el primero sirve para los ajustes y la segunda para mostrar los datos históricos.

Cree un recopilador haciendo clic derecho en «Recopilador de datos históricos» y eligiendo «Nuevo recopilador de datos históricos».

Nota: CommandHMI admite varios grupos de datos históricos; se pueden crear hasta cuatro recopiladores.

No se pueden crear más de cuatro grupos; si no, aparece este mensaje de error:

<img src="../../setting/history-data.files/image008.jpg" width="456" />

Haga doble clic en «Recopilador de datos históricos 0» en el gestor de proyecto para abrir el cuadro de diálogo de la figura 7-19:

<img src="../../setting/history-data.files/image009.jpg" width="627" />

Figura 7-19     Cuadro de diálogo Recopilador de datos históricos

• Nombre: nombre mostrado en el gestor de proyecto.

• Longitud de muestreo: número de datos leídos de la memoria en cada muestreo.

• Número total de muestras: número de lecturas.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Nota: memoria necesaria = (20 + bytes de todos los elementos de datos según su tipo) \* número total de muestras.

«20» son los bytes de la hora y la fecha;

«Bytes de todos los elementos» es la suma de los tamaños de los tipos de dato elegidos para cada elemento en la página «Elementos de datos».

Ejemplo, figura 7-20:

a, si todos los elementos son «entero positivo de 16 bits», los bytes de todos los elementos = 2 +2 +2 +2 +2; la memoria necesaria es (20 + 10) \* 2, es decir, 60; los datos de 16 bits ocupan 2 bytes y los de 32 bits 4 bytes.

b\. Si «LH1» y «LH3» son «entero positivo de 32 bits» (las direcciones de los «Elementos de datos» son entonces LH0, LH1, LH3, LH5, LH6), los bytes de todos los elementos = 2 + 4 + 4 + 2 + 2 = 14; la memoria necesaria = (20 + 14) \* 2 = 68.

Dirección de lectura: dirección inicial de los datos leídos (véase «Elementos de datos»)

Modo de muestreo:

• Periódico: lee los datos con el intervalo definido.

• Disparo: lee los datos cuando la dirección de disparo vale 1.

• Reloj: lee los datos a partir de la hora definida por el usuario, con el intervalo indicado.

Comportamiento con la memoria llena: qué ocurre al alcanzar el número máximo de muestras.

Detener el muestreo: detiene el muestreo con la memoria llena; sin esta opción, los datos nuevos sustituyen a los más antiguos.

Notificación: pone a 1 una dirección al alcanzar el número máximo de muestras.

Haga clic en la pestaña «Elementos de datos» y defina las propiedades, como en la figura 7-20:

<img src="../../setting/history-data.files/image002.jpg" width="627" />

Figura 7-20 Elementos de datos del recopilador de datos históricos

En un proyecto multilingüe, cada nuevo elemento de datos debe tener nombre en todos los idiomas; si no, no puede añadirse.

En CommandHMI, las direcciones de un grupo de datos históricos pueden no ser consecutivas, según los registros LW; por ejemplo: S1 = LW1, S2 = LW89, S3 = LW8905.

Haga clic en un elemento de la lista para definir sus propiedades.

Ejemplo detallado:

En la página «General», ponga la dirección de lectura LW1, con registros consecutivos y longitud de muestreo 5; en la página «Elementos de datos», añada 5 columnas (LH0-LH4). Defina para cada una el nombre, la dirección, el tipo de dato, el número total de cifras, los decimales y el escalado.

Supongamos que los nombres, tipos y escalados de LH0-LH4 son los de la figura 7-20 y las demás propiedades tienen sus valores por defecto:

LH0 - entero positivo de 16 bits, escalado con ganancia 3 y offset 2

LH1 - entero positivo de 32 bits, escalado con ganancia 2 y offset 1

LH2 - entero de 16 bits, sin escalado

LH3 - entero de 32 bits, sin escalado

LH4 - coma flotante, escalado con ganancia 4 y offset 5

Como la longitud de muestreo es 5 (página «General»), se leen 5 valores consecutivos a partir de la «Dirección de lectura», cada uno según el tipo de dato de su elemento.

Con datos de 16 bits, las direcciones leídas son consecutivas; con datos de 32 bits, van de dos en dos. Con escalado, el valor final es el valor leído multiplicado por la ganancia más el offset.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Nota: la ganancia del escalado debe ser mayor que 1.

Según el tipo de dato y el escalado, las direcciones leídas son:

LH0-LW1 (datos de 16 bits, dirección de lectura + 1) Valor final de LH0 = valor de LW1 × 3 + 2

LH1-LW2 (datos de 32 bits, dirección de lectura + 2) Valor final de LH1 = valor de LW2 × 2 + 1

LH2-LW4 (datos de 16 bits, dirección de lectura + 1) Valor final de LH2 = valor de LW4

LH3-LW5 (datos de 32 bits, dirección de lectura + 2) Valor final de LH3 = valor de LW5

LH4-LW7 (datos de 32 bits, dirección de lectura + 2) Valor final de LH4 = valor de LW7 × 4 + 5

Haga clic en «Aceptar». Haga clic en el icono «Visualización de datos históricos» de la barra de herramientas y ajuste 5 líneas en el cuadro de diálogo; las demás propiedades quedan por defecto.

Haga clic en «Aceptar»; se genera automáticamente una tabla en la pantalla, como en la figura 7-21:

Figura 7-21 Tabla de visualización de datos históricos

Significado de la tabla:

• Fecha: fecha de lectura del valor

• Hora: hora de lectura del valor

• «LH0»: valor de LW1 en un momento dado.

• «LH1»: valor de LW2 en un momento dado.

• «LH2»: valor de LW4 en un momento dado.

• «LH3»: valor de la dirección LW5 en un momento dado.

• «LH4»: valor de la dirección LW7 en un momento dado.

Ejemplo: dirección de lectura LW1, longitud de muestreo 3, número total de muestras 10, modo de muestreo por disparo, intervalo de 1 segundo, tipo de dato por defecto;

1). Opción «Detener el muestreo» no marcada:

Los valores de LW1, LW2 y LW3 se leen cada segundo. Como el número total es 10, a los 10 segundos se han leído 10 grupos de datos. Como «Detener el muestreo» no está marcado, el muestreo continúa. Una zona de memoria fija, que depende de la longitud de muestreo, del número total y del tipo de dato, almacena los datos; al alcanzar el «número total de muestras», el dato más reciente sustituye al más antiguo.

2). Opción «Detener el muestreo» marcada:

La única diferencia es que el muestreo se detiene al alcanzar el número total de muestras.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Con las «[Tendencias históricas](../configuration-guide/extended-controls/histrendgraphics.md)» o la «[Visualización de datos históricos](../configuration-guide/extended-controls/history-record.md)» los valores se leen de forma más intuitiva.
