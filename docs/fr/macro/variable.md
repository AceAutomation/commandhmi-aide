# Valeur initiale des variables et conversion de type

**1.  Initialisation des variables**

Dans un programme, on donne souvent une valeur initiale aux variables : c'est l'initialisation, qui peut se faire de plusieurs façons. Dans la déclaration, la forme générale est :

spécificateur de type variable 1 = 1, variable 2 = 2, …… ; par exemple :

```c
int a=b=c=5;
float x=3.2,y=3f,z=0.75;
char ch1='K',ch2='P';
```

Remarque : l'affectation en cascade est interdite dans la déclaration : par exemple a=b=c=5 n'est pas valide.

**2.  Conversion de type des variables**

Le type d'une variable peut être converti de deux façons : conversion automatique ou conversion forcée.

Conversion automatique

Quand une opération met en jeu des données de types différents, le compilateur les convertit automatiquement selon les règles suivantes :

1\.  Si les types des données sont différents, ils sont d'abord convertis en un même type, puis l'opération est effectuée.

2\.  La conversion se fait vers le type le plus long, pour préserver la précision. Par exemple, dans une opération entre int et long, int est converti en long.

3\.  Tous les calculs flottants se font en double : même une expression ne contenant que des float est convertie en double.

4\.  char et short sont convertis en int pour le calcul.

5\.  Dans une affectation, si les types de part et d'autre du signe « = » diffèrent, la valeur de droite est convertie dans le type de gauche. Si le type de droite est plus long, une partie des données est perdue et la précision diminue ; la partie perdue est arrondie.

**3.  Conversion de type forcée**

La conversion forcée se fait avec l'opérateur de conversion, de forme générale (spécificateur de type) (expression). Elle convertit le résultat dans le type indiqué. Par exemple, (float) a convertit a en float, (int)(x+y) convertit le résultat de x+y en entier. Points à noter :

1\.  Le spécificateur de type et l'expression doivent être entre parenthèses (une variable seule peut ne pas l'être). Écrire (int)(x+y)

sous la forme (int)x+y signifie convertir x en int puis lui ajouter y.

2\.  Conversion forcée ou automatique, il ne s'agit que d'une conversion temporaire pour le calcul : le type déclaré de la variable ne change pas.
