# HTTP

<img src="../../setting/lisanbaojing.files/image007.jpg" width="133" alt="lisanbaojing2414" /> Seul l'écran distant prend en charge cette fonction

![](../../setting/http.files/open.png)

Cette fonction permet de régler facilement les paramètres du serveur HTTP

Ø  onglet « Général »

<img src="../../setting/http.files/general.png" width="606" />

- Nom

Nom de la connexion

- URL

URL de destination de la requête HTTP

- Méthode

Méthode de la requête HTTP : GET ou POST

- Encodage

Format d'encodage

- En-tête de requête

En-tête de la requête HTTP

- Timeout

Délai de réponse HTTP

- Formats

au choix : JSON (général) ou JSON (avancé), [comme pour 【MQTT】](mqtttheme.md#anchor-name)

- Modes de transmission

au choix : automatique ou déclenché par bit

Ø  Onglet « Adresse » (JSON général)

Disponible quand le format \[JSON général\] est choisi dans l'onglet \[Général\].

Ajoute une valeur, de type bit ou mot : valeur fixe ou donnée lue à une adresse indiquée. [Voir 【MQTT】](mqtttheme.md#anchor-name1)

Ø  Onglet « Envoi JSON » (JSON avancé)

Disponible quand le format \[JSON avancé\] est choisi dans l'onglet \[Général\].
<img src="../../setting/http.files/sendjson.png" width="606" />

Règle les données envoyées ; le réglage des adresses accepte une arborescence (éléments, tableaux, etc.), l'horodatage et le nom des données sont personnalisables. [Voir 【MQTT】](mqtttheme.md#anchor-name1)

Ø  Onglet « Réception JSON »

<img src="../../setting/http.files/receivejson.png" width="606" />

Règle les données reçues ; le réglage des adresses accepte une arborescence (éléments, tableaux, etc.), l'horodatage et le nom des données sont personnalisables. Voir [【Envoi JSON】](#anchor-name)

Ø  onglet « Sécurité »

Voir l'onglet \[Sécurité\] de [\[MQTT\].](mqtttheme.md#anchor-name2)
