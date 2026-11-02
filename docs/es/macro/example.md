# Un script sencillo

Cree un proyecto y elija el modelo de HMI adecuado. El script realizará este cálculo aritmético sencillo: el script Init inicializa los objetos de «Visualización numérica» con los valores del array char source \[4\] = {2, 3, 4, 5}; los datos se introducen desde el exterior con las visualizaciones numéricas; al pulsar el botón «=» se ejecuta el script ADDSUM y su resultado se muestra en el objeto.

Pasos detallados:

**Paso 1: &lt;Crear un script&gt;**

Haga clic en el botón de acceso rápido «Editor de scripts» a la izquierda de la barra de herramientas; se abre un cuadro de diálogo.

**Paso 2: &lt;Crear el script Init&gt;**

Haga clic en el botón <img src="../../macro/example.files/example866.png" width="25" /> del editor de scripts; aparece un script nuevo en la lista «No guardado», como en la figura 5-7. Cambie el nombre del script en el campo correspondiente y escriba el código fuente en la ventana de edición, como en la figura 5-8

<img src="../../macro/example.files/example1100.png" width="886" />

Figura 5-7      Nuevo script

<img src="../../macro/example.files/example1126.png" width="1087" />

Figura 5-8 Edición del script Init

<img src="../../macro/example.files/example1156.png" width="130" />

El nombre de un script solo puede contener cifras (0-9), letras (a-z, A-Z) y guion bajo (\_). Introduzca el contenido de la figura 5-9:

**Paso 3: &lt;Ajuste de variables&gt;**

En la ventana de la figura 5-9 se definen el nombre, el tipo, etc. de las variables. Haga doble clic en la ventana «Ajuste de variables», o clic derecho y «Nueva variable», para abrir el cuadro de diálogo de la figura 5-10 y definir las variables externas.

<img src="../../macro/example.files/example1677.png" width="499" />

Figura 5-9 Código del script

Nombre: introduzca LW0, LW1, LW2, LW3 como nombres de variable;

Tipo de dato: entero de 16 bits;

Lectura / escritura: elija lectura y escritura;

Direcciones: LW0 = 0, LW1 = 1, LW2 = 2, LW3 = 3;

El resultado se muestra en la figura 5-10.

<img src="../../macro/example.files/example1981.png" width="843" />

Figura 5-10     Ajuste de variables

**Paso 4: &lt;Compilar el código fuente&gt;**

A continuación, compile: haga clic en el botón de compilación de la figura 5-11; el script se guarda, se compila, se enlaza y se comprueban los errores automáticamente.

<img src="../../macro/example.files/example2223.png" width="800" />

Figura 5-11    Ventana de salida

Si la ventana de salida muestra «0 errors! Compile successfully», el script se ha creado correctamente y se añade a la lista de scripts compilados; si no, se muestra un mensaje de error y el script se añade a la lista de compilaciones fallidas. Corrija el script hasta que compile sin errores.

**Paso 5: &lt;Crear el script ADDSUM&gt;**

Siga los pasos 2 a 4 para crear el script ADDSUM, como en la figura 5-13

&lt;1&gt;: introduzca «ADDSUM» como nombre del script.

&lt;2&gt;: introduzca el contenido marcado en la ventana de edición de código.

&lt;3&gt;: defina las propiedades de las variables en la ventana de ajuste de variables.

&lt;4&gt;: haga clic en el botón «Compilar».

<img src="../../macro/example.files/example2991.png" width="1168" />

Figura 5-13    Creación del script ADDSUM

**Paso 6: &lt;Editar los objetos&gt;**

&lt;1&gt;. Coloque los objetos en la pantalla del proyecto y ajuste su tamaño, como en la figura 5-14.

<img src="../../macro/example.files/example3164.png" width="558" />

Figura 5-14    Disposición de los objetos

&lt;2&gt;. Defina las propiedades de los objetos

Haga clic derecho en cada objeto «Entrada numérica» y defina su dirección y sus propiedades, como en la figura 5-15.

<img src="../../macro/example.files/example3375.png" width="660" />

Figura 5-15    Propiedades de la entrada numérica

Es imprescindible que las variables LW0, LW1, LW2, LW3 y SumLW correspondan a la «dirección de escritura» (figura 5-15) de cada objeto. Haga clic en «Aceptar» para guardar.

&lt;3&gt;. Propiedades del botón de bit

<img src="../../macro/example.files/example3658.png" width="661" />

Figura 5-16 (Propiedades del botón de bit)

&lt;4&gt;. Propiedades del temporizador

Elija el script Init y haga clic en «Aceptar» para guardar.

<img src="../../macro/example.files/example3792.png" width="661" />

Figura 5-17    Propiedades del temporizador

&lt;5&gt;. En la página «Etiqueta» -&gt; «Texto» del botón de función, escriba el carácter «+», como en la figura 5-18.

<img src="../../macro/example.files/example3963.png" width="662" />

Figura 5-18    Propiedades del botón de función

**Paso 7: compilar y descargar al HMI**

&lt;1&gt;: haga clic en el icono de compilación.

<img src="../../macro/example.files/example4101.png" width="64" />

Figura 5-19    Compilación del proyecto

&lt;2&gt;: elija «Download (D) -&gt; USB download (D)» y haga clic en «Descargar» en el cuadro de diálogo. Reinicie el HMI.

También puede usar el botón de acceso rápido «Compilar y descargar».

**Paso 8: &lt;Prueba del resultado&gt;**

Tras reiniciar el HMI, aparece la pantalla de la figura 5-20.

Esto se debe a que, al arrancar, el temporizador ejecuta primero el script Init.

<img src="../../macro/example.files/example4642.png" width="484" />

Figura 5-20    Valores iniciales

Introduzca por ejemplo «31,42,53,64» en los objetos de «Visualización numérica» y pulse «=»: se ejecuta el script ADDSUM y el resultado es 190, como en la figura 5-21:

<img src="../../macro/example.files/example5009.png" width="481" />

Figura 5-21     Resultado

Se han completado así la edición, compilación, descarga y prueba del script y todas las funciones necesarias.
