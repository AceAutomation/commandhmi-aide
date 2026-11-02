# Connexion « un équipement, plusieurs IHM »

Les écrans tactiles IHM CommandHMI permettent de relier plusieurs IHM à un automate (« un équipement, plusieurs IHM ») via le protocole MODBUS. Les écrans tactiles sont reliés les uns aux autres, le premier étant relié à l'automate. Première possibilité : tous les écrans tactiles sont en station esclave et l'automate en station maître. Double-cliquez sur « Connexion COM1 » dans le gestionnaire de projet : la boîte des propriétés du port de communication s'ouvre. Dans le champ « Service équipement » de l'onglet « Général », choisissez Modbus RTU, puis Modbus RTU Slave à droite. Deuxième possibilité : le premier écran tactile relié à l'automate est en station maître, l'automate et les autres écrans en station esclave. Dans ce cas, pour les propriétés du port de communication du premier écran, choisissez Modbus RTU dans « Service équipement » de l'onglet « Général », puis Modbus RTU Master à droite ; passez en mode étendu dans l'onglet « Paramètres » et attribuez les adresses des écrans tactiles. Les écrans tactiles en station esclave peuvent alors communiquer avec l'automate par l'intermédiaire du premier écran. Dans les deux cas, seule la station maître communique avec les stations esclaves ; les esclaves ne peuvent pas communiquer entre eux.

Automate en station maître et tous les écrans tactiles en station esclave :

1. Le port de communication de l'automate est en RS232 ; le câblage et les réglages sont présentés sur les figures 8-1, 8-2 et 8-3 :

<img src="../../multpoint/multhmi.files/multhmi1428.png" width="577" />

Figure 8-1  Schéma de la connexion « un équipement, plusieurs IHM » avec l'automate (RS232) en station maître

<img src="../../multpoint/multhmi.files/multhmi1528.png" width="589" />

Figure 8-2 Choix du protocole MODBUS et réglage en station esclave

<img src="../../multpoint/multhmi.files/multhmi1593.png" width="588" />

Figure 8-3 Attribution de l'adresse de station de l'IHM

2. Le port de communication de l'automate est en RS485 ; le câblage est présenté sur la figure 8-4 :

<img src="../../multpoint/multhmi.files/multhmi1744.png" width="598" />

Figure 8-4  Schéma de la connexion « un équipement, plusieurs IHM » avec l'automate (RS485) en station maître

Si le port de communication de l'automate est en RS485, tous les écrans tactiles étant esclaves, les réglages sont les mêmes qu'en RS232. Voir les figures 8-2 et 8-3.

Lorsque tous les écrans de la série sont en station esclave, jusqu'à 255 écrans peuvent être reliés. Mais plus il y a d'écrans tactiles, plus la réponse est lente.

 Premier écran tactile en station maître, automate et autres écrans en station esclave :

1.Le port de communication de l'automate est en RS232 ; le câblage et les réglages sont présentés sur les figures 8-5, 8-6 et 8-7 :

<img src="../../multpoint/multhmi.files/multhmi2462.png" width="579" />

Figure 8-5   Schéma de la connexion « un équipement, plusieurs IHM » avec l'automate (RS232) en station esclave

<img src="../../multpoint/multhmi.files/multhmi2563.png" width="588" />

Figure 8-6 Choix du protocole MODBUS pour le premier écran et réglage en station maître

<img src="../../multpoint/multhmi.files/multhmi2650.png" width="590" />

Figure 8-7 Le mode étendu est nécessaire lorsque le premier écran tactile est en station maître

Les réglages des écrans tactiles en station esclave sont semblables à ceux des figures 8-2 et 8-3.

<img src="../../multpoint/multhmi.files/multhmi2852.png" width="130" />

Remarque : le RS232 ne permettant pas de liaison multipoint, si l'automate de la connexion « un équipement, plusieurs IHM » n'a pas de port RS485, un convertisseur RS485/RS232 est nécessaire.

Remarque : lorsqu'un écran tactile de la série est en station maître dans la connexion « un équipement, plusieurs IHM », le mode d'adressage de cet écran doit être réglé en multiprotocole.

Avec Modbus en station maître, on peut en principe ajouter jusqu'à 255 stations esclaves ; mais plus il y a d'esclaves, plus la communication est lente.
