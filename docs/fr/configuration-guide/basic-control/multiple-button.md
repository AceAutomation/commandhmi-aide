# Bouton multi-états

Le bouton multi-états et le voyant multi-états ont des fonctions pratiquement identiques ; la seule différence est que le bouton multi-états permet de saisir une valeur, au lieu de se contenter d'afficher un état. Procédure :

Cliquez sur l'icône<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button271.png" width="31" />dans la barre d'outils pour ouvrir la boîte de dialogue de la figure 4-87.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button336.png" width="663" />

Figure 4-87 Boîte de dialogue Bouton multi-états

• État : l'utilisateur peut changer la valeur d'état ainsi que la couleur de bordure, de premier plan, de fond et le motif de l'objet pour chaque état

• Type d'état : (on suppose que la valeur saisie est n)

• Valeur : la valeur écrite est un nombre de zéro au nombre total d'états.

• Bit de registre : la valeur écrite est 2 puissance n.

E.g:

Choisissez « Valeur » comme type d'état, « Saisie clavier » comme mode, LW3 comme adresse d'écriture, cochez « Adresse de surveillance identique à l'adresse d'écriture » et réglez le nombre total d'états à 8. Cliquez ensuite sur OK pour ajouter l'objet à l'écran, puis enregistrez le projet.

En simulation ou sur l'écran, un appui sur l'objet ouvre un clavier de saisie de la valeur d'état. Si l'on saisit 3, la valeur écrite dans LW3 est 2 puissance 3, et l'objet affiche le texte de l'état 3 (défini dans la page Texte). Inversement, si LW3 reçoit la valeur 8, l'objet affiche le texte de l'état 3. Si LW3 reçoit la valeur 5, l'objet n'affiche aucun état.

• Valeurs d'état personnalisées : si cette option est cochée, un bouton « Définir les valeurs d'état... » apparaît, comme sur la figure 4-88 :

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1611.png" width="662" />

Figure 4-88 Bouton multi-états avec valeurs d'état personnalisées

Cliquez sur « Définir les valeurs d'état... » : la boîte « Valeurs d'état personnalisées » s'ouvre, comme sur la figure 4-89 :

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1799.png" width="333" />

Figure 4-89 Boîte de dialogue de définition des valeurs d'état

Dans cette boîte, la colonne « S # » indique l'état. La valeur de la ligne sélectionnée est la valeur associée à cet état ; double-cliquez pour la saisir.

Par exemple, choisissez « Valeurs d'état personnalisées » comme type d'état, « Saisie clavier » comme mode, LW3 comme adresse d'écriture, cochez « Adresse de surveillance identique à l'adresse d'écriture » et réglez le nombre total d'états à 8. Cliquez sur OK pour ajouter l'objet à l'écran, puis enregistrez le projet. En simulation ou sur l'écran, un appui sur l'objet ouvre un clavier de saisie. Si l'on saisit 1, la valeur écrite dans LW3 est 22 et l'objet affiche le texte de l'état 1 (défini dans la page Texte). Inversement, si LW3 reçoit la valeur 33, l'objet affiche le texte de l'état 2. Si LW3 reçoit la valeur 2, l'objet n'affiche aucun état.

• Mode : six fonctions sont proposées : « Saisie clavier », « Constante », « Incrémenter », « Décrémenter », « Incrémenter en boucle » et « Décrémenter en boucle ».

• Saisie clavier : les trois options de « Type d'état » sont disponibles. En simulation ou sur l'écran, un appui sur l'objet ouvre un clavier pour saisir la valeur, comme sur la figure 4-90 :

![](../../../configuration-guide/basic-control/multiple-button.files/001.png)

Figure 4-90 Clavier

• Constante : seule l'option « Valeur » du « Type d'état » est disponible. Un champ « Constante » apparaît pour la saisir. En simulation ou sur l'écran, un appui sur l'objet écrit cette valeur constante

• Incrémenter : seule l'option « Valeur » du « Type d'état » est disponible. En simulation ou sur l'écran, chaque appui augmente l'état de 1 ; l'incrémentation s'arrête au nombre total d'états.

• Décrémenter : seule l'option « Valeur » du « Type d'état » est disponible. En simulation ou sur l'écran, chaque appui diminue l'état de 1 ; la décrémentation s'arrête à la limite.

• Incrémenter en boucle : seule l'option « Valeur » du « Type d'état » est disponible. En simulation ou sur l'écran, chaque appui augmente l'état de 1 ; au-delà du nombre total d'états, on revient à l'état 0.

• Décrémenter en boucle : seule l'option « Valeur » du « Type d'état » est disponible. En simulation ou sur l'écran, chaque appui diminue l'état de 1 ; au-delà de l'état 0, on revient à l'état maximal.

• Type de données : type de données de l'adresse d'écriture et de l'adresse de surveillance (lecture)

• Adresse de surveillance : adresse lue pour obtenir la valeur d'état et afficher l'état courant sur l'objet.

• Nombre total d'états : nombre maximal d'états

• Utiliser une macro : si cette option est cochée, un appui sur l'objet en simulation ou sur l'écran exécute la macro choisie par l'utilisateur.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button5026.png" width="130" />

Remarque : pour Forme, Couleur de bordure, Couleur de premier plan, Couleur de fond et Motif, voir l'objet « Bouton de bit ».

Remarque : pour les pages « Texte » et « Image », voir l'objet « Voyant multi-états ».

Remarque : pour les pages « Avancé » et « Visibilité », voir l'objet « Bouton de bit » ; pour les raccourcis clavier, voir le bouton de bit.

Une fois les propriétés réglées, cliquez sur « OK » pour ajouter l'objet à la zone de vue (l'écran)
