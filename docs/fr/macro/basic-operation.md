# Opérateurs de base et expressions

**Catégories, priorité et associativité des opérateurs**

Le langage C dispose de nombreux opérateurs et expressions, ce qui est rare parmi les langages de haut niveau. Cette richesse d'opérateurs et d'expressions fait la force du C ; c'est l'une de ses principales caractéristiques.

Les opérateurs du C ont des priorités différentes et chacun a son associativité. Dans une expression, l'ordre des opérations dépend de la priorité des opérateurs et de leur associativité, qui fixe le sens d'évaluation de gauche à droite ou de droite à gauche. Cette notion d'associativité, absente des autres langages de haut niveau, rend le C plus complexe.

Catégories d'opérateurs

Les opérateurs du C se classent comme suit :

**1.  Opérateurs arithmétiques**

Pour les calculs : addition (+), soustraction (-), multiplication (\*), division (/), modulo (%), incrémentation (++) et décrémentation (--).

**2.  Opérateurs relationnels**

Pour les comparaisons : supérieur à (&gt;), inférieur à (&lt;), égal à (==), supérieur ou égal à (&gt;=), inférieur ou égal à (&lt;=) et différent de (! =).

**3.  Opérateurs logiques**

Pour les opérations logiques : ET (&&), OU (\|\|) et NON (!).

**4.  Opérateurs bit à bit**

Les données sont traitées bit par bit : ET bit à bit (&), OU bit à bit (\|), NON bit à bit (~), OU exclusif (^), décalage à gauche (&lt;&lt;) et décalage à droite (&gt;&gt;).

**5.  Opérateurs d'affectation**

Pour les affectations : affectation simple (=), affectation arithmétique composée (+=,-=,\*=, /=, %=)

et affectation bit à bit composée (&=,\|=, ^=,&gt;&gt;=,&lt;&lt;=).

**6.  Opérateur conditionnel**

Opérateur ternaire d'évaluation conditionnelle (?:).

**7.  Opérateur virgule**

Réunit plusieurs expressions en une seule (, ).

**8.  Opérateurs de pointeur**

Deux opérations : contenu de (\*) et adresse de (&).

**9.  Opérateur sizeof**

Calcule la taille d'une donnée.

**10. Opérateurs spéciaux**

Parenthèses (), indice \[\], etc.
