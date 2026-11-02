# Planificateur

Le planificateur permet de programmer des événements. Par exemple, une usine démarre les machines à 8 h et les arrête à 18 h les jours ouvrés.

Cliquez sur « Planificateur » dans la « Liste standard » : la boîte du planificateur s'ouvre, comme ci-dessous.

<img src="../../setting/schedule.files/schedule706.png" width="728" />

 Figure 7-49 Boîte du planificateur

Cliquez sur le bouton « Nouveau » : une nouvelle boîte s'ouvre, comme ci-dessous, sur l'onglet « Général ».

<img src="../../setting/schedule.files/schedule984.png" width="694" />

  Figure 7-50 Boîte de création d'une planification

• Description :

Texte libre pour indiquer la fonction de cette planification.

• Exécuter l'action de début/fin à la mise sous tension :

Si l'IHM est mise sous tension après l'heure de début, l'action de début/fin est exécutée.

• Adresse cible :

Type et adresse de la cible ; la valeur y est écrite à l'heure de début/fin.

• Opération d'écriture :

Deux types : « Constante » et « Adresse ». Avec « Constante », on indique la valeur écrite à l'adresse cible. Avec « Adresse », on indique une adresse dont la valeur est écrite à l'adresse cible à l'heure de début/fin.

• Utiliser l'opération de fin :

Si cette option est cochée, la valeur de l'opération d'écriture est écrite à l'adresse cible à l'heure de fin.

 Une fois l'onglet « Général » réglé, cliquez sur l'onglet « Plage horaire », comme ci-dessous.

<img src="../../setting/schedule.files/schedule2016.png" width="694" />

  Figure 7-51 Onglet « Plage horaire »

• Constante : cochez les heures de début/fin ; à ces heures, l'écriture correspondante est effectuée.

• Adresse : une plage d'adresses définit les heures de début et de fin de la planification, comme ci-dessous.

 <img src="../../setting/schedule.files/schedule2396.png" width="693" />

 Figure 7-52 Commande par adresse

Par exemple, avec l'adresse LW0, LW0~LW10 servent à la planification.

LW0 : adresse de commande ; quand LW0 == 1, les horaires sont chargés dans l'IHM et la planification démarre. Après le chargement, LW0 est remis à 0 ;

LW1 : état de la planification ; une fois les horaires chargés (LW0==0), LW1 passe à 1.

LW2 : mode d'action ; si LW2 vaut 1 et que l'heure actuelle est après l'heure de début, l'écriture est effectuée. Si LW2 vaut 0, l'opération de début/fin est effectuée quand l'heure actuelle atteint l'heure de début/fin.

LW3 : jour de l'heure de début ; sa valeur vaut 2^(numéro du jour), LW3 = (0,1,4,8,16,32,64)

LW4~LW6 : heures, minutes et secondes de l'heure de début.

LW7 : jour de l'heure de fin ; sa valeur vaut 2^(numéro du jour), LW3 = (0,1,4,8,16,32,64)

LW8~LW10 : heures, minutes et secondes de l'heure de fin.

De même, si LWn est l'adresse de commande, LWn~LWn+10 servent à la planification, comme ci-dessus.

**Conseil :** si « Adresse » est coché, n'oubliez pas de mettre l'adresse de commande à 1 après avoir réglé les heures de début/fin, pour charger la planification. Sinon, elle ne fonctionne pas.

Onglet « Interdiction », comme ci-dessous :

<img src="../../setting/schedule.files/schedule3691.png" width="694" />

 Figure 7-53 Onglet « Interdiction »

Si « Utiliser l'interdiction » est coché, la planification ne fonctionne que lorsque l'adresse de bit remplit la condition (0 ou 1).

Une fois les paramètres réglés, cliquez sur « OK » pour créer l'élément de planification, comme ci-dessous.

<img src="../../setting/schedule.files/schedule4054.png" width="732" />

  Figure 7-50 Planification créée
