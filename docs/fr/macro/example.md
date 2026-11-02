# Un bloc macro simple

Créez un projet et choisissez le modèle d'IHM. Le script réalise un calcul simple : le script d'initialisation Init remplit les objets « Affichage numérique » avec les éléments du tableau char source \[4\] = {2, 3, 4, 5} ; l'utilisateur saisit des données dans ces objets ; un appui sur le bouton « = » exécute le script ADDSUM, dont le résultat s'affiche dans l'objet prévu.

Procédure détaillée :

**Étape 1 : &lt;Créer un script&gt;**

Cliquez sur le bouton « Éditeur de scripts » à gauche de la barre d'outils : une boîte de dialogue s'ouvre.

**Étape 2 : &lt;Créer la macro Init&gt;**

Cliquez sur le bouton <img src="../../macro/example.files/example866.png" width="25" /> de l'éditeur de scripts : un nouveau script apparaît dans la liste « Non enregistrés », comme sur la figure 5-7. Modifiez le nom du script dans le champ Script et saisissez le code source dans la fenêtre d'édition, comme sur la figure 5-8

<img src="../../macro/example.files/example1100.png" width="886" />

Figure 5-7      Nouveau script

<img src="../../macro/example.files/example1126.png" width="1087" />

Figure 5-8 Édition du script Init

<img src="../../macro/example.files/example1156.png" width="130" />

Les noms de macro ne peuvent contenir que des chiffres (0-9), des lettres (a-z, A-Z) et le caractère de soulignement (\_). Saisissez le contenu de la figure 5-9 :

**Étape 3 : &lt;Réglage des variables&gt;**

Les attributs des variables (nom, type, etc.) se règlent dans la fenêtre de la figure 5-9. Double-cliquez dans la fenêtre « Variables », ou faites un clic droit et choisissez « Nouvelle variable » pour ouvrir la boîte de dialogue de la figure 5-10, où l'on règle les variables externes.

<img src="../../macro/example.files/example1677.png" width="499" />

Figure 5-9 Code du script

Nom : saisissez LW0, LW1, LW2, LW3 comme noms de variables ;

Type de données : entier 16 bits ;

Lecture/écriture : choisissez lecture et écriture ;

Adresses : LW0 = 0, LW1 = 1, LW2 = 2, LW3 = 3 ;

Le résultat est présenté sur la figure 5-10.

<img src="../../macro/example.files/example1981.png" width="843" />

Figure 5-10     Réglage des variables

**Étape 4 : &lt;Compiler le fichier source&gt;**

Il faut ensuite compiler : cliquez sur le bouton de compilation, comme sur la figure 5-11 ; le logiciel enregistre, compile, effectue l'édition de liens et vérifie les erreurs automatiquement.

<img src="../../macro/example.files/example2223.png" width="800" />

Figure 5-11    Fenêtre de sortie

Quand la fenêtre de sortie affiche « 0 errors! Compile successfully », la macro est créée et ajoutée automatiquement à la liste des scripts compilés ; sinon, un message d'erreur s'affiche et la macro est placée dans la liste des compilations échouées. Corrigez la macro jusqu'à ce que la compilation réussisse.

**Étape 5 : &lt;Créer le script ADDSUM&gt;**

Répétez les étapes 2 à 4 pour créer le script ADDSUM, comme sur la figure 5-13

&lt;1&gt; : saisissez « ADDSUM » comme nom de script.

&lt;2&gt; : saisissez le contenu entouré dans la fenêtre d'édition du code.

&lt;3&gt; : réglez les attributs des variables dans la fenêtre des variables.

&lt;4&gt; : cliquez sur le bouton Compiler.

<img src="../../macro/example.files/example2991.png" width="1168" />

Figure 5-13    Création du script ADDSUM

**Étape 6 : &lt;Éditer les objets&gt;**

&lt;1&gt;. Placez les objets dans l'écran du projet et ajustez leur taille, comme sur la figure 5-14.

<img src="../../macro/example.files/example3164.png" width="558" />

Figure 5-14    Disposition des objets

&lt;2&gt;. Réglez les propriétés des objets

Faites un clic droit sur l'objet « Saisie numérique » et réglez l'adresse et les attributs de chaque objet, comme sur la figure 5-15.

<img src="../../macro/example.files/example3375.png" width="660" />

Figure 5-15    Propriétés de la saisie numérique

Les adresses des variables LW0, LW1, LW2, LW3 et SumLW doivent correspondre à l'« adresse d'écriture » (figure 5-15) de chaque objet. Cliquez sur « OK » pour enregistrer.

&lt;3&gt;. Réglez les propriétés du bouton de bit

<img src="../../macro/example.files/example3658.png" width="661" />

Figure 5-16 (Propriétés du bouton de bit)

&lt;4&gt;. Propriétés du temporisateur

Choisissez le script Init et cliquez sur « OK » pour enregistrer.

<img src="../../macro/example.files/example3792.png" width="661" />

Figure 5-17    Propriétés du temporisateur

&lt;5&gt;. Dans la page « Étiquette » -&gt; « Texte » du bouton de fonction, saisissez le caractère « + » dans la zone de texte, comme sur la figure 5-18.

<img src="../../macro/example.files/example3963.png" width="662" />

Figure 5-18    Propriétés du bouton de fonction

**Étape 7 : Compiler et télécharger dans l'IHM**

&lt;1&gt; : cliquez sur l'icône de compilation.

<img src="../../macro/example.files/example4101.png" width="64" />

Figure 5-19    Compilation du projet

&lt;2&gt; : choisissez « Téléchargement (D) -&gt; Téléchargement USB (D) », puis cliquez sur « Télécharger » dans la boîte de dialogue. Redémarrez l'IHM.

Vous pouvez aussi utiliser le bouton Compiler et télécharger.

**Étape 8 : &lt;Test du résultat&gt;**

Après le redémarrage de l'IHM, l'écran de la figure 5-20 s'affiche.

En effet, au démarrage, le script Init est le premier exécuté par le temporisateur.

<img src="../../macro/example.files/example4642.png" width="484" />

Figure 5-20    Affichage des valeurs initiales

Saisissez par exemple « 31,42,53,64 » dans les objets « Affichage numérique » et appuyez sur « = » : le script ADDSUM est exécuté et affiche 190, comme sur la figure 5-21 :

<img src="../../macro/example.files/example5009.png" width="481" />

Figure 5-21     Affichage du résultat

L'édition, la compilation, le téléchargement et le test du script sont ainsi terminés avec succès.
