# Alarmes numériques

Les réglages d'alarme servent à afficher les alarmes ; sans eux, l'objet « Alarmes » et le bandeau d'alarmes ne fonctionnent pas (ils affichent en fait les messages des « alarmes numériques » et des « alarmes analogiques »).

Faites un clic droit sur « Alarmes » dans le gestionnaire de projet et choisissez « Nouvelle alarme numérique », comme sur la figure 7-22 :

<img src="../../setting/dig-alarm.files/image001.jpg" width="274" alt="ScreenShot00094.jpg" />

Figure 7-22    Choix du journal d'alarmes

Double-cliquez sur l'option « Alarmes numériques » pour ouvrir la boîte de réglage, comme sur la figure 7-23 :

<img src="../../setting/dig-alarm.files/dig-alarm508.png" width="558" />

Figure 7-23    Choix des bits consécutifs

Pour créer des alarmes numériques, procédez ainsi :

• Saisissez d'abord l'adresse de lecture ; on suppose ici l'adresse interne LB1.

• Dans la colonne « Taille » (Size), choisissez le nombre total d'alarmes, c'est-à-dire le nombre d'adresses de bit consécutives. On suppose ici la valeur 6.

• Réglez le « Temps de scrutation » (Scanning time) des alarmes de bit, c'est-à-dire la fréquence de scrutation.

• Cliquez sur une ligne de la liste, puis allez dans le module « Message » à droite ; saisissez le texte de l'alarme dans le champ « Texte ». On suppose ici les messages de la figure 7-23.

• Si « Utiliser » est coché, l'alarme s'affiche dans l'objet « Alarmes » ou le « Bandeau d'alarmes ». Sinon, le message n'apparaît pas, même si l'adresse correspondante vaut 1. Si l'adresse vaut 0, l'alarme ne s'affiche pas.

• Alarme sur OFF : si cette option est cochée, l'alarme se déclenche quand l'adresse vaut 0 (OFF). Sinon, elle se déclenche quand l'adresse vaut 1 (ON). Par défaut, l'alarme se déclenche quand l'adresse vaut 1 (ON).

• Export U : exporte les réglages des alarmes

• Import U : importe les réglages des alarmes

Exemple, avec le type « Bits consécutifs » :

• Si LB1 vaut 0, l'alarme ne s'affiche ni dans l'objet « Alarmes » ni dans le « Bandeau d'alarmes », que l'option « Utiliser » soit cochée ou non.

• Si LB1 vaut 1 et que l'option « Utiliser » n'est pas cochée, l'alarme ne s'affiche ni dans l'objet « Alarmes » ni dans le « Bandeau d'alarmes ».

• Si LB1 vaut 1 et que l'option « Utiliser » est cochée, l'alarme s'affiche dans l'objet « Alarmes » et le « Bandeau d'alarmes ».

Cliquez sur « OK » pour terminer le réglage. Ajoutez 6 boutons de bit en mode « Alterné », d'adresses LB1-LB6 ; placez dans l'écran un objet « Alarmes » et un « Bandeau d'alarmes » ; lancez la simulation hors ligne pour vérifier l'affichage des alarmes.

Exemple de simulation hors ligne, figure 7-24 :

<img src="../../setting/dig-alarm.files/dig-alarm2644.png" width="1182" />

Figure 7-24    Simulation hors ligne des alarmes numériques

Si le type choisi est « Bits consécutifs d'un mot », comme sur la figure 7-25 :

<img src="../../setting/dig-alarm.files/dig-alarm2789.png" width="559" />

Figure 7-25    Choix des bits consécutifs d'un mot

Si « Utiliser » est coché pour un numéro de bit, l'alarme se déclenche quand ce bit vaut 1.

<img src="../../setting/dig-alarm.files/dig-alarm2952.png" width="130" />

Remarque : si vous copiez le texte des alarmes depuis d'autres documents, vérifiez qu'il ne contient pas de saut de ligne (invisible). Il est conseillé de saisir les messages à la main plutôt que par copier-coller, pour éviter des erreurs d'affichage.

Si le type choisi est « Valeur de mot », comme sur la figure 7-26 :

<img src="../../setting/dig-alarm.files/dig-alarm3352.png" width="556" />

Figure 7-26    Boîte d'alarme numérique « Valeur de mot »

L'alarme se déclenche quand la valeur de l'adresse est égale à la valeur choisie dans la liste.

Placez un objet « Alarmes » de 7 lignes comme dans l'exemple de la figure 7-24, et un bandeau d'alarmes dynamique dont les propriétés sont celles de la figure 7-27 :

<img src="../../setting/dig-alarm.files/dig-alarm3691.png" width="675" />

Figure 7-27    Propriétés du bandeau d'alarmes dynamique

Ajoutez enfin six boutons de bit d'adresses d'écriture LB1-LB6, avec les fonctions « Alterné », « Surveillance » et « Adresse de surveillance identique à l'adresse d'écriture ». Cliquez ensuite sur « Enregistrer » dans la barre d'outils, lancez la commande « Hors ligne » du menu « Téléchargement », puis cliquez sur les boutons LB1, LB2, LB4 et LB6 : l'objet « Alarmes » et le bandeau d'alarmes dynamique affichent les alarmes numériques de LB1, LB2, LB4 et LB6. Un nouveau clic les remet à 0 (fonction alternée) : l'objet « Alarmes » et le bandeau d'alarmes dynamique n'affichent plus rien.

<img src="../../setting/dig-alarm.files/dig-alarm4400.png" width="130" />

Remarque : avec le changement de langue, chaque langue peut avoir ses propres textes d'alarme.

Remarque : 10 alarmes numériques au maximum pour les IHM de la série HM.
