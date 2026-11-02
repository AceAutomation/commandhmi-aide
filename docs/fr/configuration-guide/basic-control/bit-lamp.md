# Voyant de bit

Le voyant de bit permet de surveiller l'état ON/OFF d'un contact (bit) de l'équipement connecté et de l'afficher sur l'écran de l'IHM.

Comme sur la figure 4-78 ci-dessous :

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image007.jpg" width="554" alt="2018_11_20_14_25_09.jpg" />

Figure 4-78

Créer un voyant de bit :

1\. Sélectionnez l'icône Voyant de bit<img src="../../../configuration-guide/basic-control/bit-lamp.files/image002.jpg" width="31" /> dans la barre d'outils : la boîte de dialogue de la figure 4-79 s'ouvre :

Figure 4-79    Boîte de dialogue Voyant de bit

• Type de données : la liste propose trois options : Bit, Bit de mot et Bit de double mot. Avec « Bit de double mot », l'adresse surveillée (lue) est une adresse de double mot.

• Numéro de bit : pour les types « Bit de mot » ou « Bit de double mot », l'état ON/OFF est déterminé par la valeur du bit indiqué : de 0 à 15 pour un bit de mot, de 0 à 31 pour un bit de double mot.

Par exemple, avec « Bit de mot », l'adresse surveillée LW1 vaut 23 ; si le numéro de bit est 3, l'état est 0, car 23 s'écrit 10111 en binaire et son 3e chiffre en partant de la droite est 0.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Remarque : <span id="OLE_LINK707"></span><span id="OLE_LINK706"></span>pour Forme, Couleur de bordure, Couleur de premier plan, Couleur de fond et Motif, voir l'objet Bouton de bit.

2\. Dans la page « Général » du voyant de bit, choisissez l'adresse surveillée par ce voyant. Dans « Étiquette », vous pouvez définir les textes et images affichés et choisir le clignotement.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Remarque : la page « Étiquette » du « Voyant de bit » est identique à celle du « Bouton de bit ».

3\. Pour modifier les propriétés du voyant, double-cliquez dessus et modifiez-les dans la boîte de dialogue.

<img src="../../../configuration-guide/basic-control/bit-lamp.files/image004.jpg" width="130" />

Remarque : la page Visibilité du Voyant de bit est identique à celle du Bouton de bit.

Une fois les propriétés réglées, cliquez sur « OK » pour ajouter l'objet à la zone de vue (l'écran)
