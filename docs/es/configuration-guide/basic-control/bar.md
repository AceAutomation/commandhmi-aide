# Gráfico de barras

El gráfico de barras representa en tiempo real la evolución de valores numéricos en forma de barras, para que el usuario la vea de forma más visual. Puede mostrar la evolución de los registros de datos del PLC u otros equipos conectados, así como de todas las magnitudes analógicas del proceso. Véase la figura siguiente.

<img src="../../../configuration-guide/basic-control/bar.files/image006.jpg" width="535" alt="2018_11_20_14_27_19.jpg" />

Figura 4-101   Gráfico de barras

Para añadir un gráfico de barras y modificar sus propiedades:

1\. Elija el icono de gráfico de barras <img src="../../../configuration-guide/basic-control/samdra8.gif" width="20" /> en la barra de herramientas o en el menú «Herramientas». Se abre el cuadro de diálogo de la figura 4-102.

2\. Defina las propiedades del gráfico de barras en el cuadro de diálogo y haga clic en «Aceptar»:

• Color de fondo: color de fondo del gráfico de barras

• Color del borde: color del borde de la barra. En la figura 4-102 el color del borde no tiene efecto; elija otra «forma» de barra para ver el cambio.

• Transparente: fondo de la barra transparente

• Dirección: sentido de llenado de la barra, en cuatro direcciones: hacia arriba, hacia abajo, hacia la izquierda y hacia la derecha.

• Hacia arriba: al aumentar el valor de la dirección de monitorización, la barra se llena de abajo arriba

• Hacia abajo: al aumentar el valor de la dirección de monitorización, la barra se llena de arriba abajo

• Hacia la izquierda: al aumentar el valor de la dirección de monitorización, la barra se llena de derecha a izquierda

• Hacia la derecha: al aumentar el valor de la dirección de monitorización, la barra se llena de izquierda a derecha

• Tipo de dato: tipo del valor leído, es decir, dirección de palabra o de doble palabra.

• Dirección de monitorización: dirección del registro de datos mostrado en la barra, es decir, la dirección de lectura

• Máximo: valor máximo de la dirección de monitorización (lectura). Si el valor es mayor, la barra está llena y ya no cambia

• Mínimo: valor mínimo de la dirección de monitorización (lectura). Si el valor es menor, la barra está vacía y ya no cambia

• Rango variable: los valores máximo y mínimo cambian dinámicamente según la dirección indicada por el usuario; el tipo de dato de la dirección es el «Tipo de dato» configurado

• Barra bipolar: la barra puede mostrarse a ambos lados según el valor del registro de datos.

• Punto medio: punto medio de la barra bipolar.

<img src="../../../configuration-guide/basic-control/bar.files/image002.jpg" width="675" />

Figura 4-102   Cuadro de diálogo Gráfico de barras

Por ejemplo, con un máximo de 100, un mínimo de 10 y llenado hacia arriba, si se marca la barra bipolar y se introduce 70 como «Punto medio», el valor de la dirección de monitorización aumentando desde 0 se muestra como en la figura 4-103.

<img src="../../../configuration-guide/basic-control/samdra10.gif" width="534" />

Figura 4-103 Gráfico de barras bipolar

3\. Modificar el gráfico de barras: haga clic en él; aparecen ocho puntos verdes que puede arrastrar con el ratón para cambiar su tamaño.

Página «Rango»:

Esta página muestra el valor de la dirección de monitorización con distintos colores de primer plano y de fondo según el rango indicado. Las propiedades se muestran en la figura 4-104:

Figura 4-104   Página «Rango» del gráfico de barras

• Mostrar rango: si se marca, el usuario define los límites inferior y superior y los colores de fondo bajo y alto. El valor monitorizado (leído) se representa con colores distintos según esos límites.

• Rango variable: los valores «Límite inferior» y «Límite superior» cambian dinámicamente según la dirección indicada por el usuario

• Límite inferior: límite inferior de visualización. Si el valor es menor, el fondo toma el color definido en «Color de fondo nivel bajo».

• Límite superior: límite superior de visualización. Si el valor es mayor, el fondo toma el color definido en «Color de fondo nivel alto».

<span id="OLE_LINK727"></span><span id="OLE_LINK726"></span>Tras los ajustes, haga clic en «Aceptar» para añadir el objeto a la zona de trabajo (la pantalla)

<img src="../../../configuration-guide/basic-control/bar.files/image004.jpg" width="130" />

Nota: si el valor de la dirección de monitorización está entre el máximo y el mínimo, los colores de primer plano y de fondo son los de la página «General».

Nota: para la «Visibilidad», véase el «Botón de bit».
