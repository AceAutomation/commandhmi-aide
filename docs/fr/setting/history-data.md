# Collecteur de données historiques

Le collecteur de données historiques fonctionne avec l'objet [Affichage des données historiques](../configuration-guide/extended-controls/history-record.md) de la barre d'outils : le premier sert au réglage des paramètres, le second à l'affichage des données historiques.

Pour créer un collecteur, faites un clic droit sur « Collecteur de données historiques » et choisissez « Nouveau collecteur de données historiques » dans le menu.

Remarque : CommandHMI permet désormais plusieurs groupes de données historiques ; on peut créer jusqu'à quatre collecteurs.

Au-delà de quatre groupes, une boîte d'erreur s'affiche :

<img src="../../setting/history-data.files/image008.jpg" width="456" />

Double-cliquez sur « Collecteur de données historiques 0 » dans le gestionnaire de projet pour ouvrir la boîte de la figure 7-19 :

<img src="../../setting/history-data.files/image009.jpg" width="627" />

Figure 7-19     Boîte du collecteur de données historiques

• Nom : nom affiché dans le gestionnaire de projet.

• Longueur d'échantillonnage : nombre de données lues en mémoire à chaque fois.

• Nombre total d'échantillons : nombre de lectures.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Remarque : mémoire nécessaire = (20 + octets de tous les éléments de données selon leur type) \* nombre total d'échantillons.

« 20 » correspond aux octets occupés par l'heure et la date ;

« Octets de tous les éléments de données » est la somme des tailles des types choisis pour chaque élément de l'onglet « Éléments de données ».

Par exemple, figure 7-20 :

a, si chaque élément est de type « entier positif 16 bits », les octets de tous les éléments = 2 +2 +2 +2 +2 ; la mémoire nécessaire est (20 + 10) \* 2, soit 60 ; une donnée 16 bits occupe 2 octets, une donnée 32 bits 4 octets.

