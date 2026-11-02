# Instructions sur les objets CommandHMI

Le logiciel CommandHMI propose des objets de base complets. Double-cliquez ou faites un clic droit sur un objet dans la zone de vue pour régler ses propriétés. La position et la taille des objets se modifient dans la barre d'état en bas ou directement à la souris.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/image002.jpg" width="829" alt="2018_11_20_08_51_35.jpg" />

Saisie d'adresse des objets : pour travailler sur une adresse d'automate, on peut saisir l'adresse directement au clavier. Le nom d'adresse n'est pas sensible à la casse.

Liste des états : la barre d'outils comporte une liste déroulante qui affiche et modifie l'état des boutons de bit, voyants de bit, boutons multi-états, voyants multi-états, déplacements graphiques, affichages de messages et affichages d'images.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice675.png" width="92" />

Quand un objet de ce type est sélectionné, son état courant s'affiche dans cette liste, qui permet de le changer.

Recherche d'adresse : recherche l'utilisation d'une adresse et liste les objets qui l'utilisent ; double-cliquez sur une ligne pour sélectionner l'objet.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice997.png" width="299" />

Saisissez l'adresse et cliquez sur « Rechercher » : la fenêtre de sortie liste les résultats :

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1102.png" width="406" />

Double-cliquez sur un résultat pour sélectionner l'objet qui utilise l'adresse.

Affichage des adresses : cliquez sur « Affichage des adresses » pour afficher la liste des adresses utilisées par le projet ; double-cliquez sur une ligne pour ouvrir les propriétés de l'objet qui utilise cette adresse et les modifier rapidement.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1461.png" width="719" />

Le mode d'affichage permet de limiter l'affichage aux adresses choisies ou de tout afficher pour tous les écrans.

Superposition d'objets : en superposant des objets, un seul appui déclenche plusieurs actions. CommandHMI permet de superposer jusqu'à 32 objets. Quand des objets superposés sont touchés, leurs actions sont exécutées dans l'ordre de superposition, comme sur la figure ci-dessous :

Avec les objets 1, 2 et 3 superposés, un appui exécute successivement les commandes 1, 2 et 3.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice1966.png" width="435" />

Si l'un des objets superposés est un bouton de changement d'écran, l'écran change quand vient son tour, et les commandes des boutons situés après lui ne sont pas exécutées. De même, si un clavier de saisie s'ouvre, les commandes suivantes ne sont pas exécutées.

<img src="../../../configuration-guide/extended-controls/operation-notice.files/operation-notice2303.png" width="494" />
