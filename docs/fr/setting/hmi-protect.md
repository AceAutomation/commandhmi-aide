# Protection IHM

La protection IHM définit une période pendant laquelle l'IHM fonctionne normalement. Au-delà, l'IHM bascule sur un écran donné, où un mot de passe est nécessaire pour la réutiliser.

Double-cliquez sur l'option « Protection IHM » dans le gestionnaire de projet pour ouvrir la boîte de la figure 7-14 :

<img src="../../setting/hmi-protect.files/hmi-protect343.png" width="622" />

Figure 7-14    Boîte de protection IHM

Exemple d'utilisation de cette fonction :

➢Cochez « Mot de passe de déverrouillage » : un mot de passe sera demandé pour accéder à la protection IHM la fois suivante.

➢Cochez « Lever tous les niveaux » : la saisie de ce mot de passe au déverrouillage lève tous les niveaux de protection IHM.

➢Cochez « Protection IHM » : l'onglet « Réglages de protection » s'ouvre automatiquement, comme ci-dessous :

<img src="../../setting/hmi-protect.files/hmi-protect743.png" width="623" />

Figure 7-15    Réglages de la protection IHM

Réglez le « Nombre total de niveaux de mot de passe » sur 3 ; choisissez le bouton 1, puis 2009-04-01 et 12-00-00 dans la colonne « Limite de temps » des « Paramètres » ; choisissez l'écran 1 comme « Écran d'avertissement » ; réglez le « Mot de passe de déverrouillage » sur 1111. La protection de niveau 1 est réglée.

De la même façon, réglez les limites de temps et les mots de passe des niveaux 2 et 3.

• lever tous les niveaux

Une fois cette fonction activée et le mot de passe défini, ce mot de passe lève tous les niveaux de protection IHM

•  mot de passe à l'ouverture

Une fois cette fonction activée et le mot de passe défini, ce mot de passe sera demandé la fois suivante pour ouvrir la protection IHM et en consulter les informations

•  activer la protection par mot de passe

Active la protection IHM. Le détail se règle dans « Réglages de protection ».

• réglages de protection

Nombre total de niveaux de mot de passe : jusqu'à 15 niveaux de protection IHM, pour différentes périodes selon les besoins

Niveau de mot de passe courant : les paramètres ci-dessous s'appliquent au niveau courant

Paramètres :

Durée d'utilisation : date d'expiration de la protection IHM

Écran d'avertissement d'expiration : écran affiché à l'expiration de la protection IHM

Mot de passe de déverrouillage : mot de passe qui lève la protection IHM à son expiration

Réglages avancés :

Afficher les jours restants : affiche le nombre de jours restant avant la fin de la durée de protection IHM

Avance :

Nombre de jours avant la fin de la durée de protection IHM à partir duquel l'avertissement s'affiche

Retard :

Une fois la durée de protection IHM écoulée, l'écran indiqué s'affiche à l'intervalle indiqué pendant le nombre de jours réglé

Priorité entre avance et retard

Avance cochée, retard coché : l'avance s'applique

Avance non cochée, retard coché : le retard s'applique

Avance cochée, retard coché, fonction « Déverrouillage différé de la protection IHM » du bouton de fonction non utilisée : l'avance s'applique

Avance cochée, retard coché, fonction « Déverrouillage différé de la protection IHM » du bouton de fonction utilisée : le retard s'applique

•  exemple d'utilisation :

Supposons que le nombre total de niveaux de mot de passe réglé dans cette boîte soit 3. Choisissez ensuite 0 dans « Niveau de mot de passe courant ». Dans « Paramètres », choisissez la date d'expiration dans la colonne « Durée d'utilisation », par exemple 2009/04/01. Saisissez l'heure dans la colonne suivante, par exemple 12:00:00. Choisissez l'écran affiché à l'expiration dans l'option « Écran d'avertissement d'expiration », par exemple l'écran 1. Saisissez dans « Mot de passe de déverrouillage » le mot de passe qui lève la protection, par exemple 1111. La protection IHM de niveau 1 est réglée.

Choisissez ensuite 1 dans « Niveau de mot de passe courant ». Dans « Paramètres », choisissez la date dans la colonne « Durée d'utilisation », par exemple 2009-04-05. Saisissez l'heure dans la colonne suivante, par exemple 12-00-00. Choisissez l'écran affiché à l'expiration dans l'option « Écran d'avertissement d'expiration », par exemple l'écran 2. Saisissez dans « Mot de passe de déverrouillage » le mot de passe qui lève la protection, par exemple 2222. La protection IHM de niveau 2 est réglée.

Choisissez ensuite 2 dans « Niveau de mot de passe courant ». Dans « Paramètres », choisissez la date dans la colonne « Durée d'utilisation », par exemple 2009-04-10. Saisissez l'heure dans la colonne suivante, par exemple 12-00-00. Choisissez l'écran affiché à l'expiration dans l'option « Écran d'avertissement d'expiration », par exemple l'écran 3. Saisissez dans « Mot de passe de déverrouillage » le mot de passe qui lève la protection, par exemple 3333. La protection IHM de niveau 3 est réglée.

3 Réglages de protection IHM après un clic sur « OK ».

Supposons que nous soyons le 2009-04-01 à 08-00-00. La durée d'utilisation de la protection IHM de niveau 1 se termine le 2009-04-01 à 12-00-00 : l'échéance n'étant pas atteinte, l'IHM fonctionne normalement. Quatre heures plus tard, le 2009-04-01 à 12-00-00, l'IHM bascule automatiquement sur l'écran réglé pour cette échéance. Pour continuer à utiliser l'IHM et accéder aux autres écrans, l'utilisateur peut ajouter dans cet écran (écran 1) un bouton de fonction avec la fonction « Déverrouiller la protection IHM » : à l'échéance du niveau 1, un appui sur ce bouton ouvre une boîte où l'on saisit le mot de passe de déverrouillage du niveau 1, ici 1111, ce qui lève la protection.

Une fois le niveau 1 déverrouillé, l'IHM fonctionne normalement. Plus tard, le 2009-04-05 à 12-00-00, l'échéance du niveau 2 étant atteinte, l'IHM bascule automatiquement sur l'écran de protection réglé (écran 2) ; de la même façon, l'utilisateur utilise le bouton de fonction « Déverrouiller la protection IHM » et saisit le mot de passe de niveau 2 (2222) : l'IHM fonctionne de nouveau normalement.

La protection IHM de niveau 3 étant réglée, de la même façon, le 2009-04-10 à 12-00-00, l'utilisateur utilise le bouton de fonction « Déverrouiller la protection IHM » et saisit le mot de passe de déverrouillage de niveau 3 (3333) : l'IHM fonctionne de nouveau normalement.

Une fois les 3 niveaux déverrouillés, la protection IHM n'est plus active et l'IHM fonctionne normalement.

Cet exemple illustre l'utilisation de la protection IHM. Le réglage des autres niveaux de mot de passe se fait de la même façon.
