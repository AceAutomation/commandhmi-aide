# Resumen de la sección

1\.  Según su ejecución, un programa se compone de tres estructuras básicas: secuencial, con bifurcaciones y con bucles.

2\.  La unidad básica de ejecución es la instrucción. En C hay cinco tipos de instrucciones:

(1)   Instrucción de expresión: cualquier expresión seguida de punto y coma. La más habitual es la asignación.

(2)   Llamada a función: una llamada a función seguida de punto y coma.

(3)   Instrucción de control: controla el flujo del programa; consta de una palabra clave especial y de las expresiones necesarias. Incluye sobre todo instrucciones condicionales, bucles, saltos, etc.

(4)   Instrucción compuesta: varias instrucciones entre {}. Se considera una sola instrucción y puede usarse donde se admite una instrucción, por ejemplo como cuerpo de un bucle.

(5)   Instrucción vacía: solo un punto y coma, sin efecto.

3\.  Las expresiones relacionales y lógicas son dos tipos importantes de expresión, usados sobre todo para las condiciones de ejecución y de los bucles.

4\.  C ofrece varias instrucciones condicionales para crear bifurcaciones. (1)   if, sobre todo para una elección simple.

(2)   if-else, para una elección entre dos opciones.

(3)   if-else-if y switch, para una elección entre varias opciones. Estas formas suelen poder sustituirse unas por otras.

5\.  C ofrece tres instrucciones de bucle.

(1)   for, sobre todo para bucles con variable inicializada, incremento y número de iteraciones definido. (2)   Si el número de iteraciones o la condición se determinan durante el bucle, se usa while

o do-while.

(3)   Los tres tipos de bucle pueden anidarse entre sí. Los bucles pueden ir uno tras otro pero no cruzarse. (4)   Una instrucción de salto puede sacar el flujo de un bucle, pero no puede entrar en un bucle desde fuera.

(5)   Evite los bucles infinitos: la variable del bucle debe modificarse durante la ejecución para que la condición acabe siendo falsa y el bucle termine.

6\.  Resumen de las instrucciones de C

Nombre                                Forma general

Instrucción simple                Instrucción de expresión; instrucción vacía                           ;

Instrucción condicional          if(expresión)instrucción;

if(expresión)instrucción 1; else instrucción 2;

if(expresión 1)instrucción 1;   else if(expresión 2) instrucción 2…else instrucción n; instrucción switch                 switch(expresión){ case constante: instrucción…default: instrucción;   } instrucción de bucle                           instrucción while

```c
while(expression)statement;
for statement for(expression 1; expression 2; expression 3) statement; break statement break;
continue statement continue;
return statement return(expression);
```
