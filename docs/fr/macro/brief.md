# Résumé de la section

**1.  Types de données du C**

Types de base, types construits, pointeurs et type void

**2.  Classification et caractéristiques des types de base**

|                   |        |                                         |
|-------------------|--------|-----------------------------------------|
| Spécificateur de type | Octets | Plage de valeurs                    |
| char              | 1      | jeu de caractères C                     |
| int               | 4      | -214783648～214783647                   |
| short int         | 4      | -214783648～214783647                   |
| long int          | 8      | -922337203685477808～922337203685477807 |
| unsigned          | 4      | 0～4294967295                           |
| unsigned long     | 8      | 0～1844744073709551615                  |
| float             | 4      | 3/4E-38～3/4E+38                        |
| double            | 8      | 1/7E-308～1/7E+308                      |

**3.  Suffixes des constantes**

L ou l pour long int

U ou u pour unsigned

F ou f pour float

**4.  Types de constantes**

Entier, entier long, non signé, flottant, caractère, chaîne de caractères, constante symbolique et caractère d'échappement

**5.  Conversion de types**

Conversion automatique

Le système convertit automatiquement les données de types différents dans une même opération, du type le plus court vers le type le plus long. Lors d'une affectation entre types différents, il convertit aussi automatiquement la valeur de droite dans le type de gauche.

Conversion forcée

Elle se fait avec l'opérateur de conversion (cast).

**6.  Priorité et associativité des opérateurs**

En général, les opérateurs unaires ont une priorité élevée et l'affectation une priorité faible. Les opérateurs arithmétiques ont une priorité plus élevée que les opérateurs relationnels et logiques. La plupart des opérateurs sont associatifs à gauche ; les opérateurs unaires, ternaire et d'affectation sont associatifs à droite.

**7.  Expressions**

Une expression est une formule composée de constantes, de variables et de fonctions reliées par des opérateurs. Chaque expression a une valeur et un type. Elle est évaluée dans l'ordre fixé par la priorité et l'associativité des opérateurs.

**8.  Tableaux**

1\.  Le tableau est la structure de données la plus courante en programmation. On distingue les tableaux numériques (int, float), les tableaux de caractères, ainsi que les tableaux de pointeurs et de structures décrits plus loin.

2\.  Un tableau peut avoir une, deux ou plusieurs dimensions.

3\.  La déclaration d'un tableau comprend le spécificateur de type, le nom et la longueur (nombre d'éléments). L'élément de tableau est aussi appelé variable indicée. Le type du tableau est le type de ses variables indicées.

4\.  Un tableau peut être rempli de trois façons : initialisation, saisie dynamique par une fonction d'entrée et instruction d'affectation. Un tableau numérique ne peut pas être affecté, lu ou écrit en bloc : il faut traiter les éléments un à un avec une boucle.
