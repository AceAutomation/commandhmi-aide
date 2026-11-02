# Pilote d'équipements Modicon

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Modicon NEZA/TWIDO/M218. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Modicon. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Modicon NEZA/TWIDO/M218.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate Modicon NEZA/TWIDO/M218</p>
<p><strong>1.  Raccordement matériel</strong></p>
<p><span id="OLE_LINK19"></span><span id="OLE_LINK20"></span>Câble de liaison :</p>
<p>RS<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>485</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><span id="OLE_LINK60"></span><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Modicon NEZA/TWIDO/M218</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modicon.files/image002.gif" width="281" /><img src="../../drivers/modicon.files/image003.gif" width="130" /><img src="../../drivers/modicon.files/image004.gif" width="145" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate Modicon NEZA/TWIDO/M218 est un MD8M.

**2. Paramétrage logiciel**

Choisissez Modicon Corp. dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Modicon NEZA/TWIDO/M218.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | NEZA Series                 | NEZA/TWIDO/M218 Series                       |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | ODD                         | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 1                           | 0~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Oui                         |

**3. Registres utilisables et plages d'adresses**

Série NEZA

|                   |                    |                 |                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                     |
| **%MW**           | ddddd              | 0~65535         | Mot : <span id="OLE_LINK50"></span>registre de données mot |

Série TWIDO

|                   |                    |                 |                                                                                    |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                  |
| **%M**            | ddddd              | 0~65535         | Bit : <span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>registre de données bit |
| **%MW**           | ddddd              | 0~65535         | Mot : <span id="OLE_LINK53"></span><span id="OLE_LINK54"></span>registre de données mot |

Série M218

|                   |                    |                 |                          |
|-------------------|--------------------|-----------------|--------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**        |
| **%MX**           | ddddd.o            | 0~131071.7      | Bit : registre de données bit |
| **%MW**           | ddddd              | 0~65535         | Mot : registre de données mot |

<img src="../../drivers/modicon.files/image005.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/modicon.files/image006.gif" width="595" />
