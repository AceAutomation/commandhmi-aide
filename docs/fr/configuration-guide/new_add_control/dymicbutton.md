# Animation

Animation : vous définissez à l'avance la trajectoire d'un élément, puis commandez sa position sur cette trajectoire avec deux registres : l'un pour l'état, l'autre pour la position.

Son icône dans la barre d'outils est : <img src="../../../configuration-guide/new_add_control/dymicbutton.files/image002.jpg" width="28" /> ; dessinez les points de passage dans la zone de l'écran (64 points au maximum), puis faites un clic droit pour terminer.

Double-cliquez sur l'objet pour ouvrir la boîte de dialogue de la figure 4-118 :

Figure 4-118   Page Général de l'animation

Nombre total d'états : nombre d'états de l'élément

Position :

Registre : avec « Registre », l'état et la position de l'élément sont commandés par les données d'un registre.

Adresse de lecture : si l'état et la position dépendent d'un registre, l'adresse de lecture doit être correctement définie. Son format est indiqué dans le tableau ci-dessous.

|           |                            |                              |
|-----------|----------------------------|------------------------------|
| Type de données | Adresse de contrôle de l'état | Adresse de contrôle de la position |
| 16 bits   | Adresse                    | Adresse + 1                  |
| 32 bits   | Adresse                    | Adresse + 2                  |

Par exemple, avec le registre \[LW100\] et le format « entier positif 16 bits », \[LW100\] contient l'état de l'élément et \[LW101\] sa position. Sur la figure 4-119, \[LW100\] = 2 et \[LW101\] = 1 : l'élément est à l'état 2 et à la position 1.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image004.gif" width="520" />

Figure 4-119

• Horloge : avec « Horloge », l'élément change automatiquement d'état et de position. L'option « Contrôle automatique de la position » définit le mode de changement d'état et de position.

• Vitesse : vitesse de changement de position, en dixièmes de seconde. Par exemple, 10 signifie un changement de position par seconde.

• Retour : soit un élément à quatre positions, 0 à 3. Si cette option n'est pas cochée, l'élément revient à la position initiale (0) après la dernière position (3), puis recommence le même cycle.

Position 0-&gt; position 1-&gt; position 2-&gt; position 3-&gt; position 0-&gt; position 1-&gt; position 2...

Si cette option est cochée, l'élément revient en arrière après la dernière position. L'ordre de déplacement est le suivant :

Position 0-&gt; position 1-&gt; position 2-&gt; position 3-&gt; position 2-&gt; position 1-&gt; position 0...

Changement d'état : mode de changement d'état

Au choix : Selon la position ou Selon le temps. « Selon la position » : l'état change avec la position.

« Selon le temps » : la position et l'état changent selon les points de l'écran.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image005.jpg" width="484" />

Figure 4-120   Contrôle automatique de la position

**Page Profil :**

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image006.jpg" width="484" />

Taille du graphique :

• Largeur : largeur de l'<span id="OLE_LINK520"></span><span id="OLE_LINK521"></span>objet graphique de la page Général.

• Hauteur : hauteur de l'objet graphique de la page Général.

• Trajectoire : sélectionnez les points de la trajectoire pour ajuster leur position.

Pour les pages « Texte » et « Image », voir le « Voyant multi-états ».

<span id="OLE_LINK676"></span><span id="OLE_LINK677"></span>Pour la page « Visibilité », voir le « Bouton de bit ».
