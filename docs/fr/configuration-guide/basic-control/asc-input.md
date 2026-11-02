# Saisie ASCII

Cliquez sur l'icône Saisie ASCII<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input38.png" width="30" /> : la boîte de dialogue de la figure 4-100 s'ouvre :

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input93.png" width="665" />

Figure 4-100 Boîte de dialogue Saisie ASCII

• Adresse d'écriture : adresse dans laquelle le texte ASCII saisi est écrit.

• Surveillance : valeur d'adresse lue et affichée par cet objet.

• Adresse de surveillance identique à l'adresse d'écriture : l'adresse surveillée est la même que l'adresse d'écriture.

• Adresse de surveillance : adresse à lire

• Total : nombre maximal de caractères affichables.

• Taille de police : taille des caractères affichés

• Inverser les octets haut et bas de la saisie : l'octet haut de la valeur saisie est échangé avec l'octet bas, puis la donnée ainsi obtenue est enregistrée à l'adresse de mot surveillée.

• Mot de passe : si cette option est cochée, l'objet n'affiche pas les caractères mais des astérisques (\*)

• Utiliser UNICODE : la valeur de l'adresse de surveillance est affichée en codage Unicode

Alignement :

• Gauche : le texte est affiché dans la partie gauche de la zone d'affichage.

• Centre : le texte est affiché au centre de la zone d'affichage.

• Droite : le texte est affiché dans la partie droite de la zone d'affichage.

• Utiliser une macro : cochez « Use Macro » pour afficher la liste des macros. L'utilisateur peut en choisir une à exécuter à l'appui sur le bouton. Seules les macros compilées figurent dans la liste.

<img src="../../../configuration-guide/basic-control/asc-input.files/asc-input1310.png" width="130" />

Remarque : par exemple, avec un type de données 32 bits, l'adresse occupe 2 mots. Si l'on écrit dans un registre de données d'un automate SIEMENS à l'adresse V10, les registres occupés sont V10 et V11 ; si un autre objet surveille aussi V11, une erreur se produit. Faites attention à l'utilisation des types 32 bits pour éviter les erreurs de données et d'adresses.

Remarque : les autres fonctions de la page Général sont identiques à celles de l'Affichage ASCII.

Remarque : pour les pages « Avancé » et « Visibilité », voir le Bouton de bit.
