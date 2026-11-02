# Instruction for

L'instruction for est une boucle très puissante et très utilisée du langage C. Sa forme générale est :

For (expression 1;expression 2;expression 3)

instruction;

Expression 1 : en général, initialise la variable de boucle ; c'est une affectation. L'initialisation peut aussi se faire hors du for ; l'expression peut alors être omise.

Expression 2 : en général, la condition de boucle, expression relationnelle ou logique. Expression 3 : en général, modifie la variable de boucle ; c'est une affectation.

Chacune de ces trois expressions peut être une expression virgule, c'est-à-dire composée de plusieurs expressions. Les trois sont facultatives et peuvent être omises.

L'« instruction » de la forme générale est le corps de boucle. Déroulement de l'instruction for :

1\.  Évaluation de l'expression 1.

2\.  Évaluation de l'expression 2. Si elle est vraie (non nulle), le corps de boucle est exécuté une fois ; sinon, on sort de la boucle.

3\.  Évaluation de l'expression 3, puis retour à l'étape 2. L'expression 1 n'est évaluée qu'une fois ; les expressions 2 et 3 peuvent l'être plusieurs fois. Le corps de boucle peut être exécuté de nombreuses fois ou jamais.

Points à noter sur l'instruction for :

1\.  Chaque expression du for peut être omise, mais les points-virgules doivent rester. Par exemple :

&lt;1&gt;for(expression; expression) une expression est omise

&lt;2&gt;for(expression; expression;) une expression est omise

&lt;3&gt;for(;expression; expression) toutes les expressions sont omises

2\.  Si la variable de boucle est déjà initialisée, l'expression 1 peut être omise, comme dans l'exemple 3.27. Si l'expression

2 ou 3 est omise, la boucle risque d'être infinie : il faut alors la terminer dans le corps de boucle.

3\.  Le corps de boucle peut être une instruction vide.

```c
#include" stdio.h" void main(){
int n=0;
printf("input a string:\n"); for(;getchar()!='\n';n++); printf("%d",n);
}
```

Dans cet exemple, l'expression 1 du for est omise et l'expression 3 ne modifie pas la variable de boucle mais compte les caractères saisis. Le comptage, normalement fait dans le corps de boucle, est fait dans l'expression : le corps de boucle est donc une instruction vide. Attention : le point-virgule de l'instruction vide est indispensable ; sans lui, l'instruction printf suivante deviendrait le corps de boucle. Inversement, si le corps de boucle n'est pas vide, il ne faut pas mettre de point-virgule après la parenthèse du for : le corps serait alors considéré comme vide et ne serait pas répété. Ce sont des erreurs fréquentes, à surveiller attentivement.
