# Télécharger le projet

<img src="../../start-new-project/download-project.files/image012.jpg" width="368" />

Figure 3-11    Message d'erreur de compilation

Corrigez d'après le message d'erreur de la fenêtre de sortie ; vous pouvez aussi double-cliquer sur l'erreur : CommandHMI trouve et sélectionne automatiquement l'objet en cause. Double-cliquez ensuite sur l'objet pour voir ses propriétés, trouver la cause de l'erreur et la corriger. Cliquez ensuite sur « Enregistrer » et relancez la compilation. S'il n'y a pas d'erreur, une boîte indique au bout d'un moment que la compilation a réussi. Cliquez sur OK pour terminer, comme sur la figure 3-12 :

<img src="../../start-new-project/download-project.files/image013.jpg" width="364" />

Figure 3-12    Fenêtre de sortie

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Il faut compiler avant de télécharger, et enregistrer avant de compiler, sinon la compilation échoue, comme sur la figure 3-11. Après toute modification, il faut recompiler.

<img src="../../start-new-project/download-project.files/image014.jpg" width="425" />

Figure 3-13    Rappel de compilation

Enfin, lancez la commande « USB » du menu « Téléchargement » pour télécharger par câble USB ; on peut aussi choisir directement « Compiler + Télécharger » dans ce menu. La boîte de la figure 3-14 s'ouvre :

<img src="../../start-new-project/download-project.files/image015.jpg" width="716" />

Figure 3-14    Boîte de téléchargement

Cliquez sur « Télécharger » ; la barre de progression indique l'avancement. Une fois le téléchargement terminé, une fenêtre indique la fin du téléchargement USB. Cliquez sur OK pour terminer, comme sur la figure 3-15 :

<img src="../../start-new-project/download-project.files/image005.jpg" width="720" alt="2018_11_20_09_02_42.jpg" />

Figure 3-15    Téléchargement terminé

Étape suivante : relier l'automate pour vérifier que le projet fonctionne correctement dans l'IHM.

Les modes de connexion entre l'IHM et l'automate ou le PC sont décrits dans la partie « Connexion » du manuel matériel.

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Ne coupez pas l'alimentation de l'IHM ou du PC, ne débranchez pas le câble USB et évitez toute autre opération pendant le transfert, sous peine de le perturber.

Installez les pilotes USB avant de télécharger, sinon le PC ne pourra pas se connecter à l'IHM et le téléchargement sera impossible.

<img src="../../start-new-project/download-project.files/image017.jpg" width="716" />

Figure 3-16    Message du pilote USB

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

La boîte de la figure 3-16 indique que le PC ne reconnaît pas l'IHM. Vérifiez alors que le pilote USB est installé : reliez le PC, mettez l'IHM sous tension, puis cherchez « CommandHMI HMI Tech Corp USB drive » dans Windows, « Poste de travail » - « Propriétés » - « Matériel » - « Gestionnaire de périphériques » - « Contrôleurs de bus USB » (vous pouvez débrancher puis rebrancher le câble USB pour vérifier que le PC reconnaît l'IHM) :

**Téléchargement du projet par Ethernet**

• Réglez les paramètres réseau de l'IHM

Mettez les commutateurs DIP 1 et 3 sur ON ; réglez l'IP (ici 192.168.1.100), la passerelle, le masque de sous-réseau et le port. Le port est fixé à 12345.

• Compilez le projet

Pour télécharger le projet par Ethernet, saisissez l'adresse IP et le numéro de port dans la boîte de saisie. L'IP est celle de l'IHM cible, ici 192.168.1.100, et le port est fixé à 12345. Cliquez ensuite sur « Redémarrer et télécharger », comme sur la figure 3-18 :

![](../../start-new-project/download-project.files/001.png)

Figure 3-18 Téléchargement du projet par Ethernet

Vous pouvez aussi cliquer sur le bouton Scan pour rechercher les adresses IP

![](../../start-new-project/download-project.files/002.png)

Vous pouvez vérifier l'adresse IP trouvée et la modifier dans la zone de modification ci-dessous

![](../../start-new-project/download-project.files/003.png)

Cliquez sur le bouton de droite pour modifier les informations à l'écran ; une fenêtre s'affiche une fois l'opération terminée.

![](../../start-new-project/download-project.files/004.png)

Cliquez alors sur Rescan : les modifications apparaissent dans la liste.

![](../../start-new-project/download-project.files/005.png)

Cochez l'adresse IP à utiliser et cliquez sur le bouton Select pour sélectionner l'IP cible ; les informations IP sont reportées dans la fenêtre de téléchargement.

**Attention !**

Pour utiliser la recherche d'adresses IP, les trois conditions suivantes doivent être remplies :

1. Les écrans tactiles fabriqués avant le 30 décembre 2024 doivent recevoir manuellement le correctif de recherche IP correspondant ; si le fichier « hmi.patch » est absent du répertoire d'installation, contactez le support technique pour l'obtenir.
     2. La version du logiciel de configuration doit être au moins HMITOOLV7.1_022
     3. La version du firmware doit être au moins Simulator 8.1.0.10.

![](../../start-new-project/download-project.files/006.png)
