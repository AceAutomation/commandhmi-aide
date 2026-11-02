# Courbe de tendance XY

**Présentation de la courbe de tendance XY :**

Affichage dynamique et continu de valeurs variables.

Affiche les courbes de plusieurs données, chacune prenant deux registres consécutifs comme coordonnées en abscisse et en ordonnée, pour observer précisément et visuellement leur évolution.

Jusqu'à 8 courbes peuvent être affichées (graphique linéaire).

L'ajout et le paramétrage d'une courbe XY sont semblables à ceux de la courbe de tendance ; reportez-vous à la page « Courbe de tendance ». Icône :<img src="../../../configuration-guide/extended-controls/xy-trend.files/image002.jpg" width="36" />

Ouvrez la boîte de propriétés de la courbe XY ; voir les propriétés de la « Courbe de tendance ». À noter : dans la courbe de tendance, chaque courbe représente la valeur d'adresses consécutives à partir de l'adresse lue, alors que dans la courbe XY, chaque courbe utilise deux adresses consécutives à partir de l'adresse lue.

**Utilisation de la courbe de tendance XY :**

Couleur : couleur de la ligne de lecture (ligne de référence).

Adresse de lecture : la valeur à la position de la ligne de lecture (ligne de référence) est écrite à cette adresse.

Par exemple, avec le type 16 bits et 4 groupes de données, si l'adresse saisie est LW3, 8 valeurs consécutives sont lues :

LW3 : courbe 1, valeur X

LW4 : courbe 1, valeur Y

LW5 : courbe 2, valeur X

LW6 : courbe 2, valeur Y

LW7 : courbe 3, valeur X

LW8 : courbe 3, valeur Y

LW9 : courbe 4, valeur X

LW10 : courbe 4, valeur Y

Les adresses lues sont LW3 à LW10, soit 8 adresses. Ainsi, avec des données 16 bits et N groupes, 2 \* N valeurs sont lues consécutivement selon les règles d'adressage de l'automate.

Avec le type 32 bits et 3 groupes de données, si l'adresse saisie est LW3, il faut lire 12 adresses consécutives.

LW3 : courbe 1, valeur X

LW5 : courbe 1, valeur Y

LW7 : courbe 2, valeur X

LW9 : courbe 2, valeur Y

LW11 : courbe 3, valeur X

LW13 : courbe 3, valeur Y

Les adresses lues sont LW3 à LW14, soit 12 adresses. Ainsi, avec des données 32 bits et N groupes, 2 \* N valeurs sont lues à des adresses espacées de 2, selon les règles d'adressage de l'automate.
