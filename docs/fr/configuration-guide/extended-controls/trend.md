# Courbe de tendance

**Présentation de la courbe de tendance :**

<span id="OLE_LINK525"></span><span id="OLE_LINK526"></span>Affichage dynamique et continu de valeurs variables.

Affiche les courbes de plusieurs données, avec le temps en abscisse et la valeur en ordonnée, pour juger précisément et visuellement l'évolution d'une valeur sur une période.

Jusqu'à 8 courbes peuvent être affichées (graphique linéaire).

Propriétés de la courbe de tendance :

1. Sélectionnez l'icône Courbe de tendance<img src="../../../configuration-guide/extended-controls/trend.files/image002.jpg" width="35" /> dans la barre d'outils : la boîte de propriétés s'ouvre, comme sur la figure 4-50

Figure 4-50    Boîte de dialogue générale de la courbe de tendance

• Couleur de fond : couleur de fond de la courbe. Le changement n'est visible qu'après avoir cliqué sur OK.

• Type de données : 7 types de données disponibles.

• Bit de déclenchement de lecture : la courbe n'avance que lorsque ce bit vaut 1.

• Nombre de courbes : jusqu'à 8.

• Remise à zéro automatique du bit de déclenchement : quand le bit de lecture vaut 1, il est remis à 0.

• Nombre de points par groupe : <span id="OLE_LINK492"></span><span id="OLE_LINK493"></span>nombre de données affichées sur l'<span id="OLE_LINK494"></span><span id="OLE_LINK495"></span>axe X.

• Période d'échantillonnage : fréquence d'échantillonnage.

• Adresse de lecture : sa valeur représente la valeur de chaque courbe sur l'axe Y. Selon le nombre de groupes et le type de données, les adresses sont lues de façon consécutive (16 bits) ou espacée (32 bits).

• Nombre de points variable : le « Nombre de points par groupe » est défini dynamiquement par la valeur d'une adresse. Si cette option est cochée, la valeur par défaut de l'adresse est la valeur initiale du nombre de points par groupe.

**Curseur de lecture**

• Activé : active ou non la ligne de lecture (ligne de référence).

• Couleur : couleur de la ligne de lecture (ligne de référence).

<span id="OLE_LINK527"></span><span id="OLE_LINK528"></span><span id="OLE_LINK543"></span>• Adresse de lecture du curseur : la valeur à la position de la ligne de lecture (ligne de référence) est écrite à cette adresse.

• Utiliser une adresse de contrôle : définit dynamiquement le minimum et le maximum de l'axe Y selon la valeur de l'adresse de contrôle. Elle occupe cinq offsets consécutifs : minimum et maximum de l'échelle de l'axe Y et retour éventuel à l'état initial.

|                |                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Offset d'adresse | Élément contrôlé par le registre                                                                                                                                   |
| 0              | 16 bits bas de la valeur minimale                                                                                                                                  |
| 1              | 16 bits hauts de la valeur minimale                                                                                                                                |
| 2              | 16 bits bas de la valeur maximale                                                                                                                                  |
| 3              | 16 bits hauts de la valeur maximale                                                                                                                                |
| 4              | Retour à l'état initial du maximum et du minimum : la valeur 1 indique une variation dynamique, sinon les valeurs initiales sont rétablies                          |

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

L'adresse de contrôle ne peut être qu'une adresse interne ; le minimum et le maximum occupent chacun deux mots consécutifs.

E.g.:

Avec le type 16 bits et 8 groupes de données, si l'adresse saisie est LW3, 8 valeurs consécutives sont lues :

LW3 : valeur de la courbe 1

LW4 : <span id="OLE_LINK513"></span><span id="OLE_LINK514"></span>valeur de la courbe 2

LW5 : <span id="OLE_LINK515"></span><span id="OLE_LINK516"></span>valeur de la courbe 3

LW6 : valeur de la courbe 4

LW7 : valeur de la courbe 5

LW8 : valeur de la courbe 6

LW9 : valeur de la courbe 7

LW10 : valeur de la courbe 8

Ainsi, avec des données 16 bits et N groupes, les N valeurs sont lues consécutivement selon les règles d'adressage de l'automate.

Avec le type 32 bits et 5 groupes de données, si l'adresse saisie est LW3, 5 valeurs sont lues :

LW3 : <span id="OLE_LINK517"></span><span id="OLE_LINK518"></span>valeur de la courbe 1

LW5 : valeur de la courbe 2

LW7 : valeur de la courbe 3

LW9 : valeur de la courbe 4

LW11 : valeur de la courbe 5

Ainsi, avec des données 32 bits et N groupes, les N valeurs sont lues à des adresses espacées de 2, selon les règles d'adressage de l'automate.

• Direction :

• De gauche à droite : la courbe avance depuis la gauche.

• De droite à gauche : la courbe avance depuis la droite.

• Couleur de fond : couleur de la courbe

• Bit d'effacement : efface toutes les courbes quand la valeur de l'adresse passe de 0 à 1 (front montant). Les courbes ne changent pas quand la valeur passe de 1 à 0 (front descendant) ou reste stable.

La page « Courbes » de la courbe de tendance est présentée sur la figure 4-51 : elle permet de régler le maximum, le minimum, le style et la couleur de chaque courbe.

<img src="../../../configuration-guide/extended-controls/trend.files/image005.jpg" width="774" />

Figure 4-51    Boîte de dialogue Courbes de la tendance

Le type de données choisi dans la page Général détermine celui des valeurs maximale et minimale.

Par exemple, si le maximum ou le minimum est un nombre flottant, il faut d'abord choisir le type flottant 32 bits dans la page Général ; sinon, une erreur se produit en cliquant sur « OK ».

3\. La page « Axes XY » de la courbe de tendance est présentée sur la figure 4-52 :

<img src="../../../configuration-guide/extended-controls/trend.files/image006.jpg" width="774" />

Figure 4-52    Boîte de dialogue Axes XY de la tendance

• Axe X

• Afficher les graduations : affiche ou non les graduations de l'axe X.

• Afficher la grille Y : affiche ou non la grille de l'axe Y.

• Couleur axe / graduations : couleur de l'axe X et de ses graduations.

• Couleur de la grille : couleur de la grille de l'axe X.

• Graduations principales : graduations principales de l'axe X.

• Graduations secondaires : graduations secondaires de l'axe X.

Afficher les graduations : affiche ou non les graduations de l'axe X.

• Axe Y

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

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

Pour la page « Visibilité », voir l'objet « Bouton de bit ».
