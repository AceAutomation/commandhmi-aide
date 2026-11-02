# Affichage d'images

L'affichage d'images est une extension de l'image statique : l'image statique n'affiche qu'une image, l'affichage d'images peut en afficher jusqu'à 32. Son fonctionnement dépend du type d'état choisi par l'utilisateur.

Procédure :

Cliquez sur l'icône Affichage d'images<img src="../../../configuration-guide/basic-control/picture-display.files/image002.jpg" width="32" /> dans la barre d'outils. La boîte de dialogue de la figure 4-110 s'ouvre :

Figure 4-110   Boîte de dialogue Affichage d'images

• Bit : avec Bit, il n'y a que deux états, 0 et 1. L'adresse de surveillance est forcément une adresse de bit. L'objet affiche l'image correspondant à l'état 0 ou 1 de cette adresse.

• Valeur : avec Valeur, le nombre d'états peut atteindre 2048 et l'image affichée dépend de la valeur de l'adresse surveillée : si elle vaut 0, l'image de l'état 0 est affichée, etc.

• Défilement automatique : avec cette option, le nombre d'états peut atteindre 2048 et l'image ne dépend pas d'une adresse : il suffit de définir le nombre total d'états et la fréquence de changement. Sur l'IHM, l'objet fait défiler les images automatiquement.

<img src="../../../configuration-guide/basic-control/picture-display.files/image004.jpg" width="130" />

Remarque : la page « Image » de l'affichage d'images est semblable à celle de l'objet « Voyant multi-états ».

Remarque : pour la « Visibilité », voir l'objet « Bouton de bit ».

Une fois les réglages faits, cliquez sur « OK » pour ajouter l'objet à la zone de vue (l'écran).
