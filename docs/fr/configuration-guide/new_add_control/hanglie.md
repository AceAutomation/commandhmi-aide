# Tableau de données

Cet élément affiche les données définies par l'utilisateur sous forme de grille, avec une interface simple de sélection et de manipulation. Ses fonctions incluent le changement de page automatique, l'insertion, la suppression, la copie et le collage.

Page Général

![](../../../configuration-guide/new_add_control/hanglie.files/001.png)

Réglages des données

Nombre total de champs : nombre de colonnes du tableau

Nombre initial d'éléments : nombre initial de lignes du tableau

Nombre d'éléments par page : nombre de lignes affichées sur une page

Adresse de départ : adresse du premier élément du tableau

Offset d'adresse : offset d'adresse de chaque ligne de la colonne

Aperçu des adresses

Affiche la répartition des adresses du tableau

Réglages des champs

Champ courant : colonne courante

Type de champ : état, chaîne ou numérique

Largeur du champ : largeur de la colonne

Alignement : alignement des éléments de la colonne

Nombre total d'états : nombre d'états de l'élément de la colonne

Avancé

![](../../../configuration-guide/new_add_control/hanglie.files/002.png)

état

Élément sélectionné : élément sélectionné

Nombre réel d'éléments : nombre réel d'éléments

Nombre d'éléments visibles : nombre total d'éléments visibles

Page courante : numéro de la page courante

Nombre de pages : nombre total de pages

Mise à jour automatique des données de la page : Oui : mise à jour automatique ; sinon, commandée par l'adresse définie

Mise à jour des données : adresse de mise à jour

Opérations

Bit d'invisibilité : rend les données invisibles

Niveau d'invisibilité : condition d'activation du bit d'invisibilité

Adresse de déclenchement page précédente : passe à la page précédente

Adresse de déclenchement page suivante : passe à la page suivante

Adresse de déclenchement élément précédent : sélectionne l'élément précédent de la colonne

Adresse de déclenchement élément suivant : sélectionne l'élément suivant de la colonne

Adresse de déclenchement copier : copie l'élément courant

Adresse de déclenchement coller : colle les données

Adresse de déclenchement remplacer : écrase l'élément courant avec les données collées

Adresse de déclenchement insérer : insère un élément à la position courante

Adresse de déclenchement couper : coupe les données

Bit de protection tactile : protection contre le toucher

Adresse de sélection d'élément : définit l'élément à sélectionner

Déclenchement de la sélection : active la sélection définie

Adresse du nombre total d'éléments : définit le nombre total d'éléments

Déclenchement du nombre total d'éléments : active le nombre total d'éléments défini

Avancé 2

La zone tampon est une zone de mémoire temporaire pour les données des éléments. Ses données peuvent être insérées, ajoutées ou écrites dans l'élément sélectionné, et les données de l'élément sélectionné peuvent y être lues.

![](../../../configuration-guide/new_add_control/hanglie.files/003.png)

Zone tampon

Adresse de départ : adresse de départ de la zone tampon

Bit d'insertion à l'élément sélectionné : à ON, insère les données du tampon (adresse : début du tampon + offset de l'élément) à l'élément sélectionné ; le nombre réel d'éléments augmente de 1. Si le nombre maximal est déjà atteint, l'insertion est impossible.

Bit d'ajout après l'élément sélectionné : à ON, ajoute les données du tampon (adresse : début du tampon + offset de l'élément) à l'élément sélectionné ; le nombre réel d'éléments augmente de 1. Si le nombre maximal est déjà atteint, l'ajout est impossible.

Ajouter à la fin : à ON, ajoute les données du tampon (adresse : début du tampon + offset de l'élément) à la fin ; le nombre réel d'éléments augmente de 1. Si le nombre maximal est déjà atteint, l'ajout est impossible.

Lire l'élément sélectionné : à ON, lit le contenu de l'élément sélectionné dans le tampon (adresse : début du tampon + offset de l'élément)

Écrire l'élément sélectionné : à ON, écrit les données du tampon (adresse : début du tampon + offset de l'élément) dans l'élément sélectionné

Apparence

![](../../../configuration-guide/new_add_control/hanglie.files/004.png)

Réglages des champs

Définit la numérotation du tableau, etc.

style

Définit les lignes de grille, la couleur de fond, la couleur de sélection, etc.
