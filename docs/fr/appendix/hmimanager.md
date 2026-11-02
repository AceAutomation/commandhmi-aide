# Utilisation de HMIManager

Accédez à la page des outils de téléchargement

![](../../appendix/hmimanageer.files/002.png)

Page Téléchargement :

Paramètres de communication :
USB : le PC est relié à l'IHM par USB
WAN : le PC est relié à l'IHM par Ethernet

Vous pouvez aussi cliquer sur le bouton Scan pour rechercher les adresses IP

![](../../appendix/hmimanageer.files/a1.png)

Vous pouvez vérifier l'adresse IP trouvée et la modifier dans la zone de modification ci-dessous

![](../../appendix/hmimanageer.files/a2.png)

Cliquez sur le bouton de droite pour modifier les informations à l'écran ; une fenêtre s'affiche une fois l'opération terminée.

![](../../appendix/hmimanageer.files/a3.png)

Cliquez alors sur Rescan : les modifications apparaissent dans la liste.

![](../../appendix/hmimanageer.files/a4.png)

Cochez l'adresse IP à utiliser et cliquez sur le bouton Select pour sélectionner l'IP cible ; les informations IP sont reportées dans la fenêtre de téléchargement.

**Attention !**

Pour utiliser la recherche d'adresses IP, les trois conditions suivantes doivent être remplies :

1. Les écrans tactiles fabriqués avant le 30 décembre 2024 doivent recevoir manuellement le correctif de recherche IP correspondant ; si le fichier « hmi.patch » est absent du répertoire d'installation, contactez le support technique pour l'obtenir.
     2. La version du logiciel de configuration doit être au moins HMITOOLV7.1_022
     3. La version du firmware doit être au moins Simulator 8.1.0.10.

Choix du téléchargement :
Télécharger la configuration : il faut générer le fichier de projet u-disk-prj.bin ; dans le logiciel de configuration, choisissez Download-&gt;Extract Project Save As-&gt;Generate pour générer le fichier u-disk-prj.bin, cliquez sur Browse pour sélectionner le fichier, puis sur Start pour mettre à jour la configuration de l'IHM.
Télécharger la recette : compilez le projet IHM, ouvrez le dossier compile dans le répertoire d'installation du logiciel : deux fichiers recipe60.bin et recipe62.bin y sont générés. Pour une version inférieure ou égale à 6.0, choisissez recipe60.bin ; pour une version supérieure à 6.0, choisissez recipe62.bin. Cliquez sur Browse pour sélectionner le fichier, puis sur Start Download.

![](../../appendix/hmimanageer.files/003.png)

Page Upload (transfert vers le PC) :

Paramètres de communication :
Identiques à ceux du téléchargement.

Choix de l'upload :
Zone de choix : l'upload n'est possible que si les paramètres de l'écran tactile autorisent l'upload de la configuration et si le programme de l'IHM contient des recettes, des données historiques ou des alarmes historiques ; sinon les fichiers correspondants ne peuvent pas être transférés.
Upload des données historiques : cliquez sur Browse pour choisir l'emplacement et le nom du fichier, puis sur Start Upload pour transférer le fichier zip des données historiques et le fichier .csv ; voir « Upload des données historiques » pour les détails.
Upload de la configuration : cliquez sur Browse pour choisir l'emplacement et le nom du fichier, puis sur Start Upload pour transférer le fichier zip de la configuration ; décompressez-le ensuite pour consulter et modifier normalement le projet ; voir « Upload du programme de configuration ».
Upload de la recette : cliquez sur Browse pour choisir l'emplacement et le nom du fichier, puis sur Start Upload pour transférer le fichier de recettes de l'IHM.
Upload des alarmes historiques : cliquez sur Browse pour choisir l'emplacement et le nom du fichier, puis sur Start Upload pour transférer le fichier d'alarmes de l'IHM.

![](../../appendix/hmimanageer.files/004.png)

Page Version :

Paramètres de communication :
Identiques à ceux du téléchargement.

Informations de version : informations de version de l'IHM actuellement connectée.

![](../../appendix/hmimanageer.files/005.png)

Page Firmware :

Paramètres de communication :
Identiques à ceux du téléchargement.

Infos firmware
Informations firmware : sélectionnez avec Browse le firmware à mettre à jour, puis cliquez sur Upgrade

![](../../appendix/hmimanageer.files/006.png)

Page Simulation :

Sélectionnez avec Browse le fichier de projet .vpm pour lancer une simulation en ligne ou hors ligne.

![](../../appendix/hmimanageer.files/007.png)

Page Adresses :

Service : choisissez le fabricant de l'équipement.
Model : sélectionnez le modèle d'équipement
Affiche toutes les adresses de l'équipement sélectionné.
