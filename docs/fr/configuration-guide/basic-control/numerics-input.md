# Saisie numérique

La saisie numérique est l'objet le plus utilisé, presque indispensable dans tout contrôle de procédé. Elle permet de saisir, afficher et enregistrer une valeur dans un registre de données de l'automate ou d'un autre équipement connecté : vitesse, courant, pression, etc.

La saisie numérique et l'affichage numérique ont des fonctions pratiquement identiques ; la seule différence est que la saisie numérique permet d'écrire des valeurs dans le registre de l'automate ou de l'équipement connecté, en plus de les afficher.

Pour créer une touche de saisie numérique :

Sélectionnez l'icône Saisie numérique<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input596.png" width="31" />dans la barre d'outils : une boîte de dialogue s'ouvre, comme sur la figure 4-95.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input665.png" width="662" />

Figure 4-95 Boîte de dialogue Saisie numérique

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input705.png" width="130" />

Remarque : pour Forme, Couleur de bordure, Couleur de premier plan, Couleur de fond et Motif, voir l'objet « Bouton de bit ».

Remarque : pour « Alignement », « Justification », « Décimales » et « Nombre total de chiffres », voir l'objet « Affichage numérique ».

Remarque : double-cliquez sur l'objet pour modifier son contenu et ses propriétés. Quand l'objet fonctionne sur l'IHM, un clavier à l'écran s'ouvre pour permettre la saisie de données, comme sur la figure 4-96.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1192.png" width="693" />

Figure 4-96 Clavier de saisie numérique

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1228.png" width="130" />

Remarque : avec un type de données 32 bits, l'adresse occupe 2 mots. Par exemple, si l'on écrit dans un registre de données d'un automate SIEMENS à l'adresse V10, les registres occupés sont V10 et V11 ; si un autre objet surveille aussi V11, une erreur se produit. Faites attention à l'utilisation des types 32 bits pour éviter les erreurs de données et d'adresses.

Remarque : le nombre de décimales influe sur l'affichage. Pour un type entier positif ou entier 16/32 bits, la valeur affichée est obtenue en décalant la virgule de la valeur lue du nombre de décimales défini : si la valeur lue est 212 avec 2 décimales, 2.12 est affiché. Pour un type flottant 32 bits, la valeur n'est pas décalée : seul le nombre de décimales affichées est limité. Si la valeur lue est 2.123 avec 2 décimales, 2.12 est affiché.

Remarque : le nombre total de chiffres est la somme des longueurs de la partie entière et de la partie décimale. Si la partie entière de la valeur est plus longue que prévu, elle est affichée en entier. Par exemple, pour la valeur 2123 avec 2 chiffres et 1 décimale, l'affichage indique 212.3.

• Saisie de mot de passe : les caractères saisis par l'utilisateur sont affichés sous forme de « \* » pendant la saisie et l'affichage.

• Utiliser une macro : cochez « Use Macro » pour afficher la liste des macros. L'utilisateur peut en choisir une à exécuter à l'appui sur l'objet. Seules les macros compilées figurent dans la liste.

• Nombre total de chiffres : somme des chiffres de la partie entière et de la partie décimale. Il limite la taille des valeurs saisies et affichées. Avec 4 chiffres dont 1 décimale, la valeur maximale est 999.9, valeur maximale saisissable et affichable par l'objet. Une saisie supérieure est refusée ; à l'affichage, les chiffres en trop sont ignorés et seul le nombre de chiffres défini est affiché. Exemple : 4 chiffres, 1 décimale, valeur réelle 12345 : l'objet affiche 234.5.

Page « Avancé » : elle permet de régler le gain, l'offset et le contrôle de plage des données saisies (vérification que la valeur saisie est dans la plage définie). Elle comporte aussi les options « Contrôle d'activation » et « Notification », identiques à celles de l'objet « Bouton de bit ».

Cliquez sur l'onglet « Avancé », comme sur la figure 4-97 :

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input3958.png" width="675" />

