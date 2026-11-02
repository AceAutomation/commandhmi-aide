# Liste déroulante

La liste déroulante affiche une liste d'éléments que l'utilisateur peut consulter et sélectionner. Quand un élément est sélectionné, sa valeur est écrite à l'adresse de contrôle du registre de mot.

Son icône dans la barre d'outils est<img src="../../../configuration-guide/new_add_control/combobox.files/combobox771.png" width="35" /> ; cliquez dessus pour ouvrir la boîte de dialogue de la figure 4-115 :

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1012.png" width="677" />

Figure 4-115   Page Général de la liste déroulante

• Nombre total d'états : nombre d'états de l'objet. Chaque élément de la liste représente un état ; sa valeur peut être écrite dans \[Adresse de contrôle\].

• Couleur de fond : couleur de fond de l'élément sélectionné

• Couleur du texte : couleur du texte de l'élément sélectionné

• Adresse de contrôle : adresse d'écriture

• Utiliser une macro : exécute la macro choisie si l'objet est actif.

Réglage des états : cliquez sur la page « Réglage des états » ; elle se présente comme sur la figure 4-116 :

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1554.png" width="675" />

Figure 4-116   Page Réglage des états de la liste déroulante

• Langue : la « police » et la « taille de police » sont communes à tous les états, mais peuvent différer selon la langue.

• Valeur : définit une valeur pour chaque élément, selon les deux règles suivantes :

a\. \[Lecture\] : si le système détecte un changement de \[Adresse de contrôle\], l'objet compare son contenu aux valeurs et sélectionne le premier élément correspondant. Si aucun ne correspond, l'objet passe à l'état d'erreur et active le bit de notification d'erreur (s'il est défini).

b\. \[Écriture\] : quand un élément est sélectionné, le système écrit sa valeur dans \[Adresse de contrôle\].

• Libellé : texte de chaque élément. Le menu affiche les textes de tous les éléments de la liste pour consultation et sélection.

• Notification d'erreur

a\. Par exemple, avec \[Nombre d'états\] à 8, l'état 8 est l'état d'erreur. De même, avec 11, l'état 11 est l'état d'erreur.

b\. En cas d'erreur, la liste affiche le texte de l'état d'erreur.

En cas d'erreur, le système met un bit donné à ON / OFF (écrit dans \[Adresse de notification d'erreur\]). Ce bit peut servir à déclencher une action corrective.

Pour les pages « Avancé » et « Visibilité », voir le « Bouton de bit ».
