# Propriétés du port de communication

Les propriétés du port de communication règlent les paramètres de communication entre l'IHM et les équipements reliés.

Double-cliquez sur « Liaison » (Link), puis sur Liaison 1, comme sur la figure 7-1 :

<img src="../../setting/com.files/image004.jpg" width="532" />

Figure 7-1      Boîte des propriétés du port COM1

L'onglet « Liaison » propose de nombreuses marques et modèles d'automates, ainsi que le « Nom de la liaison » et l'« Intervalle d'adresses automate consécutives »

Cliquez sur l'onglet « Paramètres » de la boîte de dialogue, comme sur la figure 7-2 :

<img src="../../setting/com.files/image005.jpg" width="532" />

Figure 7-2      Paramètres du port de communication COM1

**Réglage des paramètres :**

Service équipement : fabricant, marque d'automate et modèle de CPU.

Port : RS232 / 485/ 422

Vitesse : 1200/2400/4800/9600/19200/38400/57600/115200 / 187.5k

Parité : impaire / paire / aucune

Bits de données : 7/8

Bits de stop : 1/2

Modèle : modèle d'automate

Numéro de station IHM : numéro de station de l'IHM

Temps de communication : l'IHM envoie des données à l'automate et reçoit sa réponse ; elle ne peut renvoyer de données qu'après ce temps de communication.

Timeout 1 et timeout 2 : le timeout se calcule à partir des valeurs Timeout 1 et Timeout 2 ; dans la figure ci-dessus, il vaut 200 ms. Il y a timeout si l'IHM n'a pas reçu de réponse 200 ms après l'envoi.

Nombre de tentatives : nombre de réémissions après un timeout

Mode d'adressage : ① Mode standard : un port série relié à un seul automate ; ② Mode étendu : un port série relié à plusieurs automates du même type

Intervalle d'adresses automate consécutives : nombre maximal de mots que l'automate peut lire en une fois
