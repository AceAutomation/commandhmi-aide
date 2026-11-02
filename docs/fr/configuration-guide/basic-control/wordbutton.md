# Bouton de mot

Le bouton de mot permet d'agir sur un registre de données de l'équipement connecté : Constante, Saisie de valeur, Incrémentation, Décrémentation, Saisie de mot de passe, Addition et Soustraction.

Pour ajouter un bouton de mot :

• Sélectionnez l'icône Bouton de mot<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton222.png" width="29" />dans la barre d'outils : la boîte de dialogue suivante s'ouvre, comme sur la figure 4-76 :

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton308.png" width="664" />

Figure 4-76 Boîte de dialogue Bouton de mot

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton345.png" width="130" />

Pour Forme, Couleur de bordure, Couleur de premier plan, Couleur de fond et Motif, voir l'objet « Bouton de bit ».

**Fonction :**

• Écrire une constante : plusieurs types de données sont disponibles : entier positif 16/32 bits, entier 16/32 bits, BCD positif 16/32 bits et flottant 32 bits. La constante définie est écrite à l'adresse d'écriture. Par exemple, avec l'adresse LW1 et la constante 10, LW1 prend la valeur 10 à chaque appui, quelle que soit sa valeur actuelle.

• Saisir une valeur : choisissez le type de données ; un appui sur le bouton de mot ouvre un clavier pour saisir une valeur comprise entre le minimum et le maximum, comme sur la figure 4-77 :

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton1128.png" width="693" />

Figure 4-77

• Incrémentation : si le paramètre Délai vaut 0, la fonction est identique à Addition. Sinon, la valeur de l'adresse d'écriture augmente de la constante et est écrite dans le registre.

• Décrémentation : si le paramètre Délai vaut 0, la fonction est identique à Soustraction. Sinon, après un certain temps, la valeur de l'adresse d'écriture diminue de la constante et est écrite dans le registre.

• Saisie de mot de passe : identique à « Saisir une valeur », sans l'option de décimales.

• Addition : après avoir défini le type de données, l'adresse d'écriture, la constante et la valeur maximale, chaque appui sur le bouton de mot ajoute la constante à la valeur actuelle du registre, sans dépasser la valeur maximale définie. Par exemple, avec l'adresse LW1, la constante 5 et le maximum 65535, chaque appui ajoute 5 à LW1, sans dépasser 65535.

• Soustraction : après avoir défini le type de données, l'adresse d'écriture, la constante et la valeur minimale, chaque appui sur le bouton de mot soustrait la constante de la valeur actuelle du registre, sans descendre sous la valeur minimale définie. Par exemple, avec l'adresse LW1, la constante 5 et le minimum 0, chaque appui retire 5 à LW1, sans descendre sous 0.

• Nombre total de chiffres : nombre de chiffres, décimales comprises.

• Décimales : si le type de données n'est pas « flottant 32 bits » et qu'il y a des décimales, la valeur maximale saisissable est divisée par 10 puissance n. Par exemple, avec le type « entier positif 32 bits » et 3 décimales, l'utilisateur ne peut saisir que des valeurs de 0 à 99999.999.

• Macro : en cochant « Use Macro », la liste des macros s'affiche. L'utilisateur peut choisir une macro à exécuter à l'appui sur le bouton de mot. Seules les macros compilées figurent dans la liste.

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton3632.png" width="130" />

L'onglet « Étiquette » du « Bouton de mot » est semblable à celui du « Bouton de bit », sauf qu'il ne comporte ni Texte état 1 ni Image état 1, le bouton de mot n'ayant qu'un seul état.

Si le bouton de mot utilise un type de données 32 bits, l'adresse occupe deux mots. Par exemple, si l'on écrit dans le registre V10 d'un automate SIEMENS, les registres occupés sont V10 et V11. Si un autre objet surveille V11, cela ne fonctionnera pas. Faites attention aux types 32 bits pour éviter les erreurs.

Les pages Avancé et Visibilité du bouton de mot sont identiques à celles du bouton de bit ; pour les raccourcis clavier, voir le bouton de bit.
