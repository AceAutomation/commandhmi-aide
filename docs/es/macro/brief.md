# Resumen de la sección

**1.  Tipos de datos de C**

Tipos básicos, tipos construidos, punteros y void

**2.  Clasificación y características de los tipos básicos**

|                   |        |                                         |
|-------------------|--------|-----------------------------------------|
| Especificador de tipo    | Byte   | Rango de valores                            |
| char              | 1      | Juego de caracteres de C                         |
| int               | 4      | -214783648～214783647                   |
| short int         | 4      | -214783648～214783647                   |
| long int          | 8      | -922337203685477808～922337203685477807 |
| unsigned          | 4      | 0～4294967295                           |
| unsigned long     | 8      | 0～1844744073709551615                  |
| float             | 4      | 3/4E-38～3/4E+38                        |
| double            | 8      | 1/7E-308～1/7E+308                      |

**3.  Sufijos de constantes**

L o l para long int

U o u para unsigned

F o f para float

**4.  Tipos de constantes**

Int, long int, unsigned, float, char, cadena de caracteres, constante simbólica y carácter de escape

**5.  Conversión de tipos**

Conversión automática

En operaciones con datos de distintos tipos, el sistema los convierte automáticamente del tipo más pequeño al más grande. En la asignación entre tipos distintos, el sistema convierte automáticamente el tipo de la derecha al de la izquierda.

Conversión forzada

Se realiza con el operador de conversión de tipo (cast).

**6.  Prioridad y asociatividad de los operadores**

En general, los operadores unarios tienen más prioridad y los de asignación menos. Los aritméticos tienen más prioridad que los relacionales y lógicos. La mayoría de operadores son asociativos por la izquierda; los unarios, el ternario y los de asignación lo son por la derecha.

**7.  Expresiones**

Una expresión es una fórmula que combina constantes, variables y funciones mediante operadores. Cada expresión tiene un valor y un tipo. Se evalúa en el orden que fijan la prioridad y la asociatividad de los operadores.

**8.  Arrays**

1\.  El array es la estructura de datos más común en programación. Hay arrays numéricos (de enteros, de floats), de caracteres, de punteros y de estructuras, que se describen más adelante.

2\.  Un array puede ser unidimensional, bidimensional o multidimensional.

3\.  La declaración de un array consta del especificador de tipo, el nombre y la longitud (número de elementos). Los elementos se llaman también variables indexadas. El tipo del array es el tipo de sus elementos.

4\.  Hay tres formas de asignar valores a un array: inicialización, asignación dinámica con funciones de entrada y asignación con instrucciones. Un array numérico no puede asignarse, leerse ni escribirse entero con una asignación; hay que tratar sus elementos uno a uno, por ejemplo con una instrucción do.
