# Paramètres de l'IHM

Le modèle d'IHM se choisit à la création du projet ; il peut être modifié ensuite via « Paramètres de l'IHM » dans le gestionnaire de projet.

Double-cliquez sur « Paramètres de l'IHM » dans le gestionnaire de projet : la boîte de la figure 7-3 s'ouvre :

**Réglage des paramètres :**

1\. Les paramètres se modifient via « Préférences » dans le menu « Paramètres », ou par un double-clic sur « Paramètres de l'IHM » dans le gestionnaire de projet. La boîte de la figure 7-3 s'ouvre :

<img src="../../setting/paramater.files/image002.jpg" width="643" alt="ScreenShot00218.jpg" />

Figure7-3 Boîte des paramètres de l'IHM

Modèle d'IHM : change le modèle d'IHM

Désignation des modèles :

Ex. : HM-043BE

HM : série HM CommandHMI

043 : taille de l'écran de l'IHM

BE : type B ; il existe aussi le type E ; les types diffèrent par la résolution.

Mode d'affichage : affichage horizontal ou vertical.

Démarrage de l'IHM

Écran de démarrage : écran affiché à la mise sous tension de l'IHM

Délai de l'économiseur d'écran : règle le délai de l'économiseur d'écran

Fréquence de clignotement : fréquence de clignotement des objets qui clignotent ; on la modifie en saisissant directement une valeur ou avec les flèches.

Son d'alarme : en cas d'alarme, l'écran tactile peut avertir l'utilisateur par un son ; la liste déroulante à droite propose avec ou sans son.

Son tactile : la liste déroulante à droite propose avec ou sans son.

Écran de l'économiseur : choisissez un des écrans existants comme économiseur d'écran ; il suffit de toucher l'écran pour revenir à l'écran précédent.

Écran de chargement : si cette option est cochée, l'IHM affiche l'écran de chargement choisi pendant un moment après la mise sous tension, puis passe à l'écran de démarrage ; on peut y afficher des conseils ou remarques.

Clignotement de l'écran en cas d'alarme : alterne la couleur de fond de l'objet « Alarmes » ou du bandeau d'alarmes et celle de l'écran, à la fréquence de clignotement ci-dessus. Sans effet si le fond est une image ou si le motif de fond est transparent.

• Autres réglages

• Masquer le curseur de la souris : affiche ou non la souris

• Réglages des flottants :

• \[Standard\] : octets de poids fort du flottant en premier, poids faible ensuite ;

• \[Personnalisé\] : l'utilisateur choisit l'ordre.

• Toucher invalide : en cochant « Utiliser un marquage personnalisé », les objets non touchables sont signalés par l'image choisie par l'utilisateur.

• Mode d'utilisation : choix entre le toucher classique et la souris USB.

• Effet visuel à l'appui : CommandHMI ajoute un effet visuel à l'appui. Lorsqu'il est activé, une trace rectangulaire apparaît quand on touche l'objet, dans la couleur choisie par l'utilisateur. Actuellement, les objets Bouton de bit, Bouton de mot, Bouton d'écran, Bouton de fonction, Saisie numérique et Saisie ASCII prennent en charge cet effet. Par défaut : aucun effet.

<img src="../../setting/paramater.files/paramater2873.png" width="130" />

Remarque : l'effet d'appui des objets elliptiques reste rectangulaire.

2、Mots de passe utilisateur :

<img src="../../setting/paramater.files/paramater2964.png" width="605" />

Figure 7-4      Mots de passe utilisateur

• Cette fonction gère 8 jeux de mots de passe utilisateur, chacun avec huit niveaux de mot de passe.

• Niveau utilisateur par défaut : le niveau par défaut est NULL.

• Autoriser le chargement du projet : si cette option est cochée, le projet peut être chargé de l'IHM vers le PC ; sinon, non.

• Mot de passe au chargement : indique si le chargement du projet nécessite un mot de passe.

• Mot de passe de mise à jour par clé USB : si un mot de passe est défini, il est demandé lors de la mise à jour du projet de l'IHM par clé USB.

• Mot de passe de niveau maximal : ce mot de passe donne accès à tous les objets limités par niveau.

• Chargement : indique si ce mot de passe permet de charger le projet de l'IHM vers le PC.

• Droits : indique si ce mot de passe permet toutes les opérations limitées.

3、**Réglages de l'imprimante et du téléchargement**

Cliquez sur le bouton « Réglages de la connexion IHM-imprimante », comme sur la figure 7-5 :

<img src="../../setting/paramater.files/paramater3938.png" width="605" />

Figure 7-5      Paramètres de la connexion entre l'imprimante et l'IHM

Cet onglet contient les paramètres de connexion entre l'imprimante et l'IHM ; choisissez les paramètres selon le modèle d'imprimante.

Réglages du téléchargement :

Mode de téléchargement : USB ou Ethernet. En Ethernet, il faut indiquer l'adresse IP et le numéro de port (ceux de l'IHM).

Effacer l'historique des alarmes : efface ou non les alarmes historiques avant le téléchargement.

Effacer l'historique des données : efface ou non les données historiques avant le téléchargement.

Télécharger les recettes : télécharge ou non les recettes du projet courant dans l'IHM.

Options de téléchargement des images :

Conserver le format d'origine : le format des images est conservé lors du téléchargement.

Convertir en JPG : toutes les images sont converties en JPG avant le téléchargement dans l'IHM.

(Remarque : les images BMP occupant beaucoup de place, cette option est conseillée.)

**4. Emplacement de stockage et système d'alarme, comme ci-dessous**

<img src="../../setting/paramater.files/paramater5054.png" width="605" />

Figure 7-6      Emplacement de stockage et système d'alarme

• Emplacement de stockage : emplacement des données historiques, des alarmes historiques et des captures d'écran. Choix entre « Local (FLASH) » et « Clé USB » selon les besoins. Par défaut : Local (FLASH).

• Système d'alarme

• Utiliser le système d'alarme : utilise ou non l'alarme système. En cas d'alarme, le système affiche l'alarme courante en haut ou en bas de chaque écran, selon les options choisies.

• Couleur de fond, couleur du texte, police et taille de police : propriétés de l'affichage des alarmes système, à régler selon les besoins.

• Mode d'affichage : « Affichage permanent » : l'alarme reste affichée ; « Affichage cyclique » : l'alarme apparaît et disparaît périodiquement, pour un effet de clignotement.

• Position du bandeau d'alarmes : position d'affichage du bandeau d'alarmes.

**5. Autres, comme ci-dessous**

<img src="../../setting/paramater.files/paramater5969.png" width="691" />

Figure 7-6      Mot de passe de déverrouillage de l'économiseur d'écran

Avec le mot de passe de déverrouillage de l'économiseur d'écran, il faut saisir le mot de passe défini pour quitter l'économiseur.

<img src="../../setting/paramater.files/paramater6121.png" width="130" />

Remarque : le délai de l'économiseur d'écran n'est pris en compte que si un « Écran de l'économiseur » est choisi ; il suffit de toucher l'économiseur pour revenir à l'écran précédent.
