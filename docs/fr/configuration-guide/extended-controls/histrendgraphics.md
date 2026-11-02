# Courbe de tendance historique

• Présentation : cette courbe s'utilise avec le « [Collecteur de données historiques](../../setting/history-data.md) » du gestionnaire de projet : elle affiche les valeurs enregistrées par ce collecteur.

• Présentation de la courbe de tendance XY :

Affichage dynamique et continu de la valeur des variables.

Affiche plusieurs courbes de référence, avec le temps en axe X et la valeur des adresses en axe Y, pour juger précisément et visuellement l'évolution d'une valeur sur une période.

Jusqu'à 8 courbes peuvent être affichées (graphique linéaire).

• Ajouter la courbe et modifier ses propriétés :

1. Sélectionnez l'icône Tendance<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image002.jpg" width="34" /> dans la barre d'outils : la boîte Propriétés de la tendance historique s'ouvre, comme sur la figure 4-53 :

Figure 4-53    Page Général de la tendance historique

• Couleur de fond : couleur de fond de la courbe de tendance. Le changement n'est visible qu'après avoir cliqué sur « OK ».

• Transparence : transparence de la couleur de fond.

• Collecte de données : par défaut, le « Collecteur de données historiques » du gestionnaire de projet. CommandHMI gérant plusieurs groupes de données historiques, cette option permet de choisir le groupe à utiliser, comme ci-dessous :

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image004.jpg" width="774" />

• Nombre de courbes : nombre de courbes affichées, jusqu'à 8.

• Couleur de fond : couleur du tracé (de la plume).

• Utiliser une adresse de contrôle : active l'adresse de contrôle. Elle occupe 28 offsets et commande l'affichage de chaque courbe, les valeurs maximale et minimale, l'heure de fin, la période (minutes), le maximum et le minimum de l'axe Y, l'affichage de l'axe Y et le retour à l'état initial.

|                |                                                                                                         |
|----------------|---------------------------------------------------------------------------------------------------------|
| Offset d'adresse | Élément contrôlé par le registre                                                                    |
| 0              | Nombre total de courbes affichées                                                                       |
| 1              | <span id="OLE_LINK534"></span><span id="OLE_LINK533"></span>Afficher la courbe 1                         |
| 2              | Afficher la courbe 2                                                                                    |
| 3              | Afficher la courbe 3                                                                                    |
| 4              | Afficher la courbe 4                                                                                    |
| 5              | Afficher la courbe 5                                                                                    |
| 6              | Afficher la courbe 6                                                                                    |
| 7              | Afficher la courbe 7                                                                                    |
| 8              | Afficher la courbe 8                                                                                    |
| 9              | Valeur maximale de l'axe Y                                                                              |
| 10             |                                                                                                         |
| 11             | Valeur minimale de l'axe Y                                                                              |
| 12             |                                                                                                         |
| 13             | 0 : utilise le maximum et le minimum par défaut ; 1 : utilise les limites haute et basse définies       |
| 14             | Heure de début de la recherche                                                                          |
| 15             |                                                                                                         |
| 16             |                                                                                                         |
| 17             |                                                                                                         |
| 18             |                                                                                                         |
| 19             |                                                                                                         |
| 20             | Heure de fin de la recherche                                                                            |
| 21             |                                                                                                         |
| 22             |                                                                                                         |
| 23             |                                                                                                         |
| 24             |                                                                                                         |
| 25             |                                                                                                         |
| 26             | 1 : lance la recherche, puis revient automatiquement à 0                                                |
| 27             | 1 : revient à l'état initial, puis revient automatiquement à 0                                          |

Afficher ou non l'adresse de contrôle :

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/2020-03-23_091355.jpg" width="774" />

**Curseur de lecture**

• Activé : active ou non la ligne de lecture (ligne de référence).

• Couleur : couleur de la ligne de lecture (ligne de référence).

• Adresse de lecture : la valeur à la position de la ligne de lecture (ligne de référence) est écrite dans ce registre.

• Afficher l'heure de lecture : l'heure correspondant à la position de la ligne de lecture est écrite dans ce registre, à afficher avec un objet Affichage ASCII, 19 mots au total.

• Écart de temps du point de lecture : la différence entre l'heure de la ligne de lecture et l'heure de début est écrite dans ce registre, à afficher avec un objet Affichage numérique, entier 16 bits, en secondes.

2\. La page « Courbes » de la tendance historique est présentée sur la figure 4-54.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image005.jpg" width="774" />

Figure 4-54    Onglet Courbes de la tendance historique

Cette page permet de régler le maximum, le minimum, le style et la couleur de chaque courbe. La source de données est le « [Collecteur de données historiques](../../setting/history-data.md) » du gestionnaire de projet ; chaque courbe peut avoir sa propre source.

3\. La page « Axes XY » de la tendance historique est présentée sur la figure 4-55.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image006.jpg" width="774" />

Figure 4-55    Onglet Axes XY de la tendance historique

**Axe X**

• Afficher les graduations : affiche ou non les graduations de l'axe X.

• Afficher la grille Y : affiche ou non la grille de l'axe Y.

• Couleur axe / graduations : couleur de l'axe X et de ses graduations.

• Couleur de la grille : couleur de la grille de l'axe X.

• Graduations principales : graduations principales de l'axe X.

• Graduations secondaires : graduations secondaires de l'axe X.

• Affichage du temps : format et taille de police de l'heure.

• Plage de temps : plage de temps affichée sur la courbe.

**Axe Y**

• Afficher les graduations : affiche ou non les graduations de l'axe Y.

• Afficher la grille X : affiche ou non la grille de l'axe X.

• Couleur axe / graduations : couleur de l'axe Y et de ses graduations.

• Couleur de la grille : couleur de la grille de l'axe Y.

• Graduations principales : nombre de graduations principales de l'axe Y.

• Graduations secondaires : nombre de graduations secondaires de l'axe Y.

• Afficher les valeurs : affiche ou non les valeurs des graduations de l'axe Y.

• Taille de police : taille des valeurs de l'axe Y.

• Minimum : valeur minimale de l'axe Y.

• Maximum : valeur maximale de l'axe Y.

• Total : nombre maximal de chiffres affichés.

• Décimales : nombre maximal de chiffres après la virgule.

• Afficher plusieurs axes : affiche ou non plusieurs axes.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image007.jpg" width="130" />

Pour la page « Visibilité », voir l'objet « Bouton de bit ».
