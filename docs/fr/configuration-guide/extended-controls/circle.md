# Cercle dynamique

Le cercle dynamique est un graphique placé sur l'écran qui se déplace et change de taille selon une certaine trajectoire. Ce mouvement et ce changement de taille dépendent de la valeur de l'adresse de surveillance. Pour ajouter un graphique dynamique et modifier ses propriétés :

Sélectionnez l'icône Cercle dynamique<img src="../../../configuration-guide/extended-controls/circle.files/image002.jpg" width="32" /> dans la barre d'outils, comme sur la figure 4-56 :

Figure 4-56    Boîte de dialogue Cercle dynamique

Le cercle dynamique lit trois valeurs d'adresse, qui représentent respectivement l'abscisse et l'ordonnée du centre et le rayon du cercle. La façon dont ces trois adresses sont lues dépend du type de données choisi.

• Contrôle :

• Centre : le cercle se déplace selon la position de son centre ; le rayon ne change pas.

• Rayon : seul le rayon change ; la position reste fixe.

• Centre et rayon : le rayon varie avec la valeur de l'adresse correspondante, et le centre avec les valeurs des adresses des coordonnées x et y.

• Transparence : modifie la transparence de la couleur de fond du cercle dynamique.

<span id="OLE_LINK564"></span><span id="OLE_LINK565"></span>• Plein :

Si Plein n'est pas coché, le cercle est vide (sans couleur de fond). Sinon, il est plein et l'option Couleur de fond permet de choisir sa couleur.

• Bordure

Si cette option n'est pas cochée, le cercle n'a pas de contour et sa couleur n'est pas modifiable. Sinon, le cercle a un contour dont la couleur se règle avec l'option Couleur de bordure.

Exemple :

Choisissez le type « entier 16 bits » : trois données consécutives sont lues, représentant l'abscisse et l'ordonnée du centre et le rayon, selon le format d'adresse de l'automate. Avec l'adresse de surveillance LW1, <span id="OLE_LINK548"></span><span id="OLE_LINK549"></span>les valeurs lues sont LW1, LW2 et LW3, avec la signification suivante :

La valeur de LW1 est l'abscisse du centre.

<span id="OLE_LINK552"></span><span id="OLE_LINK553"></span>         La valeur de LW2 est l'ordonnée du centre.

La valeur de LW3 est le rayon du cercle.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Que l'on choisisse Centre ou Rayon dans l'option Contrôle, l'IHM lit toujours les trois adresses, avec la même signification. Par exemple, si l'on choisit Rayon avec l'adresse de surveillance LW1, seule la valeur de LW3 commande le rayon.

Avec le type « entier 32 bits » et l'adresse de surveillance LW1, les valeurs lues sont les suivantes :

<span id="OLE_LINK550"></span><span id="OLE_LINK551"></span>La valeur de LW1 est l'abscisse du centre.

La valeur de LW3 est l'ordonnée du centre.

La valeur de LW5 est le rayon du cercle.

Avec le type « entier 32 bits », selon le format d'adresse de l'automate, les trois données (abscisse, ordonnée du centre et rayon) sont lues à des adresses espacées de 2 à partir de l'adresse de surveillance.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Pour la page « Visibilité », voir l'objet « Bouton de bit ».
