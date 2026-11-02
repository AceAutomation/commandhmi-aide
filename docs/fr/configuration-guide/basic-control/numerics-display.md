# Affichage numérique

L'affichage numérique est un objet très courant qui affiche la valeur d'un registre de données de l'automate ou d'un autre équipement connecté : vitesse, courant, pression, etc.

Sélectionnez l'icône Affichage numérique<img src="../../../configuration-guide/basic-control/numerics-display.files/image002.jpg" width="30" /> dans la barre d'outils : une boîte de dialogue s'ouvre, comme sur la figure 4-91 :

Figure 4-91 Boîte de dialogue Affichage numérique

Dans cette boîte de dialogue, vous réglez l'affichage de la valeur du registre de données de l'automate ou de l'équipement connecté : nombre de chiffres, décimales, taille de police, couleur, alignement et justification.

• Type de données : choisissez le type correspondant à la valeur du registre surveillé.

• Type d'affichage : choisissez le format d'affichage selon les besoins du projet.

• Adresse de surveillance : adresse lue. L'objet affiche la donnée contenue dans ce registre de l'automate ou de l'équipement connecté.

• Décimales : nombre de décimales affichées.

• Police : police standard ou police numérique.

• Taille de police : taille des caractères affichés.

• Alignement : centré par défaut.

• Gauche : la valeur est affichée dans la partie gauche de la zone d'affichage.

• Centre : la valeur est affichée au centre de la zone d'affichage.

• Droite : la valeur est affichée dans la partie droite de la zone d'affichage.

• Justification : suppression des zéros par défaut.

• Suppression des zéros : les zéros non significatifs ne sont pas affichés. <span id="OLE_LINK668"></span><span id="OLE_LINK669"></span>Si l'adresse surveillée contient 00123 (entier positif 16 bits), l'affichage indique 123.

• Zéros en tête : les zéros non significatifs sont affichés. Si l'adresse surveillée contient 00123 (entier positif 16 bits), l'affichage indique 00123.

• Espaces en tête : des espaces remplacent les zéros non significatifs. Si l'adresse surveillée contient 00123 (entier positif 16 bits), l'affichage indique   123.

• Couleur du texte : couleur des données affichées ;

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Remarque : pour Forme, Couleur de bordure, Couleur de premier plan, Couleur de fond et Style, voir l'objet « Bouton de bit ».

Remarque : <span id="OLE_LINK678"></span><span id="OLE_LINK679"></span>double-cliquez sur l'objet pour modifier son contenu et ses propriétés. Quand l'objet fonctionne sur l'IHM, un clavier à l'écran s'ouvre pour permettre la saisie de données.

Remarque : <span id="OLE_LINK684"></span><span id="OLE_LINK685"></span>le nombre de décimales influe sur l'affichage. Pour un type entier positif ou entier 16/32 bits, la valeur affichée est obtenue en décalant la virgule de la valeur lue du nombre de décimales défini : si la valeur lue est 212 avec 2 décimales, 2.12 est affiché. Pour un type flottant 32 bits, la valeur n'est pas décalée : seul le nombre de décimales affichées est limité. Si la valeur lue est 2.123 avec 2 décimales, 2.12 est affiché.

Remarque : le nombre total de chiffres est la somme des longueurs de la partie entière et de la partie décimale. Si la partie entière de la valeur est plus longue que prévu, elle est affichée en entier. Par exemple, pour la valeur 2123 avec 2 chiffres et 1 décimale, l'affichage indique 212.3.

La page Avancé de l'affichage numérique offre des fonctions puissantes, dont la mise à l'échelle et l'affichage par plage, comme sur la figure 4-92 :

<img src="../../../configuration-guide/basic-control/numerics-display.files/image005.jpg" width="675" />

Figure 4-92    Page Avancé de l'affichage numérique

• Mise à l'échelle : si cette option est cochée, la valeur affichée est : valeur de l'adresse surveillée (lue) × gain + offset

<span id="OLE_LINK696"></span><span id="OLE_LINK697"></span>• Afficher la plage : si cette option est cochée, l'utilisateur peut définir les limites basse et haute ainsi que les couleurs de fond correspondantes. La valeur surveillée est alors représentée avec des couleurs différentes selon ces limites.

• Plage variable : les « limites basse et haute » varient dynamiquement selon l'adresse saisie par l'utilisateur

• Limite basse : limite basse d'affichage. Si la valeur affichée est inférieure, la couleur de fond devient la couleur de fond niveau bas.

• Limite haute : limite haute d'affichage. Si la valeur affichée est supérieure, la couleur de fond devient la couleur de fond niveau haut.

Par exemple, si l'on règle la couleur de fond et la couleur du texte dans la page Général et que l'on choisit les couleurs de plage comme sur la figure 4-93 :

<img src="../../../configuration-guide/basic-control/numerics-display.files/image006.jpg" width="673" />

<img src="../../../configuration-guide/basic-control/numerics-display.files/image007.jpg" width="349" />

Figure 4-93 Réglage de l'affichage par plage

Quand la valeur surveillée change, le texte et le fond de l'affichage numérique changent en conséquence, comme sur la figure 4-94 :

<img src="../../../configuration-guide/basic-control/samdra93.gif" width="508" />

Figure 4-94    Exemple d'affichage numérique

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Remarque : pour la page Visibilité, voir l'utilisation de l'objet « Bouton de bit ».

Remarque : <span id="OLE_LINK682"></span><span id="OLE_LINK683"></span>avec un type de données 32 bits, l'adresse occupe 2 mots. Par exemple, si l'on écrit dans un registre de données d'un automate SIEMENS à l'adresse V10, les registres occupés sont V10 et V11 ; si un autre objet surveille aussi V11, une erreur se produit. Faites attention à l'utilisation des types 32 bits pour éviter les erreurs de données et d'adresses.

Une fois les réglages faits, cliquez sur « OK » pour ajouter l'objet à la zone de vue (l'écran)
