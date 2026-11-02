# Recette

Dans l'industrie, une recette décrit les proportions des matières utilisées pour fabriquer un produit : c'est un ensemble de valeurs de paramètres utilisées en production. Par exemple, la fabrication du pain nécessite une recette de base, qui peut indiquer le poids ou la proportion de chaque ingrédient : eau, farine, sucre, œufs, huile, etc. Elle peut aussi prévoir des ingrédients facultatifs (fruits, noix, chocolat…) ajoutés à la recette de base pour obtenir des pains de saveurs différentes. Autre exemple, dans une usine sidérurgique, une recette peut être un jeu de paramètres machine. Pour les machines de traitement par lots, une recette peut décrire les différentes étapes du traitement.

Une machine peut fabriquer du pain et des gâteaux, avec des pains de saveurs différentes et des gâteaux de formes variées. On appelle ici « recette » les proportions d'ingrédients d'un pain, et « fichier » l'ensemble des proportions des différentes saveurs de pain. Les enregistrements de recettes sont donc contenus dans des fichiers de recettes.

CommandHMI propose une fonction de configuration des recettes, accessible par le menu « Recette » ou le gestionnaire de projet : elle ouvre la boîte de configuration des recettes, où l'on ajoute un nouveau groupe de recettes, comme sur la figure 7-32 :

<img src="../../setting/formula.files/formula1334.png" width="515" />

Figure 7-32 Propriétés d'une recette continue

• Nom : nom du fichier de recettes courant.

• Description : description du fichier de recettes courant ;

• Longueur de la recette : longueur et nombre d'adresses lues par la recette courante. Les adresses de la table de recettes sont attribuées automatiquement à la suite par le système et ne sont pas modifiables. Longueur maximale d'une recette : 4096.

• Nombre total : nombre de recettes, 512 au maximum ;

• Groupe de recettes modifiable dans l'IHM : autorise la modification de la recette dans l'IHM.

<img src="../../setting/formula.files/formula1872.png" width="794" />

Figure 7-33 Propriétés d'une recette discrète

• Nom du groupe : nom du fichier de recettes courant.

• Description de la recette : description du fichier de recettes courant ;

• Indicateur d'écriture de recette terminée : une fois la recette courante écrite dans l'automate, l'adresse de bit indiquée passe à 1 ;

• Groupe de recettes modifiable dans l'IHM : autorise la modification de la recette dans l'IHM.

<img src="../../setting/formula.files/formula2225.png" width="130" />

Remarque : longueur de la recette \* octets du type de données \* nombre total &lt;= 512 Ko

• Type de données : type de données du registre ;

• Écrire la recette dans l'automate : adresse du registre de l'automate associé à la recette ;

• Lire la recette depuis l'automate : adresse du registre de l'automate associé à la recette ;

• Mémoire de recettes : plage d'adresses mémoire des recettes dans l'IHM, générée automatiquement et non modifiable ;

• Recette courante : adresses mémoire de la recette dans l'IHM et registres de l'automate, générées automatiquement dans l'ordre et non modifiables ;

• Registre du numéro de recette : les recettes sont numérotées automatiquement dans l'ordre, sans modification possible ; ce numéro correspond à l'ordre des noms de recettes dans les données.

Données d'une recette continue, voir figure 7-33 :

<img src="../../setting/formula.files/formula2990.png" width="514" />

Figure 7-34 Onglet des données d'une recette continue

• Nom : nom de la recette courante ;

• Données : saisit et affiche la valeur de chaque adresse de la recette courante ;

• Copier les données de recette : copie les données de la recette source vers la recette de destination. « OK » enregistre la recette courante, « Annuler » ferme la boîte. Une fois les recettes configurées, on peut créer les écrans pour les utiliser dans l'IHM.

Exemple d'utilisation des recettes :

1\. Créez une configuration de recettes comme décrit ci-dessus. Le résultat est présenté sur la figure 7-34 :

<img src="../../setting/formula.files/formula3531.png" width="515" />

Figure 7-35  Copie des données d'une recette continue

