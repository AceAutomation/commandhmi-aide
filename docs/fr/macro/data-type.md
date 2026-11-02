# Types de données du langage C

**1.  Entiers**

Les entiers comprennent les constantes entières et les variables entières. En langage C, il existe trois sortes de constantes entières : octales, hexadécimales et décimales.

**2.  Constantes entières**

1\.  Constantes entières octales

Une constante octale commence par 0 : 0 est le préfixe des constantes octales. Ses chiffres vont de 0 à 7. Les constantes octales sont généralement non signées. Exemples de constantes octales valides :

015 (décimal : 13) 0101 (décimal : 65) 0177777 (décimal : 65535)

Exemples non valides : 256 (sans préfixe 0)    03A2 (chiffres non octaux)             -0127 (signe négatif)

2\.  Constantes entières hexadécimales

Les constantes hexadécimales ont le préfixe 0X ou 0x. Leurs chiffres sont 0-9, A-F ou a-f.

Exemples de constantes hexadécimales valides :

0X2A (décimal : 42) 0XA0 (décimal : 160)    0XFFFF (décimal : 65535) Exemples non valides :

5A (sans préfixe 0X)                0X3H (chiffres non hexadécimaux)

3\.  Constantes entières décimales

Les constantes décimales n'ont pas de préfixe. Leurs chiffres vont de 0 à 9. Exemples de constantes décimales valides :

237   -568   65535    1627

Exemples non valides :

023 (le préfixe 0 est interdit)          23D (chiffres non décimaux)

Dans un programme, ces notations se distinguent par leur préfixe : attention à ne pas se tromper de préfixe, sous peine de résultats erronés.

4\.  Sur un ordinateur 16 bits, l'entier de base occupe 16 bits : la plage des valeurs est donc limitée. Les constantes décimales non signées vont de 0 à 65535, les signées de -32768 à +32767. Les octales non signées vont de 0 à 0177777, les hexadécimales non signées de 0X0 à 0XFFFF ou de 0x0 à 0xFFFF. Au-delà, il faut utiliser un entier long, signalé par le suffixe « L » ou « l ». Par exemple :

Constante entière longue décimale 158L (décimal : 158)   358000L (décimal : -358000)

Constante entière longue octale    012L (décimal : 10)   077L (décimal : 63)    0200000L (décimal : 65536)

Constante entière longue hexadécimale   0X15L (décimal : 21)    0XA5L (décimal : 165)   0X10000L (décimal : 65536). Les valeurs 158L et 158 sont identiques, mais 158L étant un entier long, le compilateur C

lui réserve 4 octets, alors que 158, entier de base, n'en occupe que 2. Faites donc attention aux opérations et aux formats de sortie. Un nombre non signé s'indique aussi par un suffixe : « U » ou « u ». Par exemple :     358u,

0x38Au, 235Lu sont des nombres non signés. Préfixes et suffixes peuvent se combiner. Par exemple,

0XA5Lu désigne l'entier long non signé hexadécimal A5, soit 165 en décimal.

**3.  Variables entières**

Les variables entières se classent comme suit :

1\.  Int

Son spécificateur de type est int ; elle occupe 2 octets en mémoire. Sa valeur est toujours un entier de base.

2\.  Entier court

Son spécificateur de type est short int ou short. Taille et plage de valeurs identiques à celles de int.

3\.  Entier long

Son spécificateur de type est long int ou long ; elle occupe 4 octets en mémoire. Sa valeur est toujours un entier long.

4\.  Entier non signé

Son spécificateur de type est unsigned.

Le qualificatif non signé peut se combiner avec les trois types précédents :

(1)   Entier non signé : unsigned int ou unsigned. (2)   Entier court non signé : unsigned short.

(3)   Entier long non signé : unsigned long.

Un entier non signé occupe autant d'octets que l'entier signé correspondant, mais sans bit de signe il ne peut pas représenter de nombre négatif. Le tableau suivant indique la taille mémoire et la plage de valeurs des différents entiers sur ARM.

