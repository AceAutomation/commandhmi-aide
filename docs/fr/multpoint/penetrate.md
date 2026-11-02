# Connexion passante

Les écrans tactiles IHM permettent un mode de connexion particulier : une IHM distante surveille ou commande un automate ou un autre équipement via le port série d'une autre IHM reliée à cet équipement. L'équipement relié peut ainsi être commandé depuis deux postes ou plus. La connexion passante est une fonction très utile de l'IHM.

Avant d'utiliser la connexion passante, il faut connaître les termes suivants :

• IHM locale : l'IHM reliée à l'automate ou à l'équipement.

• IHM distante : l'IHM reliée à l'IHM locale, qui commande les équipements par la connexion passante.

Pour réaliser une connexion passante, l'IHM locale doit avoir deux ports série. Les schémas de la connexion passante figurent sur les figures 8-12 et 8-13 :

Connexion passante à deux écrans :

<img src="../../multpoint/penetrate.files/penetrate789.png" width="578" />

Figure 8-12    Schéma de la connexion passante à deux écrans

Connexion passante à plusieurs écrans :

<img src="../../multpoint/penetrate.files/penetrate913.png" width="792" />

Figure 8-13    Schéma de la connexion passante à plusieurs écrans

IHM locale : réglages logiciels :

Double-cliquez sur la connexion créée : la boîte des propriétés du port de communication s'ouvre. Choisissez COM1 comme port de connexion. Prenons l'exemple d'une connexion passante MITSUBISHI : le COM1 de l'IHM locale est relié à un automate MITSUBISHI FX2N. Les paramètres de communication doivent correspondre à ceux de l'automate ou de l'équipement relié. Voir les figures 8-14 et 8-15 :

<img src="../../multpoint/penetrate.files/penetrate1423.png" width="589" />

Figure 8-14    Onglet « Général » des propriétés du port de communication de l'IHM locale

<img src="../../multpoint/penetrate.files/penetrate1500.png" width="587" />

Figure 8-15 : onglet COM1 des propriétés du port de communication de l'IHM locale

Créez une nouvelle connexion, choisissez COM2 comme port de connexion, n'ajoutez aucun protocole dans « Connexion », réglez les propriétés comme ci-dessous, avec les mêmes paramètres série que le port 1. Paramètres recommandés : 9600, 8, None, 1. Pour la propriété de connexion passante, choisissez « Port vers écran esclave » (Connect Slave Screen Port) et indiquez le nombre d'écrans selon le cas réel. Voir les figures 8-16 et 8-17.

<img src="../../multpoint/penetrate.files/image001.jpg" width="598" alt="ScreenShot00093.jpg" />

Figure 8-16    Onglet « Général » des propriétés du port de communication de l'IHM locale

<img src="../../multpoint/penetrate.files/penetrate2042.png" width="589" />

Figure 8-17    Onglet « Paramètres » des propriétés du port de communication de l'IHM locale

Laissez les valeurs par défaut des autres paramètres. Le réglage de l'IHM locale est terminé.

IHM distante : réglages logiciels :

Double-cliquez sur la connexion créée : la boîte des propriétés du port de communication s'ouvre. Choisissez COM1 comme port de connexion et « Distant » (Remote) comme emplacement de l'IHM ; réglez les mêmes paramètres de communication que dans l'onglet COM2 de l'IHM locale (voir la figure 6 ci-dessus), comme sur les figures 8-18 et 8-19.

<img src="../../multpoint/penetrate.files/penetrate2646.png" width="589" />

Figure 8-18    Onglet « Général » des propriétés du port de communication de l'IHM distante

<img src="../../multpoint/penetrate.files/penetrate2724.png" width="588" />

Figure 8-19    Onglet « Paramètres » des propriétés du port de communication de l'IHM distante

Laissez les valeurs par défaut des autres paramètres. Le réglage de l'IHM distante est terminé.

<img src="../../multpoint/penetrate.files/penetrate2924.png" width="130" />

Remarque : ces réglages concernent la connexion passante à deux écrans.

Remarque : dans une connexion passante à plusieurs écrans, le réglage COM des IHM distantes est identique à celui de l'IHM locale.

Remarque : toutes les données transitant vers l'automate par le COM1 de l'IHM locale, la communication est lente dans une connexion passante à plusieurs écrans.
