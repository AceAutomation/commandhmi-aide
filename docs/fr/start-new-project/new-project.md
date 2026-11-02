# Créer un projet

Pour créer un projet, choisissez « Nouveau projet » dans le menu « Fichier » ou cliquez sur le bouton « Nouveau projet » <img src="../../start-new-project/new-project.files/new-project136.png" width="28" /> de la barre d'outils : CommandHMI ouvre la boîte « Nouveau projet », où l'on indique le nom et l'emplacement du projet. Choisissez le modèle d'IHM ; cliquez sur OK pour créer le projet et passer à la boîte de réglage du port de communication ; « Annuler » ferme la boîte.

**1.Boîte « Nouveau projet »**

Nom du projet :

Chemin : emplacement du nouveau fichier de projet ; par défaut C: \\

Modèle : modèles disponibles pour le projet :

HM-035AE(320\*240)        HM-035UE(320\*240)        HM-043AE()480\*272        HM-043D(480\*272)        HM-043AD(480-272)        HM-043BE(480\*272)        HM-043BS(480\*272)        HM-043QE(480\*272)        HM-043UE(480\*272)        HM-043TE(480\*272)        HM-050AS(480\*272)        HM-050AE(480\*272)        HM-050BS(800\*480)        HM-050BE(800\*480)        HM-057AE(640\*480)        HM-070AS(800\*480)        HM-070AE(800\*480)        HM-070BS(800\*480)        HM-070BE(800\*480)        HM-070GS(800\*480)        HM-070GE(800\*480)        HM-070QS(800\*480)        HM-070QE(800\*480)        HM-070GG(800\*480)        HM-070GW(800\*480)        HM-070MS(800\*480)        HM-070ME(800\*480)        HM-070MG(800\*480)        HM-070MW(800\*480)        HM-T070XS(1024\*600)        HM-102AS(800\*480)        HM-102AE(800\*480)        HM-102BS(1024\*600)        HM-102BE(1024\*600)        HM-102CW(1024\*600)        HM-102CG(1024\*600)        HM-102HE(1024\*600)        HM-102HS(1024\*600)        HM-121AS(800\*600)        HM-121AE(800\*600)        HM-H150AS(1024\*768)        HM-156QS(1920\*1080)

Le modèle par défaut est HM-070AE(800\*480) ; la résolution entre parenthèses (800 \* 480) ne s'affiche pas dans la boîte.

Mode d'affichage : orientation de l'écran tactile du projet. Choix possibles :

Horizontal : écran tactile à l'horizontale.

Vertical : écran tactile à la verticale.

Par défaut : horizontal.

<img src="../../start-new-project/new-project.files/image002.jpg" width="547" alt="ScreenShot00217.jpg" />

Figure 3-1      Boîte « Nouveau projet »

Dans la boîte « Nouveau projet » ci-dessus, indiquez le nom, le chemin, le modèle et le mode d'affichage, puis cliquez sur « Suivant » pour régler le port de communication.

Le modèle à choisir dépend de l'IHM de l'utilisateur.

<img src="../../start-new-project/new-project.files/new-project1533.png" width="130" />

Le nom du projet ne peut pas contenir les caractères suivants : \\ /: \* "&lt;&gt; \|?.

L'emplacement du projet ne peut pas contenir les caractères suivants : \\ /: \* "&lt;&gt; \|?.

## 2. Boîte de réglage de la communication

Cette boîte règle les paramètres du port de communication de l'IHM. Seuls des paramètres corrects garantissent une communication normale entre l'automate et l'écran tactile. Les paramètres dépendent du modèle d'automate relié.

Nom de la connexion : nom du port de communication.

Service équipement : choix de la marque d'automate et du type de CPU.

Interface de connexion : port COM ou port Ethernet.

Intervalle d'adresses automate consécutives : espace d'adresses consécutives de l'automate ; la valeur par défaut est conseillée.

##

<img src="../../start-new-project/new-project.files/new-project2298.png" width="624" />

Figure 3-2      Boîte de réglage de la communication

Dans la boîte ci-dessus, choisissez le service équipement selon le type d'équipement relié. Pour une connexion Ethernet, choisissez « Connexion directe (Ethernet) » dans « Type de connexion ».

ID de connexion : paramètre interne, non modifiable !

Les propriétés de communication peuvent aussi être réglées depuis la connexion dans le gestionnaire de projet ; les autres paramètres se règlent dans les propriétés de communication.

**3.       Boîte des propriétés de l'écran**

Cliquez sur « Suivant » dans la boîte de réglage de la communication : la boîte « Nouvel écran » s'ouvre, où l'on règle le nom et la couleur de fond de l'écran. Le nom par défaut est un numéro d'écran ; la couleur de fond par défaut est le bleu. À chaque création d'écran, le logiciel CommandHMI lui attribue un numéro, qui indique l'ordre des écrans du projet. La numérotation commence à 1 : le premier écran porte le numéro 1, le n° 5 est le cinquième écran. Pour changer la couleur de fond du nouvel écran, cliquez sur le rectangle à côté de « Couleur de fond » : la palette de couleurs s'ouvre. Avec plus de deux cents couleurs prêtes à l'emploi, CommandHMI offre un très large choix. Si cela ne suffit pas, cliquez en bas à droite de la palette pour définir une couleur personnalisée. Dans la boîte « Couleurs personnalisées », choisissez d'abord une couleur de base, puis la teinte dans la zone carrée centrale en faisant glisser la souris ; ajustez aussi avec le rectangle vertical à droite, puis cliquez sur OK. Vous pouvez aussi saisir directement les valeurs de la couleur.

<img src="../../start-new-project/new-project.files/new-project4278.png" width="626" />

Figure 3-3      Boîte « Nouvel écran »

<img src="../../start-new-project/new-project.files/new-project4313.png" width="506" />

Figure 3-4      Boîte de choix de couleur

On peut aussi choisir une image comme fond d'écran. Cliquez sur l'icône de chemin pour indiquer l'emplacement de l'image.

<img src="../../start-new-project/new-project.files/new-project4463.png" width="331" />

Figure 3-5      Chemin de l'image

Cliquez sur OK pour terminer : le système ouvre aussitôt l'écran créé. La préparation du nouveau projet est terminée ; vous pouvez maintenant éditer votre projet.
