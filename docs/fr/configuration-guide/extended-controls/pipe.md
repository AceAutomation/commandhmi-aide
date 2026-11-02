# Bloc de flux

Le bloc de flux est un graphique animé qui simule l'écoulement d'un liquide dans un tuyau. L'écoulement dépend de l'état de l'adresse de déclenchement : à 1, le bloc s'écoule ; à 0, il est immobile. La vitesse est réglable. Cliquez sur le bouton<img src="../../../configuration-guide/extended-controls/pipe.files/image002.jpg" width="28" /> de la barre d'outils : la boîte de dialogue suivante s'ouvre :

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

<img src="../../../configuration-guide/extended-controls/pipe.files/image004.jpg" width="130" />

Pour la page « Visibilité », voir l'objet « Bouton de bit ».
