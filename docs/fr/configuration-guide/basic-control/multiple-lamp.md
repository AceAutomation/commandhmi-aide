# Voyant multi-états

Le voyant multi-états affiche différents états selon la valeur de l'adresse de surveillance. Il peut afficher jusqu'à 32 états.

Cliquez sur l'icône Voyant multi-états<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image002.jpg" width="28" /> dans la barre d'outils pour ouvrir la boîte de dialogue de la figure 4-83.

Figure 4-83    Boîte de dialogue Voyant multi-états

1\. Général :

• État : l'utilisateur peut changer la valeur d'état pour modifier la couleur de bordure, de premier plan, de fond et le motif de l'objet pour chaque état

• Type d'état : (on suppose que la valeur saisie est n)

• Valeur : la valeur écrite va de zéro au nombre total d'états moins 1.

• Bit de registre : la valeur écrite est 2 puissance n.

E.g.:

<span id="OLE_LINK657"></span><span id="OLE_LINK511"></span><span id="OLE_LINK510"></span>L'adresse de surveillance (lecture) est LW3 et le nombre total d'états est 8. Cliquez sur OK pour ajouter l'objet à l'écran, ajoutez ensuite un objet de saisie numérique dont l'adresse d'écriture et de surveillance est LW3, puis enregistrez le projet.

En simulation ou sur l'écran, l'utilisateur touche l'objet de saisie numérique et saisit une valeur d'état au clavier. Si la valeur saisie est 2, l'état lu est 1 et l'objet affiche le texte de l'état 1 (défini dans la page Texte) ; de même, si LW3 reçoit la valeur 8, l'objet affiche le texte de l'état 3. Si LW3 reçoit la valeur 3, le voyant multi-états n'affiche aucun état.

• Valeurs d'état personnalisées : si cette option est cochée, un bouton « Définir les valeurs d'état » apparaît. Cliquez dessus pour ouvrir la boîte « Valeurs d'état personnalisées », comme sur la figure 4-84 :

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image004.jpg" width="333" />

Figure 4-84    Boîte de dialogue des valeurs d'état personnalisées

Dans cette boîte, la colonne « S \# » indique l'état ; la valeur sélectionnée est la valeur associée à cet état. Double-cliquez sur une valeur pour saisir celle à associer à l'état.

Par exemple : l'adresse de surveillance (lecture) est LW3 et le nombre total d'états est 8. Cliquez sur OK pour ajouter l'objet à l'écran, ajoutez un objet de saisie numérique dont l'adresse d'écriture et de surveillance est LW3, puis enregistrez le projet.

En simulation ou sur l'écran, l'utilisateur touche l'objet de saisie numérique et saisit une valeur d'état au clavier. Si la valeur saisie est 1, l'état lu est 1 et l'objet affiche le texte de l'état 1 (défini dans la page Texte) ; de même, si LW3 reçoit la valeur 33, l'objet affiche le texte de l'état 2. Si LW3 reçoit la valeur 2, le voyant multi-états n'affiche aucun état.

• Type de données : type de données de l'adresse d'écriture et de l'adresse de surveillance (lecture)

• Adresse de surveillance : adresse lue pour obtenir la valeur d'état, qui détermine l'état affiché par l'objet.

• Nombre total d'états : réglable selon les besoins, jusqu'à 32 états, de l'état 0 à l'état 31.

Par exemple, avec un type entier positif 16 bits et 32 états au total : si l'adresse surveillée vaut 0, le voyant affiche le texte et l'image de l'état 0 ; si elle vaut 5, ceux de l'état 5. Si elle vaut 60, le voyant affiche toujours l'état 31, car le nombre d'états est limité à 32.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Remarque : pour Forme, Couleur de bordure, Couleur de premier plan, Couleur de fond et Motif, voir l'objet « Bouton de bit ».

Remarque : si le « Voyant multi-états » utilise un type de données 32 bits, l'adresse occupe 2 mots. <span id="OLE_LINK673"></span><span id="OLE_LINK672"></span>Par exemple, si l'on écrit dans un registre de données d'un automate SIEMENS à l'adresse V10, les registres occupés sont V10 et V11 ; si un autre objet surveille aussi V11, une erreur se produit. Faites attention à l'utilisation des types 32 bits pour éviter les erreurs de données et d'adresses.

Remarque : le type de données doit correspondre aux données à afficher.

2\. Texte :

Cliquez sur l'onglet « Texte » des propriétés du voyant multi-états pour afficher les réglages de texte, comme sur la figure 4-85 :

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image006.jpg" width="675" />

Figure 4-85 Page Texte du voyant multi-états

Toutes les langues utilisent le texte de la première langue : option utile en multilingue, c'est-à-dire lorsque le nombre de langues défini dans « Langue » du gestionnaire de projet est supérieur à 1 ; le texte de l'objet ne change alors pas avec la langue.

<span id="OLE_LINK737"></span><span id="OLE_LINK736"></span>• Langue : option utile en multilingue. En choisissant une langue, vous pouvez saisir un texte différent pour chaque état. (Dans un bouton de fonction, choisissez « Changer de langue » et la langue cible ; en simulation ou sur l'écran, un appui sur ce bouton fait passer tous les objets avec texte dans la langue choisie.) Le texte, la police et la taille peuvent différer d'une langue à l'autre, mais la couleur, l'espacement et la position sont communs.

• Police : police du texte saisi ; chaque état et chaque langue peuvent avoir leur propre police.

• Taille de police : taille du texte saisi ; chaque état et chaque langue peuvent avoir leur propre taille.

• Couleur, Espacement, Position : couleur, espacement et alignement du texte sélectionné. Si plusieurs langues sont définies dans le gestionnaire de projet et que vous choisissez une autre langue que la langue 1 dans la page Texte, ces trois réglages sont inactifs, car ils reprennent ceux de la langue 1.

3\. Image :

Cliquez sur l'onglet Image des propriétés du voyant multi-états pour afficher les réglages de la figure 4-86.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image007.jpg" width="675" />

Figure 4-86 Page Image du voyant multi-états

Cette page permet de charger une image pour chaque état. Par défaut, aucune image n'est associée ; vous pouvez en ajouter selon vos besoins.

• Procédure : sélectionnez dans la liste l'état dont l'image doit changer, puis choisissez l'image dans la bibliothèque système ou dans un dossier Windows. En cliquant sur les différents états, les images correspondantes s'affichent en dessous. Vous pouvez aussi choisir d'ajuster ou non l'image à l'objet : sinon, la marge et la position de l'image restent modifiables pour soigner l'aspect.

• Ajuster à l'objet : si cette option est cochée, l'image prend la taille de l'objet défini dans la page Général et les options Marge et Position sont masquées ; sinon, elles apparaissent.

Si vous importez une image depuis un fichier externe, l'option « Transparent » est disponible : elle rend une couleur choisie transparente

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Remarque : pour la page Visibilité, voir l'objet « Bouton de bit ».

Une fois toutes les propriétés réglées, cliquez sur « OK » puis ajoutez l'objet dans l'écran