|                |                                        |                |
|----------------|----------------------------------------|----------------|
| Spécificateur de type | Plage de valeurs                   | Octets réservés |
| Int            | -2147483648~2147483647                 | ■■■■           |
| Short int      | -2147483648~2147483647                 | ■■■■           |
| Signed int     | -2147483648~2147483647                 | ■■■■           |
| Unsigned int   | 0~4294967295                           | ■■■■           |
| Long int       | -922337203685477808~922337203685477807 | ■■■■■■■■       |
| Unsigned long  | 0~18446744073709551615                 | ■■■■■■■■       |

**4.  Déclaration des variables entières**

La forme générale d'une déclaration de variable est : spécificateur de type, identificateur de variable, …. Exemples :

```c
int a,b,c; (a,b,c is integer variable)
long x,y; (x,y is long integer variable)
```

unsigned p,q;    (p, q sont des entiers non signés)

Points à respecter lors de la déclaration des variables :

1\.  Plusieurs variables de même type peuvent suivre le même spécificateur de type, séparées par des virgules. Il faut au moins un espace entre le spécificateur de type et le nom de variable.

2\.  Le dernier nom de variable doit être suivi de « ; ».

3\.  La déclaration d'une variable doit précéder son utilisation ; elle se place en général au début du corps de la fonction.

\[Practice\]    //1int a,b;

short int c; short d=100; a=d-20; b=a+d;

```c
c=a+b+d;
d=d-a+c-b.
```

**5.  Constantes flottantes**

Les constantes réelles sont aussi appelées constantes flottantes. En langage C, les flottants ne s'écrivent qu'en décimal, sous deux formes : forme décimale et forme exponentielle

1\.  Forme décimale

Elle se compose des chiffres 0-9 et d'un point décimal. Par exemple : 0.0,.25,5.789,0.13,5.0,300.,-267.8230 sont des flottants valides.

2\.  Forme exponentielle

