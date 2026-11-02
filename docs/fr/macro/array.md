# Tableaux à une dimension

En programmation, un tableau regroupe de façon ordonnée plusieurs variables de même type. On appelle tableau l'ensemble ordonné d'éléments de données de même type. En langage C, le tableau est un type construit. Un tableau se compose de plusieurs éléments, qui peuvent être de type de base ou de type construit. On distingue ainsi, selon le type des éléments, les tableaux numériques, les tableaux de caractères, les tableaux de pointeurs, les tableaux de structures, etc.

Cette section présente les tableaux numériques et les tableaux de caractères ; les autres seront décrits dans les sections suivantes. En langage C, un tableau doit être déclaré avant d'être utilisé. La forme générale de la déclaration est : spécificateur de type nom du tableau    \[expression constante\]. Le spécificateur de type est un type de base ou construit. Le nom du tableau est l'identificateur choisi par l'utilisateur. L'expression constante entre crochets indique le nombre d'éléments, appelé aussi longueur du tableau.

Par exemple :

int a\[10\]; le tableau d'entiers a contient 10 éléments.

float b\[10\],c\[20\]; le tableau de flottants b contient 10 éléments, le tableau c 20 éléments. char ch\[20\]; le tableau de caractères ch contient 20 éléments.

Quelques remarques sur la déclaration des tableaux :

1\.  Le type du tableau est en fait le type de ses éléments. Dans un même tableau, tous les éléments ont le même type.

2\.  Le nom du tableau suit les règles d'écriture des identificateurs.

3\.  Le nom du tableau ne doit pas être identique à celui d'une autre variable. Par exemple :   void main ()

```c
{
int a;
float a[10];
```

……

} est incorrect

4\.  L'expression constante entre crochets indique le nombre d'éléments. Par exemple, a \[5\] indique que le tableau a contient 5 éléments. Les indices commencent à 0 : les cinq éléments sont donc a\[0\],a\[1\],a\[2\],a\[3\],a\[4\].

5\.  Les crochets ne peuvent pas contenir une variable comme nombre d'éléments, mais une constante symbolique ou une expression constante est admise. Par exemple :

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

6\.  Une même déclaration peut décrire plusieurs tableaux et plusieurs variables.

Par exemple : int a,b,c,d,k1\[10\],k2\[20\];

**1.  Désignation des éléments d'un tableau**

L'élément est l'unité de base du tableau. C'est aussi une variable, identifiée par le nom du tableau et un indice, qui indique son rang dans le tableau. La forme générale est : nom du tableau \[indice\], l'indice étant une constante ou une expression entière. S'il a une partie décimale, le C le convertit automatiquement en entier. Par exemple, a\[5\],a\[i+j\],a\[i++\] sont des éléments valides. On appelle souvent l'élément variable indicée. Une variable indicée ne peut être utilisée qu'une fois le tableau défini. En C, on utilise les variables indicées une à une et non le tableau entier.

La forme générale de l'initialisation est : static spécificateur de type nom du tableau \[expression constante\]=\[valeur……\]. static désigne la classe de stockage statique. En langage C, seuls les tableaux statiques et externes peuvent être initialisés (les notions de stockage statique et externe sont présentées au chapitre 5). Les données entre {    } sont les valeurs initiales des éléments, séparées par des virgules, par exemple static int a\[10\]={    0,1,2,3,4,5,6,7,8,9   }, ce qui équivaut à a\[0\]=0;a\[1\]=1...a\[9\]=9;

**2.  Règles d'initialisation des tableaux en langage C :**

1\.  On peut n'initialiser qu'une partie des éléments. Si les valeurs entre {    } sont moins nombreuses que les éléments, seuls les premiers sont initialisés. Par exemple : static int a\[10\]={0,1,2,3,4} indique que la valeur initiale

est donnée aux 5 premiers éléments a\[0\]～a\[4\] ; les 5 derniers reçoivent automatiquement 0.

2\.  Les valeurs initiales se donnent élément par élément ; on ne peut pas affecter le tableau en bloc. Par exemple, pour mettre 1 dans les 10 éléments, il faut écrire static int a\[10\]={1,1,1,1,1,1,1,1,1,1} et non static int a\[10\]=1.

3\.  Si un tableau initialisable n'est pas initialisé, tous ses éléments valent 0.

4\.  Si tous les éléments sont initialisés, le nombre d'éléments peut être omis dans la déclaration. Par exemple : static int a\[5\]={1,2,3,4,5} peut s'écrire     static int a\[\]={1,2,3,4,5}. Les éléments peuvent aussi être affectés dynamiquement pendant l'exécution, par exemple un à un avec une boucle do et la fonction scanf.

**3.  Tableaux de caractères**

Un tableau qui contient des caractères est un tableau de caractères. Sa déclaration a la même forme que celle d'un tableau numérique, par exemple : char c\[10\]. Caractères et entiers étant proches, on peut aussi le déclarer int c\[10\], mais chaque élément occupe alors 2 octets en mémoire. Un tableau de caractères peut avoir deux dimensions : par exemple, char c\[5\]\[10\] est un tableau de caractères à deux dimensions. Un tableau de caractères peut être initialisé dans sa déclaration, par exemple static char c\[10\]={\`c\`,\`    \`,\`p\`,\`r\`,o\`,g\`,r\`,\`a\`,\`m\`}. Après initialisation, les éléments du tableau C sont c\[0\]c\[1\]c\[2\]c\[3\]c\[4\]c \[5\]c\[6\]c\[7\]c\[8\]c\[9\] ; c\[9\], non initialisé, reçoit automatiquement 0. Si tous les éléments sont initialisés, la longueur peut être omise, par exemple static char c\[\]={\`c\`,\`    \`,\`p\`,\`r\`,\`o\`,\`g\`,\`r\`,\`a\`,\`m\`} : la longueur du tableau C est alors 9.

Le langage C permet d'initialiser un tableau de caractères avec une chaîne. Par exemple, static char c\[\]={'c', ' ','p','r','o','g','r','a','m'} peut s'écrire static char c\[\]={"C program"} ou static char c\[\]="C program" sans {}. L'initialisation par chaîne occupe un octet de plus que l'initialisation caractère par caractère : il contient le caractère de fin de chaîne '\0'. Le tableau c est donc stocké en mémoire sous la forme C program\0, le '\0' étant ajouté automatiquement par le compilateur. Grâce à ce caractère de fin, on ne précise généralement pas la longueur du tableau lors d'une initialisation par chaîne : le système la calcule. Avec les chaînes, l'entrée et la sortie des tableaux de caractères deviennent simples : en plus de l'initialisation par chaîne, on peut lire ou écrire une chaîne entière en une fois avec printf et scanf, sans boucle do caractère par caractère.
