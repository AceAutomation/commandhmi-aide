# Receta

En fabricación, una receta describe las proporciones de los materiales para un producto: un conjunto de valores de parámetros de producción. Por ejemplo, para hacer pan se necesita una receta básica con el peso o la proporción de todos los ingredientes: agua, harina, azúcar, huevos, aceite, etc. También puede incluir ingredientes opcionales, como fruta, frutos secos o chocolate, que se añaden a la receta básica para obtener distintos tipos de pan. Otro ejemplo: en una acería, una receta puede ser un conjunto de parámetros de máquina. En las máquinas de proceso por lotes, una receta puede describir las etapas del proceso.

Una máquina puede fabricar pan y pasteles, panes de distintos sabores y pasteles de distintas formas. Aquí llamamos «receta» a las proporciones de un pan y «archivo» al conjunto de proporciones de los distintos panes. Los registros de receta están contenidos, pues, en archivos de recetas.

CommandHMI ofrece la configuración de recetas desde el menú «Receta» o el gestor de proyecto: en el cuadro de diálogo de configuración se crea un nuevo grupo de recetas, como en la figura 7-32:

<img src="../../setting/formula.files/formula1334.png" width="515" />

Figura 7-32 Propiedades de una receta continua

• Nombre: nombre del archivo de recetas actual.

• Descripción: descripción del archivo de recetas actual;

• Longitud de receta: longitud y número de direcciones leídas por la receta actual. Las direcciones de la tabla de recetas las asigna automáticamente el sistema de forma consecutiva y no pueden cambiarse. Longitud máxima de receta: 4096.

• Número total: número de recetas, máximo 512;

• Grupo de recetas editable en el HMI: permite editar la receta en el HMI.

<img src="../../setting/formula.files/formula1872.png" width="794" />

Figura 7-33 Propiedades de una receta discreta

• Nombre del grupo: nombre del archivo de recetas actual.

• Descripción de la receta: descripción del archivo de recetas actual;

• Indicador de receta escrita: cuando la receta actual se ha escrito en el PLC, la dirección de bit indicada pasa a 1;

• Grupo de recetas editable en el HMI: permite editar la receta en el HMI.

<img src="../../setting/formula.files/formula2225.png" width="130" />

Nota: longitud de receta \* bytes del tipo de dato \* número total &lt;= 512 KB

• Tipo de dato: tipo de dato del registro de datos;

• Escribir receta en el PLC: dirección del registro de datos del PLC asociado;

• Leer receta del PLC: dirección del registro de datos del PLC asociado;

• Memoria de recetas: rango de direcciones de la receta en el HMI, generado automáticamente y no modificable;

• Receta actual: direcciones de memoria de la receta en el HMI y registros de datos del PLC, generados automáticamente en orden y no modificables;

• Registro del número de receta: las recetas se numeran automáticamente en orden, sin poder modificarse; el número corresponde al orden de los nombres de receta en los datos.

Datos de una receta continua, véase la figura 7-33:

<img src="../../setting/formula.files/formula2990.png" width="514" />

Figura 7-34 Página «Datos» de una receta continua

• Nombre: nombre de la receta actual;

• Datos: introducción y visualización de los valores de las direcciones de la receta actual;

• Copiar datos de receta: copia los datos de la receta de origen en la receta de destino. «Aceptar» guarda; «Cancelar» cierra el cuadro de diálogo. Una vez configuradas las recetas, se pueden diseñar las pantallas para manejarlas en el HMI.

Ejemplo de uso de recetas:

1\. Cree una configuración de recetas como se ha descrito. El resultado se muestra en la figura 7-34:

<img src="../../setting/formula.files/formula3531.png" width="515" />

Figura 7-35  Copia de datos de una receta continua

Esta receta tiene 4 subrecetas de 16 elementos cada una, guardadas de RWI: 1 a RWI: 16 en la memoria del HMI.

2. Tras configurar las recetas, pueden mostrarse en la pantalla, modificarse o descargarse directamente al PLC. Para ello se usan los objetos siguientes.

• Visualización de la receta: haga clic en «Entrada/visualización numérica» <img src="../../setting/formula.files/formula3946.png" width="23" /> (véase «Entrada/visualización numérica»)

Elija la dirección interna RWI: 0 para crear una entrada/visualización numérica en la pantalla. El valor introducido y mostrado es el número de receta: RWI0 = 0 corresponde a la receta n.º 1, RWI0 = 1 a la n.º 2, etc.

• Haga clic en el botón de función <img src="../../setting/formula.files/formula4264.png" width="21" />: para su uso, véase «Botón de función».

Con las funciones correspondientes se pueden crear botones para escribir la receta en el PLC, leerla del PLC, guardarla y elegir la receta anterior o siguiente.

Varios grupos de recetas: CommandHMI admite varios grupos de recetas, pero como máximo diez; si se supera, aparece un mensaje, como en 7-34-2

<img src="../../setting/formula.files/formula4682.png" width="248" />

Figura 7-35-1

<img src="../../setting/formula.files/formula4698.png" width="321" />

Figura 7-35-2

LW61141 sirve para introducir el grupo de recetas; RWI0 sigue sirviendo para el número de receta. Para elegir una receta hay que ajustar a la vez LW61141 y RWI0. Por ejemplo: grupo 0 en LW61141 y número 2 en RWI0 seleccionan los datos de la receta 2 del grupo 0.

3. Así puede crearse una pantalla como la de la figura 7-35:

Supongamos que la dirección de escritura y de monitorización es D0, la longitud de receta 16 y el número total 4.

<img src="../../setting/formula.files/formula5250.png" width="746" />

Figura 7-36 Resultado de la receta

Con botones de función y entradas/visualizaciones numéricas es fácil modificar, guardar, leer y escribir recetas. Hay que tener en cuenta lo siguiente:

• La lista de recetas debe crearse antes de usar las funciones de receta.

• Al introducir los parámetros de receta, cuidado con el tipo de dato: un dato de 16 bits ocupa una palabra y uno de 32 bits dos palabras. Elija un tipo coherente. Preste especial atención a las direcciones de 32 bits: como ocupan dos palabras, las direcciones de escritura y de monitorización no deben solaparse.

• La dirección RWI0 está reservada y solo sirve para cambiar el número de receta. RWI0 = 0 indica la primera receta, etc.

• Las direcciones de los parámetros de receta son consecutivas.

Datos de una receta discreta, véase la figura 7-33:

<img src="../../setting/formula.files/formula6181.png" width="795" />

Figura 7-41  Página «Datos» de una receta discreta

• Número de recetas: máximo 128;

• Idioma: los nombres de los elementos y de las recetas pueden definirse por idioma.

• Nombre de receta: cambia el nombre de la receta actual, p. ej. «receta1», «receta2».

• Nuevo: abre el cuadro de diálogo «Elemento de receta» para crear un elemento, como abajo.

  <img src="../../setting/formula.files/formula6495.png" width="517" />

Figura 7-42  Nuevo elemento de receta discreta

• Eliminar: elimina el elemento de receta actual.

• Eliminar todo: elimina todos los elementos de esta receta.

• Modificar: abre el cuadro «Elemento de receta» del elemento actual para editarlo.

• Exportar: abre un cuadro de guardado para guardar la receta como archivo \*.csv en la ruta y con el nombre elegidos.

• Importar: abre un cuadro de apertura para cargar un archivo \*.csv como receta actual.
