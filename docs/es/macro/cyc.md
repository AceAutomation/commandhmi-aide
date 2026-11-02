# Programas con bucles

El bucle es una estructura importante de los programas. Mientras se cumple una condición, se repite un fragmento de programa hasta que deja de cumplirse. La condición se llama condición del bucle y el fragmento repetido, cuerpo del bucle. C ofrece varias instrucciones de bucle para crear distintas estructuras.

**1.  Instrucción while**

Forma general de la instrucción while: While (expresión) instrucción;

La expresión es la condición del bucle y la instrucción es el cuerpo del bucle.

Significado de while: se calcula la expresión; mientras su valor es verdadero (distinto de 0), se ejecuta el cuerpo del bucle.

Puntos a tener en cuenta en la instrucción while:

1\.  La expresión de while suele ser relacional o lógica. Mientras su valor es verdadero (distinto de 0), el bucle continúa.

2\.  Si el cuerpo del bucle contiene varias instrucciones, deben ir entre {} para formar una instrucción compuesta.

3\.  Cuidado con la condición del bucle para evitar bucles infinitos.

**2.  Instrucción do-while**

Forma general de la instrucción do-while:

```c
do statement;
while (expression);
```

La instrucción es el cuerpo del bucle y la expresión es la condición. Significado de do-while:

Primero se ejecuta una vez el cuerpo del bucle y después se evalúa la expresión. Si es verdadera (distinta de 0), el bucle continúa; si no, termina.

La diferencia entre do-while y while es que do-while ejecuta primero y evalúa después; por eso ejecuta el cuerpo al menos una vez. while evalúa primero y ejecuta después; si la condición no se cumple, el cuerpo no se ejecuta ni una vez.

while y do-while suelen poder reescribirse uno en otro.

En este ejemplo, la condición del bucle se reescribe como –n; si no, se ejecutaría una iteración de más. Puntos a tener en cuenta en do-while:

1\.  En if y while no va punto y coma tras la expresión; en do-while, la expresión debe terminar en punto y coma.

2\.  do-while puede formar bucles anidados y anidarse con while.

3\.  Si el cuerpo entre do y while tiene varias instrucciones, deben ir entre {} para formar una instrucción compuesta.

4\.  Al convertir entre do-while y while, preste atención a modificar la condición del bucle.
