# Array unidimensional

En programación, un array agrupa de forma ordenada varias variables del mismo tipo. El conjunto ordenado de elementos de datos del mismo tipo se llama array. En C, el array es un tipo de dato construido. Un array se divide en varios elementos, que pueden ser de tipo básico o construido. Por eso, según el tipo de sus elementos, hay arrays numéricos, de caracteres, de punteros, de estructuras, etc.

Esta sección presenta los arrays numéricos y de caracteres; los demás se describen en las secciones siguientes. En C, un array debe declararse antes de usarse. La forma general de la declaración es: especificador de tipo nombre del array    \[expresión constante\]. El especificador de tipo es cualquier tipo básico o construido. El nombre del array es el identificador definido por el usuario. La expresión constante entre corchetes indica el número de elementos, también llamado longitud del array.

Por ejemplo:

int a\[10\]; el array de enteros a contiene 10 elementos.

float b\[10\],c\[20\]; el array de floats b contiene 10 elementos y el array c contiene 20. char ch\[20\]; el array de caracteres ch contiene 20 elementos.

Sobre la declaración de arrays hay que tener en cuenta lo siguiente:

1\.  El tipo del array es el tipo de valor de sus elementos. Todos los elementos de un mismo array son del mismo tipo.

2\.  El nombre del array sigue las reglas de los identificadores.

3\.  El nombre del array no puede coincidir con el de otra variable. Por ejemplo:   void main ()

```c
{
int a;
float a[10];
```

……

} es incorrecto

4\.  La expresión constante entre corchetes es el número de elementos. Por ejemplo, a \[5\] indica que el array a contiene 5 elementos. Pero los índices empiezan en 0, así que los cinco elementos son a\[0\],a\[1\],a\[2\],a\[3\],a\[4\].

5\.  Entre corchetes no puede haber variables, pero sí constantes simbólicas o expresiones constantes. Por ejemplo:

\#define FD    5

```c
void main ()
{
int a[3+2],b[7+FD];
```

……

```c
} is legal. However, the following expression form is incorrect. void main()
{
int n=5;
int a[n];
```

……

}

6\.  Una misma declaración de tipo puede declarar varios arrays y varias variables.

Por ejemplo: int a,b,c,d,k1\[10\],k2\[20\];

**1.  Representación de los elementos del array**

Los elementos son la unidad básica del array. Cada elemento es también una variable, identificada por el nombre del array y un índice. El índice indica la posición del elemento en el array. La forma general de un elemento es: nombre del array \[índice\]. El índice solo puede ser una constante o expresión entera; si tiene decimales, C lo convierte automáticamente en entero. Por ejemplo, a\[5\],a\[i+j\],a\[i++\] son elementos válidos. Un elemento de array suele llamarse variable indexada. Solo puede usarse una vez definido el array. En C, las variables indexadas se usan una a una, no el array completo.

La forma general de la inicialización es: static especificador de tipo nombre del array \[expresión constante\]=\[valor……\]. static indica el almacenamiento estático. En C solo pueden inicializarse los arrays de almacenamiento estático o externo (estos conceptos se presentan en el capítulo 5). Los datos entre {    } son los valores iniciales de cada elemento, separados por comas, como static int a\[10\]={    0,1,2,3,4,5,6,7,8,9   }, equivalente a a\[0\]=0;a\[1\]=1...a\[9\]=9;

**2.  Reglas de la inicialización de arrays en C:**

1\.  Se puede inicializar solo una parte de los elementos. Si hay menos valores entre {    } que elementos, solo se inicializan los primeros. Por ejemplo: static int a\[10\]={0,1,2,3,4} indica que los valores iniciales

se asignan a los 5 primeros elementos a\[0\]～a\[4\] y que los 5 últimos valen automáticamente 0.

2\.  Los valores se asignan elemento a elemento; no se puede asignar un valor al array entero. Por ejemplo, para poner a 1 los 10 elementos hay que escribir static int a\[10\]={1,1,1,1,1,1,1,1,1,1} y no static int a\[10\]=1.

3\.  Si un array inicializado no recibe valores, todos sus elementos valen 0.

4\.  Si se inicializan todos los elementos, puede omitirse su número en la declaración. Por ejemplo: static int a\[5\]={1,2,3,4,5} puede escribirse     static int a\[\]={1,2,3,4,5}. También se pueden asignar valores durante la ejecución del programa, por ejemplo con una instrucción do y la función scanf, elemento a elemento.

**3.  Arrays de caracteres**

Un array que almacena caracteres se llama array de caracteres. Se declara igual que un array numérico. Por ejemplo: char c\[10\]. Como los caracteres y los enteros son similares, también puede definirse como int c\[10\], pero entonces cada elemento ocupa 2 bytes. Un array de caracteres puede ser bidimensional.  Por  ejemplo,  char  c\[5\]\[10\]  es  un  array  de  caracteres  bidimensional.  Puede  inicializarse  en  la  declaración. Tomemos como ejemplo static char c\[10\]={\`c\`,\`    \`,\`p\`,\`r\`,o\`,g\`,r\`,\`a\`,\`m\`}. Tras la asignación, los elementos son c\[0\]c\[1\]c\[2\]c\[3\]c\[4\]c \[5\]c\[6\]c\[7\]c\[8\]c\[9\] del array C. c\[9\] no recibe valor y el sistema le asigna automáticamente 0. Si se inicializan todos los elementos, puede omitirse la longitud, como en static char c\[\]={\`c\`,\`    \`,\`p\`,\`r\`,\`o\`,\`g\`,\`r\`,\`a\`,\`m\`}, cuya longitud es 9.

El  lenguaje  C  permite  inicializar  un  array  con  una  cadena.  Por  ejemplo,  static  char  c\[\]={'c',  ' ','p','r','o','g','r','a','m'} puede escribirse static char c\[\]={"C program"} o static char c\[\]="C program" sin {}. La asignación con cadena ocupa un byte más que la asignación elemento a elemento, para guardar el carácter de fin de cadena '\0'. El contenido real del array c en memoria es C program\0. El carácter \`\0' lo añade automáticamente el sistema C. Gracias a '\0', normalmente no se indica la longitud del array al inicializarlo con una cadena: el sistema la calcula. Con cadenas, la entrada y salida de arrays de caracteres es más sencilla: además de inicializar con una cadena, se puede leer o escribir de una vez la cadena de un array con las funciones printf y scanf, sin recorrer cada carácter con una instrucción do.
