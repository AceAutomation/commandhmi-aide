# Bouton d'écran

Le bouton d'écran sert à changer d'écran, changer de niveau utilisateur, ouvrir une fenêtre, etc. Il permet de passer d'un écran ou d'une fenêtre à un autre écran ou une autre fenêtre, en changeant éventuellement le niveau utilisateur en même temps.

• Cliquez sur l'icône <img src="../../../configuration-guide/basic-control/screen-button.files/screen-button293.png" width="30" /> dans la barre d'outils pour ouvrir la boîte de dialogue, comme sur la figure 4-80.

<img src="../../../configuration-guide/basic-control/screen-button.files/screen-button364.png" width="671" />

Figure 4-80 Boîte de dialogue Bouton d'écran

<img src="../../../configuration-guide/basic-control/screen-button.files/screen-button404.png" width="130" />

Pour Forme, Couleur de bordure, Couleur de premier plan, Couleur de fond et Motif, voir le « Bouton de bit ».

**Fonctions :**

• Ouvrir un écran : un appui sur le bouton affiche l'écran choisi. Fonction utilisable dans un écran ou une fenêtre.

• Ouvrir l'écran précédent : un appui sur le bouton revient à l'écran précédent. Fonction utilisable uniquement dans un écran.

• Fermer et ouvrir : fonction utilisable uniquement dans une fenêtre. Ferme la fenêtre courante et ouvre une autre fenêtre ou un autre écran.

• Fermer : fonction utilisable uniquement dans une fenêtre. Ferme la fenêtre courante.

**Changer de niveau utilisateur :**

• Déconnexion : ramène le niveau utilisateur courant au niveau par défaut

• Niveau utilisateur spécifié : passe au niveau utilisateur indiqué

**Déclenchement :**

• À l'appui : le changement d'écran a lieu quand l'utilisateur appuie.

• Au relâchement : le changement d'écran a lieu quand l'utilisateur relâche.

**Connexion requise si le niveau est insuffisant :**

Si l'option « Contrôlé par niveau utilisateur » est cochée dans la page « Avancé » du « Bouton d'écran » et que le « Niveau minimal effectif » a été modifié, l'objet n'est actif que si le niveau utilisateur courant est supérieur ou égal à ce niveau. Si le niveau courant est inférieur, un appui sur l'objet ouvre une zone de saisie de mot de passe, comme sur la figure 4-81 :

![](../../../configuration-guide/basic-control/screen-button.files/001.png)

Figure 4-81 Clavier de saisie du mot de passe

L'écran ne s'ouvre que si le mot de passe saisi correspond à un niveau suffisant ; le niveau utilisateur courant devient alors celui du mot de passe saisi.

**Macros :**

« Ouvrir une macro » affiche la liste des macros. L'utilisateur peut en choisir une à exécuter à l'appui sur le bouton. Seules les macros compilées figurent dans la liste.

<img src="../../../configuration-guide/basic-control/screen-button.files/screen-button2377.png" width="130" />

La page « Étiquette » du bouton d'écran est semblable à celle du « Bouton de bit ». Le bouton d'écran n'ayant qu'un état, sa page Étiquette ne comporte que le texte et l'image de l'état 1. Pour le reste, les fonctions sont identiques.

Les pages « Avancé » et « Visibilité » du « Bouton d'écran » sont identiques à celles du « Bouton de bit ».

Une fois toutes les propriétés réglées, cliquez sur « OK » : le curseur prend la forme d'une croix. Cliquez avec le bouton gauche dans la zone de vue pour ajouter l'objet à l'écran.
