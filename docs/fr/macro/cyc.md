# Programmes à structure de boucle

La boucle est une structure importante des programmes : tant qu'une condition est remplie, une partie du programme est exécutée de façon répétée. Cette condition est appelée condition de boucle, et la partie répétée corps de boucle. Le langage C offre plusieurs instructions de boucle, qui permettent différentes structures.

**1.  Instruction while**

Forme générale de l'instruction while : While (expression) instruction;

l'expression est la condition de boucle et l'instruction le corps de boucle.

Signification : on évalue l'expression ; tant qu'elle est vraie (non nulle), le corps de boucle est exécuté.

Quelques points à noter sur l'instruction while :

1\.  L'expression de while est généralement relationnelle ou logique. Tant qu'elle est vraie (non nulle), la boucle continue.

2\.  Si le corps de boucle contient plusieurs instructions, il faut les entourer de {} pour former une instruction composée.

3\.  Surveillez la condition de boucle pour éviter les boucles infinies.

**2.  Instruction do-while**

Forme générale de l'instruction do-while :

```c
do statement;
while (expression);
```

L'instruction est le corps de boucle et l'expression la condition de boucle. Signification de do-while :

Le corps de boucle est d'abord exécuté une fois, puis l'expression est évaluée. Si elle est vraie (non nulle), la boucle continue ; sinon elle s'arrête.

La différence avec while est que do-while exécute d'abord puis teste : le corps de boucle est donc exécuté au moins une fois. while teste d'abord puis exécute : si la condition n'est pas remplie, le corps de boucle n'est jamais exécuté.

while et do-while sont généralement interchangeables.

Dans cet exemple, la condition de boucle est réécrite en –n, sinon la boucle ferait un tour de trop. Quelques points à noter sur l'instruction do-while :

1\.  Dans les instructions if et while, l'expression n'est pas suivie d'un point-virgule ; dans do-while, elle doit se terminer par un point-virgule.

2\.  do-while peut former des boucles imbriquées, y compris avec while.

3\.  Si le corps de boucle entre do et while comporte plusieurs instructions, il faut les entourer de {} pour former une instruction composée.

4\.  En passant de do-while à while ou inversement, pensez à adapter la condition de boucle.