Cette recette comprend 4 sous-recettes de 16 éléments chacune. Elles sont stockées de RWI: 1 à RWI: 16 dans la mémoire de l'IHM.

2. Une fois les recettes configurées, on peut les afficher à l'écran, les modifier ou les télécharger directement dans l'automate. On utilise pour cela les objets suivants.

• Affichage de la recette : cliquez sur « Affichage/saisie numérique » <img src="../../setting/formula.files/formula3946.png" width="23" /> (voir « Affichage/saisie numérique »)

Choisissez l'adresse mémoire interne RWI: 0 pour créer un objet d'affichage/saisie numérique dans l'écran. La valeur saisie et affichée est le numéro de recette : RWI0 = 0 correspond à la recette n° 1, RWI0 = 1 à la recette n° 2, etc.

• Cliquez sur le bouton de fonction <img src="../../setting/formula.files/formula4264.png" width="21" /> : voir « Bouton de fonction » pour son utilisation.

Avec les fonctions correspondantes, on peut créer des boutons pour écrire la recette dans l'automate, la lire depuis l'automate, l'enregistrer, et choisir la recette précédente ou suivante.

Plusieurs groupes de recettes : CommandHMI permet d'utiliser plusieurs groupes de recettes, mais dix au maximum ; au-delà, un message de limite s'affiche, comme sur la figure 7-34-2

<img src="../../setting/formula.files/formula4682.png" width="248" />

Figure 7-35-1

<img src="../../setting/formula.files/formula4698.png" width="321" />

Figure 7-35-2

LW61141 sert à saisir le groupe de recettes, RWI0 restant utilisé pour le numéro de recette. Pour choisir une recette, il faut donc régler à la fois LW61141 et RWI0. Par exemple, groupe 0 dans LW61141 et numéro 2 dans RWI0 : on choisit les données de la recette 2 du groupe 0.

3. Avec ces opérations, on peut créer un écran comme celui de la figure 7-35 :

On suppose que l'adresse d'écriture et de surveillance est D0, que la recette a une longueur de 16 et qu'il y a 4 recettes au total.

<img src="../../setting/formula.files/formula5250.png" width="746" />

Figure 7-36 Résultat de la recette

Les boutons de fonction et les affichages/saisies numériques permettent de modifier, enregistrer, lire et écrire facilement les recettes. Points à surveiller :

• La liste des recettes doit être créée avant d'utiliser les fonctions de recette.

• Lors de la saisie des paramètres de recette, attention au type de données : une donnée 16 bits occupe un mot, une donnée 32 bits deux mots. Choisissez un type de données cohérent. Attention particulièrement aux adresses 32 bits : une donnée 32 bits occupant deux mots, évitez le chevauchement des adresses d'écriture et de surveillance.

• L'adresse RWI0 est réservée et sert uniquement à changer de numéro de recette. RWI0 = 0 indique la première recette, etc.

• Les adresses des paramètres de recette sont consécutives.

Données d'une recette discrète, voir figure 7-33 :

<img src="../../setting/formula.files/formula6181.png" width="795" />

Figure7-41  Onglet des données d'une recette discrète

• Nombre total de recettes : nombre de recettes, 128 au maximum ;

• Langue : permet de définir les noms d'éléments et de recettes dans chaque langue.

• Nom de la recette : modifie le nom de la recette courante, par exemple « recette1 », « recette2 ».

• Nouveau : ouvre la boîte « Élément de recette » pour créer un élément, comme ci-dessous.

  <img src="../../setting/formula.files/formula6495.png" width="517" />

Figure7-42  Boîte de création d'un élément de recette discrète

• Supprimer : supprime l'élément de recette courant.

• Supprimer tout : supprime tous les éléments de cette recette.

• Modifier : ouvre la boîte « Élément de recette » de l'élément courant pour en modifier les informations.

• Exporter : ouvre une boîte « Enregistrer sous » pour enregistrer la recette en fichier \*.csv, avec le chemin et le nom choisis.

• Importer : ouvre une boîte d'ouverture pour choisir un fichier \*.csv comme recette courante.
