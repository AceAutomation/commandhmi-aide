# Déplacement graphique

L'objet Déplacement graphique permet de déplacer un graphique de la bibliothèque ou un fichier image dans une direction donnée sur l'écran ; la valeur des variables associées commande le déplacement. Cet objet produit un effet d'animation à l'écran.

Pour ajouter l'objet Déplacement graphique et modifier ses propriétés :

Sélectionnez le bouton Déplacement graphique<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move351.png" width="35" /> dans la barre d'outils, réglez les propriétés dans la boîte de dialogue et cliquez sur OK, comme sur la figure 4-61 :

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move459.png" width="662" />

Figure 4-61 Boîte de dialogue Déplacement graphique

• Choix de l'image :

Dans la page Images, choisissez l'image à déplacer ; elle peut aussi être personnalisée.

• Adresse de surveillance :

L'adresse de surveillance du déplacement occupe trois adresses, qui correspondent au nombre total d'états, à la valeur de l'axe X et à celle de l'axe Y. Par exemple, avec l'adresse interne LW1 et le type 16 bits, les valeurs de LW1, LW2 et LW3 commandent directement le nombre d'états, le déplacement en X et le déplacement en Y ; avec le type 32 bits, le nombre d'états est en LW1, la coordonnée X en LW3 et la coordonnée Y en LW5.

• Méthode : dans les exemples suivants, l'adresse de surveillance est l'adresse interne LW1 et le type 16 bits. Chaque mode de déplacement :

• Déplacement horizontal sur l'axe X : le graphique se déplace uniquement horizontalement, sans aller sous la limite basse ni au-delà de la limite haute de l'axe X. Le nombre d'états est la valeur de LW1 et la coordonnée X celle de LW2.

• Déplacement vertical sur l'axe Y : le graphique se déplace uniquement verticalement, sans aller sous la limite basse ni au-delà de la limite haute de l'axe Y. Le nombre d'états est la valeur de LW1 et la coordonnée Y celle de LW2.

• Déplacement horizontal et vertical simultané : le graphique se déplace à la fois horizontalement et verticalement, dans les limites des axes X et Y. Le nombre d'états est la valeur de LW1, la coordonnée X celle de LW2 et la coordonnée Y celle de LW3.

• Déplacement horizontal proportionnel sur l'axe X : le graphique se déplace uniquement horizontalement, dans les limites de l'axe X. Le nombre d'états est la valeur de LW1 et la coordonnée X celle de LW2.

• Déplacement vertical proportionnel sur l'axe Y : le graphique se déplace uniquement verticalement, dans les limites de l'axe Y. Le nombre d'états est la valeur de LW1 et la coordonnée celle de LW2.

• Déplacement horizontal proportionnel inversé sur l'axe X : le graphique se déplace uniquement horizontalement, dans les limites de l'axe X. Le nombre d'états est la valeur de LW1 et la coordonnée X celle de LW2.

• Déplacement vertical proportionnel inversé sur l'axe Y : le graphique se déplace uniquement verticalement, dans les limites de l'axe Y. Le nombre d'états est la valeur de LW1 et la coordonnée celle de LW2.

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move3614.png" width="130" />

• Pour les pages « Texte » et « Image », voir l'objet « Voyant multi-états ».

• Pour la page « Visibilité », voir l'objet « Bouton de bit ».

• La modification des valeurs des deux dernières adresses de surveillance commande la position du graphique.

• La coordonnée maximale des axes X / Y correspond à la taille maximale de l'écran.
