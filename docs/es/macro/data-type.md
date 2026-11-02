# Tipos de datos del lenguaje C

**1.  Enteros**

Los enteros incluyen constantes enteras y variables enteras. En C hay tres tipos de constantes enteras: octales, hexadecimales y decimales.

**2.  Constantes enteras**

1\.  Constantes enteras octales

Una constante octal debe empezar por 0, que es su prefijo. Sus cifras van de 0 a 7. Las constantes octales suelen ser sin signo. Ejemplos de octales válidos:

015 (decimal: 13) 0101 (decimal: 65) 0177777 (decimal: 65535)

Ejemplos de octales no válidos: 256 (sin prefijo 0)    03A2 (contiene cifras no octales)             -0127 (con signo negativo)

2\.  Constantes enteras hexadecimales

Una constante hexadecimal lleva el prefijo 0X o 0x. Sus cifras son 0-9, A-F o a-f.

Ejemplos de hexadecimales válidos:

0X2A (decimal: 42) 0XA0 (decimal: 160)    0XFFFF (decimal: 65535). Ejemplos de hexadecimales no válidos:

5A (sin prefijo 0X)                0X3H (contiene cifras no hexadecimales)

3\.  Constantes enteras decimales

Una constante decimal no lleva prefijo. Sus cifras van de 0 a 9. Ejemplos de decimales válidos:

237   -568   65535    1627

Ejemplos de decimales no válidos:

023 (no se admite el prefijo 0)          23D (contiene cifras no decimales)

En el programa, estas notaciones se distinguen por el prefijo. No se equivoque al escribirlo para evitar resultados incorrectos.

4\.  Sufijos de las constantes enteras: en un ordenador de 16 bits, el entero básico es de 16 bits, por lo que el rango de valores es limitado. Las constantes decimales sin signo van de 0 a 65535 y con signo de -32768 a +32767. Los octales sin signo van de 0 a 0177777 y los hexadecimales sin signo de 0X0 a 0XFFFF o 0x0 a 0xFFFF. Fuera de estos rangos hay que usar enteros largos, con el sufijo «L» o «l». Por ejemplo:

Constantes decimales largas 158L (decimal: 158)   358000L (decimal: -358000)

Constantes octales largas    012L (decimal: 10)   077L (decimal: 63)    0200000L (decimal: 65536)

Constantes hexadecimales largas   0X15L (decimal: 21)    0XA5L (decimal: 165)   0X10000L (decimal: 65536). No hay diferencia de valor entre el entero largo 158L y la constante entera 158. Pero como 158L es un entero largo, el compilador de C

le reserva 4 bytes, mientras que a 158 le reserva 2 bytes. Tenga cuidado con las operaciones y los formatos de salida para evitar errores. Los números sin signo se indican con el sufijo «U» o «u». Por ejemplo:     358u,

0x38Au y 235Lu son números sin signo. Prefijos y sufijos pueden combinarse. Por ejemplo,

0XA5Lu es el entero largo sin signo hexadecimal A5, que en decimal vale 165.

**3.  Variables enteras**

Las variables enteras se clasifican así:

1\.  Int

Su especificador de tipo es int; ocupa 2 bytes en memoria y su valor es siempre un entero básico.

2\.  Short int

Su especificador de tipo es short int o short. Ocupa los mismos bytes y tiene el mismo rango que int.

3\.  Long int

Su especificador de tipo es long int o long; ocupa 4 bytes en memoria y su valor es siempre un entero largo.

4\.  Unsigned int

Su especificador de tipo es unsigned.

unsigned puede combinarse con los tres tipos anteriores:

(1)   El especificador de tipo de unsigned int es unsigned int o unsigned. (2)   El de unsigned short int es unsigned short.

(3)   El de unsigned long int es unsigned long.

Los enteros sin signo ocupan los mismos bytes que los enteros con signo, pero al no tener bit de signo no pueden representar números negativos. La tabla siguiente indica los bytes ocupados y el rango de cada tipo de entero en ARM.

