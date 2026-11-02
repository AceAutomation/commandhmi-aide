# Exporter des données via clé USB

Les IHM de la série HM permettent d'exporter sur clé USB les données historiques, les recettes, les alarmes historiques et les captures d'écran.

Avec la gestion de plusieurs groupes de données historiques dans CommandHMI, le numéro de groupe est nécessaire pour exporter les données historiques. LW60408 contient le numéro de groupe des données historiques sélectionnées. Par exemple : avec LW60408 à 1, l'import/export via clé USB porte sur le groupe de données historiques correspondant uniquement.

Remarque : si la valeur saisie dépasse le nombre maximal de groupes moins 1, cette fonction n'a pas d'effet.

**Exporter les données historiques via clé USB**

1\. Insérez la clé USB

2\. Indiquez dans le registre LW60408 le numéro du groupe de données historiques à importer/exporter.

3\. Mettez LB60127 à ON : l'IHM copie le fichier du groupe de données historiques sur la clé USB sous le nom hisdatai.csv (hisdata1.csv pour le groupe 1).

Mettez LB60128 à ON : l'IHM copie le fichier du groupe de données historiques sur la clé USB ; pour importer le groupe 1, nommez le fichier hisdata1.csv.

Ces bits de déclenchement repassent automatiquement à OFF à la fin de l'export

Pour l'export des données locales, utilisez les registres LW60359-LW60429

**Exporter les recettes**

Avec la gestion de plusieurs groupes de recettes dans CommandHMI, il faut renseigner LW61143 pour l'export des recettes.

1\. Insérez la clé USB.

2\. Indiquez le numéro de groupe dans LW61143.

3\. Mettez LB60163 à ON ; l'IHM copie le fichier de recettes du groupe sur la clé USB

4\. Ces bits de déclenchement repassent automatiquement à OFF à la fin de l'export

Remarque : les données historiques exportées ne peuvent pas être ouvertes directement sur l'ordinateur ; il faut l'outil de conversion SK_SQL_CSV.exe, <img src="../../appendix/usdhisdata.files/image002.jpg" width="86" />situé dans le répertoire racine du logiciel de configuration HM.

Cet outil convertit le fichier exporté en fichier CSV directement lisible. Double-cliquez pour l'ouvrir.

Progression : avancement de la conversion du fichier.

Nom du fichier : sélectionnez le fichier à convertir.

Choisissez données historiques ou alarmes selon le cas. L'encodage par défaut est ANSI et ne peut pas être modifié. Cliquez ensuite sur « Generate CSV ». Quand la barre de progression atteint 100 %, la conversion est terminée.

**Récupérer des captures d'écran via clé USB**

1\. Insérez la clé USB

2\. Dans la configuration, créez un bouton de fonction -&gt; Capture d'écran, et choisissez Export vers clé USB

3\. En touchant ce bouton de fonction, l'IHM enregistre une capture de l'écran courant à l'emplacement correspondant

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />

Remarque :

 • Ne retirez pas la clé USB pendant l'export ;

• Maintenez l'alimentation pendant l'export ;

• Vérifiez que la clé USB dispose de suffisamment d'espace.

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />
