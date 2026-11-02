# Bargraphe

Le bargraphe sert principalement à représenter sous forme de barres l'évolution en temps réel de valeurs numériques, pour une lecture plus visuelle. Il peut représenter l'évolution des registres de données de l'automate ou d'autres équipements connectés, ainsi que celle de toute grandeur analogique d'un procédé. Voir la figure ci-dessous.

<img src="../../../configuration-guide/basic-control/bar.files/image006.jpg" width="535" alt="2018_11_20_14_27_19.jpg" />

Figure 4-101   Bargraphe

Pour ajouter un bargraphe et modifier ses propriétés :

1\. Sélectionnez l'icône Bargraphe <img src="../../../configuration-guide/basic-control/samdra8.gif" width="20" /> dans la barre d'outils ou le menu Outils. La boîte de dialogue de la figure 4-102 s'ouvre.

2\. Réglez les propriétés du bargraphe dans la boîte de dialogue, puis cliquez sur OK :

• Couleur de fond : couleur de fond du bargraphe

• Couleur de bordure : couleur de la bordure de la barre. Sur la figure 4-102, ce réglage n'a pas d'effet ; choisissez une autre « forme » pour voir la différence.

• Transparent : rend le fond de la barre transparent

• Direction : sens de remplissage de la barre, quatre directions : Haut, Bas, Gauche et Droite.

• Haut : quand la valeur de l'adresse de surveillance augmente, la barre se remplit de bas en haut

• Bas : quand la valeur de l'adresse de surveillance augmente, la barre se remplit de haut en bas

• Gauche : quand la valeur de l'adresse de surveillance augmente, la barre se remplit de droite à gauche

• Droite : quand la valeur de l'adresse de surveillance augmente, la barre se remplit de gauche à droite

• Type de données : type de la valeur lue, c'est-à-dire adresse de mot ou de double mot.

• Adresse de surveillance : adresse du registre de données affiché dans la barre, c'est-à-dire l'adresse lue

• Maximum : valeur maximale de l'adresse surveillée (lue). Si la valeur est supérieure, la barre est pleine et ne varie plus

• Minimum : valeur minimale de l'adresse surveillée (lue). Si la valeur est inférieure, la barre est vide et ne varie plus

• Plage variable : les valeurs maximale et minimale varient dynamiquement selon l'adresse saisie par l'utilisateur ; le type de données de cette adresse est le même que le « Type de données » choisi

• Barre bipolaire : la barre peut s'afficher des deux côtés selon la valeur du registre.

• Point milieu : point milieu de la barre bipolaire.

<img src="../../../configuration-guide/basic-control/bar.files/image002.jpg" width="675" />

Figure 4-102   Boîte de dialogue Bargraphe

Par exemple, avec un maximum de 100, un minimum de 10 et un remplissage vers le haut, si la barre bipolaire est cochée et le « Point milieu » réglé à 70, l'augmentation de la valeur surveillée à partir de 0 donne l'affichage de la figure 4-103.

<img src="../../../configuration-guide/basic-control/samdra10.gif" width="534" />

Figure 4-103 Bargraphe bipolaire

3\. Modifier le bargraphe : cliquez dessus ; huit petits points verts apparaissent, que vous pouvez faire glisser à la souris pour le redimensionner.

Page « Plage » :

Cette page permet d'afficher la valeur surveillée avec des couleurs de premier plan et de fond différentes selon la plage. Les propriétés sont présentées sur la figure 4-104 :

Figure 4-104   Page Plage du bargraphe

• Afficher la plage : si cette option est cochée, l'utilisateur peut définir les limites basse et haute ainsi que les couleurs de fond correspondantes. La valeur surveillée est alors représentée avec des couleurs différentes selon ces limites.

• Plage variable : les « limites basse et haute » varient dynamiquement selon l'adresse saisie par l'utilisateur

• Limite basse : limite basse d'affichage. Si la valeur affichée est inférieure, la couleur de fond devient la couleur de fond niveau bas.

• Limite haute : limite haute d'affichage. Si la valeur affichée est supérieure, la couleur de fond devient la couleur de fond niveau haut.

<span id="OLE_LINK727"></span><span id="OLE_LINK726"></span>Une fois les réglages faits, cliquez sur « OK » pour ajouter l'objet à la zone de vue (l'écran)

<img src="../../../configuration-guide/basic-control/bar.files/image004.jpg" width="130" />

Remarque : si la valeur surveillée est entre le maximum et le minimum, les couleurs sont celles définies dans la page « Général ».

Remarque : pour la « Visibilité », voir le « Bouton de bit ».
