# Instrucciones de un programa C

La parte ejecutable de un programa C está formada por instrucciones, que realizan la función del programa. Las instrucciones de C se dividen en cinco categorías:

1\.  Instrucciones de expresión

2\.  Instrucciones de control

3\.  Instrucciones compuestas

4\.  Instrucciones vacías

**1.  Instrucciones de expresión**

Una instrucción de expresión consta de una expresión y un punto y coma. Su forma general es expresión;. Ejecutarla consiste en calcular la expresión. Por ejemplo, x=y+z; es una asignación; y+z; calcula una suma pero no guarda el resultado, por lo que no tiene utilidad; i++; incrementa i en 1.

**2.  Instrucciones de control**

Las instrucciones de control dirigen el flujo del programa para crear sus distintas estructuras.

Constan de palabras clave especiales. En C hay nueve instrucciones de control, de tres tipos:

(1)   Instrucciones condicionales: if, switch

(2)   Instrucciones de bucle

do while, while, for

(3)   Instrucciones de salto

break, goto, continue, return

**3.  Instrucciones vacías**

Una instrucción formada solo por un punto y coma es una instrucción vacía; no hace nada. Puede servir como cuerpo de bucle vacío. Por ejemplo, while (getchar()!='\n'): mientras el carácter introducido por teclado no sea Intro, hay que volver a introducirlo. Aquí el cuerpo del bucle es una instrucción vacía.

**4.  Instrucciones de asignación**

Una asignación consta de una expresión de asignación y un punto y coma. Su forma general es variable = expresión. Sus funciones y características son las de la expresión de asignación. Es una de las instrucciones más usadas. Puntos a tener en cuenta:

1\.  Como la expresión a la derecha de «=» puede ser a su vez una asignación, la forma variable=(variable=expresión); es válida y permite anidar. Su forma desarrollada es variable=variable=…=expresión;

Por ejemplo:

```c
a=b=c=d=e=5; according to the right associativity of assignment operator, it is equivalent to: e=5 actually;
d=e; c=d; b=c; a=b;
```

2\.  Distinga entre asignar un valor inicial en la declaración y asignar con una instrucción.

El valor inicial forma parte de la declaración: la variable inicializada se separa con una coma de las demás variables del mismo tipo, mientras que la instrucción de asignación termina en punto y coma.

3\.  En una declaración no se puede asignar en cadena un valor inicial a varias variables. Por ejemplo, la declaración int a=b=c=5 es incorrecta: hay que escribir int a=5,b=5,c=5. En cambio, una instrucción de asignación sí puede encadenarse.

4\.  Distinga entre expresión de asignación e instrucción de asignación. La expresión de asignación puede usarse en cualquier lugar donde se admita una expresión; la instrucción, no.

Esta instrucción es válida: if((x=y+5)&gt;0) z=x; significado: si la expresión x=y+5 es mayor que 0, entonces z=x.

Esta instrucción no es válida: if((x=y+5;)&gt;0) z=x; porque x=y+5; es una instrucción y no puede usarse en una expresión.
