# Bloc de flux à angles

Le bloc de flux à angles fonctionne comme le bloc de flux, mais permet en plus de dessiner des angles, ce qui le rend plus souple.

 Cliquez sur l'icône <img src="../../../configuration-guide/new_add_control/corner-flow-block.files/image001.jpg" width="74" alt="ScreenShot00054.jpg" /> dans la boîte à outils et placez le curseur dans la zone de l'écran : il prend la forme d'une croix. Cliquez au point de départ du bloc, déplacez la souris : une ligne relie le point de départ à la croix ; cliquez au point d'arrivée pour obtenir le premier segment. Le point d'arrivée devient le point de départ du segment suivant, avec un angle de 90°. On obtient ainsi un bloc de flux à plusieurs segments. Un clic droit termine le dessin. Voir la figure 4-134.

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block1511.png" width="405" />

Figure 4-134  Bloc de flux à angles

Une fois le dessin terminé, double-cliquez sur le bloc ou faites un clic droit et choisissez Propriétés : la boîte de dialogue du bloc de flux à angles s'ouvre, comme sur la figure 4-135.

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block1691.png" width="661" />

Figure 4-135 Boîte de dialogue Bloc de flux à angles

Couleur : couleurs du bloc de flux.

• Couleur de premier plan du bloc : cliquez sur le bouton de couleur pour la régler ;

• Couleur de fond du bloc : cliquez sur le bouton de couleur pour la régler ;

• Couleur de premier plan du tuyau : cliquez sur le bouton de couleur pour la régler ;

• Couleur de fond du tuyau : cliquez sur le bouton de couleur pour la régler ;

• Couleur de bordure : cliquez sur le bouton pour régler la couleur de bordure de l'objet ;

• Motif : motif de l'objet ; « Plein » par défaut.

• Adresse de déclenchement : adresse qui commande l'arrêt ou l'écoulement du bloc ; quand elle vaut 1, le bloc s'écoule.

• Attributs : propriétés du bloc de flux, comme la direction et la vitesse.

• Mode d'affichage : « Horizontal » pour un écoulement horizontal, « Vertical » pour un écoulement vertical.

• Direction : en mode « Horizontal », « Gauche » ou « Droite » ; sinon, « Haut » ou « Bas ».

• Inverser le sens d'écoulement par l'adresse de déclenchement : quand la valeur de l'« Adresse de déclenchement » est égale à l'« État effectif » défini, le sens d'écoulement est inversé.

Par exemple, avec la direction « Gauche », cette option cochée, l'adresse LB2 et l'état effectif 1 : quand LB2 vaut 1, le bloc s'écoule vers la « Droite » ; quand LB2 vaut 0, il revient vers la « Gauche ».

• Blocs : nombre d'unités de flux, de 1 à 30 ;

• Sans bordure : si cette option est cochée, les bords du bloc sont masqués.

• Vitesse : fixe ou dynamique

• Vitesse fixe : rapide, moyenne ou lente.

• Vitesse dynamique : la vitesse dépend de la valeur d'une adresse de mot, comprise entre 1 et 10. À 0, le bloc ne s'écoule pas ; à 1, il s'écoule à la vitesse la plus lente ; à 10, à la vitesse la plus rapide.

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block3818.png" width="130" />

Pour la page « Visibilité », voir l'objet « Bouton de bit ».
