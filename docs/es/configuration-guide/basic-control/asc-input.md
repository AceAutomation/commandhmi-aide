# Entrada ASCII

Haga clic en el icono de entrada ASCII<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input38.png" width="30" />; se abre el cuadro de diálogo de la figura 4-100:

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input93.png" width="665" />

Figura 4-100 Cuadro de diálogo Entrada ASCII

• Dirección de escritura: el texto ASCII se escribe en esta dirección.

• Monitorizar: valor de dirección que el objeto lee y muestra.

• Dirección de monitorización igual a la de escritura: la dirección de monitorización es la misma que la de escritura.

• Dirección de monitorización: dirección leída

• Total: número máximo de caracteres que se pueden mostrar.

• Tamaño de fuente: tamaño de los caracteres mostrados

• Intercambiar bytes alto y bajo de la entrada: en el valor introducido por el usuario se intercambian el byte alto y el bajo, y el resultado se guarda en la dirección de palabra monitorizada.

• Contraseña: si se marca, el objeto no muestra los caracteres sino asteriscos (\*)

• Usar UNICODE: el valor de la dirección de monitorización se muestra en codificación Unicode

Alineación:

• Izquierda: los caracteres se muestran en la parte izquierda de la zona de visualización.

• Centro: los caracteres se muestran en el centro de la zona de visualización.

• Derecha: los caracteres se muestran en la parte derecha de la zona de visualización.

• Usar script: marque «Usar script» para ver la lista de scripts. El usuario elige uno que se ejecuta al pulsar el botón. La lista solo muestra los scripts compilados.

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input1310.png" width="130" />

Nota: por ejemplo, con el tipo de dato de 32 bits la dirección ocupa 2 palabras. Si se escribe en el registro de datos V10 de un PLC SIEMENS, se ocupan V10 y V11; si otro objeto monitoriza también V11, se produce un error. Tenga cuidado con los tipos de 32 bits para evitar errores de datos y direcciones.

Nota: las demás funciones de la página «General» son iguales a las de la Visualización ASCII.

Nota: para las páginas «Avanzado» y «Visibilidad», véase el Botón de bit.
