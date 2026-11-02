# Régler les paramètres et ajouter des objets

**Réglage des paramètres :**

1\. Les paramètres se modifient via « Préférences » dans le menu « Paramètres », ou par un double-clic sur [Paramètres de l'IHM](../setting/paramater.md) dans le gestionnaire de projet. La boîte de la figure 3-6 s'ouvre :

<img src="../../start-new-project/setting-parameter.files/image001.jpg" width="643" alt="ScreenShot00218.jpg" />

Figure 3-6     Boîte des paramètres généraux

• Modèle d'IHM : change le modèle d'IHM.

• Mode d'affichage : affichage horizontal ou vertical.

• Démarrage de l'IHM

• Écran de démarrage : écran affiché à la mise sous tension de l'IHM

• Délai de l'économiseur d'écran : règle le délai de l'économiseur d'écran

• Fréquence de clignotement : fréquence de clignotement des objets qui clignotent ; on la modifie en saisissant directement une valeur ou avec les flèches.

• Son d'alarme : en cas d'alarme, l'écran tactile peut avertir l'utilisateur par un son ; la liste déroulante à droite propose avec ou sans son.

• Son tactile : la liste déroulante à droite propose avec ou sans son.

• Écran de l'économiseur : choisissez un des écrans existants comme économiseur d'écran ; il suffit de toucher l'écran pour revenir à l'écran précédent.

• Écran de chargement : si cette option est cochée, l'IHM affiche l'écran de chargement choisi pendant un moment après la mise sous tension, puis passe à l'écran de démarrage ; on peut y afficher des conseils ou remarques.

• Autres réglages

• Masquer le curseur de la souris : affiche ou non la souris

• Réglages des flottants :

\[Standard\] : octets de poids fort du flottant en premier, poids faible ensuite ;

\[Personnalisé\] : l'utilisateur choisit l'ordre.

• Toucher invalide : en cochant « Utiliser un marquage personnalisé », les objets non touchables sont signalés par l'image choisie par l'utilisateur.

• Effet visuel à l'appui : CommandHMI ajoute un effet visuel à l'appui. Lorsqu'il est activé, une trace rectangulaire apparaît quand on touche l'objet, dans la couleur choisie par l'utilisateur. Actuellement, les objets Bouton de bit, Bouton de mot, Bouton d'écran, Bouton de fonction, Saisie numérique et Saisie ASCII prennent en charge cet effet. Par défaut : aucun effet.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2109.png" width="130" />

L'effet d'appui des objets elliptiques reste rectangulaire.

<img src="../../start-new-project/setting-parameter.files/setting-parameter2172.png" width="230" />

Figure 3-7

2、Mots de passe utilisateur

<img src="../../start-new-project/setting-parameter.files/setting-parameter2206.png" width="692" />

Figure 3-8     Mots de passe utilisateur dans les paramètres de l'IHM

Cette fonction gère 8 jeux de mots de passe utilisateur, chacun avec huit niveaux de mot de passe.

• Niveau utilisateur par défaut : le niveau par défaut est NULL.

• Autoriser le chargement du projet : si cette option est cochée, le projet peut être chargé de l'IHM vers le PC ; sinon, non.

• Mot de passe au chargement : indique si le chargement du projet nécessite un mot de passe.

• Mot de passe de mise à jour par clé USB : si un mot de passe est défini, il est demandé lors de la mise à jour du projet de l'IHM par clé USB.

• Mot de passe de niveau maximal : ce mot de passe donne accès à tous les objets limités par niveau.

• Chargement : indique si ce mot de passe permet de charger le projet de l'IHM vers le PC.

• Droits : indique si ce mot de passe permet toutes les opérations limitées.

**3.Réglages de l'imprimante <span id="OLE_LINK247"></span><span id="OLE_LINK246"></span>et du téléchargement**

Cliquez sur le bouton « Réglages de la connexion IHM-imprimante », comme sur la figure 3-9 :

<img src="../../start-new-project/setting-parameter.files/setting-parameter3209.png" width="693" />

Figure3-9      Réglages de la connexion entre l'IHM et l'imprimante

<span id="OLE_LINK245"></span><span id="OLE_LINK244"></span>Cet onglet contient les paramètres de connexion entre l'imprimante et l'IHM ; choisissez les paramètres selon le modèle d'imprimante.

**Réglages du téléchargement :**

• Mode de téléchargement : USB ou Ethernet. En Ethernet, il faut indiquer l'adresse IP et le numéro de port (ceux de l'IHM).

• Effacer l'historique des alarmes : efface ou non les alarmes historiques avant le téléchargement.

• Effacer l'historique des données : efface ou non les données historiques avant le téléchargement.

• Télécharger les recettes : télécharge ou non les recettes du projet courant dans l'IHM.

**Options de téléchargement des images :**

• Conserver le format d'origine : le format des images est conservé lors du téléchargement.

• Convertir en JPG : toutes les images sont converties en JPG avant le téléchargement dans l'IHM.

(Remarque : les images BMP occupant beaucoup de place, cette option est conseillée.)

4.Emplacement de stockage et système d'alarme, comme ci-dessous

<img src="../../start-new-project/setting-parameter.files/setting-parameter4305.png" width="692" />

Figure 3-10   Boîte de l'emplacement de stockage et du système d'alarme

• Emplacement de stockage : emplacement des données historiques, des alarmes historiques et des captures d'écran. Choix entre « Local (FLASH) » et « Clé USB » selon les besoins. Par défaut : Local (FLASH).

• IP de l'IHM : paramètres réseau de l'écran tactile

• Système d'alarme

Utiliser le système d'alarme : utilise ou non l'alarme système. En cas d'alarme, le système affiche l'alarme courante en haut ou en bas de chaque écran, selon les options choisies.

Couleur de fond, couleur du texte, police et taille de police : propriétés de l'affichage des alarmes système, à régler selon les besoins.

Mode d'affichage : « Affichage permanent » : l'alarme reste affichée ; « Affichage cyclique » : l'alarme apparaît et disparaît périodiquement, pour un effet de clignotement.

Position du bandeau d'alarmes : position d'affichage du bandeau d'alarmes.

5.Autres réglages, comme ci-dessous

<img src="../../start-new-project/setting-parameter.files/setting-parameter5287.png" width="690" />

Figure 3-11   Mot de passe de déverrouillage de l'économiseur d'écran

• Si cette option est cochée, l'utilisateur doit saisir ce mot de passe pour quitter l'économiseur d'écran.

<img src="../../start-new-project/setting-parameter.files/setting-parameter5429.png" width="130" />

Le délai de l'économiseur d'écran n'est pris en compte que si un « Écran de l'économiseur » est choisi ; il suffit de toucher l'économiseur pour revenir à l'écran précédent.
