# Botón de palabra

El botón de palabra permite las operaciones Constante, Introducir valor, Incrementar, Decrementar, Introducir contraseña, Sumar y Restar sobre una dirección de registro de datos del equipo conectado.

Para añadir un botón de palabra:

• Elija el icono de botón de palabra<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton222.png" width="29" /> en la barra de herramientas; se abre el cuadro de diálogo de la figura 4-76:

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton308.png" width="664" />

Figura 4-76 Cuadro de diálogo Botón de palabra

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton345.png" width="130" />

Para forma, color del borde, color de primer plano, color de fondo y trama, véase el objeto «Botón de bit».

**Función:**

• Constante: CommandHMI ofrece varios tipos de dato: entero positivo de 16/32 bits, entero de 16/32 bits, entero positivo BCD de 16/32 bits y coma flotante de 32 bits. La constante definida se escribe en la dirección de escritura. Por ejemplo, con la dirección LW1 y la constante 10, cada toque del botón pone LW1 a 10, sea cual sea su valor actual.

• Introducir valor: se elige el tipo de dato; al tocar el botón de palabra aparece un teclado para introducir un valor entre el mínimo y el máximo. Como en la figura 4-77:

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton1128.png" width="693" />

Figura 4-77

• Incrementar: si el retardo es 0, funciona como «Sumar». Si no es 0, el valor de la dirección de escritura aumenta en la constante y se escribe en el registro.

• Decrementar: si el retardo es 0, funciona como «Restar». Si no es 0, transcurrido el tiempo el valor de la dirección disminuye en la constante y se escribe en el registro.

• Introducir contraseña: igual que «Introducir valor», pero sin opción de decimales.

• Sumar: tras definir el tipo de dato, la dirección de escritura, la constante y el máximo, cada toque del botón de palabra suma la constante al valor actual del registro, sin superar el máximo definido. Por ejemplo, con la dirección LW1, la constante 5 y el máximo 65535, cada clic suma 5 a LW1, que nunca supera 65535.

• Restar: tras definir el tipo de dato, la dirección de escritura, la constante y el mínimo, cada toque del botón de palabra resta la constante al valor actual del registro, sin bajar del mínimo definido. Por ejemplo, con la dirección LW1, la constante 5 y el mínimo 0, cada clic resta 5 a LW1, que nunca baja de 0.

• Número total de cifras: número de cifras del dato, incluidos los decimales.

• Decimales: si el tipo de dato no es «coma flotante de 32 bits» y hay decimales, el valor máximo introducible se divide por 10 elevado a n. Por ejemplo: con «entero positivo de 32 bits» y 3 decimales, el usuario solo puede introducir de 0 a 99999.999.

• Script: marque «Usar script» para ver la lista de scripts. El usuario elige uno que se ejecuta al pulsar el botón de palabra. La lista solo muestra los scripts compilados.

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton3632.png" width="130" />

La página «Etiqueta» del botón de palabra es similar a la del objeto «Botón de bit», salvo que no tiene Texto estado 1 ni Imagen estado 1, porque el botón de palabra solo tiene un estado.

Con un tipo de dato de 32 bits, la dirección del botón de palabra ocupa dos palabras. Por ejemplo, si se escribe en V10 de un PLC SIEMENS, se ocupan V10 y V11. Si otro objeto monitoriza V11, no funcionará correctamente. Tenga cuidado con los tipos de 32 bits.

Las páginas «Avanzado» y «Visibilidad» del botón de palabra son iguales a las del objeto Botón de bit; para las teclas de acceso rápido, véase el Botón de bit.