b\. Si « LH1 » et « LH3 » sont de type « entier positif 32 bits » (les adresses des « Éléments de données » s'affichent alors LH0, LH1, LH3, LH5, LH6), les octets de tous les éléments = 2 + 4 + 4 + 2 + 2 = 14 ; la mémoire nécessaire = (20 + 14) \* 2 = 68.

Adresse de lecture : adresse de début de la lecture (pour le détail, voir « Éléments de données »)

Mode d'échantillonnage :

• Périodique : lit les données à l'intervalle réglé.

• Déclenchement : lit les données quand l'adresse de déclenchement vaut 1.

• Horloge : lit les données à partir de l'heure et à l'intervalle réglés par l'utilisateur.

Traitement en cas d'échantillonnage plein : comportement quand le nombre total maximal d'échantillons est atteint.

Arrêter l'échantillonnage : arrête l'échantillonnage quand il est plein ; si l'option n'est pas cochée, les nouvelles données remplacent les plus anciennes.

Notification : met à 1 une adresse quand le nombre maximal d'échantillons est atteint.

Cliquez sur l'onglet « Éléments de données » et réglez ses propriétés, comme sur la figure 7-20 :

<img src="../../setting/history-data.files/image002.jpg" width="627" />

Figure 7-20 Éléments de données du collecteur de données historiques

Si le multilingue est activé, il faut donner un nom dans chaque langue à chaque nouvel élément ; sinon, l'élément ne peut pas être ajouté.

Dans CommandHMI, les adresses de chaque groupe de données historiques peuvent être discontinues, selon les registres LW utilisés, par exemple : S1 = LW1, S2 = LW89, S3 = LW8905.

Cliquez sur une ligne de la liste pour régler ses propriétés.

Exemple détaillé :

Dans l'onglet « Général », réglez l'adresse de lecture sur LW1, avec des registres consécutifs et une longueur d'échantillonnage de 5 ; dans l'onglet « Éléments de données », ajoutez 5 colonnes (LH0-LH4). Pour chacune, réglez le nom, l'adresse, le type de données, le nombre total de chiffres, les décimales et la mise à l'échelle.

On suppose que les noms, types de données et mises à l'échelle de LH0-LH4 sont ceux de la figure 7-20, les autres propriétés restant par défaut :

LH0 - entier positif 16 bits, mise à l'échelle avec un gain de 3 et un offset de 2

LH1 - entier positif 32 bits, mise à l'échelle avec un gain de 2 et un offset de 1

LH2 - entier 16 bits, sans mise à l'échelle

LH3 - entier 32 bits, sans mise à l'échelle

LH4 - flottant, mise à l'échelle avec un gain de 4 et un offset de 5

La longueur d'échantillonnage étant de 5 (onglet « Général »), 5 valeurs consécutives sont lues à partir de l'« Adresse de lecture ». Les adresses sont lues selon le type de données de chaque élément.

En 16 bits, les adresses lues sont consécutives ; en 32 bits, elles sont espacées. Avec la mise à l'échelle, la valeur finale est la valeur lue multipliée par le gain, plus l'offset.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Remarque : le gain de la mise à l'échelle doit être supérieur à 1 !

Selon le type de données et la mise à l'échelle de chaque élément, les adresses lues sont les suivantes :

LH0-LW1 (donnée 16 bits, adresse de lecture + 1) Valeur finale de LH0 = valeur de LW1 × 3 + 2

LH1-LW2 (donnée 32 bits, adresse de lecture + 2) Valeur finale de LH1 = valeur de LW2 × 2 + 1

LH2-LW4 (donnée 16 bits, adresse de lecture + 1) Valeur finale de LH2 = valeur de LW4

LH3-LW5 (donnée 32 bits, adresse de lecture + 2) Valeur finale de LH3 = valeur de LW5

LH4-LW7 (donnée 32 bits, adresse de lecture + 2) Valeur finale de LH4 = valeur de LW7 × 4 + 5

Cliquez ensuite sur « OK ». Cliquez sur l'icône « Affichage des données historiques » de la barre d'outils ; dans la boîte qui s'ouvre, réglez le nombre de lignes sur 5, les autres propriétés restant par défaut.

Cliquez sur « OK » : un tableau est créé automatiquement dans l'écran, comme sur la figure 7-21 :

Figure 7-21 Tableau de l'affichage des données historiques

Lecture du tableau ci-dessus :

• Date : date de lecture de la valeur

• Heure : heure de lecture de la valeur

• « LH0 » : valeur de LW1 à un instant donné.

• « LH1 » : valeur de LW2 à un instant donné.

• « LH2 » : valeur de LW4 à un instant donné.

• « LH3 » : valeur de l'adresse LW5 à un instant donné.

• « LH4 » : valeur de l'adresse LW7 à un instant donné.

Par exemple : adresse de lecture LW1, longueur d'échantillonnage 3, nombre total d'échantillons 10, mode d'échantillonnage par déclenchement, intervalle de 1 seconde, type de données par défaut ;

1). Option « Arrêter l'échantillonnage » non cochée :

Les valeurs de LW1, LW2 et LW3 sont lues toutes les secondes. Le nombre total d'échantillons étant de 10, 10 groupes de données sont lus au bout de 10 secondes. L'option « Arrêter l'échantillonnage » n'étant pas cochée, l'échantillonnage continue. Une zone mémoire fixe, dépendant de la longueur d'échantillonnage, du nombre total d'échantillons et du type de données, stocke les données lues : une fois le « nombre total d'échantillons » atteint, la dernière donnée lue remplace la plus ancienne.

2). Option « Arrêter l'échantillonnage » cochée :

Seule différence : l'échantillonnage s'arrête une fois le nombre total d'échantillons atteint.

<img src="../../setting/history-data.files/image004.jpg" width="130" />

Utilisez les « [Tendances historiques](../configuration-guide/extended-controls/histrendgraphics.md) » ou l'« [Affichage des données historiques](../configuration-guide/extended-controls/history-record.md) » pour lire les valeurs plus facilement.
