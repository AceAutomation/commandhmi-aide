# Instrucción for

La instrucción for es la instrucción de bucle más potente y versátil de C. Su forma general es:

For (expresión 1; expresión 2; expresión 3)

instrucción;

Expresión 1: suele asignar el valor inicial de la variable del bucle; es una asignación. El valor inicial también puede asignarse fuera de la instrucción for; en ese caso puede omitirse.

Expresión 2: suele ser la condición del bucle, una expresión relacional o lógica. Expresión 3: suele modificar el valor de la variable del bucle; es una asignación.

Las tres expresiones pueden ser expresiones con coma, es decir, compuestas por varias expresiones. Las tres son opcionales y pueden omitirse.

La «instrucción» de la forma general es el cuerpo del bucle. Significado de for:

1\.  Primero se calcula la expresión 1.

2\.  Después se calcula la expresión 2. Si es verdadera (distinta de 0), se ejecuta el cuerpo del bucle; si no, se sale del bucle.

3\.  Se calcula la expresión 3 y se vuelve al paso 2. En un for, la expresión 1 se calcula una sola vez y las expresiones 2 y 3 pueden repetirse varias veces. El cuerpo puede ejecutarse muchas veces o ninguna.

Puntos a tener en cuenta en la instrucción for:

1\.  Cada expresión puede omitirse, pero los puntos y coma deben estar. Por ejemplo:

&lt;1&gt;for(expresión; expresión) se omite una expresión

&lt;2&gt;for(expresión; expresión;) se omite una expresión

&lt;3&gt;for(;expresión; expresión) se omite una expresión

2\.  Si la variable del bucle ya tiene valor inicial, puede omitirse la expresión 1, como en el ejemplo 3.27. Si se omite la expresión

2 o 3, puede producirse un bucle infinito; en ese caso hay que terminar el bucle en su cuerpo.

3\.  El cuerpo del bucle puede ser una instrucción vacía.

```c
#include" stdio.h" void main(){
int n=0;
printf("input a string:\n"); for(;getchar()!='\n';n++); printf("%d",n);
}
```

En este ejemplo se omite la expresión 1 del for, y la expresión 3 no modifica la variable del bucle sino que lee y cuenta los caracteres. El recuento que debería hacerse en el cuerpo se hace en la expresión, por lo que el cuerpo es una instrucción vacía. Atención: el punto y coma de la instrucción vacía es imprescindible; si falta, la instrucción printf siguiente se ejecutaría como cuerpo del bucle. A la inversa, si el cuerpo no está vacío, no debe ponerse punto y coma tras el paréntesis de las expresiones, porque el cuerpo se consideraría vacío y no se repetiría. Son errores frecuentes a los que hay que prestar mucha atención.
