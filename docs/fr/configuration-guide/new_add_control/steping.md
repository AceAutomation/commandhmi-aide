# Bouton pas à pas

Cette commande crée un bouton pas à pas dans l'écran courant, qui fait défiler cycliquement les états. Cliquez sur l'icône<img src="../../../configuration-guide/new_add_control/steping.files/image002.jpg" width="31" /> pour ouvrir la boîte de dialogue de la figure 4-113 :

<img src="../../../configuration-guide/new_add_control/steping.files/image004.jpg" width="675" />

Figure 4-113   Boîte de dialogue Bouton pas à pas

Ordre des états : sens d'affichage du texte sur l'objet

Par exemple, avec 3 états, les textes des états 0, 1 et 2 sont respectivement 0, 1, 2.

• De gauche à droite : objet horizontal, texte de gauche à droite : 0, 1, 2

• De droite à gauche : objet horizontal, texte de droite à gauche : 2, 1, 0

• De haut en bas : objet vertical, texte de haut en bas : 0, 1, 2

• De bas en haut : objet vertical, texte de bas en haut : 2, 1, 0

Type d'état : voir le « Voyant multi-états ».

État courant : couleur de fond et couleur du texte de l'état courant.

Pour les pages Texte et Image, voir le « Voyant multi-états ».

Pour la page « Avancé » et les raccourcis clavier, voir le bouton de bit.

Par exemple, avec le type d'état « Valeur », l'adresse d'écriture LW1, 3 états et les textes 0, 1 et 2 pour les états 0, 1 et 2 : une fois le projet chargé dans l'IHM, chaque appui sur l'objet fait passer l'état de 0 à 2 en boucle, et la valeur correspondante est écrite dans LW1.