Figure 4-97 Page Avancé de la saisie numérique

• Contrôlé par bit : si cette option est cochée, l'objet n'est actif que sous certaines conditions. Si l'« État valide » est 1, l'objet n'est actif que lorsque le « Bit de contrôle » vaut 1. Si l'« État valide » est 0, il n'est actif que lorsque le bit de contrôle vaut 0. Sinon, l'objet est sans effet.

• Contrôlé par niveau utilisateur : plusieurs options peuvent être cochées. En simulation ou sur l'IHM, le système vérifie alors que le niveau de l'utilisateur courant dispose de l'autorisation.

• Raccourcis clavier : voir le bouton de bit.

• Afficher la valeur : si cette option est cochée, la valeur actuelle de l'objet est affichée dans le clavier lors de la saisie. Par exemple, si la valeur affichée est 389, la zone de saisie du clavier indique 389 ; sinon elle est vide, comme ci-dessous :

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4972.png" width="93" />

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4974.png" width="630" />

Par exemple, si les options 2 et 3 sont cochées dans le niveau effectif de la page Avancé de l'objet, et que les mots de passe utilisateur dans les paramètres de l'écran tactile sont ceux de la figure 4-98 :

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input5185.png" width="605" />

Figure 4-98 Mots de passe utilisateur dans les paramètres de l'écran tactile

Si le niveau utilisateur par défaut est NULL, l'objet n'est pas actif ; il faut alors utiliser la fonction « Changer de niveau utilisateur » d'un bouton de fonction. Par exemple, si l'utilisateur saisit 6666, correspondant au niveau 6 qui n'a que l'option 1 (ni 2 ni 3), le système indique que le mot de passe est incorrect ; s'il saisit 2222 ou 3333, ces deux utilisateurs ayant l'option 2, le mot de passe est valide et l'objet devient actif. Si le niveau par défaut est l'utilisateur 2 ou 3, l'objet est actif dès le démarrage, en simulation comme sur l'écran ; dans le cas contraire, il ne l'est pas. Le réglage par défaut est présenté ci-dessous :

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6241.png" width="266" />

Si « Changer de niveau si insuffisant » est coché, quand le niveau utilisateur ne convient pas, une fenêtre de connexion s'ouvre pour choisir un niveau adapté et se reconnecter, comme ci-dessous :

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6435.png" width="268" />

• Notification : lorsque l'objet est actif, en simulation ou sur l'écran, après un appui et une saisie de valeur au clavier, l'état défini (1 ou 0) est écrit à l'adresse « Bit de notification ».

• Mise à l'échelle : si cette option est cochée, valeur écrite = (valeur saisie au clavier - offset) / gain ; valeur affichée (valeur de l'adresse surveillée) = valeur de l'adresse surveillée × gain + offset

• Afficher la plage : si cette option est cochée, l'utilisateur peut définir les limites basse et haute ainsi que les couleurs de fond correspondantes. La valeur surveillée est alors représentée avec des couleurs différentes selon ces limites.

• Plage variable : les « limites basse et haute » varient dynamiquement selon l'adresse saisie par l'utilisateur

• Limite basse : limite basse d'affichage. Si la valeur affichée est inférieure, la couleur de fond devient la couleur de fond niveau bas.

• Limite haute : limite haute d'affichage. Si la valeur affichée est supérieure, la couleur de fond devient la couleur de fond niveau haut.

• Contrôle de plage : vérifie que la valeur saisie ne dépasse pas les valeurs maximale et minimale définies.

Une fois les réglages faits, cliquez sur « OK » pour ajouter l'objet à la zone de vue (l'écran)

• Avec le réglage de la page Général ci-dessous, le nombre est affiché en binaire mais saisi en décimal. Pour les autres types d'affichage, le type de saisie est le même que le type d'affichage.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input8099.png" width="663" />

• Une fois les propriétés réglées, cliquez sur OK : le curseur prend la forme d'une croix. Tracez un rectangle dans l'écran avec la souris pour y ajouter l'objet.
