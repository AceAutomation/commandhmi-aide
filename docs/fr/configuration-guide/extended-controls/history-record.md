# Affichage des données historiques

<span id="OLE_LINK279"></span><span id="OLE_LINK278"></span>         En pratique, les données de l'automate ou de l'équipement connecté, comme les alarmes, peuvent changer à tout moment. Pour consulter des données historiques, on utilise le collecteur de données historiques de CommandHMI.

CommandHMI propose un collecteur de données historiques, accessible depuis le gestionnaire de projet. Pour un nouveau projet, faites un clic droit sur « Collecteur de données historiques » pour en ajouter un, puis double-cliquez sur « Collecteur de données historiques 0 » pour le paramétrer. Pour les détails, voir les propriétés du « [Collecteur de données historiques](../../setting/history-data.md) » au chapitre 6.

Cliquez sur le bouton Affichage des données historiques<img src="../../../configuration-guide/extended-controls/history-record.files/history-record687.png" width="32" /> de la barre d'outils : la boîte de dialogue suivante s'ouvre :

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record747.png" width="579" />

Figure 4-65 Boîte de dialogue Affichage des données historiques

**Général :**

• Couleur de premier plan : cliquez sur la couleur pour changer la couleur de premier plan de l'affichage.

• Couleur de bordure : cliquez sur la couleur pour changer la couleur de la bordure.

• Titre : taille et style de police, couleur de fond, couleur du texte et affichage ou non de la date et de l'heure. Pour les réglages de langue, voir « Affichage des alarmes ».

• Données : taille de police, couleur et nombre maximal de lignes affichées.

Adresse de contrôle :

Écrivez 1 dans le registre à l'offset 0 (entier 16 bits, de même pour les offsets 1 à 12), l'heure de début dans les registres aux offsets 1 à 6, l'heure de fin dans ceux aux offsets 7 à 12, puis 1 dans le registre à l'offset 13 : l'affichage présente alors les données de cette période. Le registre à l'offset 13 se remet automatiquement à zéro. Pour afficher toutes les données, écrivez 0 dans le registre à l'offset 0.

Cette adresse occupe 40 offsets consécutifs, dont la signification est la suivante :

|                |                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Offset d'adresse | Élément contrôlé par le registre                                                                                                                                       |
| 0              | 1 : affiche les données entre l'heure de début et de fin ; 0 : affiche toutes les données.                                                                              |
| 1              | Heure de début (année) ; un mot                                                                                                                                          |
| 2              | Heure de début (mois) ; un mot                                                                                                                                           |
| 3              | Heure de début (jour) ; un mot                                                                                                                                           |
| 4              | Heure de début (heure) ; un mot                                                                                                                                          |
| 5              | Heure de début (minute) ; un mot                                                                                                                                         |
| 6              | Heure de début (seconde) ; un mot                                                                                                                                        |
| 7              | Heure de fin (année) ; un mot                                                                                                                                            |
| 8              | Heure de fin (mois) ; un mot                                                                                                                                             |
| 9              | Heure de fin (jour) ; un mot                                                                                                                                             |
| 10             | Heure de fin (heure) ; un mot                                                                                                                                            |
| 11             | Heure de fin (minute) ; un mot                                                                                                                                           |
| 12             | Heure de fin (seconde) ; un mot                                                                                                                                          |
| 13             | Passage de 0 à 1 avec l'offset 0 à 1 : affiche les données de la période indiquée ; remise à zéro automatique ; <span id="OLE_LINK339"></span>un mot                      |
| 14             | Nombre total d'enregistrements entre l'heure de début et l'heure de fin ; double mot                                                                                     |

Données :

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record2617.png" width="581" />

Numéro de groupe : CommandHMI propose plusieurs groupes de données historiques au choix.

Affichage des données historiques via les adresses de contrôle : la configuration est la suivante, figure 4-65-1 :

<img src="../../../configuration-guide/extended-controls/history-record.files/001.png" width="797" />

Figure 4-65-1

Dans cet exemple, saisissez 1 dans « Afficher toutes les données » et 1 dans « Rechercher » : l'objet affiche toutes les données historiques entre l'heure de début et l'heure de fin, comme sur la figure 4-65-2

<img src="../../../configuration-guide/extended-controls/history-record.files/002.png" width="795" />

Figure 4-65-2

Saisissez 1 dans « Afficher toutes les données », réglez l'heure de début à 2016-7-11 3: 30: 4 et l'heure de fin à 2016-7-11 14: 39: 4 ; quand « Rechercher » reçoit la valeur 1, seules les données de cette période sont affichées.

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record3263.png" width="130" />

Pour la page « Visibilité », voir l'objet « Bouton de bit ».
