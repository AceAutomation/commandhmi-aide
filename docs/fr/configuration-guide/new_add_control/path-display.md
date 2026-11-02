# Affichage de tracé

Cet objet dessine des éléments graphiques : points, lignes, arcs, cercles, etc.

Les adresses utilisées par cet objet sont toutes des registres internes LB ou LW

Boîte de dialogue générale de l'affichage de tracé

• Couleur de premier plan, couleur de bordure, couleur de fond, Visibilité : voir le « Bouton de bit »

• Zone de définition du tracé : zone de définition des éléments du tracé ; pour la signification des données, voir la fin de ce chapitre, « [description des adresses de la zone de définition du tracé](#路径定义区地址说明) »

• Bit de déclenchement du dessin : à ON, le dessin commence ; à OFF, il s'arrête

• Bit d'effacement : à ON, le dessin est effacé

• Fonction de sélection : sélectionne un point du dessin courant pour en afficher les informations

• Contrôlé par bit : active ou non la fonction de sélection ; avec l'adresse à OFF (par défaut), la sélection est active ; à ON, elle est désactivée

• Type de données du rapport : type de stockage des données du rapport de sélection

• Zone de réception du rapport : adresse de stockage du rapport de sélection ; pour la signification, voir la fin de ce chapitre, « [adresses de la zone de réception du rapport de sélection](#选点报告接收区地址) »

• Rayon de recherche (pixels) : rayon de recherche

• Couleur du curseur : couleur du curseur

• notification :

• signal :

Niveau : avec la sélection active, la sélection d'un point du dessin met le bit de notification à l'état défini. Ce bit doit être remis à zéro manuellement pour surveiller les sélections suivantes

Impulsion : avec la sélection active, la sélection d'un point du dessin met le bit de notification à ON, puis il est remis à zéro automatiquement

Bit de notification : adresse notifiée lors du déclenchement de l'impulsion

<span id="路径定义区地址说明"></span>**Description des adresses de la zone de définition du tracé :**

Zone de définition du tracé : adresses des paramètres de dessin, au format suivant. Exemple avec l'adresse LW0 :

|                     |                                                             |
|---------------------|-------------------------------------------------------------|
| N° de mot           | description                                                 |
| LW0                 | Nombre d'éléments du tracé                                  |
| LW1~LW8             | Informations sur le 1er élément du tracé                    |
| LW9~LW16            | Informations sur le 2e élément du tracé                     |
| ...                 | ...                                                         |
| LW（8n-7）~LW（8n） | Informations sur le n-ième élément du tracé                 |

Index des éléments : [point](#点), [ligne](#线), [arc](#圆弧), [cercle](#圆), [épaisseur](#厚度), [couleur](#颜色)

<span id="点"></span>point :

|         |           |                       |
|---------|-----------|-----------------------|
| Mot     | Mnémonique | Description           |
| LW1     | type      | Code du point : 0     |
| LW2     | color     | [couleur](#颜色)      |
| LW3     | x         | Coordonnée X du point |
| LW4     | y         | Coordonnée Y du point |
| LW5~LW8 | (réservé) | Actuellement 0        |

<span id="线"></span>ligne :

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Mot</p></td>
<td><p>Mnémonique</p></td>
<td><p>Description</p></td>
</tr>
<tr class="even">
<td><p>LW1</p></td>
<td><p>type</p></td>
<td><p>Code de la ligne : 1</p></td>
</tr>
<tr class="odd">
<td><p>LW2</p></td>
<td><p>color</p></td>
<td><p><a href="#颜色">couleur</a></p></td>
</tr>
<tr class="even">
<td><p>LW3</p></td>
<td><p>X1</p></td>
<td><p>Coordonnée X du point de départ</p></td>
</tr>
<tr class="odd">
<td><p>LW4</p></td>
<td><p>Y1</p></td>
<td><p>Coordonnée Y du point de départ</p></td>
</tr>
<tr class="even">
<td><p>LW5</p></td>
<td><p>X2</p></td>
<td><p>Coordonnée X du point d'arrivée</p></td>
</tr>
<tr class="odd">
<td><p>LW6</p></td>
<td><p>Y2</p></td>
<td><p>Coordonnée Y du point d'arrivée</p></td>
</tr>
<tr class="even">
<td><p>LW7</p></td>
<td><p>style</p></td>
<td><p>Type de trait :</p>
<p>0 : non affiché</p>
<p>1 : <img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> trait plein</p>
<p>2 : <img src="../../../configuration-guide/new_add_control/path-display.files/image004.jpg" width="40" alt="ScreenShot00232.jpg" /> pointillé</p>
<p>3 : <img src="../../../configuration-guide/new_add_control/path-display.files/image005.jpg" width="40" alt="ScreenShot00234.jpg" /> trait-point</p>
<p>4 : <img src="../../../configuration-guide/new_add_control/path-display.files/image006.jpg" width="40" alt="ScreenShot00235.jpg" /> tiret-point</p>
<p>5 : <img src="../../../configuration-guide/new_add_control/path-display.files/image007.jpg" width="40" alt="ScreenShot00236.jpg" /> tiret-point-point</p>
<p>6 ou plus :<img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> trait plein</p></td>
</tr>
<tr class="odd">
<td><p>LW8</p></td>
<td><p>(réservé)</p></td>
<td><p>Actuellement 0</p></td>
</tr>
</tbody>
</table>

Arc (tracé dans le sens antihoraire du point de départ au point d'arrivée) :

|      |           |                             |
|------|-----------|-----------------------------|
| Mot  | Mnémonique | Description                 |
| 0    | type      | Code de l'arc : 2           |
| 1    | color     | [couleur](#颜色)            |
| 2    | X         | Coordonnée X du centre      |
| 3    | Y         | Coordonnée Y du centre      |
| 4    | X1        | Coordonnée X du point de départ |
| 5    | Y1        | Coordonnée Y du point de départ |
| 6    | X2        | Coordonnée X du point d'arrivée |
| 7    | Y2        | Coordonnée Y du point d'arrivée |

cercle :

|      |           |                      |
|------|-----------|----------------------|
| Mot  | Mnémonique | Description          |
| 0    | type      | Code du cercle : 3   |
| 1    | color     | [couleur](#颜色)     |
| 2    | X         | Coordonnée X du centre |
| 3    | Y         | Coordonnée Y du centre |
| 4    | r         | Rayon du cercle      |
| 5~7  | (réservé) | Actuellement 0       |

<span id="厚度"></span>Épaisseur (s'applique aux éléments suivants jusqu'à la prochaine épaisseur) :

|      |                      |                                 |
|------|----------------------|---------------------------------|
| Mot  | Mnémonique           | Description                     |
| 0    | type                 | Code de l'épaisseur : 8         |
| 1    | (réservé)            | Actuellement 0                  |
| 2    | Épaisseur            | Épaisseur du trait, en pixels   |
| 3~7  | (réservé)            | Actuellement 0                  |

<span id="颜色"></span>Valeurs de couleur usuelles :

|              |                                   |
|--------------|-----------------------------------|
| Couleur      | Valeur (hexadécimal）             |
| noir         | 0x0000                            |
| bleu         | 0x0010                            |
| vert         | 0x0400                            |
| cyan         | 0x0410                            |
| rouge        | 0x8000                            |
| magenta      | 0x8010                            |
| marron       | 0x8400                            |
| gris         | 0xc618                            |
| gris foncé   | 0x8410                            |
| bleu clair   | 0x001f                            |
| vert clair   | 0x07e0                            |
| bleu pâle    | 0x07ff                            |
| rose         | 0xf800                            |
| magenta pâle | 0xf81f                            |
| jaune        | Oxffe0                            |
| blanc        | 0xffff                            |

<span id="选点报告接收区地址"></span>**Adresses de la zone de réception du rapport de sélection**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>N° de mot</p></td>
<td colspan="3"><p>description</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="3"><p>Coordonnée X du point sélectionné</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="3"><p>Coordonnée Y du point sélectionné</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td colspan="3"><p>Numéro de l'élément auquel appartient le point sélectionné</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>3</p></td>
<td colspan="2"><p>valeur</p></td>
<td><p>description</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="2"><p>Point : le point</p>
<p>Ligne : point de départ de la ligne</p>
<p>Cercle : centre du cercle</p>
<p>Arc : point de départ de l'arc</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="2"><p>Ligne : point d'arrivée de la ligne</p>
<p>Arc : point d'arrivée de l'arc</p></td>
</tr>
<tr class="even" height="0">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>
