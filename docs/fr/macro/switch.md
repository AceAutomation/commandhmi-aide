# Instruction switch

Le langage C offre aussi l'instruction switch pour choisir entre plusieurs branches. Sa forme générale est :

switch(expression){

```c
case constant expression 1: statement 1;
case constant expression 2: statement 2;
```

…

```c
case constant expression n: statement n;
default: statement n+1;
}
```

Signification : on évalue l'expression et on la compare successivement aux expressions constantes. Dès qu'elle est égale à l'une d'elles, les instructions qui suivent sont exécutées, sans nouvelle comparaison, y compris celles des case suivants. Si elle n'est égale à aucune constante, ce sont les instructions de default qui sont exécutées.

Points à noter sur l'instruction switch :

1\.  Les valeurs des expressions constantes des case doivent toutes être différentes, sinon une erreur se produit.

2\.  Plusieurs instructions peuvent suivre un case, sans nécessairement les entourer de {}.

3\.  L'ordre des clauses case et default peut être modifié sans effet sur l'exécution.

4\.  La clause default peut être omise
