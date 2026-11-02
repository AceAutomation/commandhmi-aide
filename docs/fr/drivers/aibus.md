# Pilote d'équipements AIBUS

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état d'un équipement AIBUS via le protocole AIBUS. La liaison série est établie entre le port série de l'IHM et celui de l'équipement AIBUS. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'équipement AIBUS.

**1.  Raccordement matériel**

Câble de liaison :

RS232 (port série, protocole RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **IHM série HM COM1/COM2** |     | **Équipement AIBUS**  |     |
| 2                           | RX  | Broche définie par l'utilisateur | TX  |
| 3                           | TX  | Broche définie par l'utilisateur | RX  |
| 5                           | GND | Broche définie par l'utilisateur | GND |

<img src="../../drivers/aibus.files/image002.gif" width="157" /><img src="../../drivers/aibus.files/image003.gif" width="130" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Le port de l'écran tactile est un connecteur femelle 9 broches trapézoïdal. Le brochage de l'équipement AIBUS dépend de l'équipement.</p>
<p><strong>RS422 (port série, protocole RS422)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Équipement AIBUS</strong></p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table>
<table>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><img src="../../drivers/aibus.files/image004.gif" width="280" /></td>
</tr>
</tbody>
</table>
 &#10;<br />
&#10;<p>Le port de l'écran tactile est un connecteur femelle 9 broches trapézoïdal. Le brochage de l'équipement AIBUS dépend de l'équipement.</p>
<p><strong>RS485 (port série, protocole RS485)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Écran tactile COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Équipement AIBUS</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>D-</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>D+</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p>Le port de l'écran tactile est un connecteur femelle 9 broches trapézoïdal. Le brochage de l'équipement AIBUS dépend de l'équipement.</p></td>
</tr>
</tbody>
</table>

**2. Paramétrage logiciel**

ü Choisissez AIBUS Protocol dans le service d'équipement de la connexion.

ü Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge.

ü Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station de l'automate correspondent à ceux de l'équipement AIBUS.

ü Pour le paramétrage de l'équipement AIBUS, voir sa documentation technique.

Paramètres de connexion par défaut de l'écran tactile

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | AIBUS Protocol              | AIBUS Protocol                               |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | NONE                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 1                           | 1~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Oui                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                      |
|-------------------|--------------------|-----------------|----------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**        |
| **Parameter**     | ddd                | 0~255           | Mot : paramètre      |
| **PV**            | d                  | 0               | Mot : valeur de sortie |
| **SV**            | d                  | 0               | Mot : consigne       |
| **MV**            | d                  | 0               | Mot : valeur d'état  |
| **Status**        | d                  | 0               | Mot : valeur d'état  |

<img src="../../drivers/aibus.files/image005.gif" width="595" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Remarque : </p>
<p>• ·d : décimal, plage de saisie 0-9 ;</p>
<p>• ·« Mot » dans les remarques : le registre ne s'utilise que comme mot ;</p>
<p>• Les noms et plages des registres peuvent varier selon le modèle d'équipement.</p>
<p>Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/aibus.files/image006.gif" width="595" />
