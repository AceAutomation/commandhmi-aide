# Programas con bifurcaciones

**Operadores y expresiones relacionales**

En los programas se comparan a menudo dos datos para decidir el paso siguiente. Los operadores que comparan datos se llaman operadores relacionales. En C son los siguientes:

&lt;   menor que

&lt;= menor o igual que

&gt; mayor que

&gt;= mayor o igual que

== igual a

!= distinto de

Los operadores relacionales son binarios y asociativos por la izquierda. Su prioridad es menor que la de los aritméticos y mayor que la de asignación. De los seis, &lt;,&lt;=,&gt;,&gt;= tienen la misma prioridad, mayor que la de ==   y !=, que tienen la misma entre sí.

**Expresiones relacionales**

La    forma    general    de    una    expresión    relacional    es    expresión    operador    relacional    expresión.    Por    ejemplo, a+b&gt;c-d,x&gt;3/2,'a'+1&lt;c,-i-5\*j==k+1 son expresiones relacionales válidas. Como una expresión relacional es también una expresión, pueden anidarse, como a&gt;(b&gt;c),a!=(c==d), etc. El valor de una expresión relacional es «verdadero» o «falso», representado por «1» y «0».

**1.  Operadores y expresiones lógicos**

En C, los operadores lógicos son Y &&, O \|\| y NO !. Y && y O \|\| son binarios y asociativos por la izquierda. NO ! es unario y asociativo por la derecha. La prioridad de los operadores lógicos respecto a los demás es la siguiente:

Según la prioridad de los operadores:

a&gt;b && c&gt;d equivale a (a&gt;b) &&   (c&gt;d)

!b==c\|\|d&lt;a equivale a ((!b)==c)\|\|(d&lt;a)

a+b&gt;c && x+y&lt;b equivale a ((a+b)&gt;c) && ((x+y)&lt;b). Evaluación de las operaciones lógicas

El resultado de una operación lógica es verdadero o falso, representado por 1 y 0. Reglas de evaluación:

1\.  Y &&: el resultado es verdadero si ambos valores son verdaderos; si no, es falso. Por ejemplo, 5&gt;0

&& 4&gt;2: como 5&gt;0 y 4&gt;2 son verdaderos, el resultado es verdadero.

2\.  O \|\|: el resultado es verdadero si uno de los dos valores es verdadero, y falso si ambos son falsos. Por ejemplo, 5&gt;0\|\|5&gt;8: como 5&gt;0 es verdadero, el resultado es verdadero.

3\.  NO !: si el operando es verdadero, el resultado es falso; si es falso, el resultado es verdadero.

Por ejemplo, !(5&gt;0) es falso.

En C, el resultado de una operación lógica es «1» para «verdadero» y «0» para «falso». A la inversa, al evaluar si un valor es verdadero o falso, 0 es falso y cualquier valor distinto de 0 es verdadero. Por ejemplo, como 5 y 3 no son 0, 5&&3 vale «verdadero» (1).

Otro ejemplo: 5\|\|0 vale «verdadero» (1).

La forma general de una expresión lógica es expresión – operador lógico – expresión. Las expresiones pueden ser a su vez lógicas, lo que permite anidarlas. Por ejemplo, (a&&b) &&c puede escribirse a&&b&&c por la asociatividad por la izquierda. El valor de una expresión lógica es el resultado final de las operaciones, «1» para «verdadero» y «0» para «falso».

**2.  Instrucción if**

La instrucción if permite crear bifurcaciones: según la condición indicada, decide qué rama del programa se ejecuta. En C, if tiene tres formas básicas.

1\.  Primera forma: forma básica. if (expresión) instrucción

Significado: si la expresión es verdadera, se ejecuta la instrucción; si no, no.

2\.  Segunda forma: if-else. if(expresión)

instrucción 1; else instrucción 2;

Significado: si la expresión es verdadera, se ejecuta la instrucción 1; si no, la instrucción 2.

Introducir dos enteros y mostrar el mayor. Se comparan a y b con if-else: si a es mayor, se muestra a;

si no, b.

**3.  Tercera forma: if-else-if.**

Las dos primeras formas sirven para dos ramas. Cuando hay varias ramas posibles, se usa if-else-if. Su forma básica es:

if(expresión 1)

instrucción 1;

else if(expresión 2)

instrucción   2;

else if(expresión 3)

instrucción   3;

…

else if(expresión m)

instrucción m; else instrucción n;

Significado: se evalúan las expresiones en orden. Cuando una es verdadera, se ejecuta la instrucción correspondiente y el programa sale de la instrucción if. Si todas son falsas, se ejecuta la instrucción n. Después continúa el programa.

**Puntos a tener en cuenta en la instrucción if:**

(1)   En las tres formas, tras if va una expresión, normalmente lógica o relacional, pero puede ser otra, como una asignación o incluso una variable. Por ejemplo, if(a=5) instrucción e if(b) instrucción son válidas. Basta con que la expresión no valga 0 para ser verdadera. En if(a=5)…; la expresión nunca vale 0, así que la instrucción siguiente se ejecuta siempre. Esta situación no suele darse en un programa, pero la sintaxis es válida.

Otro ejemplo, el fragmento: if(a=b)

```c
printf("%d",a); else printf("a=0");
```

Significado: asigna b a a; si el valor no es 0, se muestra; si no, se muestra la cadena «a=0». Este uso es frecuente en los programas.

(2)   En la instrucción if, la expresión de condición debe ir entre paréntesis y la instrucción termina en punto y coma.

(3)   En las tres formas, cada instrucción debe ser única. Si hay que ejecutar un grupo de instrucciones según la condición, deben agruparse entre {} para formar una instrucción compuesta. Atención: no debe haber punto y coma tras }.

Por ejemplo:

```c
if(a>b){ a++; b++;
}
else{ a=0;
b=10;
}
```

**4.  Operador condicional y expresión condicional**

Si la instrucción condicional solo contiene una asignación, suele usarse una expresión condicional, que simplifica el programa y mejora su eficiencia.

El operador condicional ? : es ternario, es decir, intervienen tres valores. La forma general de la expresión condicional es:

Expresión 1 ? Expresión 2: Expresión 3

Regla de evaluación: si la expresión 1 es verdadera, el valor de la expresión condicional es el de la expresión 2; si no, es el de la expresión 3. La expresión condicional suele usarse en asignaciones. Por ejemplo:

```c
if(a>b) max=a;
else max=b;
```

max=(a&gt;b)?a:b; usa una expresión condicional. Significado: si a&gt;b es verdadero, se asigna a a max; si no, se asigna b.

Al usar expresiones condicionales hay que tener en cuenta lo siguiente:

1\.  La prioridad del operador condicional es menor que la de los operadores relacionales y aritméticos, pero mayor que la de asignación. Por eso max=(a&gt;b)?a:b puede escribirse sin paréntesis: max=a&gt;b?a:b.

2\.  ? y : forman un par que no puede separarse.

3\.  El operador condicional es asociativo de derecha a izquierda.
