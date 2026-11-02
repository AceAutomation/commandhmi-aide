# Programmes à structure conditionnelle

**Opérateurs et expressions relationnels**

Un programme compare souvent deux données pour décider de la suite du traitement. Les opérateurs de comparaison sont appelés opérateurs relationnels. Le langage C dispose des opérateurs relationnels suivants :

&lt;   inférieur à

&lt;= inférieur ou égal à

&gt; supérieur à

&gt;= supérieur ou égal à

== égal à

!= différent de

Les opérateurs relationnels sont binaires et associatifs à gauche. Leur priorité est inférieure à celle des opérateurs arithmétiques et supérieure à celle des opérateurs d'affectation. Parmi les six opérateurs relationnels, &lt;,&lt;=,&gt;,&gt;= ont la même priorité, supérieure à celle de ==   et !=, qui ont entre eux la même priorité.

**Expressions relationnelles**

La forme générale d'une expression relationnelle est : expression opérateur relationnel expression. Par exemple, a+b&gt;c-d,x&gt;3/2,'a'+1&lt;c,-i-5\*j==k+1 sont des expressions relationnelles valides. Les expressions pouvant elles-mêmes être relationnelles, on peut les imbriquer, par exemple a&gt;(b&gt;c),a!=(c==d), etc. La valeur d'une expression relationnelle est « vrai » ou « faux », représentée par « 1 » et « 0 ».

**1.  Opérateurs et expressions logiques**

En langage C, les opérateurs logiques sont ET &&, OU \|\| et NON !. && et \|\| sont binaires et associatifs à gauche ; ! est unaire et associatif à droite. La priorité des opérateurs logiques par rapport aux autres est la suivante :

Selon la priorité des opérateurs, on a :

a&gt;b && c&gt;d équivaut à (a&gt;b) &&   (c&gt;d)

!b==c\|\|d&lt;a équivaut à ((!b)==c)\|\|(d&lt;a)

a+b&gt;c && x+y&lt;b équivaut à ((a+b)&gt;c) && ((x+y)&lt;b) Évaluation des opérations logiques

Le résultat d'une opération logique est vrai ou faux, représenté par 1 ou 0. Les règles sont les suivantes :

1\.  ET && : le résultat est vrai si les deux valeurs sont vraies, faux sinon. Par exemple, 5&gt;0

&& 4&gt;2 : 5&gt;0 et 4&gt;2 étant vrais, le résultat est vrai.

2\.  OU \|\| : le résultat est vrai si l'une des deux valeurs est vraie, faux si les deux sont fausses. Par exemple, 5&gt;0\|\|5&gt;8 : 5&gt;0 étant vrai, le résultat est vrai.

3\.  NON ! : le résultat est faux si l'opérande est vrai, vrai si l'opérande est faux.

Par exemple, !(5&gt;0) est faux.

En C, le résultat d'une opération logique est « 1 » pour « vrai » et « 0 » pour « faux ». Inversement, pour juger si une valeur est vraie, 0 signifie faux et toute valeur non nulle signifie vrai. Par exemple, 5 et 3 étant non nuls, 5&&3 vaut « vrai » (c'est-à-dire 1).

Autre exemple : 5\|\|0 vaut « vrai » (c'est-à-dire 1).

La forme générale d'une expression logique est : expression opérateur logique expression. Les expressions peuvent elles-mêmes être logiques, ce qui permet l'imbrication, par exemple (a&&b) &&c, qui peut s'écrire a&&b&&c grâce à l'associativité à gauche. La valeur d'une expression logique est le résultat final des opérations logiques, « 1 » pour « vrai » et « 0 » pour « faux ».

**2.  Instruction if**

L'instruction if permet de construire une structure conditionnelle : selon une condition, elle détermine la branche du programme à exécuter. L'instruction if du C a trois formes de base.

1\.  Première forme : forme simple. if (expression) instruction

Signification : si l'expression est vraie, l'instruction est exécutée, sinon non.

2\.  Deuxième forme : if-else. if(expression)

instruction 1; else instruction 2;

Signification : si l'expression est vraie, l'instruction 1 est exécutée, sinon l'instruction 2.

Saisir deux entiers et afficher le plus grand. On compare a et b avec if-else : si a est plus grand, on affiche a ;

sinon b.

**3.  Troisième forme : if-else-if.**

Les deux premières formes servent à deux branches. Pour choisir entre plusieurs branches, on utilise if-else-if, dont la forme est :

if(expression 1)

instruction 1;

else if(expression 2)

instruction   2;

else if(expression 3)

instruction   3;

…

else if(expression m)

instruction m; else instruction n;

Signification : les expressions sont évaluées dans l'ordre. Dès qu'une est vraie, l'instruction correspondante est exécutée, puis le programme continue après le if. Si toutes les expressions sont fausses, l'instruction n est exécutée, puis le programme continue.

**Points à noter pour l'instruction if :**

(1)   Dans les trois formes, if est suivi d'une expression, généralement logique ou relationnelle, mais ce peut être une autre expression, par exemple une affectation, voire une simple variable. Ainsi if(a=5) instruction et if(b) instruction sont admis. Toute expression non nulle est vraie. Dans if(a=5)…;, l'expression n'est jamais nulle et l'instruction suivante est toujours exécutée. Cela n'arrive pas forcément dans un programme réel, mais la syntaxe est valide.

Autre exemple, extrait de programme : if(a=b)

```c
printf("%d",a); else printf("a=0");
```

Signification : on affecte b à a ; si la valeur n'est pas nulle, elle est affichée, sinon la chaîne « a=0 » est affichée. Cette construction est courante dans les programmes.

(2)   Dans l'instruction if, l'expression de condition doit être entre parenthèses, et l'instruction se termine par un point-virgule.

(3)   Dans les trois formes, les instructions sont des instructions simples. Pour exécuter un groupe d'instructions sous condition, il faut l'entourer de {} pour former une instruction composée. Attention : pas de point-virgule après }.

Par exemple :

```c
if(a>b){ a++; b++;
}
else{ a=0;
b=10;
}
```

**4.  Opérateur conditionnel et expression conditionnelle**

Lorsqu'une instruction conditionnelle n'exécute qu'une affectation simple, on utilise généralement une expression conditionnelle, qui simplifie le programme et améliore son efficacité.

L'opérateur conditionnel ? : est ternaire : il met en jeu trois valeurs. La forme générale d'une expression conditionnelle est :

Expression 1 ? Expression 2: Expression 3

Règle d'évaluation : si l'expression 1 est vraie, la valeur de l'expression conditionnelle est celle de l'expression 2 ; sinon, c'est celle de l'expression 3. L'expression conditionnelle s'utilise souvent dans une affectation. Par exemple :

```c
if(a>b) max=a;
else max=b;
```

max=(a&gt;b)?a:b; utilise une expression conditionnelle. Signification : si a&gt;b est vrai, a est affecté à max ; sinon b est affecté à max.

Quelques points à noter sur l'expression conditionnelle :

1\.  La priorité de l'opérateur conditionnel est inférieure à celle des opérateurs relationnels et arithmétiques, mais supérieure à celle de l'affectation. On peut donc écrire max=(a&gt;b)?a:b sans parenthèses : max=a&gt;b?a:b.

2\.  ? et : forment une paire d'opérateurs indissociables.

3\.  L'opérateur conditionnel est associatif de droite à gauche.