|                |                                        |                |
|----------------|----------------------------------------|----------------|
| Especificador de tipo | Rango de valores                           | Bytes ocupados |
| Int            | -2147483648~2147483647                 | ■■■■           |
| Short int      | -2147483648~2147483647                 | ■■■■           |
| Signed int     | -2147483648~2147483647                 | ■■■■           |
| Unsigned int   | 0~4294967295                           | ■■■■           |
| Long int       | -922337203685477808~922337203685477807 | ■■■■■■■■       |
| Unsigned long  | 0~18446744073709551615                 | ■■■■■■■■       |

**4.  Declaración de variables enteras**

Forma general de la declaración de variables: especificador de tipo, identificador de la variable, …. Por ejemplo:

```c
int a,b,c; (a,b,c is integer variable)
long x,y; (x,y is long integer variable)
```

unsigned p,q;    (p,q   son variables enteras sin signo)

Al declarar variables hay que tener en cuenta lo siguiente:

1\.  Se pueden declarar varias variables del mismo tipo tras un mismo especificador, separando los nombres con comas. Entre el especificador de tipo y el nombre debe haber al menos un espacio.

2\.  El último nombre de variable debe terminar con «;».

3\.  La declaración debe preceder al uso de la variable; suele ir al principio del cuerpo de la función.

\[Práctica\]    //1int a,b;

short int c; short d=100; a=d-20; b=a+d;

```c
c=a+b+d;
d=d-a+c-b.
```

**5.  Constantes de coma flotante**

Las constantes reales se llaman también constantes de coma flotante. En C se escriben solo en decimal y tienen dos formas: decimal y exponencial

1\.  Forma decimal

Consta de las cifras 0-9 y un punto decimal. Por ejemplo: 0.0,.25,5.789,0.13,5.0,300.,-267.8230 son números válidos.

2\.  Forma exponencial

Consta de un número decimal, el símbolo de exponente «e» o «E» y el exponente (solo entero, con signo posible). Su forma básica es a E n (a decimal, n entero decimal) y su valor es a\*10,n. Por ejemplo, 2.1E5 (igual a 2.1\*10,5), 3.7E-2    (igual a 3.7\*10,)-2\*) 0.5E7 (igual a 0.5\*10,7), -2.8E-2 (igual a -2.8\*10,)-2\*). Ejemplos no válidos: 345 (sin punto decimal)      E7 (sin cifra antes del exponente) -5 (sin símbolo de exponente) 53.-E3   (signo negativo mal colocado) 2.7E (sin exponente)

En C estándar, los números de coma flotante pueden llevar sufijo: un número con sufijo «f» o «F» es de coma flotante. Por ejemplo, 356f y 356 son equivalentes.

**6.  Variables de coma flotante**

Hay variables de simple y doble precisión, con los especificadores float y double. En Turbo C, el float ocupa 4 bytes (32 bits), con un rango de 3.4E-38～3.4E+38 y solo siete cifras significativas. El double ocupa 8 bytes (64 bits), con un rango de 1.7E-308 ～ 1.7E+308 y

dieciséis cifras significativas.

La declaración de variables de coma flotante sigue las mismas reglas que la de enteros. Por ejemplo:  float x,y;    (x,y son float de simple precisión)

double a,b,c;   (a,b,c son float de doble precisión)

Las constantes de coma flotante no se distinguen entre simple y doble precisión: todas se tratan como double. a   ■■■■

b   ■■■■■■■■

a&lt;---33333.33333

b&lt;---33333.33333333333;

\[Práctica\]    //float int a=32; float b;

double d; b=12345678; d=b\*100;

```c
d=d+a;
d=d+58.123456;
```

**7.  Caracteres**

Los caracteres incluyen constantes y variables de carácter. Constantes de carácter

