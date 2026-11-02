# Bouton de bit

Le bouton de bit permet de commander et d'afficher l'état ON/OFF ou 1/0 d'une adresse de bit de l'équipement connecté à l'écran tactile. C'est l'objet le plus fondamental et le plus utilisé.

Pour créer un bouton de bit :

1\. Cliquez sur l'icône Bouton de bit<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton263.png" width="30" /> dans la barre d'outils pour ouvrir la boîte de dialogue des propriétés, comme sur la figure 4-68 :

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton381.png" width="664" />

Figure 4-68 Boîte de dialogue Bouton de bit

2\. La boîte de dialogue comporte quatre pages : Général, Étiquette, Avancé et Visibilité.

Forme : cliquez sur le bouton Forme pour choisir la forme graphique de l'objet, comme sur la figure 4-69

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton600.png" width="472" />

Figure 4-69 Fenêtre de choix de forme

• Couleur de bordure : pour une forme avec bordure, cliquez sur ce bouton pour choisir une autre couleur de bordure.

• Couleur de premier plan : pour la modifier, cliquez sur ce bouton et choisissez une couleur dans la palette (la couleur de premier plan n'agit que si un style de dégradé est choisi).

• Couleur de fond : pour la modifier, cliquez sur ce bouton et choisissez une couleur dans la palette.

• Motif : la liste déroulante propose 21 motifs, comme sur la figure 4-70 :

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton1213.png" width="662" />

Figure 4-70 Modifier la forme et le motif

• Mise à 1 (Set) : avec cette fonction, une fois le projet chargé dans l'IHM, un appui sur le bouton met l'adresse d'écriture à 1, c'est-à-dire à ON sur l'équipement connecté, et l'état 1/ON est affiché.

• Mise à 0 (Reset) : avec cette fonction, une fois le projet chargé dans l'IHM, un appui sur le bouton met l'adresse d'écriture à 0, c'est-à-dire à OFF sur l'équipement connecté, et l'état 0/OFF est affiché.

• Impulsionnel (Inching) : on peut choisir « 1 à l'appui » ou « 0 à l'appui ». Avec « 1 à l'appui », l'adresse d'écriture passe à 1/ON quand on appuie sur le bouton et l'état 1/ON est affiché ; elle repasse à 0/OFF au relâchement et l'état 0/OFF est affiché. Avec « 0 à l'appui », l'adresse d'écriture passe à 0/OFF à l'appui et l'état 0/OFF est affiché ; elle repasse à 1/ON au relâchement et l'état 1/ON est affiché.

• Inversion (Alternate) : si l'état courant du bouton est 0/OFF, un appui met l'adresse d'écriture à 1/ON et l'état 1/ON est affiché ; si l'état courant est 1/ON, un appui la met à 0/OFF et l'état 0/OFF est affiché. L'état change à chaque appui.

• Adresse d'écriture : cliquez sur l'icône Clavier à côté de « Adresse d'écriture » pour saisir l'adresse. CommandHMI propose les symboles d'adresse selon l'équipement connecté. Par exemple, pour un automate MITSUBISHI de la série FX-2N : X désigne une entrée, Y une sortie, M un relais interne, C un compteur (état), T une temporisation (état), D un registre de données, C\* un compteur (valeur), T\* une temporisation (valeur). Autre exemple, pour un SIEMENS S7-200 : I désigne une entrée, Q une sortie, M un mémento, V un registre de données. Voir la figure 4-71 :

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton3963.png" width="251" />

Figure 4-71 Saisie de l'adresse

Le concepteur peut ainsi écrire l'état courant du bouton de bit dans l'adresse voulue de l'automate ou d'un autre équipement. L'adresse d'écriture ou d'affichage vaut 0/OFF quand le bouton est à l'état 0/OFF, et 1/ON quand il est à l'état 1/ON.

• Surveillance : cochez « Monitor » pour afficher l'« Adresse de surveillance » : le bouton de bit affiche alors l'évolution de cette adresse. Elle vaut 0/OFF quand le bouton est à l'état 0/OFF, et 1/ON quand il est à l'état 1/ON. L'adresse de surveillance peut être différente de l'adresse d'écriture. Par exemple, avec la fonction Mise à 1, un appui met l'adresse d'écriture à 1/ON ; mais si l'adresse de surveillance est alors à 0/OFF, le bouton affiche toujours l'état 0/OFF. En général, on choisit « Adresse de surveillance identique à l'adresse d'écriture » pour afficher directement la valeur écrite.

• Macro : en cochant « Use Macro », la liste des macros s'affiche. L'utilisateur peut choisir une macro à exécuter à l'appui sur le bouton. Seules les macros compilées figurent dans la liste.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5308.png" width="130" />

Si Surveillance n'est pas cochée, l'état affiché du bouton ne change pas, même quand on le touche.

**Étiquette**

Dans l'onglet Étiquette, les propriétés du Texte état 0 sont affichées, comme sur la figure 4-72 :

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton5512.png" width="664" />

Figure 4-72 Page Étiquette du bouton de bit

Cette page comporte quatre éléments : « Texte état 0 », « Texte état 1 », « Image état 0 » et « Image état 1 ».

• Texte état 0, Texte état 1 : permettent de modifier la police, la taille, la marge, la couleur et la position du texte de l'état 0 ou 1. CommandHMI propose aussi une fonction de copie des attributs de l'un vers l'autre, pratique et rapide.

• Tous les textes dans la première langue : option utile en multilingue (« Langue » dans le gestionnaire de projet). Si le nombre de langues est supérieur à 1, cochez cette option pour que le contenu de l'objet ne change pas avec la langue.

• Langue : option utile en multilingue. Saisissez le contenu dans chaque langue. (Dans un bouton de fonction, choisissez « Changer de langue » et la langue cible ; en simulation ou sur l'IHM, tous les objets avec texte s'affichent alors dans la langue choisie.) Le texte, la police et la taille peuvent différer d'une langue à l'autre, mais la couleur, l'espacement et la position sont communs

• Police : police du texte ; chaque langue peut avoir sa propre police.

• Taille de police : taille du texte ; chaque langue peut avoir sa propre taille.

• Couleur, Marge, Position : couleur, marge et alignement du texte sélectionné. En multilingue, ces options sont celles de la langue 1 et ne sont pas modifiables pour les autres langues.

• Image état 0, Image état 1 : vous pouvez ajouter des images de différents formats pour chaque état, selon la « Source d'image ». L'image choisie est ajoutée automatiquement à la page « Général ». Si « Ajuster à la taille de l'objet » est coché, l'image prend la taille de l'objet.

• Ajuster à la taille de l'objet : si cette option est cochée, l'image prend la taille de l'objet ; les options Marge et Position sont masquées.

• Si vous importez une image depuis un fichier externe, l'option « Transparence » permet de rendre une couleur transparente

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton7699.png" width="130" />

Si « Clignotement » est coché, l'objet clignote selon l'état ON/OFF. La période de clignotement par défaut est de 1 s. Pour la modifier, double-cliquez sur « Paramètres IHM » dans le « Gestionnaire de projet » et changez la « Fréquence de clignotement ».

Sélectionnez la page « Avancé » pour afficher les propriétés avancées, comme sur la figure 4-73

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8062.png" width="660" />

Figure 4-73  Page Avancé du bouton de bit

• Contrôlé par bit : si cette option est cochée et que l'« État valide » est 1, le bouton n'est actif que lorsque le « Bit de contrôle » vaut 1. Si l'« État valide » est 0, il n'est actif que lorsque le bit de contrôle vaut 0. Sinon, le bouton est sans effet.

• Contrôlé par niveau utilisateur : plusieurs options peuvent être cochées. En simulation ou sur l'IHM, le système vérifie alors que le niveau de l'utilisateur courant dispose de l'autorisation.

Par exemple, si les options 2 et 3 sont cochées dans le niveau effectif de la page Avancé de l'objet, et que les mots de passe utilisateur dans les paramètres de l'écran tactile sont ceux de la figure 4-74 :

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton8900.png" width="692" />

Figure 4-74 Mots de passe utilisateur dans les paramètres de l'écran tactile

Si le niveau utilisateur par défaut est NULL, l'objet n'est pas actif ; il faut alors utiliser la fonction « Changer de niveau utilisateur » d'un bouton de fonction. Par exemple, si l'utilisateur saisit 6666, correspondant au niveau 6 qui n'a que l'option 1 (ni 2 ni 3), le système indique que le mot de passe est incorrect ; s'il saisit 2222 ou 3333, ces deux utilisateurs ayant l'option 2, le mot de passe est valide et l'objet devient actif. Si le niveau par défaut est l'utilisateur 2 ou 3, l'objet est actif dès le démarrage, en simulation comme sur l'écran ; si c'est l'utilisateur 6, il ne l'est pas. Le réglage par défaut est présenté ci-dessous :

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton9956.png" width="459" />

Si « Changer de niveau si insuffisant » est coché, quand le niveau utilisateur ne convient pas, une fenêtre de connexion s'ouvre pour choisir un niveau adapté et se reconnecter, comme ci-dessous :

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton10150.png" width="466" />

Dans CommandHMI, seuls les objets suivants disposent de cette fonction : bouton de bit, liste déroulante, saisie ASCII, bouton de fonction, saisie clavier ASCII, bouton multifonction, bouton multi-états, sélecteur de recette, bouton d'écran, bouton radio, bouton pas à pas, bouton de mot, curseur et saisie numérique ; leur utilisation est la même que pour le bouton de bit.

• Durée d'appui minimale : durée d'appui nécessaire avant réaction, en simulation ou sur l'IHM.

• Notification : lorsque l'objet est actif en simulation ou sur l'IHM, après un appui et une saisie de valeur au clavier, l'état (1 ou 0) est écrit à l'adresse « Bit de notification ».

• Registre de notification : lorsque l'objet est actif en simulation ou sur l'IHM, après un appui et une saisie de valeur au clavier, la valeur saisie est écrite à l'adresse du « registre de notification ».

• Raccourci clavier : avec cette fonction, saisissez un chiffre ou un caractère pour obtenir le même effet qu'un appui. Par exemple, avec 1, appuyer sur la touche 1 du pavé numérique en simulation, sur l'IHM ou sur un clavier externe produit le même effet.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11418.png" width="161" />

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton11420.png" width="130" />

Le niveau utilisateur par défaut est NULL, le plus bas. Le concepteur peut le changer avec la fonction « Changer de niveau utilisateur » d'un bouton de fonction, en saisissant le mot de passe correspondant.

Un appui effectif est un appui qui produit réellement un effet : mise à 1, mise à 0, impulsion, inversion réussies. Autre exemple, la saisie numérique : quand on touche l'objet, le clavier s'ouvre, mais cela ne génère pas de notification, car rien n'est encore écrit. Quitter le clavier avec ESC ne génère pas non plus de notification. Celle-ci n'a lieu que si l'on saisit une valeur comprise entre le minimum et le maximum et que l'on appuie sur ENTER.

Sélectionnez la page « Visibilité » pour afficher ses propriétés, qui définissent si l'objet est affiché ou masqué, comme sur la figure 4-75

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12372.png" width="675" />

Figure 4-75 Page Visibilité du bouton de bit

• Contrôlé par bit : si cette option est cochée et que l'état effectif est 1, le bouton de bit n'est affiché sur l'écran tactile que lorsque le bit de contrôle vaut 1 ; si l'état effectif est 0, il n'est affiché que lorsque le bit de contrôle vaut 0.

• Contrôlé par niveau utilisateur : les conditions sont les mêmes que pour l'option de la page Avancé ; le bouton de bit n'est affiché que si elles sont remplies.

<img src="../../../configuration-guide/basic-control/bitbutton.files/bitbutton12995.png" width="130" />

Si aucune de ces deux options n'est cochée, l'objet est toujours affiché sur l'écran tactile.
