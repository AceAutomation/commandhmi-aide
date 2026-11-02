# Affichage de l'historique des alarmes

L'historique des alarmes affiche les alarmes passées ; son utilisation est la même que celle de l'affichage des alarmes. Cliquez sur le bouton Historique des alarmes <img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog791.png" width="32" /> de la barre d'outils pour ouvrir la boîte de dialogue suivante :

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog1031.png" width="650" />

Adresse de contrôle : écrivez 1 dans le registre à l'offset 0 (entier 16 bits, de même pour les offsets 1 à 12), l'heure de début dans les registres aux offsets 1 à 6 et l'heure de fin dans ceux aux offsets 7 à 12 : l'historique affiche alors les alarmes de cette période. Pour afficher tout l'historique, écrivez 0 dans le registre à l'offset 0. Le registre à l'offset 13 n'est pas utilisé pour l'instant.

Cette adresse occupe 12 offsets consécutifs, dont la signification est la suivante :

|                |                                                                                              |
|----------------|----------------------------------------------------------------------------------------------|
| Offset d'adresse | Élément contrôlé par le registre                                                              |
| 0              | 1 : affiche les données entre l'heure de début et de fin ; 0 : affiche toutes les données.    |
| 1              | Heure de début (année)                                                                       |
| 2              | Heure de début (mois)                                                                        |
| 3              | Heure de début (jour)                                                                        |
| 4              | Heure de début (heure)                                                                       |
| 5              | Heure de début (minute)                                                                      |
| 6              | Heure de début (seconde)                                                                     |
| 7              | Heure de fin (année)                                                                         |
| 8              | Heure de fin (mois)                                                                          |
| 9              | Heure de fin (jour)                                                                          |
| 10             | Heure de fin (heure)                                                                         |
| 11             | Heure de fin (minute)                                                                        |
| 12             | Heure de fin (seconde)                                                                       |

• Date d'effacement de l'alarme : date d'annulation de l'alarme

• Heure d'effacement de l'alarme : heure d'effacement de l'alarme

• Alarme effacée : la ligne d'une alarme effacée est affichée dans cette couleur

• Comptage des alarmes : active le comptage des alarmes, affiché après le message d'alarme.

• Durée cumulée : active la durée cumulée de l'alarme, affichée après le message d'alarme.

• OK : couleur d'une alarme au moment où elle se produit

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog2576.png" width="130" />

Pour l'utilisation de base, voir l'objet « Affichage des alarmes ».

Pour la page « Visibilité », voir l'objet « Bouton de bit ».