Una constante de carácter es un carácter entre comillas simples. Por ejemplo, 'a'. 'b', '=', '+', , '?' son constantes de carácter válidas. En C, las constantes de carácter tienen estas características:

1.   Deben ir entre comillas simples, no entre comillas dobles ni otros signos.

2.   Deben ser un único carácter, no una cadena.

3.   Pueden ser cualquier carácter del juego de caracteres. Pero una cifra definida como carácter no puede usarse en cálculos. Por ejemplo, '5' y 5 son distintos: '5' es una constante de carácter que no interviene en cálculos.

**8.  Variables de carácter**

El valor de una variable de carácter es una constante de carácter, es decir, un único carácter. Su especificador de tipo es char. Se declara con las mismas reglas que una variable entera.

Por ejemplo:

char a,b;

Cada variable de carácter ocupa un byte de memoria y solo guarda un carácter, almacenado por su código ASCII. Por ejemplo, el código ASCII decimal de x es 120 y el de y es

121\. Si se asignan 'x' e 'y' a las variables de carácter a y b: a='x', b='y', en realidad se guardan 120 y 121 en a y b:

a 0   1    1   1    1   0    0   0 b 0   1    1   1    1   0    0   1

Por eso pueden tratarse como enteros. C permite asignar un carácter a una variable entera y un entero a una variable de carácter, y mostrar una variable de carácter como entero y un entero como carácter. El entero

ocupa 2 bytes y el carácter 1 byte. Cuando un entero se trata como carácter, solo se usan sus ocho bits bajos. \[Práctica\]    //charint a=49;

char b; char d; b=a+10; d=a+b;

\[Práctica\]    //char c1,c2;

```c
c1='a';c2='b';
c1=c1-32;c2=c2-32;
```

**9.  Constantes de cadena**

Una constante de cadena es una secuencia de caracteres entre comillas dobles. Por ejemplo: "CHINA". "C program", "\$12.5"  son  constantes  de  cadena  válidas.  Una  constante  de  cadena  es  distinta  de  una  constante  de  carácter.  Diferencias:

1\.  La constante de carácter va entre comillas simples; la de cadena, entre comillas dobles.

2\.  La constante de carácter es un único carácter; la de cadena contiene uno o varios.

3\.  Un carácter puede asignarse a una variable de carácter, pero una cadena no. En C no existen variables de cadena como tales.

4\.  La constante de carácter ocupa un byte en memoria. Una constante de cadena ocupa el número de caracteres más 1: el byte adicional guarda el carácter "\0" (código ASCII 0), que marca el final de la cadena. Por ejemplo, "C program" ocupa en memoria C program\0. Aunque la constante de carácter 'a' y la de cadena ''a'' tienen un carácter, no ocupan lo mismo.

'a' ocupa un byte en memoria: a

''a'' ocupa dos bytes en memoria: a\0

**10. Constantes simbólicas**

En C, una constante puede representarse con un identificador, llamado constante simbólica. Debe definirse antes de usarse. Su forma general es:

\#define constante simbólica

\#define es una directiva del preprocesador, llamada directiva de definición de macro. Asocia el identificador a un valor constante. A partir de la definición, todas las apariciones del identificador en el programa se sustituyen por el valor. Por convención, las constantes simbólicas se escriben en mayúsculas y las variables en minúsculas, para distinguirlas.

```c
#define PI 3.14159 void main(){
float s,r; r=5; s=PI*r*r;
printf("s=%f\n",s);
}
```

Se define con la directiva de macro: PI vale 3.14159 y s, r son float.    5-&gt;r     PI\*r\*r-&gt;s

Resultado del programa: float s,r, con r=5 y s=PI\*r\*r. La directiva de macro, antes de la función main, define PI como 3.14159, que sustituye a PI en el programa. s=PI\*r\*r equivale a s=3.14159\*r\*r. Atención: una constante simbólica no es una variable; su valor no puede cambiar en todo su ámbito, es decir, no puede reasignarse en el programa.
