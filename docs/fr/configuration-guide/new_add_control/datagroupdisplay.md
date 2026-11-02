# Affichage de groupes de données

Affichage de groupes de données : un groupe (ou bloc) de données est un ensemble d'adresses consécutives, par exemple LW12, LW13, LW14, LW15. Cet objet affiche simultanément le contenu de plusieurs groupes de données, par exemple LW12 à LW15 et RWI12 à RWI15, pour observer et comparer les données de chaque registre. Il peut aussi tracer les courbes de plusieurs groupes, avec le numéro de point en abscisse et la valeur de chaque donnée en ordonnée, pour juger précisément et visuellement l'évolution d'une valeur. Jusqu'à 8 courbes peuvent être affichées.

Son icône dans la barre d'outils est : <img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay756.png" width="31" /> ; cliquez dessus pour ouvrir la boîte de dialogue de la figure 4-122 :

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay838.png" width="741" />

Figure 4-122 Page Général de l'affichage de groupes de données

• Couleur de fond : couleur de fond du graphique.

• Type de données : 7 types de données disponibles.

• Bit de déclenchement de lecture : la courbe n'avance que lorsque ce bit vaut 1.

• Remise à zéro automatique : quand le « bit de déclenchement de lecture » vaut 1, il est remis automatiquement à 0 au relâchement du bouton de la souris.

• Nombre de canaux : nombre de groupes de données, donc de courbes.

• Canal courant : choisissez un canal pour définir son \[Adresse de contrôle\].

• Adresse de contrôle : adresse lue. Chaque canal a sa propre adresse de contrôle.

Chaque canal peut avoir une adresse de départ différente ; la longueur occupée = Len \* nombre de points affichés (Len = 1 pour des données 16 bits, Len = 2 pour des données 32 bits).

Par exemple, si l'adresse de départ du canal 1 est LW1, avec un type entier 32 bits et 4 points affichés, le canal 1 occupe LW1 LW3 LW5 LW7 ;

• Points affichés : nombre d'adresses lues pour chaque canal.

• Curseur de lecture

• Activé : active ou non la ligne de lecture (ligne de référence).

• Couleur : couleur de la ligne de lecture (ligne de référence).

• Adresse de lecture : la valeur correspondant à la ligne de lecture est écrite dans ce registre.

• Exemple

16 bits, 4 canaux, 10 points affichés, \[Adresse de contrôle\] LW1 pour le canal 1, LW100 pour le canal 2, LW200 pour le canal 3 et RWI1 pour le canal 4. On a alors :

Courbe 1 : LW1 à LW10

Courbe 2 : LW100 à LW109

Courbe 3 : LW200 à LW209

Courbe 4 : RWI1 à RWI10

En 32 bits, les autres réglages restant identiques :

Courbe 1 : LW1 à LW20

Courbe 2 : LW100 à LW119

Courbe 3 : LW200 à LW219

Courbe 4 : RWI1 à RWI20

Ainsi, avec des données 32 bits et N groupes, les N valeurs sont lues à des adresses espacées de 2, selon les règles d'adressage de l'automate.

• Couleur de fond : couleur de la zone de tracé.

• Bit d'effacement : efface toutes les courbes quand la valeur de l'adresse passe de 0 à 1 (front montant) ; rien ne change quand elle passe de 1 à 0 (front descendant) ou reste stable.

• Marqueurs de points : chaque courbe est formée de points

• Tracer des lignes : chaque courbe est formée de segments.

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay3263.png" width="130" />

Pour la page « Visibilité », voir le « Bouton de bit ».
