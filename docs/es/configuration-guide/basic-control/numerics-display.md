# Visualización numérica

La visualización numérica es un objeto muy usado que muestra valores de los registros de datos del PLC u otros equipos conectados, como velocidad, corriente, presión, etc.

Elija el icono de visualización<img src="../../../configuration-guide/basic-control/numerics-display.files/image002.jpg" width="30" /> en la barra de herramientas; se abre un cuadro de diálogo, como en la figura 4-91:

Figura 4-91 Cuadro de diálogo Visualización numérica

En este cuadro se configura la visualización del valor del registro de datos del PLC u otro equipo: número de cifras, decimales, tamaño de fuente, color, alineación y ajuste del texto.

• Tipo de dato: el usuario elige el tipo de dato según el valor de la dirección monitorizada.

• Tipo de visualización: el usuario elige el tipo de visualización según las necesidades del proyecto.

• Dirección de monitorización: dirección de lectura. Es la dirección del registro de datos del PLC u otro equipo que contiene el dato a mostrar.

• Decimales: número de decimales mostrados.

• Fuente: fuente normal o fuente digital.

• Tamaño de fuente: tamaño de la fuente mostrada.

• Alineación: por defecto, centrada.

• Izquierda: el valor se muestra en la parte izquierda de la zona de visualización.

• Centro: el valor se muestra en el centro de la zona de visualización.

• Derecha: el valor se muestra en la parte derecha de la zona de visualización.

• Relleno: por defecto, supresión de ceros.

• Supresión de ceros: se ocultan los ceros a la izquierda de las cifras significativas. <span id="OLE_LINK668"></span><span id="OLE_LINK669"></span>Si la dirección de monitorización vale 00123 (entero positivo de 16 bits), se muestra 123.

• Ceros a la izquierda: se muestran los ceros a la izquierda. Si la dirección de monitorización vale 00123 (entero positivo de 16 bits), se muestra 00123.

• Espacios a la izquierda: se muestran espacios en lugar de ceros a la izquierda. Si la dirección de monitorización vale 00123 (entero positivo de 16 bits), se muestra   123.

• Color del texto: color de la fuente de los datos mostrados;

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Nota: para forma, color del borde, color de primer plano, color de fondo y estilo, véase el objeto «Botón de bit».

Nota: <span id="OLE_LINK678"></span><span id="OLE_LINK679"></span>haga doble clic en el campo de visualización para modificar su contenido y sus propiedades. Cuando el objeto funciona en el HMI aparece un teclado en pantalla para que el usuario introduzca datos.

Nota: <span id="OLE_LINK684"></span><span id="OLE_LINK685"></span>el número de decimales influye en la visualización. Con los tipos entero positivo o entero de 16/32 bits, el valor mostrado se obtiene desplazando la coma del valor devuelto el número de cifras indicado. Si se devuelve 212 con 2 decimales, se muestra 2.12. Con el tipo coma flotante de 32 bits, el valor no se desplaza; solo se muestran los decimales indicados. Si se devuelve 2.123 con 2 decimales, se muestra 2.12.

Nota: el número total de cifras es la suma de la parte entera y la decimal. Si la parte entera del valor es más larga que la definida, se muestra con su longitud real. Por ejemplo, para el valor 2123 con longitud 2 y 1 decimal, se muestra 212.3.

La página «Avanzado» de la visualización numérica ofrece funciones potentes, como el escalado y la visualización por rangos, como en la figura 4-92:

<img src="../../../configuration-guide/basic-control/numerics-display.files/image005.jpg" width="675" />

Figura 4-92    Página «Avanzado» de la visualización numérica

• Escalado: si se marca, el valor mostrado es: valor de la dirección de monitorización (lectura) × ganancia + offset

<span id="OLE_LINK696"></span><span id="OLE_LINK697"></span>• Mostrar rango: si se marca, el usuario define los límites inferior y superior y los colores de fondo bajo y alto. El valor monitorizado (leído) se representa con colores distintos según esos límites.

• Rango variable: los valores «Límite inferior» y «Límite superior» cambian dinámicamente según la dirección indicada por el usuario

• Límite inferior: límite inferior de visualización. Si el valor es menor, el fondo toma el color definido en «Color de fondo nivel bajo».

• Límite superior: límite superior de visualización. Si el valor es mayor, el fondo toma el color definido en «Color de fondo nivel alto».

Por ejemplo, si define el color de fondo y del texto en la página «General» y los colores de rango como en la figura 4-93:

<img src="../../../configuration-guide/basic-control/numerics-display.files/image006.jpg" width="673" />

<img src="../../../configuration-guide/basic-control/numerics-display.files/image007.jpg" width="349" />

Figura 4-93 Ajustes de la visualización por rangos

Cuando cambia el valor de la dirección monitorizada, el texto y el fondo de la visualización numérica cambian en consecuencia, como en la figura 4-94:

<img src="../../../configuration-guide/basic-control/samdra93.gif" width="508" />

Figura 4-94    Ejemplo de visualización numérica

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Nota: para la página «Visibilidad», véase el objeto «Botón de bit».

Nota: <span id="OLE_LINK682"></span><span id="OLE_LINK683"></span>con un tipo de dato de 32 bits, la dirección ocupa 2 palabras. Por ejemplo, si se escribe en el registro de datos V10 de un PLC SIEMENS, se ocupan V10 y V11; si otro objeto monitoriza también V11, se produce un error. Tenga cuidado con los tipos de 32 bits para evitar errores de datos y direcciones.

Tras los ajustes, haga clic en «Aceptar» para añadir el objeto a la zona de trabajo (la pantalla)
