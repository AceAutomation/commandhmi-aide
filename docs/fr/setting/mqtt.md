# Serveur

• **Onglet « Général »**

<img src="../../setting/mqtt.files/server-general.png" width="706" />

- IP (nom de domaine)

IP du serveur MQTT

- Port

Numéro de port du serveur MQTT

- ID client

ID du client ; certains caractères spéciaux sont autorisés

- Nom d'utilisateur

Nom d'utilisateur (nécessite l'activation de l'authentification)

- Mot de passe

Mot de passe de l'utilisateur (nécessite l'activation de l'authentification)

- Durée du test de connexion

Si le serveur MQTT ne reçoit pas de message de test de l'IHM pendant cette durée, il considère l'IHM comme déconnectée.

• **Onglet « Adresse »**

<img src="../../setting/mqtt.files/server-addr.png" width="706" />

- Adresse d'état

Groupe d'adresses de mots indiquant l'état de la connexion.

**\[adresse d'état\] (indication d'état)**

Valeur 0 : connexion au serveur arrêtée.

Valeur 1 : déconnecté du serveur.

Valeur 2 : connexion au serveur réussie.

**■   \[adresse d'état + 1\] (indication d'erreur)**

|                      |                                                                                                                                                                                                                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Valeur** | **Description** |
| 0 | Opération réussie |
| -1 | Échec de l'opération du client MQTT |
| -2 | Erreur de persistance |
| -3 | Client déconnecté |
| -4 | Nombre maximal de messages simultanés atteint |
| -5 | Chaîne UTF-8 non valide détectée |
| -6 | Paramètre vide non valide fourni |
| -7 | Sujet tronqué (la chaîne du sujet contient des caractères NULL) ; utilisez la longueur du sujet pour accéder au sujet complet |
| -8 | Le paramètre de structure n'a pas l'identifiant (eye catcher) et le numéro de version corrects |
| -9 | Le paramètre qos n'est pas 0, 1 ou 2 |
| -10 | Les 65535 msgid MQTT sont tous utilisés |
| -11 | Requête incomplète, abandonnée |
| -12 | Impossible de mettre plus de messages en mémoire tampon |
| -13 | Tentative d'utiliser la version non SSL de la bibliothèque pour une connexion SSL |
| -14 | Le préfixe de protocole du serverURI doit être : tcp:// ou mqtt:// (TCP non sécurisé), ssl:// ou mqtts:// (SSL/TLS chiffré), ws:// (WebSockets non sécurisés) ou wss:// (WebSockets sécurisés). Les préfixes TLS (ssl, mqtts, wss) ne sont valides que si la version TLS de la bibliothèque est liée |
| -15 | N'utilisez pas d'autres versions de l'option MQTT |
| -16 | Appel non applicable à la version MQTT du client |
| -17 | Longueur du sujet du message testament (Will) nulle |
| -18 | Commande de connexion ou de déconnexion ignorée, car une commande de connexion ou de déconnexion est déjà en tête de la file d'attente. Utilisez les callbacks onSuccess/onFailure pour attendre la fin de la commande précédente |
| -19 | maxBufferedMessages des options de connexion doit être &gt;=0 |

- Adresse de commande

**Le registre est de type entier 16 bits.**

Valeur inférieure ou égale à 0 : déconnexion du serveur MQTT.

Valeur supérieure à 0 : maintien de la connexion au serveur MQTT.
