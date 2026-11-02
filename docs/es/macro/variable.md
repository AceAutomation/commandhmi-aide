# Valor inicial de las variables y conversión de tipos

**1.  Asignación del valor inicial**

En los programas suele darse un valor inicial a las variables. Hay varias formas de hacerlo, que se llaman inicialización. En la declaración, la forma general es:

Especificador de tipo variable 1 = 1, variable 2 = 2, ……; por ejemplo:

```c
int a=b=c=5;
float x=3.2,y=3f,z=0.75;
char ch1='K',ch2='P';
```

Nota: en la declaración no se permite la asignación encadenada; por ejemplo, a=b=c=5 no es válido.

**2.  Conversión de tipos**

El tipo de una variable puede convertirse de dos maneras: conversión automática y conversión forzada.

Conversión automática

Cuando intervienen datos de tipos distintos en una operación, el compilador los convierte automáticamente según estas reglas:

1\.  Si los tipos de los datos son distintos, primero se convierten a un mismo tipo y después se calcula.

2\.  La conversión se hace hacia el tipo más largo para conservar la precisión. Por ejemplo, en una operación entre int y long, int se convierte en long.

3\.  Todas las operaciones de coma flotante se hacen en double, aunque la expresión solo contenga float.

4\.  char y short se convierten en int para calcular.

5\.  En una asignación, si los tipos a ambos lados del signo son distintos, el tipo de la derecha se convierte al de la izquierda. Si el dato de la derecha es más largo, se pierde una parte y la precisión disminuye; la parte perdida se redondea.

**3.  Conversión forzada de tipo**

La conversión forzada se hace con el operador de conversión. Su forma general es (especificador de tipo) (expresión). Convierte el resultado al tipo indicado. Por ejemplo, (float) a convierte a en float; (int)(x+y) convierte el resultado de x+y en entero. Puntos a tener en cuenta:

1\.  El especificador de tipo y la expresión deben ir entre paréntesis (una sola variable puede ir sin ellos). Si (int)(x+y)

se escribe (int)x+y, se convierte x en int y después se suma y.

2\.  Tanto la conversión forzada como la automática son solo temporales, para el cálculo; no cambian el tipo de la variable declarada.
