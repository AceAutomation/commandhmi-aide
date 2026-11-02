# Pilote d'équipements Nanda

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Nanda NA-200/400. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Nanda. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Nanda NA-200/400.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate Nanda NA-200/400</p>
<p><strong>1.  Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Nanda NA-200/400</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>2</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/nanda.files/image002.gif" width="130" /><img src="../../drivers/nanda.files/image003.gif" width="290" /><img src="../../drivers/nanda.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Le connecteur de l'IHM est un DB9F ; celui de l'automate Nanda NA-200/400 est un DB9M.

**2. Paramétrage logiciel**

Choisissez Nanda Auto Technology dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Nanda NA-200/400.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Nanda NA-200                | Nanda NA-200/400                             |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | NONE                        | EVEN/ODD/NONE                                |
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

Nanda NA-200

|                   |                    |                 |                                                                                                                               |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                                             |
| **I**             | ddd                | 1~128           | Bit : <span id="OLE_LINK54"></span><span id="OLE_LINK55"></span><span id="OLE_LINK56"></span>entrée TOR, lecture seule        |
| **Q**             | ddd                | 1~128           | Bit : sortie TOR                                                                                                              |
| **M**             | dddd               | 1~1024          | Bit : registre de bits                                                                                                        |
| **S**             | ddd                | 1~256           | Bit : registre de bits système                                                                                                |
| **N**             | ddd                | 1~256           | Bit : registre de bits sauvegardé (coupure d'alimentation)                                                                    |
| **IW**            | dd                 | 1~32            | Mot : entrée analogique                                                                                                       |
| **QW**            | dd                 | 1~32            | Mot : sortie analogique                                                                                                       |
| **MW**            | dddd               | 1~1024          | Mot : registre de mots                                                                                                        |
| **SW**            | ddd                | 1~256           | Mot : registre de mots système                                                                                                |
| **NW**            | ddd                | 1~256           | Mot : registre de mots sauvegardé (coupure d'alimentation)                                                                    |

Nanda NA-400

|                   |                    |                 |                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                |
| **I**             | ddd                | 1~2048          | Bit : entrée TOR, lecture seule                  |
| **Q**             | ddd                | 1~2048          | Bit : sortie TOR                                 |
| **M**             | dddd               | 1~8192          | Bit : registre de bits                           |
| **S**             | ddd                | 1~4096          | Bit : registre de bits système                   |
| **N**             | ddd                | 1~2048          | Bit : registre de bits sauvegardé (coupure d'alimentation) |
| **IW**            | dd                 | 1~512           | Mot : entrée analogique                          |
| **QW**            | dd                 | 1~512           | Mot : sortie analogique                          |
| **MW**            | dddd               | 1~8192          | Mot : registre de mots                           |
| **SW**            | ddd                | 1~2048          | Mot : registre de mots système                   |
| **NW**            | ddd                | 1~2048          | Mot : registre de mots sauvegardé (coupure d'alimentation) |

<img src="../../drivers/nanda.files/image005.gif" width="596" />

Remarque :

d : décimal, plage de saisie 0-9 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/nanda.files/image006.gif" width="595" />
