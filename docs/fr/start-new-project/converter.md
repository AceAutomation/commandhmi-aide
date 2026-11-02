# Charger l'historique des données

Lancez le logiciel de configuration CommandHMI ; cliquez sur <img src="../../start-new-project/converter.files/converter46.png" width="29" />.

![](../../start-new-project/converter.files/001.png)

« Charger l'historique des données » transfère l'historique de l'IHM vers le disque dur.

• Chemin du fichier : emplacement d'enregistrement ; cliquez sur « Parcourir » pour le choisir.

• Nom du fichier : nom du fichier chargé ; ce fichier ne s'ouvre pas directement, il faut un outil de conversion. Voir « Exporter les données et alarmes historiques sur clé USB » en annexe de l'aide.

• Cliquez sur « Charger le fichier » pour lancer le chargement ; le fichier est enregistré à l'emplacement choisi.

• CommandHMI gérant désormais plusieurs groupes de données historiques, le chargement enregistre, en plus du fichier de base de données historique, chaque groupe de données en fichier .CSV. Par exemple, pour un fichier nommé « temp », la base de données historique s'appelle « temp », le CSV du groupe 0 « temp_hisdata0.csv », celui du groupe 1 « temp_hisdata1.csv », etc.

<img src="../../start-new-project/converter.files/converter954.png" width="130" />

Le chargement de l'historique des données se fait comme celui des recettes et du projet ; la conversion de fichiers Samdraw3.3 vers CommandHMI est désactivée.
