# Modbus TCP/IP

L'IHM peut être commandée et surveillée à distance via MODBUS TCP.

**Réglages** avec l'IHM en station maître :

Après la création du projet, double-cliquez sur « Connexion 1 » (Connection 1), comme ci-dessous :

<img src="../../multpoint/modbustcpip.files/modbustcpip209.png" width="248" />

La boîte « Propriétés du port de communication » (Communication Port Properties) s'ouvre (ci-dessous).

<img src="../../multpoint/modbustcpip.files/modbustcpip286.png" width="590" />

Cliquez sur « Paramètres » (Parameter) dans la boîte « Propriétés du port » pour régler l'adresse IP et le port (ceux de l'équipement surveillé). Choisissez le mode d'adressage standard, puis cliquez sur « OK ».

<img src="../../multpoint/modbustcpip.files/modbustcpip544.png" width="588" />

En « Mode étendu » (Extended Mode), l'adresse IP et le port réglés ici ne sont pas pris en compte : ils se règlent en exécution avec le bouton de fonction « Configuration IP des esclaves » (Slave devices IP config).

Pendant l'exécution, un appui sur ce bouton ouvre une fenêtre de saisie du numéro de station ; saisissez-le pour accéder au réglage de l'IP et du port de l'esclave, comme ci-dessous :

<img src="../../multpoint/modbustcpip.files/modbustcpip985.png" width="445" />

Une fois ces réglages faits, téléchargez le projet dans l'IHM ; reliez maître et esclave directement ou via un routeur pour la surveillance et la commande.

**Réglages de la station esclave :**

**1. Régler l'IP**

Réglez d'abord l'adresse IP de l'IHM avec les commutateurs DIP 1 et 3 : dans l'écran de réglage IP qui s'affiche, saisissez l'adresse IP. Dans cet exemple, l'adresse IP de la station esclave est 192.168.1.31. 2.

**2. Créer les connexions**

Après la création du projet, double-cliquez sur « Connexion 1 » (Connection 1), comme ci-dessous :

<img src="../../multpoint/modbustcpip.files/modbustcpip1527.png" width="229" />

La boîte « Propriétés du port de communication » (Communication Port Properties) s'ouvre (ci-dessous).

<img src="../../multpoint/modbustcpip.files/modbustcpip1604.png" width="588" />

Dans la boîte de dialogue ci-dessus, effectuez les réglages suivants :

\* Port de connexion : « Ethernet » (voir figure).

<img src="../../multpoint/modbustcpip.files/modbustcpip1711.png" width="543" />

\* Emplacement de l'IHM : choisissez « Local » (voir figure).

<img src="../../multpoint/modbustcpip.files/modbustcpip1752.png" width="163" />

\* Service de connexion : choisissez « Modbus » - « Modbus Slave TCP / IP » (voir figure).

<img src="../../multpoint/modbustcpip.files/modbustcpip1830.png" width="531" />

Cliquez sur « Paramètres » (Parameter) dans la boîte « Propriétés du port » pour ouvrir la boîte ci-dessous, où l'on règle l'adresse IP (celle de la station esclave) et le numéro de port. Cliquez sur « OK » pour terminer.

<img src="../../multpoint/modbustcpip.files/modbustcpip2039.png" width="589" />

Téléchargez le projet dans l'IHM ; reliez maître et esclave directement ou via un routeur pour la surveillance et la commande.

<img src="../../multpoint/modbustcpip.files/modbustcpip2198.png" width="130" />

L'adresse est l'adresse interne lorsque l'IHM est configurée en station esclave.
