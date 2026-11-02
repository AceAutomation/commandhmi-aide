# Instructions du programme C

La partie exécutable d'un programme C se compose d'instructions, qui réalisent ses fonctions. Les instructions C se répartissent en cinq catégories :

1\.  Instruction d'expression

2\.  Instruction de contrôle

3\.  Instruction composée

4\.  Instruction vide

**1.  Instruction d'expression**

Une instruction d'expression se compose d'une expression suivie d'un point-virgule. Sa forme générale est expression;. Son exécution évalue l'expression. Par exemple, x=y+z; est une affectation ; y+z; calcule une addition sans conserver le résultat, ce qui n'a pas d'intérêt ; i++; incrémente i de 1.

**2.  Instruction de contrôle**

L'instruction de contrôle gère le déroulement du programme et réalise ses différentes structures.

Elle se compose de mots-clés particuliers. Le langage C compte neuf instructions de contrôle, en trois catégories :

(1)   Instructions conditionnelles : if, switch

(2)   Instructions de boucle

do while, while, for

(3)   Instructions de branchement

break, goto, continue, return

**3.  Instruction vide**

Une instruction réduite à un point-virgule est une instruction vide : elle n'exécute rien. Elle peut servir de corps de boucle vide. Par exemple, while (getchar()!='\n') : tant que le caractère saisi au clavier n'est pas Entrée, il faut ressaisir. Le corps de boucle est ici une instruction vide.

**4.  Instruction d'affectation**

L'instruction d'affectation se compose d'une expression d'affectation suivie d'un point-virgule. Sa forme générale est variable = expression. Ses fonctions et caractéristiques sont celles de l'expression d'affectation. C'est l'une des instructions les plus utilisées. Quelques points à noter :

1\.  L'expression à droite du signe « = » pouvant être elle-même une affectation, la forme variable=(variable=expression); est valide et forme une affectation imbriquée. Sa forme développée est variable=variable=…=expression;

Par exemple :

```c
a=b=c=d=e=5; according to the right associativity of assignment operator, it is equivalent to: e=5 actually;
d=e; c=d; b=c; a=b;
```

2\.  Attention à la différence entre l'initialisation d'une variable dans sa déclaration et l'instruction d'affectation.

L'initialisation fait partie de la déclaration : une variable initialisée est séparée des autres variables par une virgule, alors que l'instruction d'affectation se termine par un point-virgule.

3\.  Dans une déclaration, on ne peut pas initialiser plusieurs variables en cascade. Par exemple, la déclaration int a=b=c=5 est incorrecte : il faut écrire int a=5,b=5,c=5. L'instruction d'affectation, elle, peut être enchaînée.

4\.  Attention à la différence entre expression d'affectation et instruction d'affectation. L'expression d'affectation est une expression et peut s'utiliser partout où une expression est admise ; l'instruction d'affectation non.

L'instruction suivante est valide : if((x=y+5)&gt;0) z=x; : si l'expression x=y+5 est supérieure à 0, alors z=x.

L'instruction suivante n'est pas valide : if((x=y+5;)&gt;0) z=x; : x=y+5; est une instruction et ne peut pas figurer dans une expression.
