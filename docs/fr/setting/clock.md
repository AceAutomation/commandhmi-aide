# Horloge

Le réglage de l'horloge comprend trois fonctions : télécharger l'heure système dans l'IHM, écrire l'heure dans l'automate et se synchroniser avec l'automate.

Double-cliquez sur « Horloge » dans le gestionnaire de projet pour ouvrir la boîte de réglage de l'horloge.

<img src="../../setting/clock.files/image004.jpg" width="388" />

<img src="../../setting/clock.files/image005.jpg" width="388" />

Figure 7-11 Boîte de réglage de l'horloge

Télécharger l'horloge système dans l'IHM : indique s'il faut télécharger l'heure système dans l'IHM.

• Écrire l'heure/la date dans l'automate :

• Le type de données et la longueur sont des valeurs par défaut.

• Heure : année-mois-jour-heure-minute-seconde-jour de la semaine. Pour le détail, voir LW 60000~LW 60006 dans les adresses de registres. Le jour de la semaine de l'heure système n'est pas modifiable.

Adresse d'écriture : l'heure système est écrite à cette adresse de l'automate.

• Mode de déclenchement :

Périodique : écrit l'heure système à l'adresse automate indiquée, à l'intervalle indiqué.

Déclenchement : écrit l'heure système à l'adresse automate indiquée quand l'adresse de déclenchement vaut 1.

Remise à zéro auto : remet automatiquement l'adresse de déclenchement à 0 quand elle vaut 1.

**Synchronisation avec l'heure de l'automate :**

Le type de données et la longueur sont des valeurs par défaut.

 Heure : année-mois-jour-heure-minute-seconde-jour de la semaine. Pour le détail, voir LW 60000~LW 60006 dans les adresses de registres. Le jour de la semaine de l'heure système n'est pas modifiable.

• Adresse de lecture : l'information est lue à cette adresse de l'automate.

• Mode de déclenchement :

Périodique : écrit l'heure système à l'adresse automate indiquée, à l'intervalle indiqué.

Déclenchement : l'heure système est synchronisée avec l'automate quand l'adresse de déclenchement vaut 1.

Remise à zéro auto : remet automatiquement l'adresse de déclenchement à 0 quand elle vaut 1.
