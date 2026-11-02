# Connexion « une IHM, plusieurs équipements »

Les IHM de la série permettent aussi de relier plusieurs automates à une IHM (« une IHM, plusieurs équipements ») via le protocole MODBUS. Un seul écran tactile peut alors agir directement sur les registres de plusieurs automates qui lui sont reliés, à condition qu'ils prennent en charge le protocole MODBUS. Dans les réglages, choisissez Modbus RTU dans « Service équipement » de l'onglet « Général », puis Modbus RTU Master à droite : l'écran tactile est en station maître et tous les automates en station esclave. L'écran tactile peut alors agir sur les registres des automates. Les noms de registres des automates correspondent à ceux du protocole MODBUS.

<img src="../../multpoint/multmachine.files/multmachine744.png" width="506" />

Figure 8-8      Connexion « une IHM, plusieurs équipements »

<img src="../../multpoint/multmachine.files/multmachine805.png" width="590" />

Figure 8-9      Réglage de l'écran tactile en station maître

<img src="../../multpoint/multmachine.files/multmachine857.png" width="588" />

Figure 8-10    Le mode étendu est nécessaire lorsque l'écran tactile est en station maître

Après ces réglages, les adresses automate des propriétés du port de communication ne sont plus prises en compte. Lorsque l'utilisateur clique sur un objet pour saisir une adresse, la boîte de saisie d'adresse de la figure 8-11 s'ouvre. Une liste déroulante à droite du nom de registre permet de choisir l'adresse de station esclave de l'automate.

<img src="../../multpoint/multmachine.files/multmachine1294.png" width="251" />

Figure 8-11    Boîte de saisie d'adresse

<img src="../../multpoint/multmachine.files/multmachine1326.png" width="130" />

**Adresses de validation de la communication par station en mode étendu :**

Chaque port série dispose de 16 mots pour valider les numéros de station, soit au maximum 256 stations, avec LW59000 comme adresse de base

COM1 correspond à 59010~59025 : LW59010 aux stations 0~15, LW59011 aux stations 16~31, etc.

COM2 correspond à 59026~59041 : LW59026 aux stations 0~15, LW59027 aux stations 16~31, etc.

Ethernet correspond à 59026~59041 : LW59026 aux stations 0~15, LW59027 aux stations 16~31, etc.

Au démarrage de l'IHM, tout est activé par défaut ; un script peut activer ou couper la communication avec chaque numéro de station en agissant sur chaque bit.

<img src="../../multpoint/multmachine.files/multmachine1993.png" width="130" />

Remarque : le RS232 ne permettant pas de liaison multipoint, si l'automate de la connexion « une IHM, plusieurs équipements » n'a pas de port RS485, un convertisseur RS485/RS232 est nécessaire.
