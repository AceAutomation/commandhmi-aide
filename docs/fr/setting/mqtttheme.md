# Sujets

Ø  ajouter un sujet de publication

• onglet « Général »

![](../../setting/mqtttheme.files/addpublish.png)

- Nom

Nom du sujet MQTT dans le projet

- Sujet

Sujet reçu par le serveur MQTT lors de l'envoi d'un message

- Format

\[JSON (général)\] : données au format JSON en structure de liste.

\[JSON (avancé)\] : format JSON avec une arborescence librement personnalisable.

- Mode d'envoi

**■  automatique**

Sur changement de valeur : transmission automatique quand le contenu de l'adresse surveillée change.

Cyclique : le contenu de l'adresse surveillée est transmis périodiquement.

**■  déclenchement par bit**

Le contenu est transmis quand l'adresse de bit indiquée est déclenchée.

• Adresse (JSON général)

Disponible quand le format \[JSON général\] est choisi dans l'onglet \[Général\].
<img src="../../setting/mqtttheme.files/addgeneraladdr.png" width="606" />

Ajoute une valeur, de type bit ou mot : valeur fixe ou donnée lue à une adresse indiquée.

• Adresse (JSON avancé)

Disponible quand le format \[JSON avancé\] est choisi dans l'onglet \[Général\].
<img src="../../setting/mqtttheme.files/addextendaddr.png" width="606" />

Le réglage des adresses accepte une arborescence (éléments, tableaux, etc.) ; l'horodatage et le nom des données sont personnalisables.

- élément

Ajoute un élément de données. Un élément peut contenir plusieurs données, chacune avec son propre nom et sa valeur.

Les données de l'élément sont entre accolades { }.

- Tableau

Ajoute un tableau de données. Un tableau peut contenir plusieurs données, mais n'a qu'un seul nom.

Les données du tableau sont entre crochets \[ \].

- valeur

Ajoute une valeur, une chaîne ou un horodatage. Pour une valeur ou une chaîne : valeur fixe ou donnée lue à une adresse indiquée.

- modèle

Convertit un texte JSON saisi par l'utilisateur en arborescence

- Aperçu

Convertit l'arborescence courante en texte JSON

• Onglet « Sécurité »

Une fois activée, s'applique quand l'adresse de bit indiquée remplit la condition de déclenchement.
<img src="../../setting/mqtttheme.files/publishsecurity.png" width="606" />

Ø  Ajouter un sujet d'abonnement

• Onglet « Général »

<img src="../../setting/mqtttheme.files/addsubscribe.png" width="606" />

- Nom

Nom du sujet MQTT dans le projet

- Sujet

Sujet auquel s'abonner sur le serveur MQTT

- Le format est

[identique à 【Publication】](#anchor-name)

- Mode de fonctionnement

■  automatique

automatiquement.

■  Manuel

Exécution en mettant à 1 l'adresse indiquée.

• Onglet « Adresse »

[Identique à 【Publication】](#anchor-name)

• Onglet « Sécurité »

[Identique à 【Publication】](#anchor-name)
