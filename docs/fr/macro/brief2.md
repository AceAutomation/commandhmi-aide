# Résumé de la section

1\.  Du point de vue de l'exécution, un programme se compose de trois structures de base : séquentielle, conditionnelle et en boucle.

2\.  L'unité de base de l'exécution est l'instruction. Le langage C compte cinq sortes d'instructions :

(1)   Instruction d'expression : toute expression suivie d'un point-virgule. La plus courante est l'affectation.

(2)   Instruction d'appel de fonction : un appel de fonction suivi d'un point-virgule.

(3)   Instruction de contrôle : sert à contrôler le déroulement du programme ; elle se compose de mots-clés particuliers et des expressions nécessaires : instructions conditionnelles, boucles, goto, etc.

(4)   Instruction composée : plusieurs instructions entourées de {}. Elle est traitée comme une instruction unique et peut s'utiliser partout où une instruction est admise, par exemple comme corps de boucle.

(5)   Instruction vide : un simple point-virgule, sans effet.

3\.  Les expressions relationnelles et logiques sont deux types d'expressions importants, utilisés surtout comme conditions d'exécution et de boucle.

4\.  Le langage C offre plusieurs formes d'instructions conditionnelles. (1)   if sert surtout au choix simple.

(2)   if-else sert surtout au choix entre deux branches.

(3)   if-else-if et switch servent au choix entre plusieurs branches. Ces formes sont généralement interchangeables.

5\.  Le langage C offre trois instructions de boucle.

(1)   for sert surtout aux boucles avec initialisation de la variable de boucle, pas d'incrémentation et nombre de tours connu. (2)   Si le nombre de tours et la condition ne sont connus qu'en cours de boucle, on utilise while

ou do-while.

(3)   Les trois boucles peuvent être imbriquées. Les boucles peuvent être parallèles mais pas entrecroisées. (4)   Une instruction de branchement peut faire sortir du corps de boucle, mais pas y entrer de l'extérieur.

(5)   Évitez les boucles infinies : la variable de boucle doit être modifiée pendant l'exécution pour que la condition devienne fausse et que la boucle se termine.

6\.  Récapitulatif des instructions du C

Nom                                 Forme générale

Instruction simple              Instruction d'expression ; instruction vide                           ;

Instruction conditionnelle     if(expression)instruction;

if(expression)instruction 1; else instruction 2;

if(expression 1)instruction 1;   else if(expression 2) instruction 2…else instruction n; instruction switch                 switch(expression){ case constante: instruction…default: instruction;   } instruction de boucle                    instruction while

```c
while(expression)statement;
for statement for(expression 1; expression 2; expression 3) statement; break statement break;
continue statement continue;
return statement return(expression);
```
