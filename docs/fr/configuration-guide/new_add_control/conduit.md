# Tuyauterie

Cet objet dessine une tuyauterie dont le diamètre et le tracé sont définis selon la position de l'objet

<img src="../../../configuration-guide/new_add_control/conduit.files/image004.jpg" width="488" alt="ScreenShot00831.jpg" />

Boîte de dialogue générale de la tuyauterie

Ø  Style : style d'affichage de la ligne ; les effets disponibles sont présentés dans « [style](#style) »

Ø Dégradé : effet d'affichage de la tuyauterie ; les effets disponibles sont présentés dans « [dégradé](#Graduallayer) »

Ø Diamètre : diamètre de la tuyauterie, voir « [diamètre](#diameter) ».

Ø Épaisseur : épaisseur de la paroi, ajoutée au diamètre de la tuyauterie. Voir l'effet dans « [épaisseur](#thickness) »

Ø Bord : couleur de l'épaisseur de la tuyauterie ; c'est la couleur du bord quand l'épaisseur est 0

Ø  Paroi/contenu : couleur principale d'affichage de la ligne

Ø Couleur variable de paroi/contenu

<img src="../../../configuration-guide/new_add_control/conduit.files/image005.jpg" width="451" alt="ScreenShot00832.jpg" />

l  Couleur affichée : quand la couleur variable de paroi/contenu est activée, la ligne s'affiche dans la couleur choisie parmi Paroi/contenu, couleur paroi/contenu \# 2 et couleur paroi/contenu \# 3 ; ce choix ne vaut que dans le logiciel de configuration, en exécution la couleur dépend des bits du mot de contrôle

l  Couleur paroi/contenu \# 2, couleur paroi/contenu \# 3 : couleurs alternatives de la ligne

l  Contrôle du clignotement : fait clignoter la ligne

Ø  Contrôle du flux :

l  Mot de contrôle : mot, double mot

l  Effet d'écoulement : (seuls les tuyaux pour lesquels l'effet d'écoulement est activé dans la page Tuyaux peuvent recevoir les types suivants).

Type prédéfini : effet d'écoulement du tuyau

Couleur par défaut : couleur de l'écoulement

Rapport de longueur prédéfini (7) : rapport de longueur de l'écoulement

Appliquer le type, la couleur et la longueur prédéfinis à tous : applique le type à tous les tuyaux pour lesquels l'effet d'écoulement est activé

Ø Mot de contrôle :

<img src="../../../configuration-guide/new_add_control/conduit.files/image006.jpg" width="450" alt="ScreenShot00833.jpg" />

Quand l'utilisateur active la couleur variable de paroi/contenu et le contrôle de l'effet d'écoulement, chaque bit du registre de contrôle choisi produit un effet d'affichage différent. Exemple avec lw0

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>registre</strong></p></td>
<td><p><strong>Bit 0</strong></p></td>
<td><p><strong>Bit 1</strong></p></td>
<td><p><strong>Bit 2</strong></p></td>
<td><p><strong>Bit 3</strong></p></td>
<td><p><strong>Bit 4</strong></p></td>
<td><p><strong>Bit 5</strong></p></td>
<td><p><strong>Bit 6</strong></p></td>
<td><p><strong>Bit 7</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>LW0</strong></p>
<p><strong>（effet quand le bit correspondant est à ON）</strong></p></td>
<td><p>Couleur de paroi</p>
<p>Couleur paroi/contenu #3</p></td>
<td><p>Couleur de paroi</p>
<p>Couleur paroi/contenu #3</p></td>
<td><p>Clignotement de la ligne</p>
<p>Si les deux bits précédents sont tous deux à ON ou à OFF, la couleur est celle de paroi/contenu définie</p>
<p>Si un seul des deux est à ON, la couleur de la ligne alterne entre le contenu et la couleur de contenu #</p></td>
<td><p>Écoulement</p></td>
<td><p>réservé</p></td>
<td><p>réservé</p></td>
<td><p>réservé</p></td>
<td><p>réservé</p></td>
</tr>
</tbody>
</table>

Page de réglage des tuyaux :

<img src="../../../configuration-guide/new_add_control/conduit.files/image007.jpg" width="488" alt="ScreenShot00834.jpg" />

Ø  Page de réglage des tuyaux

l  X1，Y1，X2，Y2：

Coordonnées des points du tuyau : point gauche (x1,y1), point droit (x2, y2).

L'utilisateur peut modifier les coordonnées du tuyau, avec prudence : pour un tuyau horizontal, seule la coordonnée x est modifiable ; pour un tuyau vertical, seule la coordonnée y. Les coordonnées des coudes ne sont pas modifiables, mais leur style l'est.

l  Effet d'écoulement : l'utilisateur peut définir pour chaque tuyau un effet d'écoulement, une couleur, un rapport de longueur, etc.

Pour utiliser le même effet partout, activez simplement l'effet d'écoulement ici et utilisez les réglages prédéfinis de la page Général, qui s'appliquent à tous les tuyaux de l'objet où l'effet est activé.

La page d'affichage est la même que pour les autres objets ; voir la page Visibilité du « Bouton de bit ».

<span id="style"></span>style :

style 1<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="172" alt="ScreenShot00835.jpg" /> style 2<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="178" alt="ScreenShot00836.jpg" /> style 3<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="179" alt="ScreenShot00495.jpg" /> style 4<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="177" alt="ScreenShot00496.jpg" /> style 5<img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="187" alt="2019_7_30_11_37_36.jpg" />

<span id="Graduallayer"></span>Dégradé :

Couleur unie <img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="182" alt="ScreenShot00498.jpg" /> Style 3D 1<img src="../../../configuration-guide/new_add_control/conduit.files/image012.jpg" width="180" alt="ScreenShot00499.jpg" /> Style 3D 2<img src="../../../configuration-guide/new_add_control/conduit.files/image013.jpg" width="180" alt="ScreenShot00500.jpg" /> Style 3D 3<img src="../../../configuration-guide/new_add_control/conduit.files/image014.jpg" width="179" alt="ScreenShot00501.jpg" />

<span id="diameter"></span>diamètre :

diamètre 10<img src="../../../configuration-guide/new_add_control/conduit.files/image015.jpg" width="157" alt="ScreenShot00506.jpg" /> diamètre 20<img src="../../../configuration-guide/new_add_control/conduit.files/image016.jpg" width="188" alt="ScreenShot00507.jpg" /> diamètre 30<img src="../../../configuration-guide/new_add_control/conduit.files/image017.jpg" width="220" alt="ScreenShot00508.jpg" />

<span id="thickness"></span>épaisseur :

épaisseur 0<img src="../../../configuration-guide/new_add_control/conduit.files/image018.jpg" width="183" alt="ScreenShot00502.jpg" /> épaisseur 1<img src="../../../configuration-guide/new_add_control/conduit.files/image019.jpg" width="174" alt="ScreenShot00505.jpg" /> épaisseur 4<img src="../../../configuration-guide/new_add_control/conduit.files/image020.jpg" width="178" alt="ScreenShot00503.jpg" /> épaisseur 8<img src="../../../configuration-guide/new_add_control/conduit.files/image021.jpg" width="187" alt="ScreenShot00504.jpg" />
