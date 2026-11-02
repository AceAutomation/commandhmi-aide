# Rectangle dynamique

Le rectangle dynamique fonctionne comme le cercle dynamique : il reflète en temps réel l'état de l'adresse surveillée en modifiant la position ou la taille du graphique selon sa valeur.

Sélectionnez l'icône Rectangle dynamique<img src="../../../configuration-guide/extended-controls/dym-rect.files/image002.jpg" width="34" /> dans la barre d'outils pour ouvrir la boîte de dialogue de la figure 4-57.

Figure 4-57    Boîte de dialogue Rectangle dynamique

Le rectangle dynamique lit quatre valeurs d'adresse, qui représentent respectivement l'abscisse, l'ordonnée, la largeur et la hauteur du rectangle. La façon dont ces adresses sont lues dépend du type de données choisi.

• Épaisseur du trait : modifie l'épaisseur du trait

• Type : angle droit, angle coupé ou angle arrondi.

• Remarque : le type n'a d'effet que si l'épaisseur du trait est supérieure à 1.

Exemple :

Avec le type « entier 16 bits » et l'adresse de surveillance LW1, quatre valeurs sont lues : LW1, LW2, LW3 et LW4, avec la signification suivante :

La valeur de LW1 est l'abscisse <span id="OLE_LINK558"></span><span id="OLE_LINK559"></span>du rectangle ;

La valeur de LW2 est l'ordonnée du rectangle ;

La valeur de LW3 est la largeur du rectangle ;

La valeur de LW4 est la hauteur du rectangle.

Avec le type « entier 16 bits », quatre données consécutives sont lues selon le format d'adresse de l'automate : abscisse, ordonnée, largeur et hauteur du rectangle.

Avec le type « entier 32 bits » et l'adresse de surveillance LW1, les valeurs lues sont LW1, LW3, LW5 et LW7.

La valeur de LW1 est l'abscisse du rectangle ;

La valeur de LW3 est l'ordonnée du rectangle ;

La valeur de LW5 est la largeur du rectangle ;

La valeur de LW7 est la hauteur du rectangle ;

Avec le type « entier 32 bits », selon le format d'adresse de l'automate, les quatre données (abscisse, ordonnée, largeur et hauteur du rectangle) sont lues à des adresses espacées de 2 à partir de l'adresse de surveillance.

**Contrôle :**

• Position : la hauteur et la largeur du rectangle ne changent pas ; sa position suit les valeurs surveillées qui représentent ses coordonnées x et y.

• Taille : la hauteur et la largeur du rectangle varient à partir de l'un des quatre points fixes suivants ; sa position ne change pas.

• En haut à gauche : <span id="OLE_LINK562"></span><span id="OLE_LINK563"></span>le point fixe est le coin supérieur gauche ; le rectangle s'étend vers le coin inférieur droit.

• En haut à droite : le point fixe est le coin supérieur droit ; le rectangle s'étend vers le coin inférieur gauche.

• En bas à gauche : le point fixe est le coin inférieur gauche ; le rectangle s'étend vers le coin supérieur droit.

• En bas à droite : le point fixe est le coin inférieur droit ; le rectangle s'étend vers le coin supérieur gauche.

**Plein :**

Si Plein n'est pas coché, le rectangle est vide (sans couleur de fond). Sinon, il est plein et l'option Couleur de fond permet de choisir sa couleur.

**Bordure :**

Si cette option n'est pas cochée, le rectangle n'a pas de contour et sa couleur n'est pas modifiable. Sinon, le rectangle a un contour dont la couleur se règle avec l'option Couleur de bordure.

Transparence : modifie la transparence de la couleur de fond du rectangle dynamique.

<span id="OLE_LINK570"></span><span id="OLE_LINK571"></span><img src="../../../configuration-guide/extended-controls/dym-rect.files/image004.jpg" width="130" />

Pour la page « Visibilité », voir l'objet « Bouton de bit ».
