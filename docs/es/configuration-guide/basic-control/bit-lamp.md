# Lámpara de bit

La lámpara de bit monitoriza el estado ON/OFF de un contacto de bit del equipo conectado y lo muestra en la pantalla del HMI.

Como en la figura 4-78:

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image007.jpg" width="554" alt="2018_11_20_14_25_09.jpg" />

Figura 4-78

Configurar una lámpara de bit:

1\. Elija el icono de lámpara de bit<img src="../../../configuration-guide/basic-control/bit-lamp.files/image002.jpg" width="31" /> en la barra de herramientas: se abre el cuadro de diálogo de la figura 4-79:

Figura 4-79    Cuadro de diálogo Lámpara de bit

• Tipo de dato: la lista ofrece tres opciones: Bit, Bit de palabra y Bit de doble palabra. Con «Bit», la dirección de monitorización (lectura) es una dirección de bit; con «Bit de doble palabra», una dirección de doble palabra.

• Número de bit: con el tipo «Bit de palabra» o «Bit de doble palabra», el estado ON/OFF de la dirección de monitorización depende del número de bit: de 0 a 15 para Bit de palabra y de 0 a 31 para Bit de doble palabra.

Por ejemplo, con «Bit de palabra», dirección de monitorización LW1 de valor 23 y número de bit 3, el estado es 0, porque 23 en binario es 10111 y su cuarta cifra empezando por la derecha (bit 3) es 0.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Nota: <span id="OLE_LINK707"></span><span id="OLE_LINK706"></span>para forma, color del borde, color de primer plano, color de fondo y trama, véase el objeto Botón de bit.

2\. En la página «General» de la lámpara de bit, elija la dirección monitorizada. En «Etiqueta» se definen el texto y las imágenes mostrados y si la lámpara parpadea.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Nota: la página «Etiqueta» de la «Lámpara de bit» es igual a la del «Botón de bit».

3\. Para cambiar las propiedades de la lámpara, haga doble clic en ella y modifíquelas en el cuadro de diálogo.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Nota: la página «Visibilidad» de la lámpara de bit es igual a la del Botón de bit.

Tras los ajustes, haga clic en «Aceptar» para añadir el objeto a la zona de trabajo (la pantalla)
