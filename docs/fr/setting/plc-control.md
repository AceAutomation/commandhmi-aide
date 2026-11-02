# Commande par l'automate

La commande par l'automate permet à l'automate de changer d'écran, de niveau utilisateur, de recette et d'écrire une recette. Double-cliquez sur « Commande par l'automate » dans le gestionnaire de projet : la boîte de la figure 7-8 s'ouvre :

Figure 7-8      Boîte de commande par l'automate

• Changer de recette : l'IHM change de recette selon la valeur de cette adresse.

• Écrire la recette : l'IHM commande l'écriture de la recette selon la valeur de cette adresse.

• Niveau utilisateur courant : l'IHM règle le niveau utilisateur courant selon la valeur de cette adresse.

• Changement d'écran par adresse de mot : l'IHM change d'écran selon la valeur de cette adresse de mot ; si elle vaut n, elle passe à l'écran n.

• Changement d'écran par adresse de bit : double-cliquez sur la ligne « Nouveau » ; la boîte de la figure 7-9 s'ouvre :

Nouvelle commande par bit :

<img src="../../setting/plc-control.files/image004.jpg" width="458" />

Nouvelle commande d'écran par mot

<img src="../../setting/plc-control.files/image006.jpg" width="497" />

Écran : la commande par mot de l'automate ne bascule qu'entre écrans

Fenêtres : la commande par mot de l'automate ne bascule qu'entre fenêtres

Écran / fenêtre : la commande par mot de l'automate bascule entre écrans et fenêtres

<img src="../../setting/plc-control.files/image005.jpg" width="130" />

Remarque : lors d'un changement d'écran par l'automate, la première valeur lue est sans effet. Le changement n'a lieu que si la valeur du registre de l'automate diffère de la première valeur lue.
