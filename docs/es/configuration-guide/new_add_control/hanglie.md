# Tabla de datos

Este elemento muestra en forma de cuadrícula los datos definidos por el usuario y ofrece una interfaz sencilla para seleccionarlos y manipularlos. Sus funciones incluyen cambio automático de página, insertar, eliminar, copiar y pegar.

Página «General»

![](../../../configuration-guide/new_add_control/hanglie.files/001.png)

Ajustes de datos

Total de campos: número de columnas de la tabla

Número inicial de elementos: número inicial de filas de la tabla

Elementos por página: número de filas mostradas por página

Dirección inicial: dirección del primer elemento de la tabla

Offset de dirección: offset de dirección de cada fila de la columna

Vista previa de direcciones

Muestra la distribución de direcciones de la tabla

Ajustes de campo

Campo actual: columna actual

Tipo de campo: estado, cadena o numérico

Anchura del campo: anchura de la columna

Alineación: alineación de los elementos de la columna

Número total de estados: número total de estados del elemento de la columna

Avanzado

![](../../../configuration-guide/new_add_control/hanglie.files/002.png)

Estado

Elemento seleccionado: elemento seleccionado

Número real de elementos: número real de elementos

Total de elementos visibles: número total de elementos visibles

Página actual: número de la página actual

Total de páginas: número total de páginas

Actualizar automáticamente los datos de la página actual: sí: actualización automática; si no, la controla la dirección definida

Actualizar datos: dirección de actualización

Operación

Bit de invisibilidad: hace invisibles los datos

Nivel de invisibilidad: condición para que el bit de invisibilidad surta efecto

Dirección de disparo de página anterior: pasa a la página anterior

Dirección de disparo de página siguiente: pasa a la página siguiente

Dirección de disparo del elemento anterior: selecciona el elemento anterior de la columna

Dirección de disparo del elemento siguiente: selecciona el elemento siguiente de la columna

Dirección de disparo de copia: copia el elemento actual

Dirección de disparo de pegado: pega los datos

Dirección de disparo de sustitución: sobrescribe el elemento actual con los datos pegados

Dirección de disparo de inserción: inserta un elemento en el elemento actual

Dirección de disparo de corte: corta los datos

Bit de protección táctil: protección táctil

Dirección para seleccionar un elemento: indica el elemento a seleccionar

Disparo de la selección: aplica la selección indicada

Dirección del número total de elementos: define el número total de elementos

Disparo del número total de elementos: aplica el número total de elementos definido

Avanzado 2

La zona de almacenamiento temporal es un búfer donde el elemento puede guardar datos temporalmente. Los datos del búfer pueden insertarse, añadirse y escribirse en el elemento seleccionado, y los datos del elemento seleccionado pueden leerse al búfer.

![](../../../configuration-guide/new_add_control/hanglie.files/003.png)

Zona de almacenamiento temporal

Dirección inicial: dirección inicial de la zona de almacenamiento temporal

Bit «insertar elemento seleccionado»: en ON, los datos del búfer (dirección: inicio del búfer + offset de dirección del elemento) se insertan en el elemento seleccionado y el número real de elementos aumenta en 1. Si ya se ha alcanzado el máximo, no se puede insertar.

Bit «añadir elemento seleccionado»: en ON, los datos del búfer (dirección: inicio del búfer + offset de dirección del elemento) se añaden al elemento seleccionado y el número real de elementos aumenta en 1. Si ya se ha alcanzado el máximo, no se puede insertar.

Añadir al final: en ON, los datos del búfer (dirección: inicio del búfer + offset de dirección del elemento) se añaden al final y el número real de elementos aumenta en 1. Si ya se ha alcanzado el máximo, no se puede insertar.

Leer elemento seleccionado: en ON, el contenido del elemento seleccionado se lee al búfer (dirección: inicio del búfer + offset de dirección del elemento)

Escribir elemento seleccionado: en ON, los datos del búfer (dirección: inicio del búfer + offset de dirección del elemento) se escriben en el elemento seleccionado

Aspecto

![](../../../configuration-guide/new_add_control/hanglie.files/004.png)

Ajustes de campo

Número de formulario, etc.

Estilo

Líneas de cuadrícula, color de fondo, color de fondo del elemento seleccionado, etc.
