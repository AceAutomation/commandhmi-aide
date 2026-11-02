# Ejemplo de receta

El ejemplo siguiente muestra la configuración y la visualización de una receta.

1\. **Crear una receta**

En el gestor de proyecto, haga clic con el botón derecho en «Receta», como en la figura 1:

<img src="../../case/formula-case.files/formula-case168.png" width="284" />

Figura 11 Crear una receta

Haga doble clic para abrir la receta, como en la figura 2:

<img src="../../case/formula-case.files/formula-case254.png" width="514" />

Figura 12 Ajustes generales de la receta

Ajuste la longitud de receta a 4: cada receta contiene 4 datos. El número total es 10, es decir, 10 recetas. Ajuste la dirección de escritura de la receta en el PLC a D50 y elija entero positivo de 16 bits; la receta se escribe en los registros D50, D51, D52 y D53. Los ajustes de lectura son iguales a los de la dirección de escritura.

2\. **Ajuste de los elementos de datos de la receta:**

<img src="../../case/formula-case.files/formula-case637.png" width="511" />

Figura 13 Elementos de datos de la receta

Tras definir el nombre de la receta, haga clic en «Aceptar». Utilice el objeto de entrada/visualización numérica para mostrar los datos de la receta en la pantalla táctil. Elija la dirección interna RWI0 para la entrada/visualización numérica: el valor introducido y mostrado es el número de receta. RWI0 indica el número de receta; el valor 2 corresponde a la receta 2, etc. Utilice entradas/visualizaciones numéricas para mostrar los datos de D50 a D53. Para guardar o leer una receta, use las funciones del «Botón de función». Véase «Botón de función».

<img src="../../case/formula-case.files/formula-case1276.png" width="663" />

Figura 14 Objeto «Entrada/visualización numérica» para el dato de receta D50

Configure el objeto de entrada/visualización numérica y colóquelo en la pantalla:

<img src="../../case/formula-case.files/formula-case1422.png" width="746" />

Figura 15 Pantalla de visualización de la receta

Los parámetros de receta pueden modificarse con la entrada/visualización numérica; los botones de función permiten consultar, leer y escribir recetas.
