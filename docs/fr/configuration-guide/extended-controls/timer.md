# Temporisateur

Le temporisateur est un objet déclenché par le temps. Dans CommandHMI, il sert à déclencher une macro. Cliquez sur <img src="../../../configuration-guide/extended-controls/timer.files/timer152.png" width="35" /> dans la barre d'outils ou double-cliquez sur un temporisateur existant pour ouvrir ses réglages :

<img src="../../../configuration-guide/extended-controls/timer.files/timer240.png" width="662" />

**Contrôle**

• Mode d'exécution : Toujours exécuter ou Déclenché par adresse.

1\. « Toujours exécuter » : la macro est exécutée en permanence à la fréquence définie.

2\. « Déclenché par adresse » : la macro est exécutée à la fréquence définie quand le bit spécifié vaut 1, et n'est pas exécutée quand il vaut 0.

• Adresse : en mode « Déclenché par adresse », un champ apparaît pour saisir le bit qui commande l'exécution de la macro. Quand il vaut 1, la macro s'exécute.

• Fréquence : fréquence d'exécution de la macro, de 0,1 à 60 s.

• Nombre d'exécutions : nombre d'exécutions de la macro. À 0, la macro est exécutée en permanence.

**Fonction**

• Type de fonction : type de fonction à exécuter. Dans CommandHMI, la fonction du temporisateur est une macro.

• Nom : nom de la macro à exécuter. Le temporisateur ne peut pas être configuré s'il n'existe aucune macro.

<img src="../../../configuration-guide/extended-controls/timer.files/timer1240.png" width="130" />

La taille du temporisateur n'est pas modifiable, mais sa position l'est. Pendant l'exécution du projet, le temporisateur n'est pas affiché sur l'IHM.
