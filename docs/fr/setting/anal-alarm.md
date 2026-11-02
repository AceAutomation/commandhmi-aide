# Alarmes analogiques

Ouvrez la boîte de réglage des alarmes analogiques, comme sur la figure 7-28 :

Deux types : valeur numérique et comparaison numérique.

<img src="../../setting/anal-alarm.files/image002.jpg" width="145" />

Alarme par comparaison numérique :

<img src="../../setting/anal-alarm.files/image007.jpg" width="599" />

Figure 7-28    Boîte de dialogue des alarmes analogiques

Pour utiliser les alarmes analogiques, procédez ainsi :

• Saisissez d'abord l'adresse à surveiller dans la colonne « Adresse de lecture » (Read Address). On suppose ici l'adresse interne LW1.

• Choisissez le nombre total d'alarmes dans l'option « Taille » (Size), c'est-à-dire le nombre d'adresses ; le type de données détermine la façon de lire les adresses. Par défaut, chaque adresse est en 16 bits et les adresses sont consécutives, mais le type de données peut être modifié. Sur la figure 7-28, LW1 est en entier positif 32 bits, LW3 et LW4 en entier positif 16 bits. Ainsi, quand une adresse est en 32 bits, l'adresse lue suivante vaut l'adresse précédente plus 2 ; en 16 bits, l'adresse précédente plus 1.

• On peut régler le « Temps de scrutation » (Scanning time) de l'alarme, c'est-à-dire la fréquence de scrutation.

• Cliquez sur chaque ligne pour saisir une valeur dans le champ « Limite » à droite, puis le texte de l'alarme dans le champ « Texte ». On suppose ici les messages de la figure 7-28 : chaque valeur d'adresse se classe dans l'une des quatre plages Bas, Très bas, Haut, Très haut.

Voir la figure 7-29 :

<img src="../../setting/anal-alarm.files/image004.jpg" width="566" />

Figure 7-29    Les quatre plages de valeurs de l'adresse LW1

• Très bas : si la valeur est inférieure à la limite réglée et que l'option « Utiliser » est cochée, l'alarme s'affiche dans l'objet « Alarmes » ou le « Bandeau d'alarmes dynamique » ;

• Bas : si la valeur est supérieure ou égale à la limite « Très bas » et inférieure à la limite « Bas », et que l'option « Utiliser » est cochée, l'alarme s'affiche dans l'objet « Alarmes » ou le « Bandeau d'alarmes dynamique » ;

• Haut : si la valeur est supérieure à la limite « Haut » et inférieure ou égale à la limite « Très haut », et que l'option « Utiliser » est cochée, l'alarme s'affiche dans l'objet « Alarmes » ou le « Bandeau d'alarmes dynamique ».

• Très haut : si la valeur est supérieure à la limite réglée et que l'option « Utiliser » est cochée, l'alarme s'affiche dans l'objet « Alarmes » ou le « Bandeau d'alarmes dynamique ».

• Export U : exporte les réglages des alarmes

• Import U : importe les réglages des alarmes

Pour l'option « Utiliser », voir « Alarmes numériques ».

L'alarme sur valeur numérique se déclenche quand la valeur atteint la limite réglée.

Réglages ci-dessous : l'alarme se déclenche quand la valeur atteint 1, 12, 30 et 40.

<img src="../../setting/anal-alarm.files/image006.jpg" width="130" />

Remarque : 10 alarmes analogiques au maximum pour les IHM de la série HM.
