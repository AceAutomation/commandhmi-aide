# Instrucción switch

El lenguaje C ofrece otra instrucción, switch, para elegir entre varias ramas. Su forma general es:

switch(expression){

```c
case constant expression 1: statement 1;
case constant expression 2: statement 2;
```

…

```c
case constant expression n: statement n;
default: statement n+1;
}
```

Significado: se calcula la expresión y se compara uno a uno con los valores de las expresiones constantes. Cuando coincide con uno, se ejecuta la instrucción correspondiente, sin más comparaciones, y se continúa con las instrucciones de todos los case siguientes. Si no coincide con ninguno, se ejecuta la instrucción de default.

Puntos a tener en cuenta en la instrucción switch:

1\.  Los valores de las expresiones constantes de los case deben ser distintos; si no, hay un error.

2\.  Tras un case puede haber varias instrucciones, sin necesidad de {}.

3\.  El orden de los case y de default puede cambiarse sin afectar a la ejecución.

4\.  La cláusula default puede omitirse