Elle se compose d'un nombre décimal, du symbole d'exposant « e » ou « E » et de l'exposant (entier, éventuellement signé). La forme de base est a E n (a décimal, n entier décimal), de valeur a\*10,n. Par exemple, 2.1E5 (soit 2.1\*10,5), 3.7E-2    (soit 3.7\*10,)-2\*) 0.5E7 (soit 0.5\*10,7), -2.8E-2 (soit -2.8\*10,)-2\*). Exemples non valides : 345 (sans point décimal)      E7 (pas de chiffre avant le symbole d'exposant) -5 (sans symbole d'exposant) 53.-E3   (signe négatif mal placé) 2.7E (sans exposant)

En C standard, un flottant peut avoir un suffixe : « f » ou « F » indique un flottant. Par exemple, 356f et 356 sont équivalents.

**6.  Variables flottantes**

Les variables flottantes sont en simple ou double précision, de spécificateurs float et double. En Turbo C, le simple précision occupe 4 octets (32 bits), avec une plage de 3.4E-38～3.4E+38 et seulement 7 chiffres significatifs. Le double précision occupe 8 octets (64 bits), avec une plage de 1.7E-308 ～ 1.7E+308 et

16 chiffres significatifs.

La déclaration des variables flottantes suit les mêmes règles que celle des entiers. Par exemple :  float x,y;    (x, y en simple précision)

double a,b,c;   (a, b, c en double précision)

Les constantes flottantes ne sont pas distinguées en simple et double précision : toutes sont traitées en double. a   ■■■■

b   ■■■■■■■■

a&lt;---33333.33333

b&lt;---33333.33333333333;

\[Practice\]    //float int a=32; float b;

double d; b=12345678; d=b\*100;

```c
d=d+a;
d=d+58.123456;
```

**7.  Caractères**

Les caractères comprennent les constantes caractères et les variables caractères. Constante caractère

Une constante caractère est un caractère entre apostrophes. Par exemple, 'a'. 'b', '=', '+', , '?' sont des constantes caractères valides. En langage C, les constantes caractères ont les caractéristiques suivantes :

1.   Une constante caractère s'écrit entre apostrophes, et non entre guillemets ou autres délimiteurs.

2.   Une constante caractère est un seul caractère, et non une chaîne.

3.   Ce peut être n'importe quel caractère du jeu de caractères. Mais un chiffre défini comme caractère ne peut pas servir dans un calcul numérique. Par exemple, '5' et 5 sont différents : '5' est une constante caractère, qui ne participe pas aux calculs.

**8.  Variables caractères**

Une variable caractère contient une constante caractère, c'est-à-dire un seul caractère. Son spécificateur de type est char. Sa déclaration suit les mêmes règles que celle des variables entières.

Par exemple :

char a,b;

Chaque variable caractère occupe un octet en mémoire et ne contient qu'un caractère, stocké sous forme de code ASCII. Par exemple, le code ASCII décimal de x est 120, celui de y est

121\. Affecter 'x' et 'y' aux variables caractères a et b : a='x', b='y' revient à stocker 120 et 121 dans a et b :

a 0   1    1   1    1   0    0   0 b 0   1    1   1    1   0    0   1

On peut donc les considérer comme des entiers. Le C permet d'affecter un caractère à une variable entière et un entier à une variable caractère, et d'afficher une variable caractère comme un entier et inversement. L'entier occupe

2 octets, le caractère un seul : quand un entier est traité comme caractère, seul l'octet de poids faible est utilisé. \[Exercice\]    //charint a=49;

char b; char d; b=a+10; d=a+b;

\[Exercice\]    //char c1,c2;

```c
c1='a';c2='b';
c1=c1-32;c2=c2-32;
```

**9.  Constantes chaînes de caractères**

Une constante chaîne est une suite de caractères entre guillemets. Par exemple : "CHINA", "C program", "\$12.5" sont des constantes chaînes valides. Une constante chaîne diffère d'une constante caractère sur les points suivants :

1\.  La constante caractère s'écrit entre apostrophes, la constante chaîne entre guillemets.

2\.  La constante caractère ne contient qu'un caractère, la constante chaîne un ou plusieurs.

3\.  On peut affecter un caractère à une variable caractère, mais pas une constante chaîne : le C n'a pas de type variable chaîne.

4\.  La constante caractère occupe un octet en mémoire. La constante chaîne occupe autant d'octets que de caractères plus 1 : l'octet supplémentaire contient le caractère "\0" (code ASCII 0), qui marque la fin de la chaîne. Par exemple, "C program" est stocké en mémoire sous la forme C program\0. Bien que la constante caractère 'a' et la constante chaîne ''a'' contiennent toutes deux un seul caractère, elles n'occupent pas la même place en mémoire.

'a' occupe un octet en mémoire, noté a

''a'' occupe deux octets en mémoire, notés a\0.

**10. Constantes symboliques**

En langage C, une constante peut être représentée par un identificateur, appelé constante symbolique. Elle doit être définie avant utilisation. Sa forme générale est :

\#define identificateur constante

\#define est une directive du préprocesseur, appelée directive de définition de macro. Elle associe l'identificateur à la valeur constante : ensuite, toutes les occurrences de cet identificateur dans le programme sont remplacées par cette valeur. Par convention, les constantes symboliques s'écrivent en majuscules et les variables en minuscules pour les distinguer.

```c
#define PI 3.14159 void main(){
float s,r; r=5; s=PI*r*r;
printf("s=%f\n",s);
}
```

La directive de macro définit PI comme 3.14159, et s, r sont déclarés en float.    5-&gt;r     PI\*r\*r-&gt;s

Le programme affiche float s,r, avec r=5 et s=PI\*r\*r. PI est défini par une directive de macro avant la fonction main : il vaut 3.14159 et remplace PI dans le programme ; s=PI\*r\*r équivaut à s=3.14159\*r\*r. Attention : une constante symbolique n'est pas une variable ; sa valeur ne peut pas changer dans sa portée, et on ne peut pas lui affecter une nouvelle valeur dans le programme.
