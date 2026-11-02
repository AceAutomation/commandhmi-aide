# Bouton de fonction

Le bouton de fonction est un objet essentiel de l'IHM : il permet de réaliser facilement et rapidement de nombreuses fonctions. Cliquez sur <img src="../../../configuration-guide/basic-control/function-button.files/function-button143.png" width="28" /> pour ouvrir la boîte de dialogue de propriétés du bouton de fonction, comme sur la figure 4-82 :

<img src="../../../configuration-guide/basic-control/function-button.files/function-button223.png" width="660" />

Figure 4-82 Boîte de dialogue Bouton de fonction

<img src="../../../configuration-guide/basic-control/function-button.files/function-button264.png" width="130" />

Remarque : pour Forme, Couleur de bordure, Couleur de premier plan, Couleur de fond et Motif, voir l'objet Bouton de bit.

**1. Éteindre le rétroéclairage**

Avec cette fonction, un appui sur le bouton éteint le rétroéclairage, l'IHM continuant de fonctionner normalement. Pour le rallumer, il suffit de toucher l'écran à n'importe quel endroit.

**2. Acquitter l'alarme**

Avec cette fonction, un appui sur le bouton acquitte l'alarme sélectionnée

**3. Redémarrer**

Si le bouton de fonction est réglé sur Redémarrage système, un appui sur ce bouton redémarre l'écran tactile.

**4. Régler le délai de l'économiseur d'écran**

Avec cette fonction, un appui sur le bouton ouvre une fenêtre de réglage du délai de l'économiseur d'écran.

**5. Écrire la recette dans l'automate**

Avec cette fonction, un appui sur le bouton transmet la recette enregistrée dans l'IHM aux registres de données consécutifs de l'automate ou d'un autre équipement connecté (adresse d'écriture définie par le concepteur lors de la création de la recette).

**6. Lire la recette depuis l'automate**

Avec cette fonction, un appui sur le bouton lit les données de recette dans les registres de données consécutifs de l'automate ou d'un autre équipement connecté (adresse d'écriture définie par le concepteur lors de la création de la recette).

**7. Régler la date et l'heure**

Avec cette fonction, un appui sur le bouton permet de régler l'heure et la date internes.

**8. Effacer l'alarme**

Avec cette fonction, un appui sur le bouton efface l'alarme sélectionnée et acquittée.

**9. Recette précédente**

Avec cette fonction, un appui sur le bouton ouvre la recette précédant la recette courante. Si la recette courante est la première ou s'il n'y a qu'une recette, les paramètres de recette ne changent pas.

**10. Recette suivante**

Avec cette fonction, un appui sur le bouton ouvre la recette suivant la recette courante. Si la recette courante est la dernière ou s'il n'y a qu'une recette, les paramètres de recette ne changent pas.

**11. Enregistrer la recette courante**

Avec cette fonction, un appui sur le bouton enregistre comme recette courante les données des registres de données consécutifs de l'automate ou de l'équipement connecté, définis par le concepteur lors de la création de la recette.

**12. Captures d'écran**

Avec la fonction Capture d'écran, un appui sur le bouton enregistre l'écran courant sous forme d'image à l'emplacement choisi par l'utilisateur. Le nom de l'image peut être saisi par une Saisie ASCII ; il ne doit pas contenir de caractères tels que :#￥%&\*-+&lt;&gt;, et sa longueur ne doit pas dépasser 20 caractères.

**13. Paramètres système**

Avec cette fonction, un appui sur le bouton sur l'IHM ouvre l'écran des paramètres système, où l'on peut modifier l'heure système, le délai de l'économiseur d'écran, le contraste du rétroéclairage, etc.

**14. Connexion**

Avec la fonction Connexion, un appui sur le bouton ouvre une fenêtre de connexion. Après le choix du nom d'utilisateur, un clavier s'ouvre pour saisir le mot de passe et obtenir les droits d'accès.

**15. Déconnexion de l'utilisateur**

Avec cette fonction, un appui sur le bouton déconnecte l'utilisateur courant et annule ses droits : le niveau utilisateur redevient le plus bas.

**16. Son d'alarme (ON/OFF)**

Le son d'alarme retentit lorsqu'une alarme se produit. Ce bouton permet de l'activer ou de le désactiver : s'il est activé, un appui le coupe, et inversement

**17. Son au toucher (ON/OFF)**

Avec cette fonction, un appui sur le bouton active ou désactive le son au toucher : s'il est activé, un appui le coupe, et inversement.

**18. Effacer toutes les données historiques**

Les données historiques enregistrées dans l'IHM sont effacées.

**19. Effacer les alarmes historiques**

Les alarmes historiques enregistrées dans l'IHM sont effacées.

**20. Déverrouiller la protection IHM**

Saisissez le mot de passe pour désactiver la protection IHM.

**21. Lire et enregistrer la recette**

Lit et enregistre la recette.

**22. Fonction de réserve**

Fonction de réserve uniquement ; elle n'effectue aucune opération.

**23. Recharger la recette**

Recharge les données de recette de la mémoire flash dans les adresses RWI correspondantes.

**24. Changer de langue**

Bascule le texte de tous les objets dans la langue spécifiée

**25. Imprimer l'écran sur une imprimante série**

Imprime l'écran défini sur une imprimante série. Le paramétrage du pilote d'imprimante se trouve dans « Paramètres IHM » -&gt; « Paramètres d'imprimante et de téléchargement », dans le volet gauche du logiciel.

**26. Configuration IP des équipements esclaves**

Cette fonction nécessite le « Mode étendu », réglable dans les « Propriétés du port de communication ». Pour une communication Ethernet multi-équipements, il faut ajouter devant l'objet concerné un numéro de station et le registre qui contrôle ce numéro. Pendant l'exécution du projet sur l'IHM, un appui sur cet objet affiche le numéro de station défini dans la boîte « IP config » ; réglez alors les paramètres IP correspondant à ce numéro de station pour réaliser la communication Ethernet multi-équipements.

**27. Fonctions des interrupteurs DIP 1 et 3**

Fonctions disponibles quand les interrupteurs DIP 1 et 3 sont sur ON : principalement réglage IP, réglage de l'heure système et paramètres de rétroéclairage. Après réglage, cliquez sur OK pour redémarrer.

Utiliser une macro : en cochant « Use macro », la liste des macros s'affiche ; l'utilisateur peut en choisir une à exécuter avec la fonction. Seules les macros compilées figurent dans la liste.

<img src="../../../configuration-guide/basic-control/function-button.files/function-button6119.png" width="130" />

Remarque : en passant à l'écran système, le système ferme le projet courant ; au retour de l'écran système, le projet redémarre sur son écran de démarrage.

Remarque : la page « Étiquette » du bouton de fonction est semblable à celle du « Bouton de bit », sauf qu'elle ne comporte ni Texte état 1 ni Image état 1, le bouton n'ayant qu'un seul état.

Remarque : les pages Avancé et Visibilité du bouton de fonction sont identiques à celles du bouton de bit ; pour les raccourcis clavier, voir le bouton de bit.

Remarque : les opérations Recette précédente, Recette suivante, Enregistrer la recette, Lire et enregistrer la recette ne s'appliquent qu'au groupe de recettes courant. Pour agir sur un autre groupe, réglez d'abord LW61141.

Remarque : effacer les données historiques efface tous les groupes de données historiques.

Une fois toutes les propriétés réglées, cliquez sur « OK » pour ajouter le bouton à la zone de vue (l'écran)
