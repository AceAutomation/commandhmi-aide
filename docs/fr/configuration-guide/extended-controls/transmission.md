# Transmission de données

Sert à transmettre des données entre l'automate et l'IHM ou entre deux automates. Cliquez sur « Transmission de données » dans le gestionnaire de projet pour afficher la liste des transmissions.

<img src="../../../configuration-guide/extended-controls/transmission.files/image005.jpg" width="564" />

Figure 7-36

La liste détaille toutes les transmissions. L'utilisateur peut les créer, les supprimer et les modifier. CommandHMI prend en charge jusqu'à 512 transmissions de données.

Pour créer ou modifier une transmission, il faut ouvrir sa page de propriétés :

<img src="../../../configuration-guide/extended-controls/transmission.files/image006.jpg" width="339" />

Figure 7-37

**1. Attributs**

Périodique / Déclenché : mode de déclenchement de la transmission.

Périodique : transmission à l'intervalle défini.

Déclenché : la transmission est commandée par une adresse ; elle a lieu quand l'adresse vaut 1.

Remise à zéro automatique : quand l'adresse de déclenchement vaut 1, elle est remise automatiquement à 0.

Type d'adresse : type des données transmises : bit / mot / double mot.

Mot / Bit : longueur des données à transmettre, de 1 à 64.

**2. Adresses**

Adresse source : adresse d'origine des données, <span id="OLE_LINK497"></span><span id="OLE_LINK498"></span>du même type que celui défini dans « Attributs ».

Adresse de destination : adresse de destination des données, du même type que celui défini dans « Attributs ».

<img src="../../../configuration-guide/extended-controls/transmission.files/image004.jpg" width="130" />

L'adresse de destination et l'adresse source ne peuvent pas être sur le même automate.
